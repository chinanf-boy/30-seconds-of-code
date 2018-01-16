### issymbol

检查给定的参数是否是一个符号. 

使用`类型`检查一个值是否被分类为符号原语. 

```js
const isSymbol = val => typeof val === 'symbol';
```

```js
isSymbol(Symbol('x')); // true
```