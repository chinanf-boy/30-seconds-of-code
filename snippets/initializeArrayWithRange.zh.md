### initializearraywithrange

初始化包含指定范围中的数字的数组`开始`和`结束`是包容性的,有共同的区别`步`. 

使用`array.from(math.ceil((端+ 1开始)/步))`创建一个所需长度的数组(元素的数量等于`(端开始)/步`要么`(端+ 1开始)/步`为包容性结束),`array.map()`在一个范围内填充所需的值. 你可以省略`开始`使用默认值`0`你可以省略`步`使用默认值`1`. 

```js
const initializeArrayWithRange = (end, start = 0, step = 1) =>
  Array.from({ length: Math.ceil((end + 1 - start) / step) }).map((v, i) => i * step + start);
```

```js
initializeArrayWithRange(5); // [0,1,2,3,4,5]
initializeArrayWithRange(7, 3); // [3,4,5,6,7]
initializeArrayWithRange(9, 0, 2); // [0,2,4,6,8]
```