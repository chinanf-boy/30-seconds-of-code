### invertkeyvalues

反转对象的键值对,而不会改变它. 

使用`object.keys()`和`array.reduce()`反转对象的键值对. 

```js
const invertKeyValues = obj =>
  Object.keys(obj).reduce((acc, key) => {
    acc[obj[key]] = key;
    return acc;
  }, {});
```

```js
invertKeyValues({ name: 'John', age: 20 }); // { 20: 'age', John: 'name' }
```