### randomintegerinrange

返回指定范围内的随机整数. 

使用`的Math.random()`生成一个随机数并将其映射到期望的范围,使用`math.floor()`使其成为一个整数. 

```js
const randomIntegerInRange = (min, max) => Math.floor(Math.random() * (max - min + 1)) + min;
```

```js
randomIntegerInRange(0, 5); // 2
```