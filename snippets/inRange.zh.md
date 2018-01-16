### 在范围内

检查给定的数字是否落在给定范围内. 

使用算术比较来检查给定的数字是否在指定的范围内. 如果第二个参数,`结束`,没有指定,范围被认为是从`0`至`开始`. 

```js
const inRange = (n, start, end = null) => {
  if (end && start > end) end = [start, (start = end)][0];
  return end == null ? n >= 0 && n < start : n >= start && n < end;
};
```

```js
inRange(3, 2, 5); // true
inRange(3, 4); // true
inRange(2, 3, 5); // false
inrange(3, 2); // false
```