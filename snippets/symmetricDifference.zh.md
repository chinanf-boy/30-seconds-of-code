### 对称差

返回两个数组之间的对称差异. 

创建一个`组`从每个数组中,然后使用`array.filter()`在他们每个人只保留价值不包含在另一个. 

```js
const symmetricDifference = (a, b) => {
  const sA = new Set(a),
    sB = new Set(b);
  return [...a.filter(x => !sB.has(x)), ...b.filter(x => !sA.has(x))];
};
```

```js
symmetricDifference([1, 2, 3], [1, 2, 4]); // [3,4]
```