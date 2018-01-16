### 多少次

返回次数`NUM`可以分为`除数`(整数或小数),而不会得到一个小数的答案. 

如果`除数`是`-1`要么`1`返回`无穷`. 如果`除数`是`-0`要么`0`返回`0`另外,不要分开`NUM`同`除数`并递增`一世`,而结果是一个整数. 返回循环执行的次数,`一世`. 

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

```js
howManyTimes(100, 2); // 2
howManyTimes(100, 2.5); // 2
howManyTimes(100, 0); // 0
howManyTimes(100, -1); // Infinity
```