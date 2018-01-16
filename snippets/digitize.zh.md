### 数字化

将数字转换为数字数组. 

将数字转换为字符串,使用扩展运算符(`...`)来构建一个array.use`array.map()`和`parseInt函数()`将每个值转换为一个整数. 

```js
const digitize = n => [...`${n}`].map(i => parseInt(i));
```

```js
digitize(123); // [1, 2, 3]
```