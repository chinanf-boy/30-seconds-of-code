### maxby

在使用提供的函数将每个元素映射到一个值之后,返回数组的最大值. 

使用`array.map()`将每个元素映射到返回的值`FN`,`math.max()`获得最大价值. 

```js
const maxBy = (arr, fn) => Math.max(...arr.map(typeof fn === 'function' ? fn : val => val[fn]));
```

```js
maxBy([{ n: 4 }, { n: 2 }, { n: 8 }, { n: 6 }], o => o.n); // 8
maxBy([{ n: 4 }, { n: 2 }, { n: 8 }, { n: 6 }], 'n'); // 8
```