### issorted

回报`1`如果数组按升序排序,`-1`如果按降序排列或者按照顺序排序`0`如果没有排序. 

计算顺序`方向`为前两个元素`object.entries()`循环访问数组对象并对它们进行比较. 返回`0`如果`方向`改变或`方向`如果到达最后一个元素. 

```js
const isSorted = arr => {
  const direction = arr[0] > arr[1] ? -1 : 1;
  for (let [i, val] of arr.entries())
    if (i === arr.length - 1) return direction;
    else if ((val - arr[i + 1]) * direction > 0) return 0;
};
```

```js
isSorted([0, 1, 2, 2]); // 1
isSorted([4, 3, 2]); // -1
isSorted([4, 3, 5]); // 0
```