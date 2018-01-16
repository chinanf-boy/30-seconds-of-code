### sumpower

返回所有数字的幂的和`开始`至`结束`(包括两端). 

使用`array.fill()`创建目标范围内所有数字的数组,`array.map()`和指数运算符(`**`)把他们提高到`功率`和`array.reduce()`把它们加在一起. 第二个参数,`功率`,使用默认的权力`2`. 第三个参数,`开始`,使用默认的起始值`1`. 

```js
const sumPower = (end, power = 2, start = 1) =>
  Array(end + 1 - start)
    .fill(0)
    .map((x, i) => (i + start) ** power)
    .reduce((a, b) => a + b, 0);
```

```js
sumPower(10); // 385
sumPower(10, 3); //3025
sumPower(10, 3, 5); //2925
```