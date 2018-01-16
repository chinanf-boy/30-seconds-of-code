### 区别

返回两个数组之间的差异. 

创建一个`组`从`b`,然后使用`array.filter()`上`一个`只保留不包含的值`b`. 

```js
const difference = (a, b) => {
  const s = new Set(b);
  return a.filter(x => !s.has(x));
};
```

```js
difference([1, 2, 3], [1, 2, 4]); // [3]
```