### dropright

返回一个新的数组`ñ`元素从右侧移除. 

使用`array.slice()`从右侧删除指定数量的元素. 

```js
const dropRight = (arr, n = 1) => arr.slice(0, -n);
```

```js
dropRight([1, 2, 3]); // [1,2]
dropRight([1, 2, 3], 2); // [1]
dropRight([1, 2, 3], 42); // []
```