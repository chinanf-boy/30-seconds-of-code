### 幂

返回给定数组数组的powerset. 

使用`array.reduce()`结合`array.map()`遍历元素并组合成一个包含所有组合的数组. 

```js
const powerset = arr => arr.reduce((a, v) => a.concat(a.map(r => [v].concat(r))), [[]]);
```

```js
powerset([1, 2]); // [[], [1], [2], [2,1]]
```