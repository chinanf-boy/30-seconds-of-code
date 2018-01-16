### 则IsObject

返回一个布尔值,确定传递的值是否是一个对象. 

使用`目的`构造函数为给定的值创建一个对象包装器. `如果价值是`空值`要么`未定义,创建并返回一个空的对象. 否则,返回对应于给定值的类型的对象. 

```js
const isObject = obj => obj === Object(obj);
```

```js
isObject([1, 2, 3, 4]); // true
isObject([]); // true
isObject(['Hello!']); // true
isObject({ a: 1 }); // true
isObject({}); // true
isObject(true); // false
```