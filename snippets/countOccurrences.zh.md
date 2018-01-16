### countoccurrences

统计数组中某个值的出现次数. 

使用`array.reduce()`每次遇到数组中的特定值时增加一个计数器. 

```js
const countOccurrences = (arr, val) => arr.reduce((a, v) => (v === val ? a + 1 : a + 0), 0);
```

```js
countOccurrences([1, 1, 2, 1, 2, 3], 1); // 3
```