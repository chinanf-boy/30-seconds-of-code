### objecttopairs

从一个对象中创建一个键 - 值对数组的数组. 

使用`object.keys()`和`array.map()`遍历对象的键并生成一个包含键值对的数组. 

```js
const objectToPairs = obj => Object.keys(obj).map(k => [k, obj[k]]);
```

```js
objectToPairs({ a: 1, b: 2 }); // [['a',1],['b',2]]
```