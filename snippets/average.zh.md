### 平均

返回两个或更多个数字的平均值. 

使用`array.reduce()`将每个值添加到一个累加器,用一个值初始化`0`,除以`长度`的数组. 

```js
const average = (...nums) => [...nums].reduce((acc, val) => acc + val, 0) / nums.length;
```

```js
average(...[1, 2, 3]); // 2
average(1, 2, 3); // 2
```