### 弄平

将阵列变平直到指定的深度. 

使用递归,递减`深度`用于每个深度级别1`array.reduce()`和`array.concat()`合并元素或数组.base的情况下,为`深度`等于`1`停止递归. 第二个参数,`深度`只能将其平坦化`1`(单一平坦). 

```js
const flatten = (arr, depth = 1) =>
  depth != 1
    ? arr.reduce((a, v) => a.concat(Array.isArray(v) ? flatten(v, depth - 1) : v), [])
    : arr.reduce((a, v) => a.concat(v), []);
```

```js
flatten([1, [2], 3, 4]); // [1, 2, 3, 4]
flatten([1, [2, [3, [4, 5], 6], 7], 8], 2); // [1, 2, 3, [4, 5], 6, 7, 8]
```