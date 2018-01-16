### 的binarySearch

使用递归. `如同`array.indexof()`找到数组中的值的索引. `不同的是,这个操作只适用于排序的数组,由于它与线性搜索相比具有对数性质,因此提供了主要的性能提升,或

array.indexof()`. `通过重复地将搜索间隔分成一半来搜索排序的数组. 以覆盖整个阵列的间隔开始. 如果搜索的值小于间隔中间的项目,则进入下半部分. 否则将进入上半部分. 反复递归,直到找到中间的值,或者您已经递归到大于表示该值不存在的长度并返回-1. 

```js
const binarySearch = (arr, val, start = 0, end = arr.length - 1) => {
  if (start > end) return -1;
  const mid = Math.floor((start + end) / 2);
  if (arr[mid] > val) return binarySearch(arr, val, start, mid - 1);
  if (arr[mid] < val) return binarySearch(arr, val, mid + 1, end);
  return mid;
}
```

```js
binarySearch([1, 4, 6, 7, 12, 13, 15, 18, 19, 20, 22, 24], 6); // 2
binarySearch([1, 4, 6, 7, 12, 13, 15, 18, 19, 20, 22, 24], 21); // -1
```