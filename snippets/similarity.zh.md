### 相似

返回出现在两个数组中的元素数组. 

使用`array.filter()`删除不属于的值`值`,确定使用`array.includes()`. 

```js
const similarity = (arr, values) => arr.filter(v => values.includes(v));
```

```js
similarity([1, 2, 3], [1, 2, 4]); // [1,2]
```