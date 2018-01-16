### randomnumberinrange

返回指定范围内的一个随机数. 

使用`的Math.random()`生成一个随机值,使用乘法将其映射到所需的范围. 

```js
const randomNumberInRange = (min, max) => Math.random() * (max - min) + min;
```

```js
randomNumberInRange(2, 10); // 6.0211363285087005
```