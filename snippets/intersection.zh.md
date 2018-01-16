### 路口

返回两个数组中存在的元素列表. 

创建一个`组`从`b`,然后使用`array.filter()`上`一个`只保留包含的值`b`. 

```js
const intersection = (a, b) => {
  const s = new Set(b);
  return a.filter(x => s.has(x));
};
```

```js
intersection([1, 2, 3], [4, 3, 2]); // [2,3]
```