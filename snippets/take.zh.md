### 采取

返回一个包含n个元素的数组. 

使用`array.slice()`用数组创建一个分片`ñ`从头开始的元素. 

```js
const take = (arr, n = 1) => arr.slice(0, n);
```

```js
take([1, 2, 3], 5); // [1, 2, 3]
take([1, 2, 3], 0); // []
```