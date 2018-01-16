### randomintarrayinrange

返回指定范围内的n个随机整数的数组. 

使用`array.from()`创建一个特定长度的空数组,`的Math.random()`生成一个随机数并将其映射到期望的范围,使用`math.floor()`使其成为一个整数. 

```js
const randomIntArrayInRange = (min, max, n = 1) =>
  Array.from({ length: n }, () => Math.floor(Math.random() * (max - min + 1)) + min);
```

```js
randomIntArrayInRange(12, 35, 10); // [ 34, 14, 27, 17, 30, 27, 20, 26, 21, 14 ]
```