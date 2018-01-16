### geometricprogression

初始化包含指定范围中的数字的数组`开始`和`结束`是包容性的,两项之间的比例是`步`. 如果返回错误`步`等于`1`. 

使用`array.from()`,`math.log()`和`math.floor()`创建所需长度的数组,`array.map()`在范围内填充所需的值. 第二个参数,`开始`,使用默认值`1`. 第三个参数,`步`,使用默认值`2`. 

```js
const geometricProgression = (end, start = 1, step = 2) =>
  Array.from({ length: Math.floor(Math.log(end / start) / Math.log(step)) + 1 }).map(
    (v, i) => start * step ** i
  );
```

```js
geometricProgression(256); // [1, 2, 4, 8, 16, 32, 64, 128, 256]
geometricProgression(256, 3); // [3, 6, 12, 24, 48, 96, 192]
geometricProgression(256, 1, 4); // [1, 4, 16, 64, 256]
```