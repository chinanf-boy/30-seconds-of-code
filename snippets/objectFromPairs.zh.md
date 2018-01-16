### objectfrompairs

从给定的键值对创建一个对象. 

使用`array.reduce()`创建和组合键值对. 

```js
const objectFromPairs = arr => arr.reduce((a, v) => ((a[v[0]] = v[1]), a), {});
```

```js
objectFromPairs([['a', 1], ['b', 2]]); // {a: 1, b: 2}
```