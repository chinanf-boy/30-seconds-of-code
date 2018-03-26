![Logo](/logo.png)

# 片段存档

这些片段虽然有用且有趣,但由于具有非常特定的用例或已过时,因此并未将其完全纳入存储库. 但是我们觉得他们对某些读者可能仍然有用,所以他们就是这样. 

## 目录

-   [`jsontodate.md`](#jsontodate.md)
-   [`speechsynthesis.md`](#speechsynthesis.md)
-   [`binarysearch.md`](#binarysearch.md)
-   [`collat​​z.md`](#collatz.md)
-   [`countvowels.md`](#countvowels.md)
-   [`factors.md`](#factors.md)
-   [`fibonaccicountuntilnum.md`](#fibonaccicountuntilnum.md)
-   [`fibonacciuntilnum.md`](#fibonacciuntilnum.md)
-   [`readme.md`](#readme.md)
-   [`httpdelete.md`](#httpdelete.md)
-   [`httpput.md`](#httpput.md)
-   [`isarmstrongnumber.md`](#isarmstrongnumber.md)
-   [`quicksort.md`](#quicksort.md)
-   [`removevowels.md`](#removevowels.md)
-   [`solverpn.md`](#solverpn.md)
-   [`howmanytimes.md`](#howmanytimes.md)

* * *

### jsontodate

将json对象转换为日期. 

使用`日期()`,将json格式的日期转换为可读格式(`日/月/年`). 

```js
const JSONToDate = arr => {
  const dt = new Date(parseInt(arr.toString().substr(6)));
  return `${dt.getDate()}/${dt.getMonth() + 1}/${dt.getFullYear()}`;
};
```

<details>
<summary>Examples</summary>

```js
JSONToDate(/Date(1489525200000)/); // "14/3/2017"
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### speechsynthesis

执行语音合成(实验). 

使用`speechsynthesisutterance.voice`和`window.speechsynthesis.getvoices()`将消息转换为speech.use`window.speechsynthesis.speak()`发挥消息. 

了解更多关于[speech speech api的speechsynthesisutterance界面](https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesisUtterance). 

```js
const speechSynthesis = message => {
  const msg = new SpeechSynthesisUtterance(message);
  msg.voice = window.speechSynthesis.getVoices()[0];
  window.speechSynthesis.speak(msg);
};
```

<details>
<summary>Examples</summary>

```js
speechSynthesis('Hello, World'); // // plays the message
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 的binarySearch

使用递归. 如同`array.indexof()`它可以找到数组中某个值的索引. 不同之处在于此操作仅适用于排序阵列,与线性搜索相比,它提供了主要的性能提升,因为它具有对数性质,或者`array.indexof()`. 

通过重复划分搜索间隔一半来搜索排序的数组. 从覆盖整个阵列的区间开始. 如果搜索的值小于间隔中间的项目,则进入下半部分. 否则回归上半部分. 反复递归,直到找到中间的值,或者您已递归到大于表示该值不存在并返回的长度的点`-1`. 

```js
const binarySearch = (arr, val, start = 0, end = arr.length - 1) => {
  if (start > end) return -1;
  const mid = Math.floor((start + end) / 2);
  if (arr[mid] > val) return binarySearch(arr, val, start, mid - 1);
  if (arr[mid] < val) return binarySearch(arr, val, mid + 1, end);
  return mid;
}
```

<details>
<summary>Examples</summary>

```js
binarySearch([1, 4, 6, 7, 12, 13, 15, 18, 19, 20, 22, 24], 6); // 2
binarySearch([1, 4, 6, 7, 12, 13, 15, 18, 19, 20, 22, 24], 21); // -1
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 在Collat​​z

应用collat​​z算法. 

如果`ñ`甚至是返回`n / 2个`. 否则,返回`3N + 1`. 

```js
const collatz = n => (n % 2 == 0 ? n / 2 : 3 * n + 1);
```

<details>
<summary>Examples</summary>

```js
collatz(8); // 4
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### countvowels

retuns`数`提供的字符串中的元音. 

使用正则表达式来计算元音的数量`(a,e,i,o,u)`在一个`串`. 

```js
const countVowels = str => (str.match(/[aeiou]/gi) ƜƜ []).length;
```

<details>
<summary>Examples</summary>

```js
countVowels('foobar'); // 3
countVowels('gym'); // 0
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 因素

返回给定因子的数组`NUM`. 如果第二个参数设置为`真正`仅返回主要因素`NUM`. 如果`NUM`是`1`要么`0`返回一个空数组`NUM`小于`0`返回所有因素`- 诠释`连同它们的加法逆. 

使用`array.from()`,`array.map()`和`array.filter()`找到所有的因素`NUM`如果给定`NUM`是消极的,使用`array.reduce()`将添加剂倒数添加到数组中. 如果返回所有结果`素数`是`假`,否则确定并仅返回使用的主要因素`isprime`和`array.filter()`. 第二个参数,`素数`,默认返回素数和非素数因子. 

**注意**:  -_负数不被视为素数. _

```js
const factors = (num, primes = false) => {
  const isPrime = num => {
    const boundary = Math.floor(Math.sqrt(num));
    for (var i = 2; i <= boundary; i++) if (num % i === 0) return false;
    return num >= 2;
  };
  const isNeg = num < 0;
  num = isNeg ? -num : num;
  let array = Array.from({ length: num - 1 })
    .map((val, i) => (num % (i + 2) === 0 ? i + 2 : false))
    .filter(val => val);
  if (isNeg)
    array = array.reduce((acc, val) => {
      acc.push(val);
      acc.push(-val);
      return acc;
    }, []);
  return primes ? array.filter(isPrime) : array;
};
```

<details>
<summary>Examples</summary>

```js
factors(12); // [2,3,4,6,12]
factors(12, true); // [2,3]
factors(-12); // [2, -2, 3, -3, 4, -4, 6, -6, 12, -12]
factors(-12, true); // [2,3]
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### fibonaccicountuntilnum

返回斐波纳契数字的数量`NUM`(`0`和`NUM`包括的). 

用一个数学公式来计算直到斐波那契数的个数`NUM`. 

```js
const fibonacciCountUntilNum = num =>
  Math.ceil(Math.log(num * Math.sqrt(5) + 1 / 2) / Math.log((Math.sqrt(5) + 1) / 2));
```

<details>
<summary>Examples</summary>

```js
fibonacciCountUntilNum(10); // 7
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### fibonacciuntilnum

生成一个包含斐波纳契数列的数组,直到第n项. 

创建一个特定长度的空数组,初始化前两个值(`0`和`1`). 使用`array.reduce()`使用最后两个值的总和将值添加到数组中,除了前两个值之外. 使用数学公式来计算所需数组的长度. 

```js
const fibonacciUntilNum = num => {
  let n = Math.ceil(Math.log(num * Math.sqrt(5) + 1 / 2) / Math.log((Math.sqrt(5) + 1) / 2));
  return Array.from({ length: n }).reduce(
    (acc, val, i) => acc.concat(i > 1 ? acc[i - 1] + acc[i - 2] : i),
    []
  );
};
```

<details>
<summary>Examples</summary>

```js
fibonacciUntilNum(10); // [ 0, 1, 1, 2, 3, 5, 8 ]
```

</details>

<br>[⬆返回顶部](#table-of-contents)

![Logo](/logo.png)

# 片段存档

这些片段虽然有用且有趣,但由于具有非常特定的用例或已过时,因此并未将其完全纳入存储库. 但是我们觉得他们对某些读者可能仍然有用,所以他们就是这样. 

## 目录

-   [`jsontodate.md`](#jsontodate.md)
-   [`speechsynthesis.md`](#speechsynthesis.md)
-   [`binarysearch.md`](#binarysearch.md)
-   [`collat​​z.md`](#collatz.md)
-   [`countvowels.md`](#countvowels.md)
-   [`factors.md`](#factors.md)
-   [`fibonaccicountuntilnum.md`](#fibonaccicountuntilnum.md)
-   [`readme.md`](#readme.md)
-   [`howmanytimes.md`](#howmanytimes.md)
-   [`isarmstrongnumber.md`](#isarmstrongnumber.md)
-   [`quicksort.md`](#quicksort.md)
-   [`removevowels.md`](#removevowels.md)
-   [`solverpn.md`](#solverpn.md)
-   [`fibonacciuntilnum.md`](#fibonacciuntilnum.md)

* * *

### jsontodate

将json对象转换为日期. 

使用`日期()`,将json格式的日期转换为可读格式(`日/月/年`). 

```js
const JSONToDate = arr => {
  const dt = new Date(parseInt(arr.toString().substr(6)));
  return `${dt.getDate()}/${dt.getMonth() + 1}/${dt.getFullYear()}`;
};
```

<details>
<summary>Examples</summary>

```js
JSONToDate(/Date(1489525200000)/); // "14/3/2017"
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### speechsynthesis

执行语音合成(实验). 

使用`speechsynthesisutterance.voice`和`window.speechsynthesis.getvoices()`将消息转换为speech.use`window.speechsynthesis.speak()`发挥消息. 

了解更多关于[speech speech api的speechsynthesisutterance界面](https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesisUtterance). 

```js
const speechSynthesis = message => {
  const msg = new SpeechSynthesisUtterance(message);
  msg.voice = window.speechSynthesis.getVoices()[0];
  window.speechSynthesis.speak(msg);
};
```

<details>
<summary>Examples</summary>

```js
speechSynthesis('Hello, World'); // // plays the message
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 的binarySearch

使用递归. 如同`array.indexof()`它可以找到数组中某个值的索引. 不同之处在于此操作仅适用于排序阵列,与线性搜索相比,它提供了主要的性能提升,因为它具有对数性质,或者`array.indexof()`. 

通过重复划分搜索间隔一半来搜索排序的数组. 从覆盖整个阵列的区间开始. 如果搜索的值小于间隔中间的项目,则进入下半部分. 否则回归上半部分. 反复递归,直到找到中间的值,或者您已递归到大于表示该值不存在并返回的长度的点`-1`. 

```js
const binarySearch = (arr, val, start = 0, end = arr.length - 1) => {
  if (start > end) return -1;
  const mid = Math.floor((start + end) / 2);
  if (arr[mid] > val) return binarySearch(arr, val, start, mid - 1);
  if (arr[mid] < val) return binarySearch(arr, val, mid + 1, end);
  return mid;
}
```

<details>
<summary>Examples</summary>

```js
binarySearch([1, 4, 6, 7, 12, 13, 15, 18, 19, 20, 22, 24], 6); // 2
binarySearch([1, 4, 6, 7, 12, 13, 15, 18, 19, 20, 22, 24], 21); // -1
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 在Collat​​z

应用collat​​z算法. 

如果`ñ`甚至是返回`n / 2个`. 否则,返回`3N + 1`. 

```js
const collatz = n => (n % 2 == 0 ? n / 2 : 3 * n + 1);
```

<details>
<summary>Examples</summary>

```js
collatz(8); // 4
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### countvowels

retuns`数`提供的字符串中的元音. 

使用正则表达式来计算元音的数量`(a,e,i,o,u)`在一个`串`. 

```js
const countVowels = str => (str.match(/[aeiou]/gi) ƜƜ []).length;
```

<details>
<summary>Examples</summary>

```js
countVowels('foobar'); // 3
countVowels('gym'); // 0
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 因素

返回给定因子的数组`NUM`. 如果第二个参数设置为`真正`仅返回主要因素`NUM`. 如果`NUM`是`1`要么`0`返回一个空数组`NUM`小于`0`返回所有因素`- 诠释`连同它们的加法逆. 

使用`array.from()`,`array.map()`和`array.filter()`找到所有的因素`NUM`如果给定`NUM`是消极的,使用`array.reduce()`将添加剂倒数添加到数组中. 如果返回所有结果`素数`是`假`,否则确定并仅返回使用的主要因素`isprime`和`array.filter()`. 第二个参数,`素数`,默认返回素数和非素数因子. 

**注意**:  -_负数不被视为素数. _

```js
const factors = (num, primes = false) => {
  const isPrime = num => {
    const boundary = Math.floor(Math.sqrt(num));
    for (var i = 2; i <= boundary; i++) if (num % i === 0) return false;
    return num >= 2;
  };
  const isNeg = num < 0;
  num = isNeg ? -num : num;
  let array = Array.from({ length: num - 1 })
    .map((val, i) => (num % (i + 2) === 0 ? i + 2 : false))
    .filter(val => val);
  if (isNeg)
    array = array.reduce((acc, val) => {
      acc.push(val);
      acc.push(-val);
      return acc;
    }, []);
  return primes ? array.filter(isPrime) : array;
};
```

<details>
<summary>Examples</summary>

```js
factors(12); // [2,3,4,6,12]
factors(12, true); // [2,3]
factors(-12); // [2, -2, 3, -3, 4, -4, 6, -6, 12, -12]
factors(-12, true); // [2,3]
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### fibonaccicountuntilnum

返回斐波纳契数字的数量`NUM`(`0`和`NUM`包括的). 

用一个数学公式来计算直到斐波那契数的个数`NUM`. 

```js
const fibonacciCountUntilNum = num =>
  Math.ceil(Math.log(num * Math.sqrt(5) + 1 / 2) / Math.log((Math.sqrt(5) + 1) / 2));
```

<details>
<summary>Examples</summary>

```js
fibonacciCountUntilNum(10); // 7
```

</details>

<br>[⬆返回顶部](#table-of-contents)

![Logo](/logo.png)

# 片段存档

这些片段虽然有用且有趣,但由于具有非常特定的用例或已过时,因此并未将其完全纳入存储库. 但是我们觉得他们对某些读者可能仍然有用,所以他们就是这样. 

## 目录

-   [`jsontodate.md`](#jsontodate.md)
-   [`speechsynthesis.md`](#speechsynthesis.md)
-   [`binarysearch.md`](#binarysearch.md)
-   [`collat​​z.md`](#collatz.md)
-   [`countvowels.md`](#countvowels.md)
-   [`factors.md`](#factors.md)
-   [`fibonaccicountuntilnum.md`](#fibonaccicountuntilnum.md)
-   [`readme.md`](#readme.md)
-   [`howmanytimes.md`](#howmanytimes.md)
-   [`isarmstrongnumber.md`](#isarmstrongnumber.md)
-   [`quicksort.md`](#quicksort.md)
-   [`removevowels.md`](#removevowels.md)
-   [`solverpn.md`](#solverpn.md)
-   [`fibonacciuntilnum.md`](#fibonacciuntilnum.md)

* * *

### jsontodate

将json对象转换为日期. 

使用`日期()`,将json格式的日期转换为可读格式(`日/月/年`). 

```js
const JSONToDate = arr => {
  const dt = new Date(parseInt(arr.toString().substr(6)));
  return `${dt.getDate()}/${dt.getMonth() + 1}/${dt.getFullYear()}`;
};
```

<details>
<summary>Examples</summary>

```js
JSONToDate(/Date(1489525200000)/); // "14/3/2017"
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### speechsynthesis

执行语音合成(实验). 

使用`speechsynthesisutterance.voice`和`window.speechsynthesis.getvoices()`将消息转换为speech.use`window.speechsynthesis.speak()`发挥消息. 

了解更多关于[speech speech api的speechsynthesisutterance界面](https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesisUtterance). 

```js
const speechSynthesis = message => {
  const msg = new SpeechSynthesisUtterance(message);
  msg.voice = window.speechSynthesis.getVoices()[0];
  window.speechSynthesis.speak(msg);
};
```

<details>
<summary>Examples</summary>

```js
speechSynthesis('Hello, World'); // // plays the message
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 的binarySearch

使用递归. 如同`array.indexof()`它可以找到数组中某个值的索引. 不同之处在于此操作仅适用于排序阵列,与线性搜索相比,它提供了主要的性能提升,因为它具有对数性质,或者`array.indexof()`. 

通过重复划分搜索间隔一半来搜索排序的数组. 从覆盖整个阵列的区间开始. 如果搜索的值小于间隔中间的项目,则进入下半部分. 否则回归上半部分. 反复递归,直到找到中间的值,或者您已递归到大于表示该值不存在并返回的长度的点`-1`. 

```js
const binarySearch = (arr, val, start = 0, end = arr.length - 1) => {
  if (start > end) return -1;
  const mid = Math.floor((start + end) / 2);
  if (arr[mid] > val) return binarySearch(arr, val, start, mid - 1);
  if (arr[mid] < val) return binarySearch(arr, val, mid + 1, end);
  return mid;
}
```

<details>
<summary>Examples</summary>

```js
binarySearch([1, 4, 6, 7, 12, 13, 15, 18, 19, 20, 22, 24], 6); // 2
binarySearch([1, 4, 6, 7, 12, 13, 15, 18, 19, 20, 22, 24], 21); // -1
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 在Collat​​z

应用collat​​z算法. 

如果`ñ`甚至是返回`n / 2个`. 否则,返回`3N + 1`. 

```js
const collatz = n => (n % 2 == 0 ? n / 2 : 3 * n + 1);
```

<details>
<summary>Examples</summary>

```js
collatz(8); // 4
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### countvowels

retuns`数`提供的字符串中的元音. 

使用正则表达式来计算元音的数量`(a,e,i,o,u)`在一个`串`. 

```js
const countVowels = str => (str.match(/[aeiou]/gi) ƜƜ []).length;
```

<details>
<summary>Examples</summary>

```js
countVowels('foobar'); // 3
countVowels('gym'); // 0
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 因素

返回给定因子的数组`NUM`. 如果第二个参数设置为`真正`仅返回主要因素`NUM`. 如果`NUM`是`1`要么`0`返回一个空数组`NUM`小于`0`返回所有因素`- 诠释`连同它们的加法逆. 

使用`array.from()`,`array.map()`和`array.filter()`找到所有的因素`NUM`如果给定`NUM`是消极的,使用`array.reduce()`将添加剂倒数添加到数组中. 如果返回所有结果`素数`是`假`,否则确定并仅返回使用的主要因素`isprime`和`array.filter()`. 第二个参数,`素数`,默认返回素数和非素数因子. 

**注意**:  -_负数不被视为素数. _

```js
const factors = (num, primes = false) => {
  const isPrime = num => {
    const boundary = Math.floor(Math.sqrt(num));
    for (var i = 2; i <= boundary; i++) if (num % i === 0) return false;
    return num >= 2;
  };
  const isNeg = num < 0;
  num = isNeg ? -num : num;
  let array = Array.from({ length: num - 1 })
    .map((val, i) => (num % (i + 2) === 0 ? i + 2 : false))
    .filter(val => val);
  if (isNeg)
    array = array.reduce((acc, val) => {
      acc.push(val);
      acc.push(-val);
      return acc;
    }, []);
  return primes ? array.filter(isPrime) : array;
};
```

<details>
<summary>Examples</summary>

```js
factors(12); // [2,3,4,6,12]
factors(12, true); // [2,3]
factors(-12); // [2, -2, 3, -3, 4, -4, 6, -6, 12, -12]
factors(-12, true); // [2,3]
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### fibonaccicountuntilnum

返回斐波纳契数字的数量`NUM`(`0`和`NUM`包括的). 

用一个数学公式来计算直到斐波那契数的个数`NUM`. 

```js
const fibonacciCountUntilNum = num =>
  Math.ceil(Math.log(num * Math.sqrt(5) + 1 / 2) / Math.log((Math.sqrt(5) + 1) / 2));
```

<details>
<summary>Examples</summary>

```js
fibonacciCountUntilNum(10); // 7
```

</details>

<br>[⬆返回顶部](#table-of-contents)

![Logo](/logo.png)

# 30秒的代码

这些片段虽然有用且有趣,但由于具有非常特定的用例或已过时,因此并未将其完全纳入存储库. 但是我们觉得他们对某些读者可能仍然有用,所以他们就是这样. 

## 目录

-   [`jsontodate.md`](#jsontodate.md
-   [`speechsynthesis.md`](#speechsynthesis.md
-   [`collat​​z.md`](#collat​​z.md
-   [`countvowels.md`](#countvowels.md
-   [`factors.md`](#factors.md
-   [`fibonaccicountuntilnum.md`](#fibonaccicountuntilnum.md
-   [`binarysearch.md`](#binarysearch.md
-   [`howmanytimes.md`](#howmanytimes.md
-   [`isarmstrongnumber.md`](#isarmstrongnumber.md
-   [`quicksort.md`](#quicksort.md
-   [`removevowels.md`](#removevowels.md
-   [`solverpn.md`](#solverpn.md
-   [`fibonacciuntilnum.md`](#fibonacciuntilnum.md

* * *

### jsontodate

将json对象转换为日期. 

使用`日期()`,将json格式的日期转换为可读格式(`日/月/年`). 

```js
const JSONToDate = arr => {
  const dt = new Date(parseInt(arr.toString().substr(6)));
  return `${dt.getDate()}/${dt.getMonth() + 1}/${dt.getFullYear()}`;
};
```

<details>
<summary>Examples</summary>

```js
JSONToDate(/Date(1489525200000)/); // "14/3/2017"
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### speechsynthesis

执行语音合成(实验). 

使用`speechsynthesisutterance.voice`和`window.speechsynthesis.getvoices()`将消息转换为speech.use`window.speechsynthesis.speak()`发挥消息. 

了解更多关于[speech speech api的speechsynthesisutterance界面](https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesisUtterance). 

```js
const speechSynthesis = message => {
  const msg = new SpeechSynthesisUtterance(message);
  msg.voice = window.speechSynthesis.getVoices()[0];
  window.speechSynthesis.speak(msg);
};
```

<details>
<summary>Examples</summary>

```js
speechSynthesis('Hello, World'); // // plays the message
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 在Collat​​z

应用collat​​z算法. 

如果`ñ`甚至是返回`n / 2个`. 否则,返回`3N + 1`. 

```js
const collatz = n => (n % 2 == 0 ? n / 2 : 3 * n + 1);
```

<details>
<summary>Examples</summary>

```js
collatz(8); // 4
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### countvowels

retuns`数`提供的字符串中的元音. 

使用正则表达式来计算元音的数量`(a,e,i,o,u)`在一个`串`. 

```js
const countVowels = str => (str.match(/[aeiou]/gi) ƜƜ []).length;
```

<details>
<summary>Examples</summary>

```js
countVowels('foobar'); // 3
countVowels('gym'); // 0
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 因素

返回给定因子的数组`NUM`. 如果第二个参数设置为`真正`仅返回主要因素`NUM`. 如果`NUM`是`1`要么`0`返回一个空数组`NUM`小于`0`返回所有因素`- 诠释`连同它们的加法逆. 

使用`array.from()`,`array.map()`和`array.filter()`找到所有的因素`NUM`如果给定`NUM`是消极的,使用`array.reduce()`将添加剂倒数添加到数组中. 如果返回所有结果`素数`是`假`,否则确定并仅返回使用的主要因素`isprime`和`array.filter()`. 第二个参数,`素数`,默认返回素数和非素数因子. 

**注意**:  -_负数不被视为素数. _

```js
const factors = (num, primes = false) => {
  const isPrime = num => {
    const boundary = Math.floor(Math.sqrt(num));
    for (var i = 2; i <= boundary; i++) if (num % i === 0) return false;
    return num >= 2;
  };
  const isNeg = num < 0;
  num = isNeg ? -num : num;
  let array = Array.from({ length: num - 1 })
    .map((val, i) => (num % (i + 2) === 0 ? i + 2 : false))
    .filter(val => val);
  if (isNeg)
    array = array.reduce((acc, val) => {
      acc.push(val);
      acc.push(-val);
      return acc;
    }, []);
  return primes ? array.filter(isPrime) : array;
};
```

<details>
<summary>Examples</summary>

```js
factors(12); // [2,3,4,6,12]
factors(12, true); // [2,3]
factors(-12); // [2, -2, 3, -3, 4, -4, 6, -6, 12, -12]
factors(-12, true); // [2,3]
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### fibonaccicountuntilnum

返回斐波纳契数字的数量`NUM`(`0`和`NUM`包括的). 

用一个数学公式来计算直到斐波那契数的个数`NUM`. 

```js
const fibonacciCountUntilNum = num =>
  Math.ceil(Math.log(num * Math.sqrt(5) + 1 / 2) / Math.log((Math.sqrt(5) + 1) / 2));
```

<details>
<summary>Examples</summary>

```js
fibonacciCountUntilNum(10); // 7
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 的binarySearch

使用递归. 如同`array.indexof()`它可以找到数组中某个值的索引. 不同之处在于此操作仅适用于排序阵列,与线性搜索相比,它提供了主要的性能提升,因为它具有对数性质,或者`array.indexof()`. 

通过重复划分搜索间隔一半来搜索排序的数组. 从覆盖整个阵列的区间开始. 如果搜索的值小于间隔中间的项目,则进入下半部分. 否则回归上半部分. 反复递归,直到找到中间的值,或者您已递归到大于表示该值不存在并返回的长度的点`-1`. 

```js
const binarySearch = (arr, val, start = 0, end = arr.length - 1) => {
  if (start > end) return -1;
  const mid = Math.floor((start + end) / 2);
  if (arr[mid] > val) return binarySearch(arr, val, start, mid - 1);
  if (arr[mid] < val) return binarySearch(arr, val, mid + 1, end);
  return mid;
}
```

<details>
<summary>Examples</summary>

```js
binarySearch([1, 4, 6, 7, 12, 13, 15, 18, 19, 20, 22, 24], 6); // 2
binarySearch([1, 4, 6, 7, 12, 13, 15, 18, 19, 20, 22, 24], 21); // -1
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 多少次

返回次数`NUM`可以分为`除数`(整数或小数),而不会得到小数的答案. 

如果`除数`是`-1`要么`1`返回`无穷`. 如果`除数`是`-0`要么`0`返回`0`. 另外,保持分开`NUM`同`除数`并递增`一世`,而结果是一个整数. 返回循环执行的次数,`一世`. 

```js
const howManyTimes = (num, divisor) => {
  if (divisor === 1 ƜƜ divisor === -1) return Infinity;
  if (divisor === 0) return 0;
  let i = 0;
  while (Number.isInteger(num / divisor)) {
    i++;
    num = num / divisor;
  }
  return i;
};
```

<details>
<summary>Examples</summary>

```js
howManyTimes(100, 2); // 2
howManyTimes(100, 2.5); // 2
howManyTimes(100, 0); // 0
howManyTimes(100, -1); // Infinity
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### isarmstrongnumber

检查给定的号码是否是阿姆斯特朗号码. 

将给定的数字转换为数字数组. 使用指数运算符(`**`)为每个数字获得适当的功率并对其进行总结. 如果总和等于数字本身,则返回`真正`除此以外`假`. 

```js
const isArmstrongNumber = digits =>
  (arr => arr.reduce((a, d) => a + parseInt(d) ** arr.length, 0) == digits)(
    (digits + '').split('')
  );
```

<details>
<summary>Examples</summary>

```js
isArmstrongNumber(1634); // true
isArmstrongNumber(56); // false
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 快速排序

快速排列数组(默认情况下按升序排序). 

使用递归. 使用`array.filter`和传播算子(`...`)来创建一个数组,其中所有具有小于主元的值的元素都在主元之前,并且具有大于主元的值的所有元素都会在主元之后. 如果参数`降序`是truthy,返回数组按降序排序. 

```js
const quickSort = ([n, ...nums], desc) =>
  isNaN(n)
    ? []
    : [
        ...quickSort(nums.filter(v => (desc ? v > n : v <= n)), desc),
        n,
        ...quickSort(nums.filter(v => (!desc ? v > n : v <= n)), desc)
      ];
```

<details>
<summary>Examples</summary>

```js
quickSort([4, 1, 3, 2]); // [1,2,3,4]
quickSort([4, 1, 3, 2], true); // [4,3,2,1]
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### removevowels

返回a中的所有元音`海峡`取而代之`REPL`. 

使用`与string.replace()`用正则表达式替换中的所有元音`海峡`.omot`REPL`使用默认值`""`. 

```js
const removeVowels = (str, repl = '') => str.replace(/[aeiou]/gi,repl);
```

<details>
<summary>Examples</summary>

```js
removeVowels("foobAr"); // "fbr"
removeVowels("foobAr","*"); // "f**b*r"
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### solverpn

解决了给定的数学表达式[反向波兰标记](https://en.wikipedia.org/wiki/Reverse_Polish_notation). 如果有无法识别的符号或表达式错误,则会引发适当的错误. 有效的运营商是:  -`+`,`-`,`*`,`/`,`^`,`**`(`^`&`**`是指数符号并且是相同的). 这段代码不支持任何一元运算符. 

使用字典,`运营商`指定每个运算符的匹配数学运算`与string.replace()`用正则表达式来替换`^`同`**`,`string.split()`标记字符串和`array.filter()`删除空的令牌. 使用`array.foreach()`解析每一个`符号`,将其评估为数值或运算符并解决数学表达式. 将数字值转换为浮点数并推送到`堆`,而运营商则使用该评估`运营商`字典和流行元素`堆`应用操作. 

```js
const solveRPN = rpn => {
  const OPERATORS = {
    '*': (a, b) => a * b,
    '+': (a, b) => a + b,
    '-': (a, b) => a - b,
    '/': (a, b) => a / b,
    '**': (a, b) => a ** b
  };
  const [stack, solve] = [
    [],
    rpn
      .replace(/\^/g, '**')
      .split(/\s+/g)
      .filter(el => !/\s+/.test(el) && el !== '')
  ];
  solve.forEach(symbol => {
    if (!isNaN(parseFloat(symbol)) && isFinite(symbol)) {
      stack.push(symbol);
    } else if (Object.keys(OPERATORS).includes(symbol)) {
      const [a, b] = [stack.pop(), stack.pop()];
      stack.push(OPERATORS[symbol](parseFloat(b), parseFloat(a)));
    } else {
      throw `${symbol} is not a recognized symbol`;
    }
  });
  if (stack.length === 1) return stack.pop();
  else throw `${rpn} is not a proper RPN. Please check it and try again`;
};
```

<details>
<summary>Examples</summary>

```js
solveRPN('15 7 1 1 + - / 3 * 2 1 1 + + -'); // 5
solveRPN('2 3 ^'); // 8
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### fibonacciuntilnum

生成一个包含斐波纳契数列的数组,直到第n项. 

创建一个特定长度的空数组,初始化前两个值(`0`和`1`). 使用`array.reduce()`使用最后两个值的总和将值添加到数组中,除了前两个值之外. 使用数学公式来计算所需数组的长度. 

```js
const fibonacciUntilNum = num => {
  let n = Math.ceil(Math.log(num * Math.sqrt(5) + 1 / 2) / Math.log((Math.sqrt(5) + 1) / 2));
  return Array.from({ length: n }).reduce(
    (acc, val, i) => acc.concat(i > 1 ? acc[i - 1] + acc[i - 2] : i),
    []
  );
};
```

<details>
<summary>Examples</summary>

<details>
<summary>Examples</summary>

```js
fibonacciUntilNum(10); // [ 0, 1, 1, 2, 3, 5, 8 ]
```

</details>

<br>[⬆返回顶部](#table-of-contents)

</details>

<br>[⬆返回顶部](#table-of-contents)

### 多少次

返回次数`NUM`可以分为`除数`(整数或小数),而不会得到小数的答案. 

如果`除数`是`-1`要么`1`返回`无穷`. 如果`除数`是`-0`要么`0`返回`0`. 另外,保持分开`NUM`同`除数`并递增`一世`,而结果是一个整数. 返回循环执行的次数,`一世`. 

```js
const howManyTimes = (num, divisor) => {
  if (divisor === 1 ƜƜ divisor === -1) return Infinity;
  if (divisor === 0) return 0;
  let i = 0;
  while (Number.isInteger(num / divisor)) {
    i++;
    num = num / divisor;
  }
  return i;
};
```

<details>
<summary>Examples</summary>

```js
howManyTimes(100, 2); // 2
howManyTimes(100, 2.5); // 2
howManyTimes(100, 0); // 0
howManyTimes(100, -1); // Infinity
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### isarmstrongnumber

检查给定的号码是否是阿姆斯特朗号码. 

将给定的数字转换为数字数组. 使用指数运算符(`**`)为每个数字获得适当的功率并对其进行总结. 如果总和等于数字本身,则返回`真正`除此以外`假`. 

```js
const isArmstrongNumber = digits =>
  (arr => arr.reduce((a, d) => a + parseInt(d) ** arr.length, 0) == digits)(
    (digits + '').split('')
  );
```

<details>
<summary>Examples</summary>

```js
isArmstrongNumber(1634); // true
isArmstrongNumber(56); // false
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 快速排序

快速排列数组(默认情况下按升序排序). 

使用递归. 使用`array.filter`和传播算子(`...`)来创建一个数组,其中所有具有小于主元的值的元素都在主元之前,并且具有大于主元的值的所有元素都会在主元之后. 如果参数`降序`是truthy,返回数组按降序排序. 

```js
const quickSort = ([n, ...nums], desc) =>
  isNaN(n)
    ? []
    : [
        ...quickSort(nums.filter(v => (desc ? v > n : v <= n)), desc),
        n,
        ...quickSort(nums.filter(v => (!desc ? v > n : v <= n)), desc)
      ];
```

<details>
<summary>Examples</summary>

```js
quickSort([4, 1, 3, 2]); // [1,2,3,4]
quickSort([4, 1, 3, 2], true); // [4,3,2,1]
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### removevowels

返回a中的所有元音`海峡`取而代之`REPL`. 

使用`与string.replace()`用正则表达式替换中的所有元音`海峡`.omot`REPL`使用默认值`""`. 

```js
const removeVowels = (str, repl = '') => str.replace(/[aeiou]/gi,repl);
```

<details>
<summary>Examples</summary>

```js
removeVowels("foobAr"); // "fbr"
removeVowels("foobAr","*"); // "f**b*r"
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### solverpn

解决了给定的数学表达式[反向波兰标记](https://en.wikipedia.org/wiki/Reverse_Polish_notation). 如果有无法识别的符号或表达式错误,则会引发适当的错误. 有效的运营商是:  -`+`,`-`,`*`,`/`,`^`,`**`(`^`&`**`是指数符号并且是相同的). 这段代码不支持任何一元运算符. 

使用字典,`运营商`指定每个运算符的匹配数学运算`与string.replace()`用正则表达式来替换`^`同`**`,`string.split()`标记字符串和`array.filter()`删除空的令牌. 使用`array.foreach()`解析每一个`符号`,将其评估为数值或运算符并解决数学表达式. 将数字值转换为浮点数并推送到`堆`,而运营商则使用该评估`运营商`字典和流行元素`堆`应用操作. 

```js
const solveRPN = rpn => {
  const OPERATORS = {
    '*': (a, b) => a * b,
    '+': (a, b) => a + b,
    '-': (a, b) => a - b,
    '/': (a, b) => a / b,
    '**': (a, b) => a ** b
  };
  const [stack, solve] = [
    [],
    rpn
      .replace(/\^/g, '**')
      .split(/\s+/g)
      .filter(el => !/\s+/.test(el) && el !== '')
  ];
  solve.forEach(symbol => {
    if (!isNaN(parseFloat(symbol)) && isFinite(symbol)) {
      stack.push(symbol);
    } else if (Object.keys(OPERATORS).includes(symbol)) {
      const [a, b] = [stack.pop(), stack.pop()];
      stack.push(OPERATORS[symbol](parseFloat(b), parseFloat(a)));
    } else {
      throw `${symbol} is not a recognized symbol`;
    }
  });
  if (stack.length === 1) return stack.pop();
  else throw `${rpn} is not a proper RPN. Please check it and try again`;
};
```

<details>
<summary>Examples</summary>

```js
solveRPN('15 7 1 1 + - / 3 * 2 1 1 + + -'); // 5
solveRPN('2 3 ^'); // 8
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### fibonacciuntilnum

生成一个包含斐波纳契数列的数组,直到第n项. 

创建一个特定长度的空数组,初始化前两个值(`0`和`1`). 使用`array.reduce()`使用最后两个值的总和将值添加到数组中,除了前两个值之外. 使用数学公式来计算所需数组的长度. 

```js
const fibonacciUntilNum = num => {
  let n = Math.ceil(Math.log(num * Math.sqrt(5) + 1 / 2) / Math.log((Math.sqrt(5) + 1) / 2));
  return Array.from({ length: n }).reduce(
    (acc, val, i) => acc.concat(i > 1 ? acc[i - 1] + acc[i - 2] : i),
    []
  );
};
```

<details>
<summary>Examples</summary>

<details>
<summary>Examples</summary>

```js
fibonacciUntilNum(10); // [ 0, 1, 1, 2, 3, 5, 8 ]
```

</details>

<br>[⬆返回顶部](#table-of-contents)

</details>

<br>[⬆返回顶部](#table-of-contents)

### 多少次

返回次数`NUM`可以分为`除数`(整数或小数),而不会得到小数的答案. 

如果`除数`是`-1`要么`1`返回`无穷`. 如果`除数`是`-0或`0回报`0`. 另外,保持分开`数字与`除数和递增`在`,而结果是一个整数. 返回循环执行的次数,`一世`. `⬆返回顶部`,而结果是一个整数. 返回循环执行的次数,`一世`. 

```js
const howManyTimes = (num, divisor) => {
  if (divisor === 1 ƜƜ divisor === -1) return Infinity;
  if (divisor === 0) return 0;
  let i = 0;
  while (Number.isInteger(num / divisor)) {
    i++;
    num = num / divisor;
  }
  return i;
};
```

<details>
<summary>Examples</summary>

```js
howManyTimes(100, 2); // 2
howManyTimes(100, 2.5); // 2
howManyTimes(100, 0); // 0
howManyTimes(100, -1); // Infinity
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### isarmstrongnumber

检查给定的号码是否是阿姆斯特朗号码. 

将给定的数字转换为数字数组. 使用指数运算符(`**`)为每个数字获得适当的功率并对其进行总结. 如果总和等于数字本身,则返回`真正`除此以外`假`. 

```js
const isArmstrongNumber = digits =>
  (arr => arr.reduce((a, d) => a + parseInt(d) ** arr.length, 0) == digits)(
    (digits + '').split('')
  );
```

<details>
<summary>Examples</summary>

```js
isArmstrongNumber(1634); // true
isArmstrongNumber(56); // false
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 快速排序

快速排列数组(默认情况下按升序排序). 

使用递归. 使用`array.filter`和传播算子(`...`)来创建一个数组,其中所有具有小于主元的值的元素都在主元之前,并且具有大于主元的值的所有元素都会在主元之后. 如果参数`降序`是truthy,返回数组按降序排序. 

```js
const quickSort = ([n, ...nums], desc) =>
  isNaN(n)
    ? []
    : [
        ...quickSort(nums.filter(v => (desc ? v > n : v <= n)), desc),
        n,
        ...quickSort(nums.filter(v => (!desc ? v > n : v <= n)), desc)
      ];
```

<details>
<summary>Examples</summary>

```js
quickSort([4, 1, 3, 2]); // [1,2,3,4]
quickSort([4, 1, 3, 2], true); // [4,3,2,1]
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### removevowels

返回a中的所有元音`海峡`取而代之`REPL`. 

使用`与string.replace()`用正则表达式替换中的所有元音`海峡`.omot`REPL`使用默认值`""`. 

```js
const removeVowels = (str, repl = '') => str.replace(/[aeiou]/gi,repl);
```

<details>
<summary>Examples</summary>

```js
removeVowels("foobAr"); // "fbr"
removeVowels("foobAr","*"); // "f**b*r"
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### solverpn

解决了给定的数学表达式[反向波兰标记](https://en.wikipedia.org/wiki/Reverse_Polish_notation). 如果有无法识别的符号或表达式错误,则会引发适当的错误. 有效的运营商是:  -`+`,`-`,`*`,`/`,`^`,`**`(`^`&`**`是指数符号并且是相同的). 这段代码不支持任何一元运算符. 

使用字典,`运营商`指定每个运算符的匹配数学运算`与string.replace()`用正则表达式来替换`^`同`**`,`string.split()`标记字符串和`array.filter()`删除空的令牌. 使用`array.foreach()`解析每一个`符号`,将其评估为数值或运算符并解决数学表达式. 将数字值转换为浮点数并推送到`堆`,而运营商则使用该评估`运营商`字典和流行元素`堆`应用操作. 

```js
const solveRPN = rpn => {
  const OPERATORS = {
    '*': (a, b) => a * b,
    '+': (a, b) => a + b,
    '-': (a, b) => a - b,
    '/': (a, b) => a / b,
    '**': (a, b) => a ** b
  };
  const [stack, solve] = [
    [],
    rpn
      .replace(/\^/g, '**')
      .split(/\s+/g)
      .filter(el => !/\s+/.test(el) && el !== '')
  ];
  solve.forEach(symbol => {
    if (!isNaN(parseFloat(symbol)) && isFinite(symbol)) {
      stack.push(symbol);
    } else if (Object.keys(OPERATORS).includes(symbol)) {
      const [a, b] = [stack.pop(), stack.pop()];
      stack.push(OPERATORS[symbol](parseFloat(b), parseFloat(a)));
    } else {
      throw `${symbol} is not a recognized symbol`;
    }
  });
  if (stack.length === 1) return stack.pop();
  else throw `${rpn} is not a proper RPN. Please check it and try again`;
};
```

<details>
<summary>Examples</summary>

```js
solveRPN('15 7 1 1 + - / 3 * 2 1 1 + + -'); // 5
solveRPN('2 3 ^'); // 8
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### fibonacciuntilnum

生成一个包含斐波纳契数列的数组,直到第n项. 

创建一个特定长度的空数组,初始化前两个值(`0`和`1`). 使用`array.reduce()`使用最后两个值的总和将值添加到数组中,除了前两个值之外. 使用数学公式来计算所需数组的长度. 

```js
const fibonacciUntilNum = num => {
  let n = Math.ceil(Math.log(num * Math.sqrt(5) + 1 / 2) / Math.log((Math.sqrt(5) + 1) / 2));
  return Array.from({ length: n }).reduce(
    (acc, val, i) => acc.concat(i > 1 ? acc[i - 1] + acc[i - 2] : i),
    []
  );
};
```

<details>
<summary>Examples</summary>

<details>
<summary>Examples</summary>

```js
fibonacciUntilNum(10); // [ 0, 1, 1, 2, 3, 5, 8 ]
```

</details>

<br>[⬆返回顶部](#table-of-contents)

</details>

<br>[⬆返回顶部](#table-of-contents)

### httpdelete

使一个`删除`请求传递的url. 

使用`XMLHttpRequest的`web api来制作一个`删除`请求给定`网址`处理`负载`事件,通过运行提供的`回电话`函数. 处理`的onerror`事件,通过运行提供的`呃`function.omit第三个参数,`呃`在默认情况下将请求记录到控制台的错误流. 

```js
const httpDelete = (url, callback, err = console.error) => {
  const request = new XMLHttpRequest();
  request.open("DELETE", url, true);
  request.onload = () => callback(request);
  request.onerror = () => err(request);
  request.send();
};
```

<details>
<summary>Examples</summary>

```js
httpDelete('https://website.com/users/123', request => {
  console.log(request.responseText);
}); // 'Deletes a user from the database'
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### httpput

使一个`放`请求传递的url. 

使用`XMLHttpRequest的`web api来制作一个`放`请求给定`网址`设置一个值`HTTP`请求标头`setrequestheader`方法. 处理`负载`事件,通过运行提供的`回电话`函数. 处理`的onerror`事件,通过运行提供的`呃`function.omit最后一个参数,`呃`在默认情况下将请求记录到控制台的错误流. 

```js
const httpPut = (url, data, callback, err = console.error) => {
    const request = new XMLHttpRequest();
    request.open("PUT", url, true);
    request.setRequestHeader('Content-type','application/json; charset=utf-8');
    request.onload = () => callback(request);
    request.onerror = () => err(request);
    request.send(data);
};
```

<details>
<summary>Examples</summary>

```js
const password = "fooBaz";
const data = JSON.stringify(password);
httpPut('https://website.com/users/123', data, request => {
  console.log(request.responseText);
}); // 'Updates a user's password in database'
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### isarmstrongnumber

检查给定的号码是否是阿姆斯特朗号码. 

将给定的数字转换为数字数组. 使用指数运算符(`**`)为每个数字获得适当的功率并对其进行总结. 如果总和等于数字本身,则返回`真正`除此以外`假`. 

```js
const isArmstrongNumber = digits =>
  (arr => arr.reduce((a, d) => a + parseInt(d) ** arr.length, 0) == digits)(
    (digits + '').split('')
  );
```

<details>
<summary>Examples</summary>

```js
isArmstrongNumber(1634); // true
isArmstrongNumber(56); // false
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 快速排序

快速排列数组(默认情况下按升序排序). 

使用递归. 使用`array.filter`和传播算子(`...`)来创建一个数组,其中所有具有小于主元的值的元素都在主元之前,并且具有大于主元的值的所有元素都会在主元之后. 如果参数`降序`是truthy,返回数组按降序排序. 

```js
const quickSort = ([n, ...nums], desc) =>
  isNaN(n)
    ? []
    : [
        ...quickSort(nums.filter(v => (desc ? v > n : v <= n)), desc),
        n,
        ...quickSort(nums.filter(v => (!desc ? v > n : v <= n)), desc)
      ];
```

<details>
<summary>Examples</summary>

```js
quickSort([4, 1, 3, 2]); // [1,2,3,4]
quickSort([4, 1, 3, 2], true); // [4,3,2,1]
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### removevowels

返回a中的所有元音`海峡`取而代之`REPL`. 

使用`与string.replace()`用正则表达式替换中的所有元音`海峡`.omot`REPL`使用默认值`""`. 

```js
const removeVowels = (str, repl = '') => str.replace(/[aeiou]/gi,repl);
```

<details>
<summary>Examples</summary>

```js
removeVowels("foobAr"); // "fbr"
removeVowels("foobAr","*"); // "f**b*r"
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### solverpn

解决了给定的数学表达式[反向波兰标记](https://en.wikipedia.org/wiki/Reverse_Polish_notation). 如果有无法识别的符号或表达式错误,则会引发适当的错误. 有效的运营商是:  -`+`,`-`,`*`,`/`,`^`,`**`(`^`&`**`是指数符号并且是相同的). 这段代码不支持任何一元运算符. 

使用字典,`运营商`指定每个运算符的匹配数学运算`与string.replace()`用正则表达式来替换`^`同`**`,`string.split()`标记字符串和`array.filter()`删除空的令牌. 使用`array.foreach()`解析每一个`符号`,将其评估为数值或运算符并解决数学表达式. 将数字值转换为浮点数并推送到`堆`,而运营商则使用该评估`运营商`字典和流行元素`堆`应用操作. 

```js
const solveRPN = rpn => {
  const OPERATORS = {
    '*': (a, b) => a * b,
    '+': (a, b) => a + b,
    '-': (a, b) => a - b,
    '/': (a, b) => a / b,
    '**': (a, b) => a ** b
  };
  const [stack, solve] = [
    [],
    rpn
      .replace(/\^/g, '**')
      .split(/\s+/g)
      .filter(el => !/\s+/.test(el) && el !== '')
  ];
  solve.forEach(symbol => {
    if (!isNaN(parseFloat(symbol)) && isFinite(symbol)) {
      stack.push(symbol);
    } else if (Object.keys(OPERATORS).includes(symbol)) {
      const [a, b] = [stack.pop(), stack.pop()];
      stack.push(OPERATORS[symbol](parseFloat(b), parseFloat(a)));
    } else {
      throw `${symbol} is not a recognized symbol`;
    }
  });
  if (stack.length === 1) return stack.pop();
  else throw `${rpn} is not a proper RPN. Please check it and try again`;
};
```

<details>
<summary>Examples</summary>

```js
solveRPN('15 7 1 1 + - / 3 * 2 1 1 + + -'); // 5
solveRPN('2 3 ^'); // 8
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 多少次

返回次数`NUM`可以分为`除数`(整数或小数),而不会得到小数的答案. 

如果`除数`是`-1`要么`1`返回`无穷`. 如果`除数`是`-0`要么`0`返回`0`.
Otherwise, keep dividing `num` with `divisor` and incrementing `i`, while the result is an integer.
Return the number of times the loop was executed, `i`.

```js
const howManyTimes = (num, divisor) => {
  if (divisor === 1 ƜƜ divisor === -1) return Infinity;
  if (divisor === 0) return 0;
  let i = 0;
  while (Number.isInteger(num / divisor)) {
    i++;
    num = num / divisor;
  }
  return i;
};
```

<details>
<summary>Examples</summary>

```js
howManyTimes(100, 2); // 2
howManyTimes(100, 2.5); // 2
howManyTimes(100, 0); // 0
howManyTimes(100, -1); // Infinity
```

</details>

<br>[⬆ Back to top](#table-of-contents)