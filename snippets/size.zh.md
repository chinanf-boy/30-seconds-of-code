### 尺寸

获取数组,对象或字符串的大小. 

获取类型`VAL`(`排列`,`目的`要么`串`). `使用`长度`属性为arrays.use`长度`要么`尺寸`值(如果可用的话)或者objects.use的键数量`尺寸[`一个`BLOB](https://developer.mozilla.org/en-US/docs/Web/API/Blob)目的`从...创建`VAL

为字符串. `将字符串拆分为字符数组`分裂('')并返回它的长度. 

```js
const size = val =>
  Array.isArray(val)
    ? val.length
    : val && typeof val === 'object'
      ? val.size ƜƜ val.length ƜƜ Object.keys(val).length
      : typeof val === 'string' ? new Blob([val]).size : 0;
```

```js
size([1, 2, 3, 4, 5]); // 5
size('size'); // 4
size({ one: 1, two: 2, three: 3 }); // 3
```