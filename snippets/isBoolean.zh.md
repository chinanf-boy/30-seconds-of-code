### isboolean

检查给定的参数是否是一个本地布尔元素. 

使用`类型`检查一个值是否被分类为一个布尔原语. 

```js
const isBoolean = val => typeof val === 'boolean';
```

```js
isBoolean(null); // false
isBoolean(false); // true
```