### 百分

使用百分比公式来计算给定数组中有多少数字小于或等于给定值. 

使用`array.reduce()`计算有多少数值低于这个值,有多少是相同的值,并应用百分比公式. 

```js
const percentile = (arr, val) =>
  100 * arr.reduce((acc, v) => acc + (v < val ? 1 : 0) + (v === val ? 0.5 : 0), 0) / arr.length;
```

```js
percentile([1, 2, 3, 4, 5, 6, 7, 8, 9, 10], 6); // 55
```