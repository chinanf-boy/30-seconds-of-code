### 挑

从对象中选择与给定键对应的键值对. 

使用`array.reduce()`如果密钥存在于obj中,则将过滤/拾取的密钥转换回具有对应的密钥 - 值对的对象. 

```js
const pick = (obj, arr) =>
  arr.reduce((acc, curr) => (curr in obj && (acc[curr] = obj[curr]), acc), {});
```

```js
pick({ a: 1, b: '2', c: 3 }, ['a', 'c']); // { 'a': 1, 'c': 3 }
```