### 将gettype

返回值的本机类型. 

返回小写的构造函数名称的值,`"不确定"`要么`"空值"`如果价值是`未定义`要么`空值`. 

```js
const getType = v =>
  v === undefined ? 'undefined' : v === null ? 'null' : v.constructor.name.toLowerCase();
```

```js
getType(new Set([1, 2, 3])); // 'set'
```