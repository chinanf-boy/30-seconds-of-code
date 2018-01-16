### filternonunique

过滤掉数组中的非唯一值. 

使用`array.filter()`只包含唯一值的数组

```js
const filterNonUnique = arr => arr.filter(i => arr.indexOf(i) === arr.lastIndexOf(i));
```

```js
filterNonUnique([1, 2, 2, 3, 4, 4, 5]); // [1,3,5]
```