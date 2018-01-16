### isfunction

检查给定的参数是否是一个函数. 

使用`类型`检查一个值是否被分类为一个函数原语. 

```js
const isFunction = val => typeof val === 'function';
```

```js
isFunction('x'); // false
isFunction(x => x); // true
```