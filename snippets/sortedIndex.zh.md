### sortedindex

返回值应该插入到数组中的最低索引,以保持其排序顺序. 

检查数组是否按降序(松散地)排序`array.findindex()`找到元素应该被插入的适当的索引. 

```js
const sortedIndex = (arr, n) => {
  const isDescending = arr[0] > arr[arr.length - 1];
  const index = arr.findIndex(el => (isDescending ? n >= el : n <= el));
  return index === -1 ? arr.length : index;
};
```

```js
sortedIndex([5, 3, 2, 1], 4); // 1
sortedIndex([30, 50], 40); // 1
```