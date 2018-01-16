### 块

将一个数组分块成指定大小的较小数组. 

使用`array.from()`创建一个新的数组,适合将要生产的数据块`array.slice()`将新数组的每个元素映射到块的长度`尺寸`如果原始数组不能均匀分割,最后的块将包含剩余的元素. 

```js
const chunk = (arr, size) =>
  Array.from({ length: Math.ceil(arr.length / size) }, (v, i) =>
    arr.slice(i * size, i * size + size)
  );
```

```js
chunk([1, 2, 3, 4, 5], 2); // [[1,2],[3,4],[5]]
```