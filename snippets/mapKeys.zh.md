### 映射键

通过为每个键运行提供的功能和与提供的对象相同的值来创建具有键生成的对象. 

使用`object.keys(OBJ)`遍历对象的keys.use`array.reduce()`使用相同的值和映射的键创建一个新的对象`FN`. 

```js
const mapKeys = (obj, fn) =>
  Object.keys(obj).reduce((acc, k) => {
    acc[fn(obj[k], k, obj)] = obj[k];
    return acc;
  }, {});
```

```js
mapKeys({ a: 1, b: 2 }, (val, key) => key + val); // { a1: 1, b2: 2 }
```