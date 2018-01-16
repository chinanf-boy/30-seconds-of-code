### takeright

返回一个包含n个元素的数组. 

使用`array.slice()`用来创建一个数组的切片`ñ`从最后采取的元素. 

```js
const takeRight = (arr, n = 1) => arr.slice(arr.length - n, arr.length);
```

```js
takeRight([1, 2, 3], 2); // [ 2, 3 ]
takeRight([1, 2, 3]); // [3]
```