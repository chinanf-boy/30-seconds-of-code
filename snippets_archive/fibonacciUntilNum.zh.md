### fibonacciuntilnum

生成一个包含斐波那契数列的数组,直到第n项. 

创建一个特定长度的空数组,初始化前两个值(`0`和`1`). 使用`array.reduce()`使用最后两个值的总和将值添加到数组中,除了前两个值之外,使用数学公式来计算所需数组的长度. 

```js
const fibonacciUntilNum = num => {
  let n = Math.ceil(Math.log(num * Math.sqrt(5) + 1 / 2) / Math.log((Math.sqrt(5) + 1) / 2));
  return Array.from({ length: n }).reduce(
    (acc, val, i) => acc.concat(i > 1 ? acc[i - 1] + acc[i - 2] : i),
    []
  );
};
```

```js
fibonacciUntilNum(10); // [ 0, 1, 1, 2, 3, 5, 8 ]
```