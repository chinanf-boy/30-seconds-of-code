### 素数

使用eratosthenes筛子生成达到给定数量的质数. 

从中生成一个数组`2`到给定的数字. `使用`array.filter()`过滤出可以被任何数字整除的值`2到提供的数字的平方根. 

```js
const primes = num => {
  let arr = Array.from({ length: num - 1 }).map((x, i) => i + 2),
    sqroot = Math.floor(Math.sqrt(num)),
    numsTillSqroot = Array.from({ length: sqroot - 1 }).map((x, i) => i + 2);
  numsTillSqroot.forEach(x => (arr = arr.filter(y => y % x !== 0 ƜƜ y == x)));
  return arr;
};
```

```js
primes(10); // [2,3,5,7]
```