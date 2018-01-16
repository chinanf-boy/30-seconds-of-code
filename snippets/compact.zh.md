### 紧凑

从数组中删除falsey值. 

使用`array.filter()`过滤出错误的值(`假`,`空值`,`0`,`""`,`未定义`,和`楠`). 

```js
const compact = arr => arr.filter(Boolean);
```

```js
compact([0, 1, false, 2, '', 3, 'a', 'e' * 23, NaN, 's', 34]); // [ 1, 2, 3, 'a', 's', 34 ]
```