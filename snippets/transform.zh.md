### 转变

对累加器和对象中的每个键(从左到右)应用一个函数. 

使用`object.keys(OBJ)`遍历对象中的每个键,`array.reduce()`调用对指定的累加器应用指定的函数. 

```js
const transform = (obj, fn, acc) => Object.keys(obj).reduce((a, k) => fn(a, obj[k], k, obj), acc);
```

```js
transform(
  { a: 1, b: 2, c: 1 },
  (r, v, k) => {
    (r[v] ƜƜ (r[v] = [])).push(k);
    return r;
  },
  {}
); // { '1': ['a', 'c'], '2': ['b'] }
```