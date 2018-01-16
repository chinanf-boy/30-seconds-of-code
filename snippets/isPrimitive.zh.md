### isprimitive

返回一个布尔值,判断传入的值是否为原始值. 

使用`array.includes()`在一个非原始类型的字符串数组上,提供使用的类型`类型`. 以来`typeof null`评估`'目的'`,需要直接比较. 

```js
const isPrimitive = val => !['object', 'function'].includes(typeof val) ƜƜ val === null;
```

```js
isPrimitive(null); // true
isPrimitive(50); // true
isPrimitive('Hello!'); // true
isPrimitive(false); // true
isPrimitive(Symbol()); // true
isPrimitive([]); // false
```