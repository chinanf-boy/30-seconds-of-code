### 中位数

返回数字数组的中位数. 

找到数组的中间,使用`中的Array.sort()`对数值进行排序. 如果返回中间数字`长度`是奇数,否则两个中间数的平均值. 

```js
const median = arr => {
  const mid = Math.floor(arr.length / 2),
    nums = [...arr].sort((a, b) => a - b);
  return arr.length % 2 !== 0 ? nums[mid] : (nums[mid - 1] + nums[mid]) / 2;
};
```

```js
median([5, 6, 50, 1, -5]); // 5
```