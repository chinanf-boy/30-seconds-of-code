### mapvalues

使用与提供的对象相同的键创建对象,并通过为每个值运行提供的功能生成值. 

使用`object.keys(OBJ)`遍历对象的keys.use`array.reduce()`使用相同的键和映射值创建一个新的对象`FN`. 

```js
const mapValues = (obj, fn) =>
  Object.keys(obj).reduce((acc, k) => {
    acc[k] = fn(obj[k], k, obj);
    return acc;
  }, {});
```

```js
const users = {
  fred: { user: 'fred', age: 40 },
  pebbles: { user: 'pebbles', age: 1 }
};
mapValues(users, u => u.age); // { fred: 40, pebbles: 1 }
```