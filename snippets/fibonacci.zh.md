### 斐波那契

生成一个包含斐波那契数列的数组,直到第n项. 

创建一个特定长度的空数组,初始化前两个值(`0`和`1`). 使用`array.reduce()`使用最后两个值的总和将值添加到数组中,除了前两个值之外. 

```js
const fibonacci = n =>
  Array.from({ length: n }).reduce(
    (acc, val, i) => acc.concat(i > 1 ? acc[i - 1] + acc[i - 2] : i),
    []
  );
```

```js
fibonacci(6); // [0, 1, 1, 2, 3, 5]
```