### ISNUMBER

检查给定的参数是否是一个数字. 

使用`类型`检查一个值是否被分类为数字原语. 

```js
const isNumber = val => typeof val === 'number';
```

```js
isNumber('1'); // false
isNumber(1); // true
```