### 快速排序

快速排列数组(默认为升序排序). 

使用递归. `使用`array.filter`和传播运营商(`...`)创建一个数组,其中值小于主元的所有元素都在主元之前,并且所有元素的值都大于主元. `如果参数降序是真的,返回数组按降序排序. 

```js
const quickSort = ([n, ...nums], desc) =>
  isNaN(n)
    ? []
    : [
        ...quickSort(nums.filter(v => (desc ? v > n : v <= n)), desc),
        n,
        ...quickSort(nums.filter(v => (!desc ? v > n : v <= n)), desc)
      ];
```

```js
quickSort([4, 1, 3, 2]); // [1,2,3,4]
quickSort([4, 1, 3, 2], true); // [4,3,2,1]
```