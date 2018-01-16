### minby

在使用提供的函数将每个元素映射到一个值之后,返回数组的最小值. 

使用`array.map()`将每个元素映射到返回的值`FN`,`math.min()`获得最大价值. 

```js
const minBy = (arr, fn) => Math.min(...arr.map(typeof fn === 'function' ? fn : val => val[fn]));
```

```js
minBy([{ n: 4 }, { n: 2 }, { n: 8 }, { n: 6 }], o => o.n); // 8
minBy([{ n: 4 }, { n: 2 }, { n: 8 }, { n: 6 }], 'n'); // 8
```