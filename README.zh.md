![Logo](/logo.png)

# 30秒的代码

[![License](https://img.shields.io/badge/license-CC0--1.0-blue.svg)](https://github.com/Chalarangelo/30-seconds-of-code/blob/master/LICENSE) [![npm Downloads](https://img.shields.io/npm/dt/30-seconds-of-code.svg)](https://www.npmjs.com/package/30-seconds-of-code) [![npm Version](https://img.shields.io/npm/v/30-seconds-of-code.svg)](https://www.npmjs.com/package/30-seconds-of-code) [![Gitter chat](https://img.shields.io/badge/chat-on%20gitter-4FB999.svg)](https://gitter.im/30-seconds-of-code/Lobby) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com) [![Travis Build](https://travis-ci.org/Chalarangelo/30-seconds-of-code.svg?branch=master)](https://travis-ci.org/Chalarangelo/30-seconds-of-code) [![Insight.io](https://img.shields.io/badge/insight.io-Ready-brightgreen.svg)](https://insight.io/github.com/Chalarangelo/30-seconds-of-code/tree/master/?source=0) [![js-semistandard-style](https://img.shields.io/badge/code%20style-semistandard-brightgreen.svg)](https://github.com/Flet/semistandard) [![ProductHunt](https://img.shields.io/badge/producthunt-vote-orange.svg)](https://www.producthunt.com/posts/30-seconds-of-code)

> 策划收集有用的JavaScript片段,您可以在30秒或更短的时间内理解. 

-   使用<kbd>CTRL</kbd>+<kbd>F</kbd>要么<kbd>命令</kbd>+<kbd>F</kbd>搜索一个片段. 
-   捐款欢迎,请阅读[贡献指南](CONTRIBUTING.md). 
-   片段是用es6编写的,使用[babel翻译](https://babeljs.io/)以确保向后兼容. 
-   您可以将这些代码片段导入您选择的文本编辑器(vscode,atom,sublime),使用找到的文件[这个回购](https://github.com/Rob-Rychs/30-seconds-of-code-texteditorsnippets). 
-   您可以使用这些片段导入alfred 3[这个文件](https://github.com/lslvxy/30-seconds-of-code-alfredsnippets). 

#### 包

⚠️**警告: **片段不是生产准备好的. 

你可以找到一个包含所有片段的包[NPM](https://www.npmjs.com/package/30-seconds-of-code). 

```bash
# With npm
npm install 30-seconds-of-code

# With yarn
yarn add 30-seconds-of-code
```

cdn链接

-   [es2017 full(umd)](https://unpkg.com/30-seconds-of-code)
-   [es5缩小(umd)](https://unpkg.com/30-seconds-of-code/dist/_30s.es5.min.js)

<details>

**浏览器**

> 重要的是: 更换`SRC`与完整版本链接和所需的目标规格(如es5缩小)): 

```html
<script src="https://unpkg.com/30-seconds-of-code"></script>
<script>
  _30s.average(1, 2, 3);
</script>
```

**节点**

```js
// CommonJS
const _30s = require('30-seconds-of-code');
_30s.average(1, 2, 3);

// ES Modules
import _30s from '30-seconds-of-code';
_30s.average(1, 2, 3);
```

直接导入片段: 

```js
// CommonJS
const { average } = require('30-seconds-of-code');
average(1, 2, 3);

// ES Modules
import { average } from '30-seconds-of-code';
average(1, 2, 3);
```

</details>

## 目录

### 🔌适配器

<details>
<summary>View contents</summary>

-   [`呼叫`](#call)
-   [`collectinto`](#collectinto)
-   [`翻动`](#flip)
-   [`pipefunctions`](#pipefunctions)
-   [`promisify`](#promisify)
-   [`传播开来`](#spreadover)

</details>

### 📚数组

<details>
<summary>View contents</summary>

-   [`块`](#chunk)
-   [`紧凑`](#compact)
-   [`countby`](#countby)
-   [`countoccurrences`](#countoccurrences)
-   [`deepflatten`](#deepflatten)
-   [`区别`](#difference)
-   [`differencewith`](#differencewith)
-   [`distinctvaluesofarray`](#distinctvaluesofarray)
-   [`dropelements`](#dropelements)
-   [`dropright`](#dropright)
-   [`everynth`](#everynth)
-   [`filternonunique`](#filternonunique)
-   [`sortedindex`](#findlast)
-   [`对称差`](#flatten)
-   [`尾巴`](#foreachright)
-   [`采取`](#groupby)
-   [`takeright`](#head)
-   [`联盟`](#indexofall)
-   [`无`](#initial)
-   [`压缩`](#initialize2darray)
-   [`zipobject`](#initializearraywithrange)
-   [`🌐浏览器`](#initializearraywithvalues)
-   [`arraytohtmllist`](#intersection)
-   [`bottomvisible`](#issorted)
-   [`复制到剪贴板`](#join)
-   [`的createElement`](#last)
-   [`createeventhub`](#longestitem)
-   [`CURRENTURL`](#mapobject)
-   [`detectdevicetype`](#maxn)
-   [`elementisvisibleinviewport`](#minn)
-   [`调用getScrollPosition`](#nthelement)
-   [`GetStyle为`](#partition)
-   [`hasclass`](#pick)
-   [`隐藏`](#pull)
-   [`httpsredirect`](#pullatindex)
-   [`离`](#pullatvalue)
-   [`上`](#reducedfilter)
-   [`onuserinputchange`](#remove)
-   [`重定向`](#sample)
-   [`runasync`](#samplesize)
-   [`滚动到顶部`](#shuffle)
-   [`的setStyle`](#similarity)
-   [`🗃️对象`](#sortedindex)
-   [`cleanobj`](#symmetricdifference)
-   [`等于`](#tail)
-   [`功能`](#take)
-   [`invertkeyvalues`](#takeright)
-   [`lowercasekeys`](#union)
-   [`映射键`](#without)
-   [`mapvalues`](#zip)
-   [`合并`](#zipobject)

</details>

### objectfrompairs

<details>
<summary>View contents</summary>

-   [`objecttopairs`](#arraytohtmllist)
-   [`排序依据`](#bottomvisible)
-   [`选择`](#copytoclipboard-)
-   [`shallowclone`](#createelement)
-   [`尺寸`](#createeventhub-)
-   [`转变`](#currenturl)
-   [`truthcheckcollection`](#detectdevicetype)
-   [`📜字符串`](#elementisvisibleinviewport)
-   [`字谜`](#getscrollposition)
-   [`bytesize`](#getstyle)
-   [`利用`](#hasclass)
-   [`capitalizeeveryword`](#hide)
-   [`decapitalize`](#httpsredirect)
-   [`escapehtml`](#off)
-   [`escaperegexp`](#on)
-   [`fromcamelcase`](#onuserinputchange-)
-   [`isabsoluteurl`](#redirect)
-   [`islowercase`](#runasync-)
-   [`isuppercase`](#scrolltotop)
-   [`面具`](#setstyle)
-   [`回文`](#show)
-   [`变复数`](#toggleclass)
-   [`reversestring`](#uuidgeneratorbrowser)

</details>

### sortcharactersinstring

<details>
<summary>View contents</summary>

-   [`splitlines`](#formatduration)
-   [`tocamelcase`](#getdaysdiffbetweendates)
-   [`tokebabcase`](#tomorrow)

</details>

### tosnakecase

<details>
<summary>View contents</summary>

-   [`truncatestring`](#chainasync)
-   [`unescapehtml`](#compose)
-   [`话`](#curry)
-   [`📃类型`](#defer)
-   [`将gettype`](#functionname)
-   [`IsArray的`](#memoize)
-   [`isarraylike`](#negate)
-   [`isboolean`](#once)
-   [`isfunction`](#runpromisesinseries)
-   [`一片空白`](#sleep)

</details>

### ISNUMBER

<details>
<summary>View contents</summary>

-   [`则IsObject`](#average)
-   [`isprimitive`](#averageby)
-   [`ispromiselike`](#clampnumber)
-   [`isstring`](#digitize)
-   [`issymbol`](#distance)
-   [`isvalidjson`](#elo-)
-   [`🔧实用程序`](#factorial)
-   [`cloneregexp`](#fibonacci)
-   [`合并`](#gcd)
-   [`coalescefactory`](#geometricprogression)
-   [`extendhex`](#hammingdistance)
-   [`geturlparameters`](#inrange)
-   [`hextorgb`](#isdivisible)
-   [`HTTPGET`](#iseven)
-   [`httppost`](#isprime)
-   [`parsecookie`](#lcm)
-   [`prettybytes`](#luhncheck)
-   [`randomhexcolorcode`](#maxby)
-   [`rgbtohex`](#median)
-   [`serializecookie`](#minby)
-   [`所用的时间`](#percentile)
-   [`todecimalmark`](#powerset)
-   [`toordinalsuffix`](#primes)
-   [`validatenumber`](#randomintarrayinrange)
-   [`YESNO`](#randomintegerinrange)
-   [`🔌适配器`](#randomnumberinrange)
-   [`呼叫`](#round)
-   [`给定一个键和一组参数,在给定上下文时调用它们. `](#sdbm)
-   [`主要用于组合. `](#standarddeviation)
-   [`使用闭包调用存储的参数存储的键. `](#sum)
-   [`⬆返回顶部`](#sumby)
-   [`collectinto`](#sumpower)
-   [`将接受数组的函数更改为可变参数函数. `](#tosafeinteger)

</details>

### 给定一个函数,返回一个闭包,将所有输入收集到一个数组接受函数中. 

<details>
<summary>View contents</summary>

-   [`⬆返回顶部`](#colorize)
-   [`翻动`](#hasflags)
-   [`flip将函数作为参数,然后将第一个参数作为最后一个参数. `](#istravisci)
-   [`返回一个包含可变参数输入的闭包,并在应用其余参数之前拼接最后一个参数以使其成为第一个参数. `](#jsontofile)
-   [`⬆返回顶部`](#readfilelines)
-   [`pipefunctions`](#untildify)
-   [`执行从左到右的功能组合. `](#uuidgeneratornode)

</details>

### 使用

<details>
<summary>View contents</summary>

-   [`array.reduce()`](#cleanobj)
-   [`与传播运算符(`](#equals-)
-   [`...`](#functions)
-   [`)执行从左到右的函数组合. 第一个(最左边的)函数可以接受一个或多个参数;`](#invertkeyvalues)
-   [`其余的功能必须是一元的. `](#lowercasekeys)
-   [`⬆返回顶部`](#mapkeys)
-   [`promisify`](#mapvalues)
-   [`转换异步函数以返回承诺. `](#merge)
-   [`使用currying返回一个返回a的函数`](#objectfrompairs)
-   [`诺言`](#objecttopairs)
-   [`即调用原始函数`](#orderby)
-   [`...休息`](#select)
-   [`运算符传入所有参数. `](#shallowclone)
-   [`在节点8+中,您可以使用`](#size)
-   [`util.promisify`](#transform)
-   [`⬆返回顶部`](#truthcheckcollection)

</details>

### 传播开来

<details>
<summary>View contents</summary>

-   [`接受一个可变参数函数并返回一个闭包,该闭包接受一个参数数组映射到该函数的输入. `](#anagrams)
-   [`使用闭包和展开操作符(`](#bytesize)
-   [`...`](#capitalize)
-   [`)将参数数组映射到函数的输入. `](#capitalizeeveryword)
-   [`⬆返回顶部`](#decapitalize)
-   [`📚数组`](#escapehtml)
-   [`块`](#escaperegexp)
-   [`将数组分组成一个指定大小的较小数组. `](#fromcamelcase)
-   [`使用`](#isabsoluteurl)
-   [`array.from()`](#islowercase)
-   [`创建一个新的数组,它适合将要生产的数据块`](#isuppercase)
-   [`array.slice()`](#mask)
-   [`将新数组的每个元素映射到块的长度`](#palindrome)
-   [`尺寸`](#pluralize)
-   [`如果原始数组不能均匀分割,最后的块将包含剩余的元素. `](#reversestring)
-   [`⬆返回顶部`](#sortcharactersinstring)
-   [`紧凑`](#splitlines)
-   [`从数组中删除falsey值. `](#tocamelcase)
-   [`使用`](#tokebabcase)
-   [`array.filter()`](#tosnakecase)
-   [`过滤出错误的值(`](#truncatestring)
-   [`假`](#unescapehtml)
-   [`,`](#words)

</details>

### 空值

<details>
<summary>View contents</summary>

-   [`,`](#gettype)
-   [`0`](#isarray)
-   [`,`](#isarraylike)
-   [`""`](#isboolean)
-   [`,`](#isfunction)
-   [`未定义`](#isnull)
-   [`,和`](#isnumber)
-   [`楠`](#isobject)
-   [`). `](#isprimitive)
-   [`⬆返回顶部`](#ispromiselike)
-   [`countby`](#isstring)
-   [`根据给定的函数对数组的元素进行分组,并返回每个组中元素的数量. `](#issymbol)
-   [`使用`](#isvalidjson)

</details>

### array.map()

<details>
<summary>View contents</summary>

-   [`将数组的值映射到函数或属性name.use`](#cloneregexp)
-   [`array.reduce()`](#coalesce)
-   [`创建一个对象,其中的密钥是从映射结果中产生的. `](#coalescefactory)
-   [`⬆返回顶部`](#extendhex)
-   [`countoccurrences`](#geturlparameters)
-   [`计数数组中值的出现次数. `](#hextorgb-)
-   [`使用`](#httpget)
-   [`array.reduce()`](#httppost)
-   [`每次遇到数组中的特定值时增加一个计数器. `](#parsecookie)
-   [`⬆返回顶部`](#prettybytes)
-   [`deepflatten`](#randomhexcolorcode)
-   [`深深地平整了一个阵列. `](#rgbtohex)
-   [`使用递归.use`](#serializecookie)
-   [`array.concat()`](#timetaken)
-   [`与一个空数组(`](#todecimalmark)
-   [`[]`](#toordinalsuffix)
-   [`)和扩散算子(`](#validatenumber)
-   [`...`](#yesno)

</details>

* * *

## )来展平数组. 递归地展平每个数组的元素. 

### ⬆返回顶部

区别

返回两个数组之间的差异. 

```js
const call = (key, ...args) => context => context[key](...args);
```

<details>
<summary>Examples</summary>

```js
Promise.resolve([1, 2, 3])
  .then(call('map', x => 2 * x))
  .then(console.log); //[ 2, 4, 6 ]
const map = call.bind(null, 'map');
Promise.resolve([1, 2, 3])
  .then(map(x => 2 * x))
  .then(console.log); //[ 2, 4, 6 ]
```

</details>

<br>[创建一个](#table-of-contents)

### 组

从

b

```js
const collectInto = fn => (...args) => fn(args);
```

<details>
<summary>Examples</summary>

```js
const Pall = collectInto(Promise.all.bind(Promise));
let p1 = Promise.resolve(1);
let p2 = Promise.resolve(2);
let p3 = new Promise(resolve => setTimeout(resolve, 2000, 3));
Pall(p1, p2, p3).then(console.log);
```

</details>

<br>[,然后使用](#table-of-contents)

### array.filter()

上

一个

```js
const flip = fn => (...args) => fn(args.pop(), ...args);
```

<details>
<summary>Examples</summary>

```js
let a = { name: 'John Smith' };
let b = {};
const mergeFrom = flip(Object.assign);
let mergePerson = mergeFrom.bind(null, a);
mergePerson(b); // == b
b = {};
Object.assign(b, a); // == b
```

</details>

<br>[只保留不包含的值](#table-of-contents)

### b

. 

⬆返回顶部`differencewith`滤除比较函数不返回的数组中的所有值`真正`. 

```js
const pipeFunctions = (...fns) => fns.reduce((f, g) => (...args) => g(f(...args)));
```

<details>
<summary>Examples</summary>

```js
const add5 = x => x + 5;
const multiply = (x, y) => x * y;
const multiplyAndAdd5 = pipeFunctions(multiply, add5);
multiplyAndAdd5(5, 2); // 15
```

</details>

<br>[使用](#table-of-contents)

### array.filter()

和

array.findindex()`找到合适的值. `⬆返回顶部`distinctvaluesofarray`返回数组的所有不同值. 

_使用es6[`组`](https://nodejs.org/api/util.html#util_util_promisify_original)_

```js
const promisify = func => (...args) =>
  new Promise((resolve, reject) =>
    func(...args, (err, result) => (err ? reject(err) : resolve(result)))
  );
```

<details>
<summary>Examples</summary>

```js
const delay = promisify((d, cb) => setTimeout(cb, d));
delay(2000).then(() => console.log('Hi!')); // // Promise resolves after 2s
```

</details>

<br>[和](#table-of-contents)

### ...休息

操作员放弃所有重复的值. 

⬆返回顶部`dropelements`删除数组中的元素,直到传递的函数返回

```js
const spreadOver = fn => argsArr => fn(...argsArr);
```

<details>
<summary>Examples</summary>

```js
const arrayMax = spreadOver(Math.max);
arrayMax([1, 2, 3]); // 3
```

</details>

<br>[真正](#table-of-contents)

* * *

## . 

### 返回数组中的其余元素. 

使用循环遍历数组

array.slice()`删除数组的第一个元素,直到函数的返回值为止`真正`. 返回其余元素. `⬆返回顶部`dropright`返回一个新的数组

```js
const chunk = (arr, size) =>
  Array.from({ length: Math.ceil(arr.length / size) }, (v, i) =>
    arr.slice(i * size, i * size + size)
  );
```

<details>
<summary>Examples</summary>

```js
chunk([1, 2, 3, 4, 5], 2); // [[1,2],[3,4],[5]]
```

</details>

<br>[ñ](#table-of-contents)

### 元素从右侧移除. 

使用

array.slice()`从右侧删除指定数量的元素. `⬆返回顶部`everynth`返回数组中的每个第n个元素. `使用`array.filter()`创建一个包含给定数组的每个第n个元素的新数组. `⬆返回顶部`filternonunique`过滤掉数组中的非唯一值. `使用`array.filter()`只包含唯一值的数组. `⬆返回顶部

```js
const compact = arr => arr.filter(Boolean);
```

<details>
<summary>Examples</summary>

```js
compact([0, 1, false, 2, '', 3, 'a', 'e' * 23, NaN, 's', 34]); // [ 1, 2, 3, 'a', 's', 34 ]
```

</details>

<br>[FindLast中](#table-of-contents)

### 返回提供的函数返回真值的最后一个元素. 

使用

array.filter()`删除其中的元素`FN`返回falsey值,`array.slice(-1)

```js
const countBy = (arr, fn) =>
  arr.map(typeof fn === 'function' ? fn : val => val[fn]).reduce((acc, val, i) => {
    acc[val] = (acc[val] ƜƜ 0) + 1;
    return acc;
  }, {});
```

<details>
<summary>Examples</summary>

```js
countBy([6.1, 4.2, 6.3], Math.floor); // {4: 1, 6: 2}
countBy(['one', 'two', 'three'], 'length'); // {3: 2, 5: 1}
```

</details>

<br>[得到最后一个. ](#table-of-contents)

### ⬆返回顶部

弄平

将阵列变平直至指定的深度. `使用递归,递减`深度

```js
const countOccurrences = (arr, val) => arr.reduce((a, v) => (v === val ? a + 1 : a + 0), 0);
```

<details>
<summary>Examples</summary>

```js
countOccurrences([1, 1, 2, 1, 2, 3], 1); // 3
```

</details>

<br>[使用深度为1的每个级别](#table-of-contents)

### array.reduce()

和

array.concat()`合并元素或数组.base case,for`深度`等于`1`停止递归. 第二个参数,`深度

```js
const deepFlatten = arr => [].concat(...arr.map(v => (Array.isArray(v) ? deepFlatten(v) : v)));
```

<details>
<summary>Examples</summary>

```js
deepFlatten([1, [2], [[3], 4], 5]); // [1,2,3,4,5]
```

</details>

<br>[只能平铺到一个深度](#table-of-contents)

### 1

(单一平坦). 

⬆返回顶部`foreachright`从数组的最后一个元素开始为每个数组元素执行一次提供的函数. `使用`array.slice(0)`克隆给定的数组,`array.reverse()`扭转它和`array.foreach()`遍历颠倒的数组. `⬆返回顶部

```js
const difference = (a, b) => {
  const s = new Set(b);
  return a.filter(x => !s.has(x));
};
```

<details>
<summary>Examples</summary>

```js
difference([1, 2, 3], [1, 2, 4]); // [3]
```

</details>

<br>[通过...分组](#table-of-contents)

### 根据给定的函数对数组的元素进行分组. 

使用`array.map()`将数组的值映射到函数或属性name.use

array.reduce()`创建一个对象,其中的密钥是从映射结果中产生的. `⬆返回顶部`头`返回列表的头部. 

```js
const differenceWith = (arr, val, comp) => arr.filter(a => val.findIndex(b => comp(a, b)) === -1);
```

<details>
<summary>Examples</summary>

```js
differenceWith([1, 1.2, 1.5, 3, 0], [1.9, 3, 0], (a, b) => Math.round(a) === Math.round(b)); // [1, 1.2]
```

</details>

<br>[使用](#table-of-contents)

### ARR \[0]

返回传递数组的第一个元素. 

⬆返回顶部`indexofall`返回所有的索引`VAL`在一个数组中. 

```js
const distinctValuesOfArray = arr => [...new Set(arr)];
```

<details>
<summary>Examples</summary>

```js
distinctValuesOfArray([1, 2, 2, 3, 4, 4, 5]); // [1,2,3,4,5]
```

</details>

<br>[如果](#table-of-contents)

### VAL

从不发生,返回`[]`. 

使用`array.foreach()`循环元素和`的Array.push()`为匹配元素存储索引. 返回索引数组. 

```js
const dropElements = (arr, func) => {
  while (arr.length > 0 && !func(arr[0])) arr = arr.slice(1);
  return arr;
};
```

<details>
<summary>Examples</summary>

```js
dropElements([1, 2, 3, 4], n => n >= 3); // [3,4]
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 初始

返回除最后一个数组外的所有元素. `使用`arr.slice(0,-1)

返回除数组最后一个元素外的所有元素. `⬆返回顶部`initialize2darray

```js
const dropRight = (arr, n = 1) => arr.slice(0, -n);
```

<details>
<summary>Examples</summary>

```js
dropRight([1, 2, 3]); // [1,2]
dropRight([1, 2, 3], 2); // [1]
dropRight([1, 2, 3], 42); // []
```

</details>

<br>[初始化给定宽度和高度以及值的二维数组. ](#table-of-contents)

### 使用

array.map()

生成h行,其中每个行都是一个大小为w的新数组,并用值初始化. `如果未提供该值,则默认为`空值

```js
const everyNth = (arr, nth) => arr.filter((e, i) => i % nth === nth - 1);
```

<details>
<summary>Examples</summary>

```js
everyNth([1, 2, 3, 4, 5, 6], 2); // [ 2, 4, 6 ]
```

</details>

<br>[. ](#table-of-contents)

### ⬆返回顶部

initializearraywithrange

初始化包含指定范围中的数字的数组`开始`和

```js
const filterNonUnique = arr => arr.filter(i => arr.indexOf(i) === arr.lastIndexOf(i));
```

<details>
<summary>Examples</summary>

```js
filterNonUnique([1, 2, 2, 3, 4, 4, 5]); // [1,3,5]
```

</details>

<br>[结束](#table-of-contents)

### 是包容性的,有共同的区别

步

. `使用`array.from(math.ceil((端+ 1开始)/步))`创建一个所需长度的数组(元素的数量等于`(端开始)/步`要么`(端+ 1开始)/步

```js
const findLast = (arr, fn) => arr.filter(fn).slice(-1);
```

<details>
<summary>Examples</summary>

```js
findLast([1, 2, 3, 4], n => n % 2 === 1); // 3
```

</details>

<br>[为包容性结束),](#table-of-contents)

### array.map()

在一定范围内填充所需的值. 您可以省略

开始`使用默认值`0`你可以省略`步`使用默认值`1`. `⬆返回顶部`initializearraywithvalues`使用指定的值初始化和填充数组. `使用`阵列(n)的`创建所需长度的数组,`填写(五)

```js
const flatten = (arr, depth = 1) =>
  depth != 1
    ? arr.reduce((a, v) => a.concat(Array.isArray(v) ? flatten(v, depth - 1) : v), [])
    : arr.reduce((a, v) => a.concat(v), []);
```

<details>
<summary>Examples</summary>

```js
flatten([1, [2], 3, 4]); // [1, 2, 3, 4]
flatten([1, [2, [3, [4, 5], 6], 7], 8], 2); // [1, 2, 3, [4, 5], 6, 7, 8]
```

</details>

<br>[以填充所需的值. 您可以省略](#table-of-contents)

### VAL

使用默认值

0`. `⬆返回顶部`路口`返回两个数组中存在的元素列表. `创建一个`组

```js
const forEachRight = (arr, callback) =>
  arr
    .slice(0)
    .reverse()
    .forEach(callback);
```

<details>
<summary>Examples</summary>

```js
forEachRight([1, 2, 3, 4], val => console.log(val)); // '4', '3', '2', '1'
```

</details>

<br>[从](#table-of-contents)

### b

,然后使用

array.filter()`上`一个`只保留包含的值`b

```js
const groupBy = (arr, fn) =>
  arr.map(typeof fn === 'function' ? fn : val => val[fn]).reduce((acc, val, i) => {
    acc[val] = (acc[val] ƜƜ []).concat(arr[i]);
    return acc;
  }, {});
```

<details>
<summary>Examples</summary>

```js
groupBy([6.1, 4.2, 6.3], Math.floor); // {4: [4.2], 6: [6.1, 6.3]}
groupBy(['one', 'two', 'three'], 'length'); // {3: ['one', 'two'], 5: ['three']}
```

</details>

<br>[. ](#table-of-contents)

### ⬆返回顶部

issorted

回报`1`如果数组按升序排序,

```js
const head = arr => arr[0];
```

<details>
<summary>Examples</summary>

```js
head([1, 2, 3]); // 1
```

</details>

<br>[-1](#table-of-contents)

### 如果按降序排序或

0`如果没有排序. `计算排序`方向`用于前两个元素`object.entries()`循环访问数组对象并对它们进行比较. 返回

0`如果`方向`改变或`方向

```js
const indexOfAll = (arr, val) => {
  const indices = [];
  arr.forEach((el, i) => el === val && indices.push(i));
  return indices;
};
```

<details>
<summary>Examples</summary>

```js
indexOfAll([1, 2, 3, 1, 2, 3], 1); // [0,3]
indexOfAll([1, 2, 3], 4); // []
```

</details>

<br>[如果到达最后一个元素. ](#table-of-contents)

### ⬆返回顶部

加入

将数组的所有元素连接到一个字符串并返回该字符串. `使用分隔符和结束分隔符. `使用

```js
const initial = arr => arr.slice(0, -1);
```

<details>
<summary>Examples</summary>

```js
initial([1, 2, 3]); // [1,2]
```

</details>

<br>[array.reduce()](#table-of-contents)

### 将元素组合成一个string.omit第二个参数,

分隔器

,使用默认的分隔符`''`. 试试第三个参数,`结束`,使用相同的值

```js
const initialize2DArray = (w, h, val = null) =>
  Array.from({ length: h }).map(() => Array.from({ length: w }).fill(val));
```

<details>
<summary>Examples</summary>

```js
initialize2DArray(2, 2, 0); // [[0,0], [0,0]]
```

</details>

<br>[分隔器](#table-of-contents)

### 默认. 

⬆返回顶部`持续`返回数组中的最后一个元素. `使用`arr.length  -  1`计算给定数组的最后一个元素的索引并返回它. `⬆返回顶部

longestitem`可以使用任意数量的可迭代对象或对象`长度`财产和返回最长的一个. `使用`中的Array.sort()`按所有参数排序`长度`,返回第一个(最长的). `⬆返回顶部`MapObject的`使用函数将数组值映射到对象,其中键值对由原始值作为键和映射值组成. `使用匿名内部函数作用域来声明未定义的内存空间,使用闭包存储返回值. `使用新的`排列`用数据集上的函数映射来存储数组,并使用逗号运算符返回第二步,而不需要从一个上下文移动到另一个上下文(由于关闭和操作顺序). `⬆返回顶部

```js
const initializeArrayWithRange = (end, start = 0, step = 1) =>
  Array.from({ length: Math.ceil((end + 1 - start) / step) }).map((v, i) => i * step + start);
```

<details>
<summary>Examples</summary>

```js
initializeArrayWithRange(5); // [0,1,2,3,4,5]
initializeArrayWithRange(7, 3); // [3,4,5,6,7]
initializeArrayWithRange(9, 0, 2); // [0,2,4,6,8]
```

</details>

<br>[MAXN](#table-of-contents)

### 返回

ñ

来自所提供阵列的最大元素. `如果`ñ`大于或等于提供的数组长度,则返回原始数组(按降序排列). `使用`中的Array.sort()`结合spread算子(`...`)创建一个数组的浅层克隆并按降序排序.use

```js
const initializeArrayWithValues = (n, val = 0) => Array(n).fill(val);
```

<details>
<summary>Examples</summary>

```js
initializeArrayWithValues(5, 2); // [2,2,2,2,2]
```

</details>

<br>[array.slice()](#table-of-contents)

### 获取指定数量的元素. 试试第二个参数,

ñ

,得到一个单元数组. `⬆返回顶部`明尼苏达州`返回`ñ`来自所提供阵列的最小元素. `如果`ñ`大于或等于提供的数组长度,则返回原始数组(按升序排序). `使用`中的Array.sort()

```js
const intersection = (a, b) => {
  const s = new Set(b);
  return a.filter(x => s.has(x));
};
```

<details>
<summary>Examples</summary>

```js
intersection([1, 2, 3], [4, 3, 2]); // [2,3]
```

</details>

<br>[结合spread算子(](#table-of-contents)

### ...

)创建数组的浅层克隆并按升序对其进行排序`array.slice()`获取指定数量的元素. 试试第二个参数,`ñ`,得到一个单元数组. `⬆返回顶部`nthelement

返回数组的第n个元素. `使用`array.slice()`在第一个地方获得包含第n个元素的数组. 如果索引超出范围,则返回`\[]`. 第二个参数,`ñ`,获取数组的第一个元素. `⬆返回顶部`划分`根据提供的函数对每个元素的真实性将元素分组为两个数组. 

```js
const isSorted = arr => {
  const direction = arr[0] > arr[1] ? -1 : 1;
  for (let [i, val] of arr.entries())
    if (i === arr.length - 1) return direction;
    else if ((val - arr[i + 1]) * direction > 0) return 0;
};
```

<details>
<summary>Examples</summary>

```js
isSorted([0, 1, 2, 2]); // 1
isSorted([4, 3, 2]); // -1
isSorted([4, 3, 5]); // 0
```

</details>

<br>[使用](#table-of-contents)

### array.reduce()

创建一个两个array.use的数组

的Array.push()`为其添加元素`FN`回报`真正`到第一个数组和元素`FN`回报`假`到第二个. `⬆返回顶部

```js
const join = (arr, separator = ',', end = separator) =>
  arr.reduce(
    (acc, val, i) =>
      i == arr.length - 2
        ? acc + val + end
        : i == arr.length - 1 ? acc + val : acc + val + separator,
    ''
  );
```

<details>
<summary>Examples</summary>

```js
join(['pen', 'pineapple', 'apple', 'pen'], ',', '&'); // "pen,pineapple,apple&pen"
join(['pen', 'pineapple', 'apple', 'pen'], ','); // "pen,pineapple,apple,pen"
join(['pen', 'pineapple', 'apple', 'pen']); // "pen,pineapple,apple,pen"
```

</details>

<br>[挑](#table-of-contents)

### 从对象中选择与给定键相对应的键值对. 

使用

array.reduce()`如果密钥存在于obj中,则将过滤/拾取的密钥转换回具有相应密钥值对的对象. `⬆返回顶部

```js
const last = arr => arr[arr.length - 1];
```

<details>
<summary>Examples</summary>

```js
last([1, 2, 3]); // 3
```

</details>

<br>[拉](#table-of-contents)

### 改变原始数组以过滤出指定的值. 

使用`array.filter()`和

array.includes()`提取不需要的值. 使用`array.length = 0`通过将数组的长度重置为零来改变数组中的传递`的Array.push()

```js
const longestItem = (...vals) => [...vals].sort((a, b) => b.length - a.length)[0];
```

<details>
<summary>Examples</summary>

```js
longestItem('this', 'is', 'a', 'testcase'); // 'testcase'
longestItem(...['a', 'ab', 'abc']); // 'abc'
longestItem(...['a', 'ab', 'abc'], 'abcd'); // 'abcd'
longestItem([1, 2, 3], [1, 2], [1, 2, 3, 4, 5]); // [1, 2, 3, 4, 5]
longestItem([1, 2, 3], 'foobar'); // 'foobar'
```

</details>

<br>[只用拉取的值重新填充它. ](#table-of-contents)

### (对于不改变原始数组的片段,请参阅

无

)`⬆返回顶部`pullatindex

```js
const mapObject = (arr, fn) =>
  (a => (
    (a = [arr, arr.map(fn)]), a[0].reduce((acc, val, ind) => ((acc[val] = a[1][ind]), acc), {})
  ))();
```

<details>
<summary>Examples</summary>

```js
const squareIt = arr => mapObject(arr, a => a * a);
squareIt([1, 2, 3]); // { 1: 1, 2: 4, 3: 9 }
```

</details>

<br>[改变原始数组以滤除指定索引处的值. ](#table-of-contents)

### 使用

array.filter()`和`array.includes()`提取不需要的值. 使用`array.length = 0

通过将数组的长度重置为零来改变数组中的传递`的Array.push()`重新填充它只有拉的values.use`的Array.push()`跟踪拉值`⬆返回顶部`pullatvalue`改变原始数组以过滤出指定的值. `返回删除的元素. 

```js
const maxN = (arr, n = 1) => [...arr].sort((a, b) => b - a).slice(0, n);
```

<details>
<summary>Examples</summary>

```js
maxN([1, 2, 3]); // [3]
maxN([1, 2, 3], 2); // [3,2]
```

</details>

<br>[使用](#table-of-contents)

### array.filter()

和`array.includes()`提取不需要的值. 使用`array.length = 0`通过将数组的长度重置为零来改变数组中的传递

的Array.push()`重新填充它只有拉的values.use`的Array.push()`跟踪拉值`⬆返回顶部`reducedfilter`过滤基于条件的对象数组,同时也过滤未指定的键. `使用`array.filter()

```js
const minN = (arr, n = 1) => [...arr].sort((a, b) => a - b).slice(0, n);
```

<details>
<summary>Examples</summary>

```js
minN([1, 2, 3]); // [1]
minN([1, 2, 3], 2); // [1,2]
```

</details>

<br>[根据谓词过滤数组](#table-of-contents)

### FN

以便它返回条件返回真值的对象. 

在已过滤的数组上使用`array.map()`使用返回新对象`array.reduce()`过滤掉没有提供的密钥`按键`论据. 

```js
const nthElement = (arr, n = 0) => (n > 0 ? arr.slice(n, n + 1) : arr.slice(n))[0];
```

<details>
<summary>Examples</summary>

```js
nthElement(['a', 'b', 'c'], 1); // 'b'
nthElement(['a', 'b', 'b'], -3); // 'a'
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 去掉

从给定函数返回的数组中移除元素

假`. `使用`array.filter()`找到返回真值的数组元素`array.reduce()`使用删除元素`方法Array.splice()`.the`FUNC`被调用三个参数(`值,索引,数组`). 

```js
const partition = (arr, fn) =>
  arr.reduce(
    (acc, val, i, arr) => {
      acc[fn(val, i, arr) ? 0 : 1].push(val);
      return acc;
    },
    [[], []]
  );
```

<details>
<summary>Examples</summary>

```js
const users = [{ user: 'barney', age: 36, active: false }, { user: 'fred', age: 40, active: true }];
partition(users, o => o.active); // [[{ 'user': 'fred',    'age': 40, 'active': true }],[{ 'user': 'barney',  'age': 36, 'active': false }]]
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 样品

从数组中返回一个随机元素. 

使用`的Math.random()`生成一个随机数,乘以它

```js
const pick = (obj, arr) =>
  arr.reduce((acc, curr) => (curr in obj && (acc[curr] = obj[curr]), acc), {});
```

<details>
<summary>Examples</summary>

```js
pick({ a: 1, b: '2', c: 3 }, ['a', 'c']); // { 'a': 1, 'c': 3 }
```

</details>

<br>[长度](#table-of-contents)

### 并使用它将其四舍五入到最接近的整数

math.floor()

这个方法也适用于字符串. `⬆返回顶部`采样大小`得到`ñ`随机元素来自独特的键`排列`达到大小`排列

_. [`使用. 洗牌数组`](#without)fisher-yates算法_

```js
const pull = (arr, ...args) => {
  let argState = Array.isArray(args[0]) ? args[0] : args;
  let pulled = arr.filter((v, i) => !argState.includes(v));
  arr.length = 0;
  pulled.forEach(v => arr.push(v));
};
```

<details>
<summary>Examples</summary>

```js
let myArray = ['a', 'b', 'c', 'a', 'b', 'c'];
pull(myArray, 'a', 'c'); // myArray = [ 'b', 'b' ]
```

</details>

<br>[. 使用](#table-of-contents)

### array.slice()

获得第一名

ñ`elements.omit第二个参数,`ñ`从数组中随机获取一个元素. `⬆返回顶部`拖曳`随机化数组值的顺序,返回一个新的数组. `使用`fisher-yates算法`重新排列数组的元素. `⬆返回顶部

```js
const pullAtIndex = (arr, pullArr) => {
  let removed = [];
  let pulled = arr
    .map((v, i) => (pullArr.includes(i) ? removed.push(v) : v))
    .filter((v, i) => !pullArr.includes(i));
  arr.length = 0;
  pulled.forEach(v => arr.push(v));
  return removed;
};
```

<details>
<summary>Examples</summary>

```js
let myArray = ['a', 'b', 'c', 'd'];
let pulled = pullAtIndex(myArray, [1, 3]); // myArray = [ 'a', 'c' ] , pulled = [ 'b', 'd' ]
```

</details>

<br>[相似](#table-of-contents)

### 返回出现在两个数组中的元素数组. 

使用

array.filter()`删除不属于的部分`值`,确定使用`array.includes()`. `⬆返回顶部`sortedindex`返回值应该插入到数组中的最低索引,以便维护其排序顺序. `检查数组是否按降序排列(松散地).use`array.findindex()

```js
const pullAtValue = (arr, pullArr) => {
  let removed = [],
    pushToRemove = arr.forEach((v, i) => (pullArr.includes(v) ? removed.push(v) : v)),
    mutateTo = arr.filter((v, i) => !pullArr.includes(v));
  arr.length = 0;
  mutateTo.forEach(v => arr.push(v));
  return removed;
};
```

<details>
<summary>Examples</summary>

```js
let myArray = ['a', 'b', 'c', 'd'];
let pulled = pullAtValue(myArray, ['b', 'd']); // myArray = [ 'a', 'c' ] , pulled = [ 'b', 'd' ]
```

</details>

<br>[找到元素应该插入的适当索引. ](#table-of-contents)

### ⬆返回顶部

对称差

返回两个数组之间的对称差异. `创建一个`组`从每个数组中,然后使用`array.filter()`在他们每个人只保留价值不包含在其他. `⬆返回顶部`尾巴`返回数组中除第一个元素外的所有元素. `返回`array.slice(1)

```js
const reducedFilter = (data, keys, fn) =>
  data.filter(fn).map(el =>
    keys.reduce((acc, key) => {
      acc[key] = el[key];
      return acc;
    }, {})
  );
```

<details>
<summary>Examples</summary>

```js
const data = [
  {
    id: 1,
    name: 'john',
    age: 24
  },
  {
    id: 2,
    name: 'mike',
    age: 50
  }
];

reducedFilter(data, ['id', 'name'], item => item.age > 24); // [{ id: 2, name: 'mike'}]
```

</details>

<br>[如果数组的](#table-of-contents)

### 长度

超过`1`否则,返回整个数组. 

⬆返回顶部`采取`返回一个数组,其中有n个元素从开头删除. `使用`array.slice()`用以创建一个数组的片段`ñ`从一开始就采取的元素. `⬆返回顶部`takeright`返回一个数组,其中包含从结尾删除的n个元素. 

```js
const remove = (arr, func) =>
  Array.isArray(arr)
    ? arr.filter(func).reduce((acc, val) => {
        arr.splice(arr.indexOf(val), 1);
        return acc.concat(val);
      }, [])
    : [];
```

<details>
<summary>Examples</summary>

```js
remove([1, 2, 3, 4], n => n % 2 == 0); // [2, 4]
```

</details>

<br>[使用](#table-of-contents)

### array.slice()

用以创建一个数组的片段

ñ`从最后采取的元素. `⬆返回顶部`联盟`返回两个数组中的任何一个元素. `创建一个`组

```js
const sample = arr => arr[Math.floor(Math.random() * arr.length)];
```

<details>
<summary>Examples</summary>

```js
sample([3, 7, 9, 11]); // 9
```

</details>

<br>[与所有值](#table-of-contents)

### 一个

和`b`并转换为一个数组. `⬆返回顶部`无`过滤出具有指定值之一的数组元素. `使用

array.filter()[创建一个数组排除(使用](https://github.com/chalarangelo/30-seconds-of-code#shuffle)!array.includes()`)所有给定的值. `(用于改变原始数组的细节请参阅`拉`)`⬆返回顶部`压缩

```js
const sampleSize = ([...arr], n = 1) => {
  let m = arr.length;
  while (m) {
    const i = Math.floor(Math.random() * m--);
    [arr[m], arr[i]] = [arr[i], arr[m]];
  }
  return arr.slice(0, n);
};
```

<details>
<summary>Examples</summary>

```js
sampleSize([1, 2, 3], 2); // [3,1]
sampleSize([1, 2, 3], 4); // [2,3,1]
```

</details>

<br>[创建一组元素,根据原始数组中的位置进行分组. ](#table-of-contents)

### 使用

math.max.apply()

获取参数中最长的数组. 创建一个具有该长度作为返回值并使用的数组[array.from()](https://github.com/chalarangelo/30-seconds-of-code#shuffle)用一个映射函数来创建一个分组元素数组. 如果参数数组的长度不同,

```js
const shuffle = ([...arr]) => {
  let m = arr.length;
  while (m) {
    const i = Math.floor(Math.random() * m--);
    [arr[m], arr[i]] = [arr[i], arr[m]];
  }
  return arr;
};
```

<details>
<summary>Examples</summary>

```js
const foo = [1, 2, 3];
shuffle(foo); // [2,3,1], foo = [1,2,3]
```

</details>

<br>[未定义](#table-of-contents)

### 用于没有价值的地方. 

⬆返回顶部

zipobject`给定一个有效的属性标识符和一个值数组,返回一个将属性关联到值的对象. `由于对象可以具有未定义的值,但不具有未定义的属性指针,因此使用属性数组来决定使用结果对象的结构`array.reduce()`. `⬆返回顶部`🌐浏览器

```js
const similarity = (arr, values) => arr.filter(v => values.includes(v));
```

<details>
<summary>Examples</summary>

```js
similarity([1, 2, 3], [1, 2, 4]); // [1,2]
```

</details>

<br>[arraytohtmllist](#table-of-contents)

### 将给定的数组元素转换为

&lt;LI>

标签并将它们附加到给定ID的列表中. `使用`array.map()

```js
const sortedIndex = (arr, n) => {
  const isDescending = arr[0] > arr[arr.length - 1];
  const index = arr.findIndex(el => (isDescending ? n >= el : n <= el));
  return index === -1 ? arr.length : index;
};
```

<details>
<summary>Examples</summary>

```js
sortedIndex([5, 3, 2, 1], 4); // 1
sortedIndex([30, 50], 40); // 1
```

</details>

<br>[和](#table-of-contents)

### document.queryselector()

创建一个html标签列表. 

⬆返回顶部`bottomvisible`回报`真正`如果页面的底部可见,

```js
const symmetricDifference = (a, b) => {
  const sA = new Set(a),
    sB = new Set(b);
  return [...a.filter(x => !sB.has(x)), ...b.filter(x => !sA.has(x))];
};
```

<details>
<summary>Examples</summary>

```js
symmetricDifference([1, 2, 3], [1, 2, 4]); // [3,4]
```

</details>

<br>[假](#table-of-contents)

### 除此以外. 

使用

scrolly`,`scrollHeight属性`和`clientheight`以确定页面的底部是否可见. `⬆返回顶部

```js
const tail = arr => (arr.length > 1 ? arr.slice(1) : arr);
```

<details>
<summary>Examples</summary>

```js
tail([1, 2, 3]); // [2,3]
tail([1]); // [1]
```

</details>

<br>[复制到剪贴板](#table-of-contents)

### 将一个字符串复制到剪贴板. 

仅作为用户行为的结果(即在内部

点击`事件监听器). `创建一个新的`<textarea>的`元素,用提供的数据填充它并将其添加到html document.use

```js
const take = (arr, n = 1) => arr.slice(0, n);
```

<details>
<summary>Examples</summary>

```js
take([1, 2, 3], 5); // [1, 2, 3]
take([1, 2, 3], 0); // []
```

</details>

<br>[selection.getrangeat()](#table-of-contents)

### 存储选定范围(如果有).use

document.execcommand( '复制')

复制到剪贴板. 删除`<textarea>的`元素从html文档中最终使用`选择(). 的AddRange()`恢复原来的选定范围(如果有的话). 

```js
const takeRight = (arr, n = 1) => arr.slice(arr.length - n, arr.length);
```

<details>
<summary>Examples</summary>

```js
takeRight([1, 2, 3], 2); // [ 2, 3 ]
takeRight([1, 2, 3]); // [3]
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 的createElement

从字符串中创建一个元素(不附加到文档中). 

如果给定的字符串包含多个元素,则只返回第一个元素. `使用`使用document.createElement()`创建一个新的元素`的innerHTML`到作为参数提供的字符串. `使用

```js
const union = (a, b) => Array.from(new Set([...a, ...b]));
```

<details>
<summary>Examples</summary>

```js
union([1, 2, 3], [4, 3, 2]); // [1,2,3,4]
```

</details>

<br>[parentnode.firstelementchild](#table-of-contents)

### 返回字符串的元素版本. 

⬆返回顶部

createeventhub`创建一个pub / sub(`发布 - 订阅`)事件中心与`发射

_,[`上`](#pull),和_

```js
const without = (arr, ...args) => arr.filter(v => !args.includes(v));
```

<details>
<summary>Examples</summary>

```js
without([2, 1, 2, 3], 1, 2); // [3]
```

</details>

<br>[离](#table-of-contents)

### 方法. 

使用

的Object.create(空)`创造一个空洞`枢纽`不继承属性的对象`Object.prototype中`. 对于`发射

```js
const zip = (...arrays) => {
  const maxLength = Math.max(...arrays.map(x => x.length));
  return Array.from({ length: maxLength }).map((_, i) => {
    return Array.from({ length: arrays.length }, (_, k) => arrays[k][i]);
  });
};
```

<details>
<summary>Examples</summary>

```js
zip(['a', 'b'], [1, 2], [true, false]); // [['a', 1, true], ['b', 2, false]]
zip(['a'], [1, 2], [true, false]); // [['a', 1, true], [undefined, 2, false]]
```

</details>

<br>[,根据. 解析处理程序数组](#table-of-contents)

### 事件

参数,然后运行每一个

array.foreach()`通过传递数据作为参数`上

```js
const zipObject = (props, values) =>
  props.reduce((obj, prop, index) => ((obj[prop] = values[index]), obj), {});
```

<details>
<summary>Examples</summary>

```js
zipObject(['a', 'b', 'c'], [1, 2]); // {a: 1, b: 2, c: undefined}
zipObject(['a', 'b'], [1, 2, 3]); // {a: 1, b: 2}
```

</details>

<br>[,为事件创建一个数组,如果它尚不存在,则使用](#table-of-contents)

* * *

## 的Array.push()

### 添加array.for的句柄

离`, 使用`array.findindex()

找到事件数组中的处理程序的索引并将其删除`方法Array.splice()`. `⬆返回顶部`CURRENTURL

```js
const arrayToHtmlList = (arr, listID) =>
  arr.map(item => (document.querySelector('#' + listID).innerHTML += `<li>${item}</li>`));
```

<details>
<summary>Examples</summary>

```js
arrayToHtmlList(['item 1', 'item 2'], 'myListID');
```

</details>

<br>[返回当前的网址. ](#table-of-contents)

### 使用

window.location.href`获取当前网址. `⬆返回顶部`detectdevicetype`检测到网站在移动设备或台式机/笔记本电脑上打开. 

使用正则表达式来测试`navigator.userAgent的`财产来确定设备是移动设备还是台式机/笔记本电脑. `⬆返回顶部`elementisvisibleinviewport`回报`真正

```js
const bottomVisible = () =>
  document.documentElement.clientHeight + window.scrollY >=
  (document.documentElement.scrollHeight ƜƜ document.documentElement.clientHeight);
```

<details>
<summary>Examples</summary>

```js
bottomVisible(); // true
```

</details>

<br>[如果指定的元素在视口中可见,](#table-of-contents)

### 假![advanced](/advanced.svg)

除此以外. `使用`element.getboundingclientrect()

和`window.inner(宽度Ɯ高度)`valuesto确定给定的元素在viewport中是否可见. 第二个参数用于确定元素是否完全可见,或者指定`真正`以确定是否部分可见. `⬆返回顶部`调用getScrollPosition`返回当前页面的滚动位置. `使用`pagexoffset`和

```js
const copyToClipboard = str => {
  const el = document.createElement('textarea');
  el.value = str;
  el.setAttribute('readonly', '');
  el.style.position = 'absolute';
  el.style.left = '-9999px';
  document.body.appendChild(el);
  const selected =
    document.getSelection().rangeCount > 0 ? document.getSelection().getRangeAt(0) : false;
  el.select();
  document.execCommand('copy');
  document.body.removeChild(el);
  if (selected) {
    document.getSelection().removeAllRanges();
    document.getSelection().addRange(selected);
  }
};
```

<details>
<summary>Examples</summary>

```js
copyToClipboard('Lorem ipsum'); // 'Lorem ipsum' copied to clipboard.
```

</details>

<br>[pageyoffset](#table-of-contents)

### 如果他们被定义,否则

scrollleft

和`scrollTop的`你可以省略`埃尔`使用默认值`窗口`. 

```js
const createElement = str => {
  const el = document.createElement('div');
  el.innerHTML = str;
  return el.firstElementChild;
};
```

<details>
<summary>Examples</summary>

```js
const el = createElement(
  `<div class="container">
    <p>Hello!</p>
  </div>`
);
console.log(el.className); // 'container'
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### GetStyle为![advanced](/advanced.svg)

返回指定元素的css规则的值. [使用](https://en.wikipedia.org/wiki/Publish%E2%80%93subscribe_pattern)window.getcomputedstyle()`获取指定元素的css规则的值. `⬆返回顶部`hasclass`回报`真正`如果元素具有指定的类,

假`除此以外. `使用`element.classlist.contains()`检查元素是否具有指定的类. `⬆返回顶部`隐藏`隐藏指定的所有元素. `使用扩展运算符(`...`)和`array.foreach()`申请`显示: 无`到指定的每个元素. `⬆返回顶部`httpsredirect`如果页面当前位于http,则将该页面重定向到https. `另外,按下后退按钮并不会将其取回到历史记录中的http页面. `使用`location.protocol`获取当前正在使用的协议. `如果它不是https,请使用

```js
const createEventHub = () => ({
  hub: Object.create(null),
  emit(event, data) {
    (this.hub[event] ƜƜ []).forEach(handler => handler(data));
  },
  on(event, handler) {
    if (!this.hub[event]) this.hub[event] = [];
    this.hub[event].push(handler);
  },
  off(event, handler) {
    const i = (this.hub[event] ƜƜ []).findIndex(h => h === handler);
    if (i > -1) this.hub[event].splice(i, 1);
  }
});
```

<details>
<summary>Examples</summary>

```js
const handler = data => console.log(data);
const hub = createEventHub();
let increment = 0;

// Subscribe: listen for different types of events
hub.on('message', handler);
hub.on('message', () => console.log('Message event fired'));
hub.on('increment', () => increment++);

// Publish: emit events to invoke all handlers subscribed to them, passing the data to them as an argument
hub.emit('message', 'hello world'); // logs 'hello world' and 'Message event fired'
hub.emit('message', { hello: 'world' }); // logs the object and 'Message event fired'
hub.emit('increment'); // `increment` variable is now 1

// Unsubscribe: stop a specific handler from listening to the 'message' event
hub.off('message', handler);
```

</details>

<br>[location.replace()](#table-of-contents)

### 用https版本的页面替换现有的页面. 

使用

location.href`得到完整的地址,并与之分开`string.split()

```js
const currentURL = () => window.location.href;
```

<details>
<summary>Examples</summary>

```js
currentURL(); // 'https://google.com'
```

</details>

<br>[并移除url的协议部分. ](#table-of-contents)

### ⬆返回顶部

离

从元素中删除事件侦听器. `使用`eventtarget.removeeventlistener()

```js
const detectDeviceType = () =>
  /AndroidƜwebOSƜiPhoneƜiPadƜiPodƜBlackBerryƜIEMobileƜOpera Mini/i.test(navigator.userAgent)
    ? 'Mobile'
    : 'Desktop';
```

<details>
<summary>Examples</summary>

```js
detectDeviceType(); // "Mobile" or "Desktop"
```

</details>

<br>[从元素中删除事件监听器. ](#table-of-contents)

### 省略第四个参数

OPTS`使用`假`或者根据添加事件侦听器时使用的选项来指定它. `⬆返回顶部

上`将事件侦听器添加到具有使用事件委派功能的元素. `使用`eventtarget.addeventlistener()`将一个事件监听器添加到一个元素. `如果有的话`目标

```js
const elementIsVisibleInViewport = (el, partiallyVisible = false) => {
  const { top, left, bottom, right } = el.getBoundingClientRect();
  const { innerHeight, innerWidth } = window;
  return partiallyVisible
    ? ((top > 0 && top < innerHeight) ƜƜ (bottom > 0 && bottom < innerHeight)) &&
        ((left > 0 && left < innerWidth) ƜƜ (right > 0 && right < innerWidth))
    : top >= 0 && left >= 0 && bottom <= innerHeight && right <= innerWidth;
};
```

<details>
<summary>Examples</summary>

```js
// e.g. 100x100 viewport and a 10x10px element at position {top: -1, left: 0, bottom: 9, right: 10}
elementIsVisibleInViewport(el); // false - (not fully visible)
elementIsVisibleInViewport(el, true); // true - (partially visible)
```

</details>

<br>[提供给选项对象的属性,确保事件目标匹配指定的目标,然后通过提供正确的值来调用回调](#table-of-contents)

### 这个

context.returns对自定义委托函数的引用,以便可以使用

离`. 忽略`OPTS`默认为非委托行为和事件冒泡. `⬆返回顶部`onuserinputchange`每当用户输入类型改变时运行回调(`老鼠`要么`触摸`). `用于根据输入设备启用/禁用代码. `这个过程是动态的,适用于混合设备(例如触摸屏笔记本电脑). 

```js
const getScrollPosition = (el = window) => ({
  x: el.pageXOffset !== undefined ? el.pageXOffset : el.scrollLeft,
  y: el.pageYOffset !== undefined ? el.pageYOffset : el.scrollTop
});
```

<details>
<summary>Examples</summary>

```js
getScrollPosition(); // {x: 0, y: 200}
```

</details>

<br>[使用两个事件监听器. ](#table-of-contents)

### 承担

老鼠

最初输入并绑定一个`touchstart`事件侦听器到文档. 

```js
const getStyle = (el, ruleName) => getComputedStyle(el)[ruleName];
```

<details>
<summary>Examples</summary>

```js
getStyle(document.querySelector('p'), 'font-size'); // '16px'
```

</details>

<br>[上](#table-of-contents)

### touchstart

,添加一个`鼠标移动`事件监听器连续听两次`鼠标移动`事件在20ms内发射,使用

performance.now()`. 在这些情况下,将输入类型作为参数运行回调. `⬆返回顶部

```js
const hasClass = (el, className) => el.classList.contains(className);
```

<details>
<summary>Examples</summary>

```js
hasClass(document.querySelector('p.special'), 'special'); // true
```

</details>

<br>[重定向](#table-of-contents)

### 重定向到指定的网址. 

使用

window.location.href`要么`window.location.replace()`重定向到`网址`. 传递第二个参数来模拟链接点击(`真正

```js
const hide = (...el) => [...el].forEach(e => (e.style.display = 'none'));
```

<details>
<summary>Examples</summary>

```js
hide(...document.querySelectorAll('img')); // Hides all <img> elements on the page
```

</details>

<br>[- 默认)或http重定向(](#table-of-contents)

### 假

). 

⬆返回顶部`runasync`通过使用a在一个单独的线程中运行一个函数`网络工作者`,允许长时间运行的功能不会阻止用户界面. `创建一个新的`工人`用一个`BLOB

```js
const httpsRedirect = () => {
  if (location.protocol !== 'https:') location.replace('https://' + location.href.split('//')[1]);
};
```

<details>
<summary>Examples</summary>

```js
httpsRedirect(); // If you are on http://mydomain.com, you are redirected to https://mydomain.com
```

</details>

<br>[对象url,其内容应该是提供的函数的字符串化版本. 立即发布调用函数的返回值. 返回promise,收听](#table-of-contents)

### 的onMessage

和

的onerror`事件并解析从工作人员返回的数据,或抛出错误. `⬆返回顶部`滚动到顶部`平滑滚动到页面顶部. `从顶部使用获得距离`document.documentelement.scrolltop

```js
const off = (el, evt, fn, opts = false) => el.removeEventListener(evt, fn, opts);
```

<details>
<summary>Examples</summary>

```js
const fn = () => console.log('!');
document.body.addEventListener('click', fn);
off(document.body, 'click', fn); // no longer logs '!' upon clicking on the page
```

</details>

<br>[要么](#table-of-contents)

### 的document.body.scrollTop

. 从顶部滚动一小部分距离. 

使用`window.requestanimationframe()`为动画滚动. `⬆返回顶部`的setStyle`设置指定元素的css规则的值. `使用[`element.style`](#off)将指定元素的css规则的值设置为`VAL`. 

```js
const on = (el, evt, fn, opts = {}) => {
  const delegatorFn = e => e.target.matches(opts.target) && fn.call(e.target, e);
  el.addEventListener(evt, opts.target ? delegatorFn : fn, opts.options ƜƜ false);
  if (opts.target) return delegatorFn;
};
```

<details>
<summary>Examples</summary>

```js
const fn = () => console.log('!');
on(document.body, 'click', fn); // logs '!' upon clicking the body
on(document.body, 'click', fn, { target: 'p' }); // logs '!' upon clicking a `p` element child of the body
on(document.body, 'click', fn, { options: true }); // use capturing instead of bubbling
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 显示![advanced](/advanced.svg)

显示了所有指定的元素. `使用扩展运算符(`...`)和`array.foreach()

清除`显示`属性指定的每个元素. `⬆返回顶部`toggleclass`切换一个元素的类. `使用`element.classlist.toggle()`切换元素的指定类. `⬆返回顶部`uuidgeneratorbrowser`在浏览器中生成一个uuid. `使用

```js
const onUserInputChange = callback => {
  let type = 'mouse',
    lastTime = 0;
  const mousemoveHandler = () => {
    const now = performance.now();
    if (now - lastTime < 20)
      (type = 'mouse'), callback(type), document.removeEventListener('mousemove', mousemoveHandler);
    lastTime = now;
  };
  document.addEventListener('touchstart', () => {
    if (type === 'touch') return;
    (type = 'touch'), callback(type), document.addEventListener('mousemove', mousemoveHandler);
  });
};
```

<details>
<summary>Examples</summary>

```js
onUserInputChange(type => {
  console.log('The user is now using', type, 'as an input method.');
});
```

</details>

<br>[加密](#table-of-contents)

### API来生成一个uuid,符合

rfc4122

版本4. `⬆返回顶部`⏱日期`formatduration`返回给定毫秒数的可读格式. `划分`女士`用适当的值来获得适当的值`天`,`小时

```js
const redirect = (url, asLink = true) =>
  asLink ? (window.location.href = url) : window.location.replace(url);
```

<details>
<summary>Examples</summary>

```js
redirect('https://google.com');
```

</details>

<br>[,](#table-of-contents)

### 分钟![advanced](/advanced.svg)

,[第二](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers)和

毫秒`. 使用`object.entries()`同`array.filter()`仅保留非零值`array.map()`为每个值创建字符串,适当复数化`string.join(',')

```js
const runAsync = fn => {
  const blob = `var fn = ${fn.toString()}; postMessage(fn());`;
  const worker = new Worker(
    URL.createObjectURL(new Blob([blob]), {
      type: 'application/javascript; charset=utf-8'
    })
  );
  return new Promise((res, rej) => {
    worker.onmessage = ({ data }) => {
      res(data), worker.terminate();
    };
    worker.onerror = err => {
      rej(err), worker.terminate();
    };
  });
};
```

<details>
<summary>Examples</summary>

```js
const longRunningFunction = () => {
  let result = 0;
  for (let i = 0; i < 1000; i++) {
    for (let j = 0; j < 700; j++) {
      for (let k = 0; k < 300; k++) {
        result = result + i + j + k;
      }
    }
  }
  return result;
};
/*
  NOTE: Since the function is running in a different context, closures are not supported.
  The function supplied to `runAsync` gets stringified, so everything becomes literal.
  All variables and functions must be defined inside.
*/
runAsync(longRunningFunction).then(console.log); // 209685000000
runAsync(() => 10 ** 3).then(console.log); // 1000
let outsideVariable = 50;
runAsync(() => typeof outsideVariable).then(console.log); // 'undefined'
```

</details>

<br>[将这些值组合成一个字符串. ](#table-of-contents)

### ⬆返回顶部

getdaysdiffbetweendates

返回两个日期之间的差异(以天计). `计算两者之间的差异(以天计)`日期`对象. `⬆返回顶部`明天`导致明天的date.use的字符串表示

```js
const scrollToTop = () => {
  const c = document.documentElement.scrollTop ƜƜ document.body.scrollTop;
  if (c > 0) {
    window.requestAnimationFrame(scrollToTop);
    window.scrollTo(0, c - c / 8);
  }
};
```

<details>
<summary>Examples</summary>

```js
scrollToTop();
```

</details>

<br>[新日期()](#table-of-contents)

### 获取今天的日期,添加

86400000

秒(24小时),使用`date.toisostring()`将日期对象转换为字符串. `⬆返回顶部`🎛️功能

```js
const setStyle = (el, ruleName, val) => (el.style[ruleName] = val);
```

<details>
<summary>Examples</summary>

```js
setStyle(document.querySelector('p'), 'font-size', '20px'); // The first <p> element on the page will have a font-size of 20px
```

</details>

<br>[chainasync](#table-of-contents)

### 链异步功能. 

通过一系列包含异步事件的函数进行循环调用

下一个`当每个异步事件完成时. `⬆返回顶部`撰写`执行从右到左的功能组合. `使用`array.reduce()

```js
const show = (...el) => [...el].forEach(e => (e.style.display = ''));
```

<details>
<summary>Examples</summary>

```js
show(...document.querySelectorAll('img')); // Shows all <img> elements on the page
```

</details>

<br>[执行从右到左的函数组合. 最后(最右边)的函数可以接受一个或多个参数;](#table-of-contents)

### 其余的功能必须是一元的. 

⬆返回顶部

咖喱`咖喱功能. `使用递归. 如果提供的参数数量(

```js
const toggleClass = (el, className) => el.classList.toggle(className);
```

<details>
<summary>Examples</summary>

```js
toggleClass(document.querySelector('p.special'), 'special'); // The paragraph will not have the 'special' class anymore
```

</details>

<br>[ARGS](#table-of-contents)

### )就足够了,调用传递函数

FN

. 另外,返回一个curried函数`FN`如果你想要一个接受可变数目参数的函数(一个可变参数函数,例如,[math.min()](https://www.ietf.org/rfc/rfc4122.txt)),您可以选择将参数的数量传递给第二个参数

```js
const UUIDGeneratorBrowser = () =>
  ([1e7] + -1e3 + -4e3 + -8e3 + -1e11).replace(/[018]/g, c =>
    (c ^ (crypto.getRandomValues(new Uint8Array(1))[0] & (15 >> (c / 4)))).toString(16)
  );
```

<details>
<summary>Examples</summary>

```js
UUIDGeneratorBrowser(); // '7982fcfe-5721-4632-bede-6000885be57d'
```

</details>

<br>[元数](#table-of-contents)

* * *

## . 

### ⬆返回顶部

延缓

延迟调用一个函数,直到当前的调用栈被清除. `使用`的setTimeout()`以1ms的超时时间向浏览器事件队列添加新事件,并允许渲染引擎完成其工作. `使用传播(`...`)运算符为该函数提供任意数量的参数. `⬆返回顶部`functionname`记录功能的名称. `使用`console.debug()`和`名称`传递方法的属性以将方法名称记录到`调试`控制台的通道. `⬆返回顶部`memoize的`返回memoized(缓存)的功能. `通过实例化一个新的来创建一个空的缓存

```js
const formatDuration = ms => {
  if (ms < 0) ms = -ms;
  const time = {
    day: Math.floor(ms / 86400000),
    hour: Math.floor(ms / 3600000) % 24,
    minute: Math.floor(ms / 60000) % 60,
    second: Math.floor(ms / 1000) % 60,
    millisecond: Math.floor(ms) % 1000
  };
  return Object.entries(time)
    .filter(val => val[1] !== 0)
    .map(val => val[1] + ' ' + (val[1] !== 1 ? val[0] + 's' : val[0]))
    .join(', ');
};
```

<details>
<summary>Examples</summary>

```js
formatDuration(1001); // '1 second, 1 millisecond'
formatDuration(34325055574); // '397 days, 6 hours, 44 minutes, 15 seconds, 574 milliseconds'
```

</details>

<br>[地图](#table-of-contents)

### object.return函数通过首先检查该特定输入值的函数输出是否已经被缓存,或者如果没有,则存储并返回,从而将单个参数提供给memoized函数. 

该

功能`必须使用关键字才能让memoized函数拥有它`这个

```js
const getDaysDiffBetweenDates = (dateInitial, dateFinal) =>
  (dateFinal - dateInitial) / (1000 * 3600 * 24);
```

<details>
<summary>Examples</summary>

```js
getDaysDiffBetweenDates(new Date('2017-12-13'), new Date('2017-12-22')); // 9
```

</details>

<br>[如有必要,上下文会更改. 允许访问](#table-of-contents)

### 高速缓存

通过将其设置为返回函数的属性. `⬆返回顶部`否定`否定谓词功能. `采用谓词函数并应用not运算符(`!`)与它的论据. 

```js
const tomorrow = () => new Date(new Date().getTime() + 86400000).toISOString().split('T')[0];
```

<details>
<summary>Examples</summary>

```js
tomorrow(); // 2017-12-27 (if current date is 2017-12-26)
```

</details>

<br>[⬆返回顶部](#table-of-contents)

* * *

## 一旦

### 确保函数只被调用一次. 

利用封口,使用旗帜,

叫`,并将其设置为`真正

```js
const chainAsync = fns => {
  let curr = 0;
  const next = () => fns[curr++](next);
  next();
};
```

<details>
<summary>Examples</summary>

```js
chainAsync([
  next => {
    console.log('0 seconds');
    setTimeout(next, 1000);
  },
  next => {
    console.log('1 second');
  }
]);
```

</details>

<br>[一旦函数第一次被调用,阻止它被再次调用. ](#table-of-contents)

### 为了让功能有它的功能

这个

上下文改变了(比如在事件监听器中),`功能`关键字必须被使用,并且提供的函数必须具有应用的上下文. 允许使用剩余/传播给函数提供任意数量的参数(

```js
const compose = (...fns) => fns.reduce((f, g) => (...args) => f(g(...args)));
```

<details>
<summary>Examples</summary>

```js
const add5 = x => x + 5;
const multiply = (x, y) => x * y;
const multiplyAndAdd5 = compose(add5, multiply);
multiplyAndAdd5(5, 2); // 15
```

</details>

<br>[...](#table-of-contents)

### )运营商. 

⬆返回顶部

runpromisesinseries`运行一连串的承诺. `使用`array.reduce()`创建一个承诺链,每个承诺在解决时都会返回下一个承诺. `⬆返回顶部`睡觉`延迟异步函数的执行. `延迟执行一部分`异步`功能,通过睡觉,返回一个

```js
const curry = (fn, arity = fn.length, ...args) =>
  arity <= args.length ? fn(...args) : curry.bind(null, fn, arity, ...args);
```

<details>
<summary>Examples</summary>

```js
curry(Math.pow)(2)(10); // 1024
curry(Math.min, 3)(10)(50)(2); // 2
```

</details>

<br>[诺言](#table-of-contents)

### . 

⬆返回顶部

➗数学`平均`返回两个或更多数字中的一个的平均值. `使用`array.reduce()

```js
const defer = (fn, ...args) => setTimeout(fn, 1, ...args);
```

<details>
<summary>Examples</summary>

```js
// Example A:
defer(console.log, 'a'), console.log('b'); // logs 'b' then 'a'

// Example B:
document.querySelector('#someElement').innerHTML = 'Hello';
longRunningFunction(); //Browser will not update the HTML until this has finished
defer(longRunningFunction); // Browser will update the HTML then run the function
```

</details>

<br>[将每个值添加到一个累加器,用一个值进行初始化](#table-of-contents)

### 0

,除以

长度`的阵列. `⬆返回顶部`averageby`使用提供的函数将每个元素映射到一个值后,返回数组的平均值. `使用`array.map()

```js
const functionName = fn => (console.debug(fn.name), fn);
```

<details>
<summary>Examples</summary>

```js
functionName(Math.max); // max (logged in debug channel of console)
```

</details>

<br>[将每个元素映射到返回的值](#table-of-contents)

### FN

,

array.reduce()`将每个值添加到一个累加器,用一个值进行初始化`0`,除以`长度`的阵列. `⬆返回顶部`clampnumber`夹子

```js
const memoize = fn => {
  const cache = new Map();
  const cached = function(val) {
    return cache.has(val) ? cache.get(val) : cache.set(val, fn.call(this, val)) && cache.get(val);
  };
  cached.cache = cache;
  return cached;
};
```

<details>
<summary>Examples</summary>

```js
// See the `anagrams` snippet.
const anagramsCached = memoize(anagrams);
anagramsCached('javascript'); // takes a long time
anagramsCached('javascript'); // returns virtually instantly since it's now cached
console.log(anagramsCached.cache); // The cached anagrams map
```

</details>

<br>[NUM](#table-of-contents)

### 在由边界值规定的包含范围内

一个

和`b`. 

```js
const negate = func => (...args) => !func(...args);
```

<details>
<summary>Examples</summary>

```js
[1, 2, 3, 4, 5, 6].filter(negate(n => n % 2 == 0)); // [ 1, 3, 5 ]
```

</details>

<br>[如果](#table-of-contents)

### NUM

属于范围内,回报

NUM`. 另外,返回范围内最近的数字. `⬆返回顶部`数字化`将数字转换为数字数组. `将数字转换为字符串,使用扩展运算符(`...`)来构建一个array.use`array.map()`和`parseInt函数()

```js
const once = fn => {
  let called = false;
  return function(...args) {
    if (called) return;
    called = true;
    return fn.apply(this, args);
  };
};
```

<details>
<summary>Examples</summary>

```js
const startApp = function(event) {
  console.log(this, event); // document.body, MouseEvent
};
document.body.addEventListener('click', once(startApp)); // only runs `startApp` once upon click
```

</details>

<br>[将每个值转换为整数. ](#table-of-contents)

### ⬆返回顶部

距离

返回两点之间的距离. `使用`math.hypot()

```js
const runPromisesInSeries = ps => ps.reduce((p, next) => p.then(next), Promise.resolve());
```

<details>
<summary>Examples</summary>

```js
const delay = d => new Promise(r => setTimeout(r, d));
runPromisesInSeries([() => delay(1000), () => delay(2000)]); // Executes each promise sequentially, taking a total of 3 seconds to complete
```

</details>

<br>[计算两点之间的欧氏距离. ](#table-of-contents)

### ⬆返回顶部

ELO

计算两个或两个以上对手之间的新评分`Elo评级系统`. `它需要一系列预先评分并返回一个包含评分后数组的数组. 该数组应该从最佳表演者到最差表演者(赢家 - >失败者). `使用指数

```js
const sleep = ms => new Promise(resolve => setTimeout(resolve, ms));
```

<details>
<summary>Examples</summary>

```js
async function sleepyWork() {
  console.log("I'm going to sleep for 1 second.");
  await sleep(1000);
  console.log('I woke up after 1 second.');
}
```

</details>

<br>[\*\*](#table-of-contents)

* * *

## 运算符和数学运算符计算每个对手的预期分数(获胜的可能性),并通过评分计算每个分数的新评分,使用每个排列来以成对方式计算每个玩家的评分后评分. 

### 省略使用默认值的第二个参数

K系数

32. `⬆返回顶部`阶乘`计算一个数的阶乘. `使用递归.if`ñ`小于或等于

```js
const average = (...nums) => [...nums].reduce((acc, val) => acc + val, 0) / nums.length;
```

<details>
<summary>Examples</summary>

```js
average(...[1, 2, 3]); // 2
average(1, 2, 3); // 2
```

</details>

<br>[1](#table-of-contents)

### ,返回

1

. 否则,返回产品`ñ`和阶乘`n  -  1`. 如果发生异常`ñ`是一个负数. `⬆返回顶部`斐波那契`生成一个包含斐波纳契数列的数组,直到第n项. `创建一个特定长度的空数组,初始化前两个值(

```js
const averageBy = (arr, fn) =>
  arr.map(typeof fn === 'function' ? fn : val => val[fn]).reduce((acc, val) => acc + val, 0) /
  arr.length;
```

<details>
<summary>Examples</summary>

```js
averageBy([{ n: 4 }, { n: 2 }, { n: 8 }, { n: 6 }], o => o.n); // 5
averageBy([{ n: 4 }, { n: 2 }, { n: 8 }, { n: 6 }], 'n'); // 5
```

</details>

<br>[0](#table-of-contents)

### 和

1`). 使用`array.reduce()`使用最后两个值的总和将值添加到数组中,除了前两个值之外. `⬆返回顶部`GCD`计算两个或更多数字/数组之间的最大公约数. 

内在`_gcd`函数使用recursion.base的情况是什么时候`ÿ`等于

```js
const clampNumber = (num, a, b) => Math.max(Math.min(num, Math.max(a, b)), Math.min(a, b));
```

<details>
<summary>Examples</summary>

```js
clampNumber(2, 3, 5); // 3
clampNumber(1, -1, -5); // -1
```

</details>

<br>[0](#table-of-contents)

### . 

在这种情况下,返回

X`. 另外,返回gcd的`ÿ`和其余的部门`x / y的`. `⬆返回顶部

```js
const digitize = n => [...`${n}`].map(i => parseInt(i));
```

<details>
<summary>Examples</summary>

```js
digitize(123); // [1, 2, 3]
```

</details>

<br>[geometricprogression](#table-of-contents)

### 初始化包含指定范围中的数字的数组

开始

和`结束`是包容性的,两个术语之间的比例是

```js
const distance = (x0, y0, x1, y1) => Math.hypot(x1 - x0, y1 - y0);
```

<details>
<summary>Examples</summary>

```js
distance(1, 1, 2, 3); // 2.23606797749979
```

</details>

<br>[步](#table-of-contents)

### . 如果返回错误![advanced](/advanced.svg)

步[等于](https://en.wikipedia.org/wiki/Elo_rating_system)1

. `使用`array.from()`,`math.log()

```js
const elo = ([...ratings], kFactor = 32, selfRating) => {
  const [a, b] = ratings;
  const expectedScore = (self, opponent) => 1 / (1 + 10 ** ((opponent - self) / 400));
  const newRating = (rating, i) =>
    (selfRating ƜƜ rating) + kFactor * (i - expectedScore(i ? a : b, i ? b : a));
  if (ratings.length === 2) {
    return [newRating(a, 1), newRating(b, 0)];
  } else {
    for (let i = 0; i < ratings.length; i++) {
      let j = i;
      while (j < ratings.length - 1) {
        [ratings[i], ratings[j + 1]] = elo([ratings[i], ratings[j + 1]], kFactor);
        j++;
      }
    }
  }
  return ratings;
};
```

<details>
<summary>Examples</summary>

```js
// Standard 1v1s
elo([1200, 1200]); // [1216, 1184]
elo([1200, 1200], 64); // [1232, 1168]
// 4 player FFA, all same rank
elo([1200, 1200, 1200, 1200]).map(Math.round); // [1246, 1215, 1185, 1154]
/*
For teams, each rating can adjusted based on own team's average rating vs.
average rating of opposing team, with the score being added to their
own individual rating by supplying it as the third argument.
*/
```

</details>

<br>[和](#table-of-contents)

### math.floor()

创建所需长度的数组,

array.map()`在范围内填充所需的值. 第二个参数,`开始`,使用默认值`1`. 试试第三个参数,`步`,使用默认值`2`. `⬆返回顶部`汉明距离`计算两个值之间的汉明距离. 

```js
const factorial = n =>
  n < 0
    ? (() => {
        throw new TypeError('Negative numbers are not allowed!');
      })()
    : n <= 1 ? 1 : n * factorial(n - 1);
```

<details>
<summary>Examples</summary>

```js
factorial(6); // 720
```

</details>

<br>[使用xor运算符(](#table-of-contents)

### ^

)来查找这两个数字之间的位差,使用转换为二进制字符串

的ToString(2)`.count并返回数量`1`s在字符串中使用`匹配(/ 1 /克)`. `⬆返回顶部

```js
const fibonacci = n =>
  Array.from({ length: n }).reduce(
    (acc, val, i) => acc.concat(i > 1 ? acc[i - 1] + acc[i - 2] : i),
    []
  );
```

<details>
<summary>Examples</summary>

```js
fibonacci(6); // [0, 1, 1, 2, 3, 5]
```

</details>

<br>[在范围内](#table-of-contents)

### 检查给定的数字是否落在给定的范围内. 

使用算术比较来检查给定的数字是否在指定的范围内. 如果第二个参数,

结束`,没有指定,范围被认为是从`0`至`开始`. `⬆返回顶部`isdivisible`检查第一个数字参数是否可被第二个数字整除. `使用模运算符(`%`)来检查余数是否等于`0

```js
const gcd = (...arr) => {
  const _gcd = (x, y) => (!y ? x : gcd(y, x % y));
  return [...arr].reduce((a, b) => _gcd(a, b));
};
```

<details>
<summary>Examples</summary>

```js
gcd(8, 36); // 4
gcd(...[12, 8, 32]); // 4
```

</details>

<br>[. ](#table-of-contents)

### ⬆返回顶部

甚至`回报`真正`如果给定的数字是偶数,`假`除此以外. `检查一个数是奇数还是使用模(`%`)operator.returns`真正`如果数量是偶数,

假`如果数字是奇数. `⬆返回顶部`isprime`检查提供的整数是否是质数. `检查数字`2`以给定数字的平方根. 返回`假`如果他们中的任何一个将给定的号码分开,否则返回`真正`,除非数字少于`2`. `⬆返回顶部`LCM`返回两个或更多数字的最小公倍数. 

```js
const geometricProgression = (end, start = 1, step = 2) =>
  Array.from({ length: Math.floor(Math.log(end / start) / Math.log(step)) + 1 }).map(
    (v, i) => start * step ** i
  );
```

<details>
<summary>Examples</summary>

```js
geometricProgression(256); // [1, 2, 4, 8, 16, 32, 64, 128, 256]
geometricProgression(256, 3); // [3, 6, 12, 24, 48, 96, 192]
geometricProgression(256, 1, 4); // [1, 4, 16, 64, 256]
```

</details>

<br>[使用最大公约数(gcd)公式和事实](#table-of-contents)

### lcm(x,y)= x \* y / gcd(x,y)

以确定最小公倍数. gcd公式使用递归. 

⬆返回顶部`luhncheck`的执行情况`luhn算法`用于验证各种标识号码,例如信用卡号码,imei号码,国家提供商标识号码等. `使用`string.split( '')`,`array.reverse()

```js
const hammingDistance = (num1, num2) => ((num1 ^ num2).toString(2).match(/1/g) ƜƜ '').length;
```

<details>
<summary>Examples</summary>

```js
hammingDistance(2, 3); // 1
```

</details>

<br>[和](#table-of-contents)

### array.map()

与...结合

parseInt函数()`获取一个digit.use数组`方法Array.splice(0,1)`获取最后一位数字`array.reduce()`实现luhn算法. 返回`真正

```js
const inRange = (n, start, end = null) => {
  if (end && start > end) end = [start, (start = end)][0];
  return end == null ? n >= 0 && n < start : n >= start && n < end;
};
```

<details>
<summary>Examples</summary>

```js
inRange(3, 2, 5); // true
inRange(3, 4); // true
inRange(2, 3, 5); // false
inrange(3, 2); // false
```

</details>

<br>[如果](#table-of-contents)

### 和

可以被整除

10`,`假`除此以外. `⬆返回顶部

```js
const isDivisible = (dividend, divisor) => dividend % divisor === 0;
```

<details>
<summary>Examples</summary>

```js
isDivisible(6, 3); // true
```

</details>

<br>[maxby](#table-of-contents)

### 使用提供的函数将每个元素映射到一个值后,返回数组的最大值. 

使用`array.map()`将每个元素映射到返回的值`FN`,

math.max()`获得最大价值. `⬆返回顶部`中位数`返回数字数组的中值. `找到数组的中间,使用`中的Array.sort()

```js
const isEven = num => num % 2 === 0;
```

<details>
<summary>Examples</summary>

```js
isEven(3); // false
```

</details>

<br>[对值进行排序. 如果返回中点的数字](#table-of-contents)

### 长度

是奇数,否则是两个中间数的平均值. 

⬆返回顶部`minby`使用提供的函数将每个元素映射到一个值后,返回数组的最小值. `使用`array.map()`将每个元素映射到返回的值`FN`,`math.min()

```js
const isPrime = num => {
  const boundary = Math.floor(Math.sqrt(num));
  for (var i = 2; i <= boundary; i++) if (num % i == 0) return false;
  return num >= 2;
};
```

<details>
<summary>Examples</summary>

```js
isPrime(11); // true
```

</details>

<br>[获得最大价值. ](#table-of-contents)

### ⬆返回顶部

百分

使用百分位数公式来计算给定数组中有多少数字小于或等于给定值. `使用`array.reduce()

```js
const lcm = (...arr) => {
  const gcd = (x, y) => (!y ? x : gcd(y, x % y));
  const _lcm = (x, y) => x * y / gcd(x, y);
  return [...arr].reduce((a, b) => _lcm(a, b));
};
```

<details>
<summary>Examples</summary>

```js
lcm(12, 7); // 84
lcm(...[1, 3, 4, 5]); // 60
```

</details>

<br>[计算有多少个数字低于该值,多少个数字是相同的值,然后应用百分比公式. ](#table-of-contents)

### ⬆返回顶部

幂[返回给定数组数组的powerset. ](https://en.wikipedia.org/wiki/Luhn_algorithm)使用

array.reduce()`结合`array.map()`遍历元素并组合成包含所有组合的数组. `⬆返回顶部`素数`使用eratosthenes筛子生成达到给定数量的质数. `从中生成一个数组`2`到给定的数字. `使用`array.filter()`过滤出可以被任何数字整除的值`2`到提供的数字的平方根. `⬆返回顶部`randomintarrayinrange`返回指定范围内的n个随机整数的数组. `使用`array.from()`创建一个特定长度的空数组,

```js
const luhnCheck = num => {
  let arr = (num + '')
    .split('')
    .reverse()
    .map(x => parseInt(x));
  let lastDigit = arr.splice(0, 1)[0];
  let sum = arr.reduce((acc, val, i) => (i % 2 !== 0 ? acc + val : acc + (val * 2) % 9 ƜƜ 9), 0);
  sum += lastDigit;
  return sum % 10 === 0;
};
```

<details>
<summary>Examples</summary>

```js
luhnCheck('4485275742308327'); // true
luhnCheck(6011329933655299); //  false
luhnCheck(123456789); // false
```

</details>

<br>[的Math.random()](#table-of-contents)

### 生成一个随机数并使用它将其映射到所需的范围

math.floor()

使其成为一个整数. `⬆返回顶部`randomintegerinrange`返回指定范围内的随机整数. `使用`的Math.random()`生成一个随机数并使用它将其映射到所需的范围

```js
const maxBy = (arr, fn) => Math.max(...arr.map(typeof fn === 'function' ? fn : val => val[fn]));
```

<details>
<summary>Examples</summary>

```js
maxBy([{ n: 4 }, { n: 2 }, { n: 8 }, { n: 6 }], o => o.n); // 8
maxBy([{ n: 4 }, { n: 2 }, { n: 8 }, { n: 6 }], 'n'); // 8
```

</details>

<br>[math.floor()](#table-of-contents)

### 使其成为一个整数. 

⬆返回顶部

randomnumberinrange`返回指定范围内的一个随机数. `使用`的Math.random()`生成一个随机值,使用乘法将其映射到所需的范围. 

```js
const median = arr => {
  const mid = Math.floor(arr.length / 2),
    nums = [...arr].sort((a, b) => a - b);
  return arr.length % 2 !== 0 ? nums[mid] : (nums[mid - 1] + nums[mid]) / 2;
};
```

<details>
<summary>Examples</summary>

```js
median([5, 6, 50, 1, -5]); // 5
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 回合

将数字四舍五入到指定的数字位数. 

使用`math.round()`和模板文字将数字四舍五入为指定的位数. 尝试第二个参数,`小数点`舍入为一个整数. `⬆返回顶部`SBDM

```js
const minBy = (arr, fn) => Math.min(...arr.map(typeof fn === 'function' ? fn : val => val[fn]));
```

<details>
<summary>Examples</summary>

```js
minBy([{ n: 4 }, { n: 2 }, { n: 8 }, { n: 6 }], o => o.n); // 8
minBy([{ n: 4 }, { n: 2 }, { n: 8 }, { n: 6 }], 'n'); // 8
```

</details>

<br>[将输入字符串散列为整数. ](#table-of-contents)

### 使用

string.split( '')

和`array.reduce()`创建输入字符串的散列,利用位移. 

```js
const percentile = (arr, val) =>
  100 * arr.reduce((acc, v) => acc + (v < val ? 1 : 0) + (v === val ? 0.5 : 0), 0) / arr.length;
```

<details>
<summary>Examples</summary>

```js
percentile([1, 2, 3, 4, 5, 6, 7, 8, 9, 10], 6); // 55
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### standarddeviation

返回数组数组的标准差. 

使用`array.reduce()`计算均值,方差和值的方差之和,值的方差,然后确定标准偏差. 您可以省略第二个参数以获得样本标准偏差或将其设置为`真正`得到总体标准差. 

```js
const powerset = arr => arr.reduce((a, v) => a.concat(a.map(r => [v].concat(r))), [[]]);
```

<details>
<summary>Examples</summary>

```js
powerset([1, 2]); // [[], [1], [2], [2,1]]
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 和

返回两个或更多数字/数组的总和. 

使用`array.reduce()`将每个值添加到一个累加器,用一个值进行初始化`0`. `⬆返回顶部`sumby

```js
const primes = num => {
  let arr = Array.from({ length: num - 1 }).map((x, i) => i + 2),
    sqroot = Math.floor(Math.sqrt(num)),
    numsTillSqroot = Array.from({ length: sqroot - 1 }).map((x, i) => i + 2);
  numsTillSqroot.forEach(x => (arr = arr.filter(y => y % x !== 0 ƜƜ y == x)));
  return arr;
};
```

<details>
<summary>Examples</summary>

```js
primes(10); // [2,3,5,7]
```

</details>

<br>[在使用提供的函数将每个元素映射到一个值之后,返回一个数组的总和. ](#table-of-contents)

### 使用

array.map()

将每个元素映射到返回的值`FN`,`array.reduce()`将每个值添加到一个累加器,用一个值进行初始化`0`. 

```js
const randomIntArrayInRange = (min, max, n = 1) =>
  Array.from({ length: n }, () => Math.floor(Math.random() * (max - min + 1)) + min);
```

<details>
<summary>Examples</summary>

```js
randomIntArrayInRange(12, 35, 10); // [ 34, 14, 27, 17, 30, 27, 20, 26, 21, 14 ]
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### sumpower

返回所有数字的幂的和

开始`至`结束`(包括两端). `使用

```js
const randomIntegerInRange = (min, max) => Math.floor(Math.random() * (max - min + 1)) + min;
```

<details>
<summary>Examples</summary>

```js
randomIntegerInRange(0, 5); // 2
```

</details>

<br>[array.fill()](#table-of-contents)

### 创建目标范围内所有数字的数组,

array.map()

和指数运算符(`**`)把他们提升到

```js
const randomNumberInRange = (min, max) => Math.random() * (max - min) + min;
```

<details>
<summary>Examples</summary>

```js
randomNumberInRange(2, 10); // 6.0211363285087005
```

</details>

<br>[功率](#table-of-contents)

### 和

array.reduce()

把它们加在一起. 试着第二个参数,`功率`,使用默认的权力`2`. 试试第三个参数,

```js
const round = (n, decimals = 0) => Number(`${Math.round(`${n}e${decimals}`)}e-${decimals}`);
```

<details>
<summary>Examples</summary>

```js
round(1.005, 2); // 1.01
```

</details>

<br>[开始](#table-of-contents)

### ,使用默认的起始值

1

. `⬆返回顶部`tosafeinteger`将值转换为安全整数. `使用

```js
const sdbm = str => {
  let arr = str.split('');
  return arr.reduce(
    (hashCode, currentVal) =>
      (hashCode = currentVal.charCodeAt(0) + (hashCode << 6) + (hashCode << 16) - hashCode),
    0
  );
};
```

<details>
<summary>Examples</summary>

```js
sdbm('name'); // -3521204949
```

</details>

<br>[math.max()](#table-of-contents)

### 和

math.min()

找到最接近的安全值`math.round()`转换为整数. `⬆返回顶部`📦节点

```js
const standardDeviation = (arr, usePopulation = false) => {
  const mean = arr.reduce((acc, val) => acc + val, 0) / arr.length;
  return Math.sqrt(
    arr.reduce((acc, val) => acc.concat((val - mean) ** 2), []).reduce((acc, val) => acc + val, 0) /
      (arr.length - (usePopulation ? 0 : 1))
  );
};
```

<details>
<summary>Examples</summary>

```js
standardDeviation([10, 2, 38, 23, 38, 23, 21]); // 13.284434142114991 (sample)
standardDeviation([10, 2, 38, 23, 38, 23, 21], true); // 12.29899614287479 (population)
```

</details>

<br>[上色](#table-of-contents)

### 在文本中添加特殊字符以在控制台中以彩色打印(与

的console.log()

). `使用模板文字和特殊字符将适当的颜色代码添加到字符串output.for背景颜色中,添加一个特殊字符,用于在字符串末尾重置背景颜色. `⬆返回顶部`hasflags`检查当前进程的参数是否包含指定的标志. 

```js
const sum = (...arr) => [...arr].reduce((acc, val) => acc + val, 0);
```

<details>
<summary>Examples</summary>

```js
sum(...[1, 2, 3, 4]); // 10
```

</details>

<br>[使用](#table-of-contents)

### array.every()

和

array.includes()`检查是否`process.argv`包含所有指定的标志. 使用正则表达式来测试指定的标志是否带有前缀`-`要么`-`并相应地加上前缀. `⬆返回顶部

```js
const sumBy = (arr, fn) =>
  arr.map(typeof fn === 'function' ? fn : val => val[fn]).reduce((acc, val) => acc + val, 0);
```

<details>
<summary>Examples</summary>

```js
sumBy([{ n: 4 }, { n: 2 }, { n: 8 }, { n: 6 }], o => o.n); // 20
sumBy([{ n: 4 }, { n: 2 }, { n: 8 }, { n: 6 }], 'n'); // 20
```

</details>

<br>[istravisci](#table-of-contents)

### 检查当前环境是否是

特拉维斯西`. `检查当前环境是否具有`特拉维斯`和

CI`环境变量 (`参考`). `⬆返回顶部`jsontofile`将json对象写入文件. `使用`fs.writefile()`,模板文字和`json.stringify()`写一个`JSON`反对`以.json`文件. `⬆返回顶部`readfilelines`返回指定文件中的一行数组. 

```js
const sumPower = (end, power = 2, start = 1) =>
  Array(end + 1 - start)
    .fill(0)
    .map((x, i) => (i + start) ** power)
    .reduce((a, b) => a + b, 0);
```

<details>
<summary>Examples</summary>

```js
sumPower(10); // 385
sumPower(10, 3); //3025
sumPower(10, 3, 5); //2925
```

</details>

<br>[使用](#table-of-contents)

### readfilesync

功能

FS`节点包创建一个`缓冲`从一个file.convert缓冲区到字符串使用`的toString(编码)`函数. 从文件的内容创建一个数组`分裂

```js
const toSafeInteger = num =>
  Math.round(Math.max(Math.min(num, Number.MAX_SAFE_INTEGER), Number.MIN_SAFE_INTEGER));
```

<details>
<summary>Examples</summary>

```js
toSafeInteger('3.2'); // 3
toSafeInteger(Infinity); // 9007199254740991
```

</details>

<br>[逐行列出文件内容(每一行)](#table-of-contents)

* * *

## \\ n

### ). 

⬆返回顶部`untildify`将波浪线路径转换为绝对路径. 

使用

```js
const colorize = (...args) => ({
  black: `\x1b[30m${args.join(' ')}`,
  red: `\x1b[31m${args.join(' ')}`,
  green: `\x1b[32m${args.join(' ')}`,
  yellow: `\x1b[33m${args.join(' ')}`,
  blue: `\x1b[34m${args.join(' ')}`,
  magenta: `\x1b[35m${args.join(' ')}`,
  cyan: `\x1b[36m${args.join(' ')}`,
  white: `\x1b[37m${args.join(' ')}`,
  bgBlack: `\x1b[40m${args.join(' ')}\x1b[0m`,
  bgRed: `\x1b[41m${args.join(' ')}\x1b[0m`,
  bgGreen: `\x1b[42m${args.join(' ')}\x1b[0m`,
  bgYellow: `\x1b[43m${args.join(' ')}\x1b[0m`,
  bgBlue: `\x1b[44m${args.join(' ')}\x1b[0m`,
  bgMagenta: `\x1b[45m${args.join(' ')}\x1b[0m`,
  bgCyan: `\x1b[46m${args.join(' ')}\x1b[0m`,
  bgWhite: `\x1b[47m${args.join(' ')}\x1b[0m`
});
```

<details>
<summary>Examples</summary>

```js
console.log(colorize('foo').red); // 'foo' (red letters)
console.log(colorize('foo', 'bar').bgBlue); // 'foo bar' (blue background)
console.log(colorize(colorize('foo').yellow, colorize('foo').green).bgWhite); // 'foo bar' (first word in yellow letters, second word in green letters, white background for both)
```

</details>

<br>[与string.replace()](#table-of-contents)

### 用正则表达式和

os.homedir()

取代`〜`在主目录路径的开始处. `⬆返回顶部`uuidgeneratornode`在node.js中生成一个uuid. `使用`加密`API来生成一个uuid,符合`rfc4122`版本4. 

```js
const hasFlags = (...flags) =>
  flags.every(flag => process.argv.includes(/^-{1,2}/.test(flag) ? flag : '--' + flag));
```

<details>
<summary>Examples</summary>

```js
// node myScript.js -s --test --cool=true
hasFlags('-s'); // true
hasFlags('--test', 'cool=true', '-s'); // true
hasFlags('special'); // false
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 🗃️对象

cleanobj[删除除json对象指定的属性外的所有属性. ](https://travis-ci.org/)使用

object.keys()`方法来循环给定的json对象,并删除未包含在给定数组中的键. 如果您传递一个特殊的键,`childindicator`,它也会深入地将该函数应用于内部对象. `⬆返回顶部[等于](https://docs.travis-ci.com/user/environment-variables/#Default-Environment-Variables)在两个值之间进行深入比较以确定它们是否相等. 

```js
const isTravisCI = () => 'TRAVIS' in process.env && 'CI' in process.env;
```

<details>
<summary>Examples</summary>

```js
isTravisCI(); // true (if code is running on Travis CI)
```

</details>

<br>[检查两个值是否相同,如果两者都是](#table-of-contents)

### 日期

使用同一时间的对象

date.gettime()`或者它们都是具有等价值的非对象值(严格比较).check是否只有一个值`空值`要么`未定义`或者如果它们的原型不同,如果没有满足上述条件,请使用`object.keys()`检查两个值是否具有相同的密钥数量,然后使用`array.every()

```js
const fs = require('fs');
const JSONToFile = (obj, filename) =>
  fs.writeFile(`${filename}.json`, JSON.stringify(obj, null, 2));
```

<details>
<summary>Examples</summary>

```js
JSONToFile({ test: 'is passed' }, 'testJsonFile'); // writes the object to 'testJsonFile.json'
```

</details>

<br>[通过递归调用这个方法来检查第一个值中的每个键是否存在于第二个键中,并且它们是否相等. ](#table-of-contents)

### ⬆返回顶部

功能

从一个对象的自身(和可选继承的)可枚举属性返回一个函数属性名称数组. `使用`object.keys(OBJ)`迭代对象自己的属性`遗传`是`真正`, 使用`object.get.prototypeof(OBJ)`也可以获得对象的继承properties.use`array.filter()`只保留那些是functions.omit第二个参数的属性,`遗传

```js
const fs = require('fs');
const readFileLines = filename =>
  fs
    .readFileSync(filename)
    .toString('UTF8')
    .split('\n');
```

<details>
<summary>Examples</summary>

```js
/*
contents of test.txt :
  line1
  line2
  line3
  ___________________________
*/
let arr = readFileLines('test.txt');
console.log(arr); // ['line1', 'line2', 'line3']
```

</details>

<br>[,默认情况下不包括继承属性. ](#table-of-contents)

### ⬆返回顶部

invertkeyvalues

反转对象的键值对,而不会突变它. `使用`object.keys()`和`array.reduce()`以反转对象的键值对. `⬆返回顶部

```js
const untildify = str => str.replace(/^~($Ɯ\/Ɯ\\)/, `${require('os').homedir()}$1`);
```

<details>
<summary>Examples</summary>

```js
untildify('~/node'); // '/Users/aUser/node'
```

</details>

<br>[lowercasekeys](#table-of-contents)

### 从指定的对象中创建一个新的对象,其中所有的键都是小写的. 

使用

object.keys()`和`array.reduce()[从指定的对象创建一个新对象. 将原始对象中的每个键转换为小写,使用](https://www.ietf.org/rfc/rfc4122.txt)string.tolowercase()

```js
const crypto = require('crypto');
const UUIDGeneratorNode = () =>
  ([1e7] + -1e3 + -4e3 + -8e3 + -1e11).replace(/[018]/g, c =>
    (c ^ (crypto.randomBytes(1)[0] & (15 >> (c / 4)))).toString(16)
  );
```

<details>
<summary>Examples</summary>

```js
UUIDGeneratorNode(); // '79c7c136-60ee-40a2-beb2-856f1feabefc'
```

</details>

<br>[. ](#table-of-contents)

* * *

## ⬆返回顶部

### 映射键

通过为每个键运行提供的功能以及与提供的对象相同的值来创建具有键生成的对象. 

使用`object.keys(OBJ)`遍历对象的keys.use`array.reduce()`使用相同的值和映射键创建一个新的对象

```js
const cleanObj = (obj, keysToKeep = [], childIndicator) => {
  Object.keys(obj).forEach(key => {
    if (key === childIndicator) {
      cleanObj(obj[key], keysToKeep, childIndicator);
    } else if (!keysToKeep.includes(key)) {
      delete obj[key];
    }
  });
  return obj;
};
```

<details>
<summary>Examples</summary>

```js
const testObj = { a: 1, b: 2, children: { a: 1, b: 2 } };
cleanObj(testObj, ['a'], 'children'); // { a: 1, children : { a: 1}}
```

</details>

<br>[FN](#table-of-contents)

### . ![advanced](/advanced.svg)

⬆返回顶部

mapvalues`使用与提供的对象相同的键创建对象,并通过为每个值运行提供的功能生成值. `使用`object.keys(OBJ)`遍历对象的keys.use`array.reduce()`使用相同的键和映射值创建一个新的对象`FN`. `⬆返回顶部`合并`从两个或更多对象的组合创建一个新对象. `使用

```js
const equals = (a, b) => {
  if (a === b) return true;
  if (a instanceof Date && b instanceof Date) return a.getTime() === b.getTime();
  if (!a ƜƜ !b ƜƜ (typeof a != 'object' && typeof b !== 'object')) return a === b;
  if (a === null ƜƜ a === undefined ƜƜ b === null ƜƜ b === undefined) return false;
  if (a.prototype !== b.prototype) return false;
  let keys = Object.keys(a);
  if (keys.length !== Object.keys(b).length) return false;
  return keys.every(k => equals(a[k], b[k]));
};
```

<details>
<summary>Examples</summary>

```js
equals({ a: [2, { e: 3 }], b: [4], c: 'foo' }, { a: [2, { e: 3 }], b: [4], c: 'foo' }); // true
```

</details>

<br>[array.reduce()](#table-of-contents)

### 结合

object.keys(OBJ)

遍历所有对象和keys.use`hasownproperty()`和`array.concat()`为多个对象中存在的键添加值. `⬆返回顶部`objectfrompairs`根据给定的键值对创建一个对象. `使用`array.reduce()`创建和组合键值对. `⬆返回顶部`objecttopairs

```js
const functions = (obj, inherited = false) =>
  (inherited
    ? [...Object.keys(obj), ...Object.keys(Object.getPrototypeOf(obj))]
    : Object.keys(obj)
  ).filter(key => typeof obj[key] === 'function');
```

<details>
<summary>Examples</summary>

```js
function Foo() {
  this.a = () => 1;
  this.b = () => 2;
}
Foo.prototype.c = () => 3;
functions(new Foo()); // ['a', 'b']
functions(new Foo(), true); // ['a', 'b', 'c']
```

</details>

<br>[从一个对象创建一个键 - 值对数组的数组. ](#table-of-contents)

### 使用

object.keys()

和`array.map()`遍历对象的键并生成一个包含键值对的数组. `⬆返回顶部`排序依据

```js
const invertKeyValues = obj =>
  Object.keys(obj).reduce((acc, key) => {
    acc[obj[key]] = key;
    return acc;
  }, {});
```

<details>
<summary>Examples</summary>

```js
invertKeyValues({ name: 'John', age: 20 }); // { 20: 'age', John: 'name' }
```

</details>

<br>[返回按属性和顺序排序的对象的排序数组. ](#table-of-contents)

### 使用

中的Array.sort()

,`array.reduce()`上`道具`数组的默认值为`0`,根据传递的顺序,使用数组解构来交换属性位置

```js
const lowercaseKeys = obj =>
  Object.keys(obj).reduce((acc, key) => {
    acc[key.toLowerCase()] = obj[key];
    return acc;
  }, {});
```

<details>
<summary>Examples</summary>

```js
const myObj = { Name: 'Adam', sUrnAME: 'Smith' };
const myObjLower = lowercaseKeys(myObj); // {name: 'Adam', surname: 'Smith'};
```

</details>

<br>[命令](#table-of-contents)

### 数组通过排序

'ASC'

默认. `⬆返回顶部`选择`从对象中检索给定选择器指定的一组属性. `使用`array.map()`对于每个选择器,

```js
const mapKeys = (obj, fn) =>
  Object.keys(obj).reduce((acc, k) => {
    acc[fn(obj[k], k, obj)] = obj[k];
    return acc;
  }, {});
```

<details>
<summary>Examples</summary>

```js
mapKeys({ a: 1, b: 2 }, (val, key) => key + val); // { a1: 1, b2: 2 }
```

</details>

<br>[string.split( '')](#table-of-contents)

### 分割每个选择器和

array.reduce()

以获得它所指示的值. `⬆返回顶部`shallowclone`创建一个对象的浅层克隆. `使用`object.assign()`和一个空对象(

```js
const mapValues = (obj, fn) =>
  Object.keys(obj).reduce((acc, k) => {
    acc[k] = fn(obj[k], k, obj);
    return acc;
  }, {});
```

<details>
<summary>Examples</summary>

```js
const users = {
  fred: { user: 'fred', age: 40 },
  pebbles: { user: 'pebbles', age: 1 }
};
mapValues(users, u => u.age); // { fred: 40, pebbles: 1 }
```

</details>

<br>[{}](#table-of-contents)

### )创建原始的浅层克隆. 

⬆返回顶部

尺寸`获取数组,对象或字符串的大小. `获取类型`VAL`(`排列`,`目的`要么

```js
const merge = (...objs) =>
  [...objs].reduce(
    (acc, obj) =>
      Object.keys(obj).reduce((a, k) => {
        acc[k] = acc.hasOwnProperty(k) ? [].concat(acc[k]).concat(obj[k]) : obj[k];
        return acc;
      }, {}),
    {}
  );
```

<details>
<summary>Examples</summary>

```js
const object = {
  a: [{ x: 2 }, { y: 4 }],
  b: 1
};
const other = {
  a: { z: 3 },
  b: [2, 3],
  c: 'foo'
};
merge(object, other); // { a: [ { x: 2 }, { y: 4 }, { z: 3 } ], b: [ 1, 2, 3 ], c: 'foo' }
```

</details>

<br>[串](#table-of-contents)

### ). 

使用

长度`用于arrays.use的属性`长度

```js
const objectFromPairs = arr => arr.reduce((a, v) => ((a[v[0]] = v[1]), a), {});
```

<details>
<summary>Examples</summary>

```js
objectFromPairs([['a', 1], ['b', 2]]); // {a: 1, b: 2}
```

</details>

<br>[要么](#table-of-contents)

### 尺寸

值(如果可用)或objects.use的键数量

尺寸`一个`BLOB`目的`由...创建

```js
const objectToPairs = obj => Object.keys(obj).map(k => [k, obj[k]]);
```

<details>
<summary>Examples</summary>

```js
objectToPairs({ a: 1, b: 2 }); // [['a',1],['b',2]]
```

</details>

<br>[VAL](#table-of-contents)

### 为字符串. 

将字符串拆分为字符数组

分裂('')`并返回它的长度. `⬆返回顶部`转变`对累加器和对象中的每个键(从左到右)应用一个函数. `使用`object.keys(OBJ)`遍历对象中的每个键,`array.reduce()`对给定的累加器调用apply指定的函数. `⬆返回顶部`truthcheckcollection`检查谓词(第二个参数)对集合的所有元素(第一个参数)是否真实. 

```js
const orderBy = (arr, props, orders) =>
  [...arr].sort((a, b) =>
    props.reduce((acc, prop, i) => {
      if (acc === 0) {
        const [p1, p2] = orders && orders[i] === 'desc' ? [b[prop], a[prop]] : [a[prop], b[prop]];
        acc = p1 > p2 ? 1 : p1 < p2 ? -1 : 0;
      }
      return acc;
    }, 0)
  );
```

<details>
<summary>Examples</summary>

```js
const users = [{ name: 'fred', age: 48 }, { name: 'barney', age: 36 }, { name: 'fred', age: 40 }];
orderBy(users, ['name', 'age'], ['asc', 'desc']); // [{name: 'barney', age: 36}, {name: 'fred', age: 48}, {name: 'fred', age: 40}]
orderBy(users, ['name', 'age']); // [{name: 'barney', age: 36}, {name: 'fred', age: 40}, {name: 'fred', age: 48}]
```

</details>

<br>[使用](#table-of-contents)

### array.every()

检查每个传递的对象是否具有指定的属性,以及它是否返回真值. 

⬆返回顶部`📜字符串`字谜`⚠️`警告`: 这个函数的执行时间随着每个字符呈指数级增长. `超过8到10个字符的任何内容都会导致浏览器挂起,因为它试图解决所有不同的组合. 

```js
const select = (from, ...selectors) =>
  [...selectors].map(s => s.split('.').reduce((prev, cur) => prev && prev[cur], from));
```

<details>
<summary>Examples</summary>

```js
const obj = { selector: { to: { val: 'val to select' } } };
select(obj, 'selector.to.val'); // ['val to select']
select(obj, 'selector.to.val', 'selector.to'); // ['val to select', { val: 'val to select' }]
```

</details>

<br>[生成一个字符串的所有字符串(包含重复项). ](#table-of-contents)

### 对给定字符串中的每个字母使用递归,为其余字母创建所有部分字母.use

array.map()

然后将该字母与每个部分字谜组合`array.reduce()`将所有字符组合在一个数组中. 基本情况用于字符串`长度`等于

```js
const shallowClone = obj => Object.assign({}, obj);
```

<details>
<summary>Examples</summary>

```js
const a = { x: true, y: 1 };
const b = shallowClone(a); // a !== b
```

</details>

<br>[2](#table-of-contents)

### 要么

1

. `⬆返回顶部`bytesize`以字节为单位返回字符串的长度. `将给定的字符串转换为`BLOB`目的`并找到它`尺寸`. `⬆返回顶部`利用`大写字符串的第一个字母. `使用数组解构和`string.touppercase()`首字母大写,`...休息[`在第一个字母后再获取字符数组`array.join( '')](https://developer.mozilla.org/en-US/docs/Web/API/Blob)再次使它成为一个字符串`lowerrest`参数保持字符串的其余部分不变,或将其设置为

真正`转换为小写. `⬆返回顶部

```js
const size = val =>
  Array.isArray(val)
    ? val.length
    : val && typeof val === 'object'
      ? val.size ƜƜ val.length ƜƜ Object.keys(val).length
      : typeof val === 'string' ? new Blob([val]).size : 0;
```

<details>
<summary>Examples</summary>

```js
size([1, 2, 3, 4, 5]); // 5
size('size'); // 4
size({ one: 1, two: 2, three: 3 }); // 3
```

</details>

<br>[capitalizeeveryword](#table-of-contents)

### 大写字符串中每个单词的第一个字母. 

使用

与string.replace()`匹配每个单词的第一个字符和`string.touppercase()`将其资本化. `⬆返回顶部

```js
const transform = (obj, fn, acc) => Object.keys(obj).reduce((a, k) => fn(a, obj[k], k, obj), acc);
```

<details>
<summary>Examples</summary>

```js
transform(
  { a: 1, b: 2, c: 1 },
  (r, v, k) => {
    (r[v] ƜƜ (r[v] = [])).push(k);
    return r;
  },
  {}
); // { '1': ['a', 'c'], '2': ['b'] }
```

</details>

<br>[decapitalize](#table-of-contents)

### 对字符串的第一个字母进行decapitalize. 

使用数组解构和

string.tolowercase()`为第一个字母去除资本,`...休息

```js
const truthCheckCollection = (collection, pre) => collection.every(obj => obj[pre]);
```

<details>
<summary>Examples</summary>

```js
truthCheckCollection([{ user: 'Tinky-Winky', sex: 'male' }, { user: 'Dipsy', sex: 'male' }], 'sex'); // true
```

</details>

<br>[在第一个字母后再获取字符数组](#table-of-contents)

* * *

## array.join( '')

### 再次使它成为一个字符串

upperrest**参数保持字符串的其余部分不变,或将其设置为**真正

转换为大写. 

⬆返回顶部`escapehtml`转义字符串以便在html中使用. `使用`与string.replace()`使用匹配需要转义的字符的正则表达式,使用回调函数使用字典(对象)将每个字符实例替换为其关联的转义字符. `⬆返回顶部`escaperegexp`转义字符串以在正则表达式中使用. `使用`与string.replace()

```js
const anagrams = str => {
  if (str.length <= 2) return str.length === 2 ? [str, str[1] + str[0]] : [str];
  return str
    .split('')
    .reduce(
      (acc, letter, i) =>
        acc.concat(anagrams(str.slice(0, i) + str.slice(i + 1)).map(val => letter + val)),
      []
    );
};
```

<details>
<summary>Examples</summary>

```js
anagrams('abc'); // ['abc','acb','bac','bca','cab','cba']
```

</details>

<br>[逃避特殊字符. ](#table-of-contents)

### ⬆返回顶部

fromcamelcase

从camelcase转换字符串. [`使用`与string.replace()](https://developer.mozilla.org/en-US/docs/Web/API/Blob)删除下划线,连字符和空格,并将单词转换为camelcase.omit第二个参数以使用默认值`分隔器`的

```js
const byteSize = str => new Blob([str]).size;
```

<details>
<summary>Examples</summary>

```js
byteSize('😀'); // 4
byteSize('Hello World'); // 11
```

</details>

<br>[\_](#table-of-contents)

### . 

⬆返回顶部

isabsoluteurl`回报`真正`如果给定的字符串是绝对url,`假`除此以外. `使用正则表达式来测试字符串是否是绝对url. `⬆返回顶部`islowercase`检查一个字符串是否小写. `将给定的字符串转换为小写,使用

```js
const capitalize = ([first, ...rest], lowerRest = false) =>
  first.toUpperCase() + (lowerRest ? rest.join('').toLowerCase() : rest.join(''));
```

<details>
<summary>Examples</summary>

```js
capitalize('fooBar'); // 'FooBar'
capitalize('fooBar', true); // 'Foobar'
```

</details>

<br>[string.tolowercase()](#table-of-contents)

### 并将其与原文进行比较. 

⬆返回顶部

isuppercase`检查一个字符串是否为大写. `将给定的字符串转换为大写,使用`string.touppercase()`并将其与原文进行比较. 

```js
const capitalizeEveryWord = str => str.replace(/\b[a-z]/g, char => char.toUpperCase());
```

<details>
<summary>Examples</summary>

```js
capitalizeEveryWord('hello world!'); // 'Hello World!'
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### 面具

取代除了最后一个以外的所有

NUM`具有指定掩码字符的字符. `使用`string.slice()`抓住需要被屏蔽和使用的角色部分`与string.replace()`用正则表达式替换每个字符的掩码字符. 将掩码字符与字符串中剩余的未掩码部分联合起来. 第二个参数,`NUM`,保持默认`4`字符未被掩盖. 

```js
const decapitalize = ([first, ...rest], upperRest = false) =>
  first.toLowerCase() + (upperRest ? rest.join('').toUpperCase() : rest.join(''));
```

<details>
<summary>Examples</summary>

```js
decapitalize('FooBar'); // 'fooBar'
decapitalize('FooBar', true); // 'fOOBAR'
```

</details>

<br>[如果](#table-of-contents)

### NUM

是负数,未被屏蔽的字符将在string.omit第三个参数的开始处,

面具`,使用默认字符`'\*'

```js
const escapeHTML = str =>
  str.replace(
    /[&<>'"]/g,
    tag =>
      ({
        '&': '&amp;',
        '<': '&lt;',
        '>': '&gt;',
        "'": '&#39;',
        '"': '&quot;'
      }[tag] ƜƜ tag)
  );
```

<details>
<summary>Examples</summary>

```js
escapeHTML('<a href="#">Me & you</a>'); // '&lt;a href=&quot;#&quot;&gt;Me &amp; you&lt;/a&gt;'
```

</details>

<br>[为面具. ](#table-of-contents)

### ⬆返回顶部

回文

回报`真正`如果给定的字符串是回文,

```js
const escapeRegExp = str => str.replace(/[.*+?^${}()Ɯ[\]\\]/g, '\\$&');
```

<details>
<summary>Examples</summary>

```js
escapeRegExp('(test)'); // \\(test\\)
```

</details>

<br>[假](#table-of-contents)

### 除此以外. 

转换字符串

string.tolowercase()`并使用`与string.replace()`从中删除非字母数字字符. 然后,`string.split( '')`成个人角色,`array.reverse()

```js
const fromCamelCase = (str, separator = '_') =>
  str
    .replace(/([a-z\d])([A-Z])/g, '$1' + separator + '$2')
    .replace(/([A-Z]+)([A-Z][a-z\d]+)/g, '$1' + separator + '$2')
    .toLowerCase();
```

<details>
<summary>Examples</summary>

```js
fromCamelCase('someDatabaseFieldName', ' '); // 'some database field name'
fromCamelCase('someLabelThatNeedsToBeCamelized', '-'); // 'some-label-that-needs-to-be-camelized'
fromCamelCase('someJavascriptProperty', '_'); // 'some_javascript_property'
```

</details>

<br>[,](#table-of-contents)

### 的string.join( '')

并在转换之后与原始的非反转字符串进行比较`string.tolowercase()`. `⬆返回顶部`变复数

根据输入号码返回单词的单数或复数形式. 

```js
const isAbsoluteURL = str => /^[a-z][a-z0-9+.-]*:/.test(str);
```

<details>
<summary>Examples</summary>

```js
isAbsoluteURL('https://google.com'); // true
isAbsoluteURL('ftp://www.myserver.net'); // true
isAbsoluteURL('/foo/bar'); // false
```

</details>

<br>[如果第一个参数是](#table-of-contents)

### 目的

,它将通过返回一个函数来使用闭包,该函数可以自动复数不会简单地结束的单词

小号`如果提供的字典包含该单词. `如果

```js
const isLowerCase = str => str === str.toLowerCase();
```

<details>
<summary>Examples</summary>

```js
isLowerCase('abc'); // true
isLowerCase('a3@$'); // true
isLowerCase('Ab4'); // false
```

</details>

<br>[NUM](#table-of-contents)

### 或者是

\-1

要么`1`,返回单词的单数形式. 

```js
const isUpperCase = str => str === str.toUpperCase();
```

<details>
<summary>Examples</summary>

```js
isUpperCase('ABC'); // true
isLowerCase('A3@$'); // true
isLowerCase('aB4'); // false
```

</details>

<br>[如果](#table-of-contents)

### NUM

是任何其他数字,返回复数形式. `省略第三个参数来使用单数字+的默认值`小号

或者在必要时提供定制的复数词. `如果第一个参数是`目的`,通过返回一个函数来使用闭包,该函数可以使用提供的字典来解析正确的复数形式的单词. `⬆返回顶部`reversestring`反转一个字符串. `使用扩展运算符(`...`)和`array.reverse()`以反转string.combine字符中的字符顺序以获取使用的字符串`的string.join( '')`. `⬆返回顶部

```js
const mask = (cc, num = 4, mask = '*') =>
  ('' + cc).slice(0, -num).replace(/./g, mask) + ('' + cc).slice(-num);
```

<details>
<summary>Examples</summary>

```js
mask(1234567890); // '******7890'
mask(1234567890, 3); // '*******890'
mask(1234567890, -4, '$'); // '$$$$567890'
```

</details>

<br>[sortcharactersinstring](#table-of-contents)

### 按字母顺序排列字符串中的字符. 

使用扩展运算符(`...`)`中的Array.sort()`和

string.localecompare()`排序中的字符`海峡`,使用重组`的string.join( '')`. `⬆返回顶部`splitlines`将多行字符串拆分为一行数组. `使用`string.split()`和一个正则表达式来匹配换行符并创建一个数组. `⬆返回顶部

```js
const palindrome = str => {
  const s = str.toLowerCase().replace(/[\W_]/g, '');
  return (
    s ===
    s
      .split('')
      .reverse()
      .join('')
  );
};
```

<details>
<summary>Examples</summary>

```js
palindrome('taco cat'); // true
```

</details>

<br>[tocamelcase](#table-of-contents)

### 将字符串转换为camelcase. 

将字符串分解成单词并将它们合并为每个单词的首字母大写,使用正则表达式. `⬆返回顶部`tokebabcase`将字符串转换为kebab大小写. `将字符串分解成单词并将它们相加

\-`作为分隔符,使用正则表达式. `⬆返回顶部`tosnakecase`将字符串转换为蛇情况. `将字符串分解成单词并将它们相加`\_`作为分隔符,使用正则表达式. `⬆返回顶部`truncatestring`截断一个字符串直到指定的长度. `确定字符串的`长度

```js
const pluralize = (val, word, plural = word + 's') => {
  const _pluralize = (num, word, plural = word + 's') =>
    [1, -1].includes(Number(num)) ? word : plural;
  if (typeof val === 'object') return (num, word) => _pluralize(num, word, val[word]);
  return _pluralize(val, word, plural);
};
```

<details>
<summary>Examples</summary>

```js
pluralize(0, 'apple'); // 'apples'
pluralize(1, 'apple'); // 'apple'
pluralize(2, 'apple'); // 'apples'
pluralize(2, 'person', 'people'); // 'people'

const PLURALS = {
  person: 'people',
  radius: 'radii'
};
const autoPluralize = pluralize(PLURALS);
autoPluralize(2, 'person'); // 'people'
```

</details>

<br>[大于](#table-of-contents)

### NUM

. 将字符串截断为所需的长度,并用

'...'`附加到结尾或原始字符串. `⬆返回顶部`unescapehtml`unescapes转义了html字符. `使用`与string.replace()

```js
const reverseString = str => [...str].reverse().join('');
```

<details>
<summary>Examples</summary>

```js
reverseString('foobar'); // 'raboof'
```

</details>

<br>[使用正则表达式匹配需要未转义的字符,使用回调函数使用字典(对象)将每个转义字符实例替换为与其相关联的非转义字符. ](#table-of-contents)

### ⬆返回顶部

话

将给定的字符串转换为单词数组. `使用`string.split()`使用提供的模式(默认为非alpha作为正则表达式)转换为字符串数组. `使用`array.filter()`删除任何空的strings.omit第二个参数使用默认的正则表达式. `⬆返回顶部`📃类型`将gettype`返回值的本机类型. 

```js
const sortCharactersInString = str => [...str].sort((a, b) => a.localeCompare(b)).join('');
```

<details>
<summary>Examples</summary>

```js
sortCharactersInString('cabbage'); // 'aabbceg'
```

</details>

<br>[返回小写的构造函数名称的值,](#table-of-contents)

### "不确定"

要么

"空值"`如果价值是`未定义

```js
const splitLines = str => str.split(/\r?\n/);
```

<details>
<summary>Examples</summary>

```js
splitLines('This\nis a\nmultiline\nstring.\n'); // ['This', 'is a', 'multiline', 'string.' , '']
```

</details>

<br>[要么](#table-of-contents)

### 空值

. 

⬆返回顶部

```js
const toCamelCase = str => {
  let s =
    str &&
    str
      .match(/[A-Z]{2,}(?=[A-Z][a-z]+[0-9]*Ɯ\b)Ɯ[A-Z]?[a-z]+[0-9]*Ɯ[A-Z]Ɯ[0-9]+/g)
      .map(x => x.slice(0, 1).toUpperCase() + x.slice(1).toLowerCase())
      .join('');
  return s.slice(0, 1).toLowerCase() + s.slice(1);
};
```

<details>
<summary>Examples</summary>

```js
toCamelCase('some_database_field_name'); // 'someDatabaseFieldName'
toCamelCase('Some label that needs to be camelized'); // 'someLabelThatNeedsToBeCamelized'
toCamelCase('some-javascript-property'); // 'someJavascriptProperty'
toCamelCase('some-mixed_string with spaces_underscores-and-hyphens'); // 'someMixedStringWithSpacesUnderscoresAndHyphens'
```

</details>

<br>[IsArray的](#table-of-contents)

### 检查给定的参数是否是一个数组. 

使用

array.isarray()`检查一个值是否被分类为一个数组. `⬆返回顶部

```js
const toKebabCase = str =>
  str &&
  str
    .match(/[A-Z]{2,}(?=[A-Z][a-z]+[0-9]*Ɯ\b)Ɯ[A-Z]?[a-z]+[0-9]*Ɯ[A-Z]Ɯ[0-9]+/g)
    .map(x => x.toLowerCase())
    .join('-');
```

<details>
<summary>Examples</summary>

```js
toKebabCase('camelCase'); // 'camel-case'
toKebabCase('some text'); // 'some-text'
toKebabCase('some-mixed_string With spaces_underscores-and-hyphens'); // 'some-mixed-string-with-spaces-underscores-and-hyphens'
toKebabCase('AllThe-small Things'); // "all-the-small-things"
toKebabCase('IAmListeningToFMWhileLoadingDifferentURLOnMyBrowserAndAlsoEditingSomeXMLAndHTML'); // "i-am-listening-to-fm-while-loading-different-url-on-my-browser-and-also-editing-xml-and-html"
```

</details>

<br>[isarraylike](#table-of-contents)

### 检查提供的参数是否类似数组(即可迭代). 

使用扩展运算符(

...`)来检查提供的参数是否可以在a中迭代`试着抓

```js
const toSnakeCase = str =>
  str &&
  str
    .match(/[A-Z]{2,}(?=[A-Z][a-z]+[0-9]*Ɯ\b)Ɯ[A-Z]?[a-z]+[0-9]*Ɯ[A-Z]Ɯ[0-9]+/g)
    .map(x => x.toLowerCase())
    .join('_');
```

<details>
<summary>Examples</summary>

```js
toSnakeCase('camelCase'); // 'camel_case'
toSnakeCase('some text'); // 'some_text'
toSnakeCase('some-mixed_string With spaces_underscores-and-hyphens'); // 'some_mixed_string_with_spaces_underscores_and_hyphens'
toSnakeCase('AllThe-small Things'); // "all_the_smal_things"
toSnakeCase('IAmListeningToFMWhileLoadingDifferentURLOnMyBrowserAndAlsoEditingSomeXMLAndHTML'); // "i_am_listening_to_fm_while_loading_different_url_on_my_browser_and_also_editing_some_xml_and_html"
```

</details>

<br>[块和逗号运算符(](#table-of-contents)

### ,

)返回适当的值. 

⬆返回顶部`isboolean`检查给定的参数是否是本地布尔元素. `使用`类型`检查一个值是否被分类为布尔原语. `⬆返回顶部

```js
const truncateString = (str, num) =>
  str.length > num ? str.slice(0, num > 3 ? num - 3 : num) + '...' : str;
```

<details>
<summary>Examples</summary>

```js
truncateString('boomerang', 7); // 'boom...'
```

</details>

<br>[isfunction](#table-of-contents)

### 检查给定的参数是否是一个函数. 

使用

类型`检查一个值是否被分类为一个函数原语. `⬆返回顶部

```js
const unescapeHTML = str =>
  str.replace(
    /&amp;Ɯ&lt;Ɯ&gt;Ɯ&#39;Ɯ&quot;/g,
    tag =>
      ({
        '&amp;': '&',
        '&lt;': '<',
        '&gt;': '>',
        '&#39;': "'",
        '&quot;': '"'
      }[tag] ƜƜ tag)
  );
```

<details>
<summary>Examples</summary>

```js
unescapeHTML('&lt;a href=&quot;#&quot;&gt;Me &amp; you&lt;/a&gt;'); // '<a href="#">Me & you</a>'
```

</details>

<br>[一片空白](#table-of-contents)

### 回报

真正

如果指定的值是`空值`,`假`除此以外. 

```js
const words = (str, pattern = /[^a-zA-Z-]+/) => str.split(pattern).filter(Boolean);
```

<details>
<summary>Examples</summary>

```js
words('I love javaScript!!'); // ["I", "love", "javaScript"]
words('python, javaScript & coffee'); // ["python", "javaScript", "coffee"]
```

</details>

<br>[使用严格的相等运算符来检查值和](#table-of-contents)

* * *

## VAL

### 等于

空值

. `⬆返回顶部`ISNUMBER`检查给定的参数是否是数字. `使用`类型`检查一个值是否被分类为数字原语. `⬆返回顶部`则IsObject

```js
const getType = v =>
  v === undefined ? 'undefined' : v === null ? 'null' : v.constructor.name.toLowerCase();
```

<details>
<summary>Examples</summary>

```js
getType(new Set([1, 2, 3])); // 'set'
```

</details>

<br>[返回一个布尔值,确定传递的值是否是一个对象. ](#table-of-contents)

### 使用

目的

构造函数为给定值创建对象包装. `如果值是`空值

```js
const isArray = val => Array.isArray(val);
```

<details>
<summary>Examples</summary>

```js
isArray([1]); // true
```

</details>

<br>[要么](#table-of-contents)

### 未定义

,创建并返回一个空对象. 

否则,返回一个对应于给定值的类型的对象. `⬆返回顶部`isprimitive`返回一个布尔值,确定传入的值是否为原始值. `使用`array.includes()`在一个非原始类型的字符串数组上,提供使用的类型

```js
const isArrayLike = val => {
  try {
    return [...val], true;
  } catch (e) {
    return false;
  }
};
```

<details>
<summary>Examples</summary>

```js
isArrayLike(document.querySelectorAll('.className')); // true
isArrayLike('abc'); // true
isArrayLike(null); // false
```

</details>

<br>[类型](#table-of-contents)

### . 以来

typeof null

评估为`'目的'`,需要直接比较. 

```js
const isBoolean = val => typeof val === 'boolean';
```

<details>
<summary>Examples</summary>

```js
isBoolean(null); // false
isBoolean(false); // true
```

</details>

<br>[⬆返回顶部](#table-of-contents)

### ispromiselike

回报

真正`如果一个物体看起来像一个`诺言

```js
const isFunction = val => typeof val === 'function';
```

<details>
<summary>Examples</summary>

```js
isFunction('x'); // false
isFunction(x => x); // true
```

</details>

<br>[,](#table-of-contents)

### 假

除此以外. `检查对象是否不是`空值`, 它的`类型`匹配`目的

要么`功能`如果它有一个`. 然后`财产,这也是

```js
const isNull = val => val === null;
```

<details>
<summary>Examples</summary>

```js
isNull(null); // true
```

</details>

<br>[功能](#table-of-contents)

### . 

⬆返回顶部

isstring`检查给定的参数是否是一个字符串. `使用

```js
const isNumber = val => typeof val === 'number';
```

<details>
<summary>Examples</summary>

```js
isNumber('1'); // false
isNumber(1); // true
```

</details>

<br>[类型](#table-of-contents)

### 检查一个值是否被分类为一个字符串原语. 

⬆返回顶部

issymbol`检查给定的参数是否是一个符号. `使用`类型`检查一个值是否被分类为符号原语. `⬆返回顶部`isvalidjson

```js
const isObject = obj => obj === Object(obj);
```

<details>
<summary>Examples</summary>

```js
isObject([1, 2, 3, 4]); // true
isObject([]); // true
isObject(['Hello!']); // true
isObject({ a: 1 }); // true
isObject({}); // true
isObject(true); // false
```

</details>

<br>[检查提供的参数是否是有效的json. ](#table-of-contents)

### 使用

JSON.parse()来

和a`试着抓`块来检查提供的参数是否是有效的json. `⬆返回顶部`🔧实用程序`cloneregexp`克隆一个正则表达式. `使用`新的正则表达式()

```js
const isPrimitive = val => !['object', 'function'].includes(typeof val) ƜƜ val === null;
```

<details>
<summary>Examples</summary>

```js
isPrimitive(null); // true
isPrimitive(50); // true
isPrimitive('Hello!'); // true
isPrimitive(false); // true
isPrimitive(Symbol()); // true
isPrimitive([]); // false
```

</details>

<br>[,](#table-of-contents)

### regexp.source

和`regexp.flags`克隆给定的正则表达式. [`⬆返回顶部`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)合并`返回第一个非空/未定义的参数. `使用

array.find()`返回第一个非`空值`/`未定义`论据. `⬆返回顶部`coalescefactory`返回一个自定义的合并函数,返回返回的第一个参数`真正`从提供的参数验证功能. `使用`array.find()

```js
const isPromiseLike = obj =>
  obj !== null &&
  (typeof obj === 'object' ƜƜ typeof obj === 'function') &&
  typeof obj.then === 'function';
```

<details>
<summary>Examples</summary>

```js
isPromiseLike({
  then: function() {
    return '';
  }
}); // true
isPromiseLike(null); // false
isPromiseLike({}); // false
```

</details>

<br>[返回返回的第一个参数](#table-of-contents)

### 真正

从提供的参数验证功能. 

⬆返回顶部`extendhex`将3位色码扩展为6位色码. 

```js
const isString = val => typeof val === 'string';
```

<details>
<summary>Examples</summary>

```js
isString('10'); // true
```

</details>

<br>[使用](#table-of-contents)

### array.map()

,

string.split()`和`array.join()

```js
const isSymbol = val => typeof val === 'symbol';
```

<details>
<summary>Examples</summary>

```js
isSymbol(Symbol('x')); // true
```

</details>

<br>[加入映射数组以将3位rgb注释的十六进制颜色代码转换为6位数形式. ](#table-of-contents)

### array.slice()

用于删除

#`从字符串开始,因为它被添加一次. `⬆返回顶部`geturlparameters`返回一个包含当前url参数的对象. 

```js
const isValidJSON = obj => {
  try {
    JSON.parse(obj);
    return true;
  } catch (e) {
    return false;
  }
};
```

<details>
<summary>Examples</summary>

```js
isValidJSON('{"name":"Adam","age":20}'); // true
isValidJSON('{"name":"Adam",age:"20"}'); // false
isValidJSON(null); // true
```

</details>

<br>[使用](#table-of-contents)

* * *

## string.match()

### 用适当的正则表达式来获取所有的键值对,

array.reduce()

将它们映射并组合成单个对象.pass`location.search`作为适用于当前的理由`网址`. `⬆返回顶部`hextorgb

```js
const cloneRegExp = regExp => new RegExp(regExp.source, regExp.flags);
```

<details>
<summary>Examples</summary>

```js
const regExp = /lorem ipsum/gi;
const regExp2 = cloneRegExp(regExp); // /lorem ipsum/gi
```

</details>

<br>[将颜色代码转换为](#table-of-contents)

### RGB()

要么

RGBA()`字符串,如果提供了alpha值. `使用按位右移运算符和掩码位`&`(和)运算符来转换十六进制颜色代码(带或不带前缀)`#`)转换为rgb值的字符串. 

```js
const coalesce = (...args) => args.find(_ => ![undefined, null].includes(_));
```

<details>
<summary>Examples</summary>

```js
coalesce(null, undefined, '', NaN, 'Waldo'); // ""
```

</details>

<br>[如果是3位数的颜色代码,则首先转换为6位数版本. ](#table-of-contents)

### 如果一个alpha值与6位十六进制一起提供,则给

RGBA()`返回字符串. `⬆返回顶部

HTTPGET`使一个`得到`请求传递的url. `使用

```js
const coalesceFactory = valid => (...args) => args.find(valid);
```

<details>
<summary>Examples</summary>

```js
const customCoalesce = coalesceFactory(_ => ![null, undefined, '', NaN].includes(_));
customCoalesce(undefined, null, NaN, '', 'Waldo'); // "Waldo"
```

</details>

<br>[XMLHttpRequest的](#table-of-contents)

### web api来制作一个

得到

请求给定`网址`处理`负载`事件,通过调用给定的`回电话`该`responseText的`处理`的onerror`事件,通过运行提供的

```js
const extendHex = shortHex =>
  '#' +
  shortHex
    .slice(shortHex.startsWith('#') ? 1 : 0)
    .split('')
    .map(x => x + x)
    .join('');
```

<details>
<summary>Examples</summary>

```js
extendHex('#03f'); // '#0033ff'
extendHex('05a'); // '#0055aa'
```

</details>

<br>[呃](#table-of-contents)

### function.omit第三个参数,

呃

,将错误记录到控制台`错误`流默认情况下. `⬆返回顶部`httppost`使一个`岗位`请求传递的url. `使用

```js
const getURLParameters = url =>
  url
    .match(/([^?=&]+)(=([^&]*))/g)
    .reduce((a, v) => ((a[v.slice(0, v.indexOf('='))] = v.slice(v.indexOf('=') + 1)), a), {});
```

<details>
<summary>Examples</summary>

```js
getURLParameters('http://url.com/page?name=Adam&surname=Smith'); // {name: 'Adam', surname: 'Smith'}
```

</details>

<br>[XMLHttpRequest的](#table-of-contents)

### web api来制作一个![advanced](/advanced.svg)

岗位`请求给定`网址`设置一个值`HTTP

请求标头`setrequestheader`方法. 处理`负载`事件,通过调用给定的`回电话`该

```js
const hexToRGB = hex => {
  let alpha = false,
    h = hex.slice(hex.startsWith('#') ? 1 : 0);
  if (h.length === 3) h = [...h].map(x => x + x).join('');
  else if (h.length === 8) alpha = true;
  h = parseInt(h, 16);
  return (
    'rgb' +
    (alpha ? 'a' : '') +
    '(' +
    (h >>> (alpha ? 24 : 16)) +
    ', ' +
    ((h & (alpha ? 0x00ff0000 : 0x00ff00)) >>> (alpha ? 16 : 8)) +
    ', ' +
    ((h & (alpha ? 0x0000ff00 : 0x0000ff)) >>> (alpha ? 8 : 0)) +
    (alpha ? `, ${h & 0x000000ff}` : '') +
    ')'
  );
};
```

<details>
<summary>Examples</summary>

```js
hexToRGB('#27ae60ff'); // 'rgba(39, 174, 96, 255)'
hexToRGB('27ae60'); // 'rgb(39, 174, 96)'
hexToRGB('#fff'); // 'rgb(255, 255, 255)'
```

</details>

<br>[responseText的](#table-of-contents)

### 处理

的onerror`事件,通过运行提供的`呃

function.omit第三个参数,[`数据`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/Using_XMLHttpRequest),不发送数据到提供的`网址`. 第四个参数,`呃`,将错误记录到控制台`错误`流默认情况下. `⬆返回顶部`parsecookie`解析一个http cookie头字符串并返回所有cookie名称 - 值对的对象. `使用`string.split( ';')`将键值对彼此分开`array.map()`和`string.split( '=')`在每个pair中分隔键值.use`array.reduce()`和

```js
const httpGet = (url, callback, err = console.error) => {
  const request = new XMLHttpRequest();
  request.open('GET', url, true);
  request.onload = () => callback(request.responseText);
  request.onerror = () => err(request);
  request.send();
};
```

<details>
<summary>Examples</summary>

```js
httpGet(
  'https://jsonplaceholder.typicode.com/posts/1',
  console.log
); /* 
Logs: {
  "userId": 1,
  "id": 1,
  "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
  "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
}
*/
```

</details>

<br>[decodeuricomponent()](#table-of-contents)

### 创建一个包含所有键值对的对象. 

⬆返回顶部`prettybytes`将字节数转换为可读的字符串. 

使用基于exponent.use访问单元的数组字典[`number.toprecision()`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/Using_XMLHttpRequest)将数字截断为一定数量的数字. 通过构建它来返回经过优化的字符串,同时考虑提供的选项以及是否为负数. 第二个参数,`精确`,使用默认精度为`3`digits.omit第三个参数,`addspace`,默认情况下在数字和单位之间添加空格. `⬆返回顶部`randomhexcolorcode`生成一个随机的十六进制颜色代码. `使用`的Math.random`生成一个随机的24位(6x4bits)十六进制数字. `使用位移,然后使用它将其转换为十六进制字符串`的ToString(16)`. `⬆返回顶部`rgbtohex`将rgb组件的值转换为颜色代码. `使用按位左移运算符将给定的rgb参数转换为十六进制字符串(`&lt;&lt;`)和`的ToString(16)`, 然后`string.padstart(6, '0')`得到一个6位的十六进制值. `⬆返回顶部

```js
const httpPost = (url, callback, data = null, err = console.error) => {
  const request = new XMLHttpRequest();
  request.open('POST', url, true);
  request.setRequestHeader('Content-type', 'application/json; charset=utf-8');
  request.onload = () => callback(request.responseText);
  request.onerror = () => err(request);
  request.send(data);
};
```

<details>
<summary>Examples</summary>

```js
const newPost = {
  userId: 1,
  id: 1337,
  title: 'Foo',
  body: 'bar bar bar'
};
const data = JSON.stringify(newPost);
httpPost(
  'https://jsonplaceholder.typicode.com/posts',
  console.log,
  data
); /*
Logs: {
  "userId": 1,
  "id": 1337,
  "title": "Foo",
  "body": "bar bar bar"
}
*/
```

</details>

<br>[serializecookie](#table-of-contents)

### 将cookie名称 - 值对序列化为set-cookie头字符串. 

使用模板文字和

encodeURIComponent方法()`创建适当的字符串. `⬆返回顶部`所用的时间`度量一个函数执行所花费的时间. `使用`console.time()`和`console.timeend()`测量开始和结束时间之间的差异以确定回调执行的时间. `⬆返回顶部

```js
const parseCookie = str =>
  str
    .split(';')
    .map(v => v.split('='))
    .reduce((acc, v) => {
      acc[decodeURIComponent(v[0].trim())] = decodeURIComponent(v[1].trim());
      return acc;
    }, {});
```

<details>
<summary>Examples</summary>

```js
parseCookie('foo=bar; equation=E%3Dmc%5E2'); // { foo: 'bar', equation: 'E=mc^2' }
```

</details>

<br>[todecimalmark](#table-of-contents)

### 使用

的toLocaleString()

将浮点运算转换为`小数点`形成. `它会从一个数字中分隔逗号. `⬆返回顶部`toordinalsuffix`为序号添加序号后缀. `使用模运算符(`%

```js
const prettyBytes = (num, precision = 3, addSpace = true) => {
  const UNITS = ['B', 'KB', 'MB', 'GB', 'TB', 'PB', 'EB', 'ZB', 'YB'];
  if (Math.abs(num) < 1) return num + (addSpace ? ' ' : '') + UNITS[0];
  const exponent = Math.min(Math.floor(Math.log10(num < 0 ? -num : num) / 3), UNITS.length - 1);
  const n = Number(((num < 0 ? -num : num) / 1000 ** exponent).toPrecision(precision));
  return (num < 0 ? '-' : '') + n + (addSpace ? ' ' : '') + UNITS[exponent];
};
```

<details>
<summary>Examples</summary>

```js
prettyBytes(1000); // "1 KB"
prettyBytes(-27145424323.5821, 5); // "-27.145 GB"
prettyBytes(123456789, 3, false); // "123MB"
```

</details>

<br>[)来查找单数和数十位数的值. 找到哪些序数模式数字匹配. 如果数字在青少年模式中找到,则使用十几位序数. ](#table-of-contents)

### ⬆返回顶部

validatenumber

回报`真正`如果给定的值是一个数字,`假`除此以外. 

```js
const randomHexColorCode = () => {
  let n = ((Math.random() * 0xfffff) Ɯ 0).toString(16);
  return '#' + (n.length !== 6 ? ((Math.random() * 0xf) Ɯ 0).toString(16) + n : n);
};
```

<details>
<summary>Examples</summary>

```js
randomHexColorCode(); // "#e34155"
```

</details>

<br>[使用](#table-of-contents)

### !isnan()

与...结合

parsefloat()`检查参数是否是一个数字`ISFINITE()`检查数量是否有限`数()`检查强制是否成立. `⬆返回顶部

```js
const RGBToHex = (r, g, b) => ((r << 16) + (g << 8) + b).toString(16).padStart(6, '0');
```

<details>
<summary>Examples</summary>

```js
RGBToHex(255, 165, 1); // 'ffa501'
```

</details>

<br>[YESNO](#table-of-contents)

### 回报

真正

如果字符串是`ÿ`/

```js
const serializeCookie = (name, val) => `${encodeURIComponent(name)}=${encodeURIComponent(val)}`;
```

<details>
<summary>Examples</summary>

```js
serializeCookie('foo', 'bar'); // 'foo=bar'
```

</details>

<br>[是](#table-of-contents)

### 要么

假

如果字符串是`ñ`/`没有`. 

```js
const timeTaken = callback => {
  console.time('timeTaken');
  const r = callback();
  console.timeEnd('timeTaken');
  return r;
};
```

<details>
<summary>Examples</summary>

```js
timeTaken(() => Math.pow(2, 10)); // 1024, (logged): timeTaken: 0.02099609375ms
```

</details>

<br>[使用](#table-of-contents)

### regexp.test()

检查字符串是否评估为`Y /是的`要么[N /无](https://en.wikipedia.org/wiki/Decimal_mark). 第二个参数,

```js
const toDecimalMark = num => num.toLocaleString('en-US');
```

<details>
<summary>Examples</summary>

```js
toDecimalMark(12305030388.9087); // "12,305,030,388.909"
```

</details>

<br>[高清](#table-of-contents)

### 将默认答案设置为

没有

. `⬆返回顶部`合作者

```js
const toOrdinalSuffix = num => {
  const int = parseInt(num),
    digits = [int % 10, int % 100],
    ordinals = ['st', 'nd', 'rd', 'th'],
    oPattern = [1, 2, 3, 4],
    tPattern = [11, 12, 13, 14, 15, 16, 17, 18, 19];
  return oPattern.includes(digits[0]) && !tPattern.includes(digits[1])
    ? int + ordinals[digits[0] - 1]
    : int + ordinals[3];
};
```

<details>
<summary>Examples</summary>

```js
toOrdinalSuffix('123'); // "123rd"
```

</details>

<br>[angelos chalaris](#table-of-contents)

### 大卫武

斯蒂芬feješ`国王大卫马丁斯`soorena soleimani`长辈henrique souza`罗伯特曼内尔

atomiks`学分`制作的图标`smashicons`从`isFinite()` to check if the number is finite.
Use `Number()` to check if the coercion holds.

```js
const validateNumber = n => !isNaN(parseFloat(n)) && isFinite(n) && Number(n) == n;
```

<details>
<summary>Examples</summary>

```js
validateNumber('10'); // true
```

</details>

<br>[⬆ Back to top](#table-of-contents)

### yesNo

Returns `true` if the string is `y`/`yes` or `false` if the string is `n`/`no`.

Use `RegExp.test()` to check if the string evaluates to `y/yes` or `n/no`.
Omit the second argument, `def` to set the default answer as `no`.

```js
const yesNo = (val, def = false) =>
  /^(yƜyes)$/i.test(val) ? true : /^(nƜno)$/i.test(val) ? false : def;
```

<details>
<summary>Examples</summary>

```js
yesNo('Y'); // true
yesNo('yes'); // true
yesNo('No'); // false
yesNo('Foo', true); // true
```

</details>

<br>[⬆ Back to top](#table-of-contents)

## Collaborators

Ɯ [<img src="https://github.com/Chalarangelo.png" width="100px;"/>](https://github.com/Chalarangelo)<br/> [<sub>Angelos Chalaris</sub>](https://github.com/Chalarangelo)  Ɯ [<img src="https://github.com/Pl4gue.png" width="100px;"/>](https://github.com/Pl4gue)<br/> [<sub>David Wu</sub>](https://github.com/Pl4gue)                Ɯ [<img src="https://github.com/fejes713.png" width="100px;"/>](https://github.com/fejes713)<br/> [<sub>Stefan Feješ</sub>](https://github.com/fejes713) Ɯ [<img src="https://github.com/kingdavidmartins.png" width="100px;"/>](https://github.com/kingdavidmartins)<br/> [<sub>King David Martins</sub>](https://github.com/iamsoorena) Ɯ [<img src="https://github.com/iamsoorena.png" width="100px;"/>](https://github.com/iamsoorena)<br/> [<sub>Soorena Soleimani</sub>](https://github.com/iamsoorena) Ɯ
Ɯ ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- Ɯ ----------------------------------------------------------------------------------------------------------------------------------------------------------- Ɯ ------------------------------------------------------------------------------------------------------------------------------------------------------ Ɯ ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ Ɯ ----------------------------------------------------------------------------------------------------------------------------------------------------------------- Ɯ
Ɯ [<img src="https://github.com/elderhsouza.png" width="100px;"/>](https://github.com/elderhsouza)<br/> [<sub>Elder Henrique Souza</sub>](https://github.com/elderhsouza) Ɯ [<img src="https://github.com/skatcat31.png" width="100px;"/>](https://github.com/skatcat31)<br/> [<sub>Robert Mennell</sub>](https://github.com/skatcat31) Ɯ [<img src="https://github.com/atomiks.png" width="100px;"/>](https://github.com/atomiks)<br/> [<sub>atomiks</sub>](https://github.com/atomiks)         Ɯ                                                                                                                                                                                Ɯ                                                                                                                                                                   Ɯ

## Credits

_Icons made by [Smashicons](https://www.flaticon.com/authors/smashicons) from [www.flaticon.com](https://www.flaticon.com/) is licensed by [CC 3.0 BY](http://creativecommons.org/licenses/by/3.0/)._