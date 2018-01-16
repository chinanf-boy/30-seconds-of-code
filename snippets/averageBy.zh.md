### averageby

在使用提供的函数将每个元素映射到一个值之后,返回数组的平均值. 

使用`array.map()`将每个元素映射到返回的值`FN`,`array.reduce()`将每个值添加到一个累加器,用一个值初始化`0`,除以`长度`的数组. 

```js
const averageBy = (arr, fn) =>
  arr.map(typeof fn === 'function' ? fn : val => val[fn]).reduce((acc, val) => acc + val, 0) /
  arr.length;
```

```js
averageBy([{ n: 4 }, { n: 2 }, { n: 8 }, { n: 6 }], o => o.n); // 5
averageBy([{ n: 4 }, { n: 2 }, { n: 8 }, { n: 6 }], 'n'); // 5
```