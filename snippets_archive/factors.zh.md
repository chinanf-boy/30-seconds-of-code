### 因素

返回给定因子的数组`NUM`. `如果第二个参数设置为`真正`只返回主要因素`NUM`. 如果`NUM`是`1`要么`0`返回一个空的数组`NUM`小于`0`返回所有的因素`- 诠释

连同它们的加法逆. `使用`array.from()`,`array.map()`和`array.filter()`找出所有的因素`NUM`如果给定`NUM`是消极的,使用`array.reduce()`向数组中添加倒数. 如果返回所有结果`素数`是`假`否则确定并仅返回使用的主要因素`isprime`和`array.filter()`. 第二个参数,`素数

**,默认返回素数和非素数因子. **注意_:  -负数不被视为素数. _

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

```js
factors(12); // [2,3,4,6,12]
factors(12, true); // [2,3]
factors(-12); // [2, -2, 3, -3, 4, -4, 6, -6, 12, -12]
factors(-12, true); // [2,3]
```