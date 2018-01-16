### 压缩

创建一个元素数组,根据原始数组中的位置进行分组. 

使用`math.max.apply()`获取参数中最长的数组. 创建一个具有这个长度作为返回值和使用的数组`array.from()`用一个映射函数来创建一个分组元素数组. 如果参数数组的长度不一样,`未定义`用于没有价值的地方. 

```js
const zip = (...arrays) => {
  const maxLength = Math.max(...arrays.map(x => x.length));
  return Array.from({ length: maxLength }).map((_, i) => {
    return Array.from({ length: arrays.length }, (_, k) => arrays[k][i]);
  });
};
```

```js
zip(['a', 'b'], [1, 2], [true, false]); // [['a', 1, true], ['b', 2, false]]
zip(['a'], [1, 2], [true, false]); // [['a', 1, true], [undefined, 2, false]]
```