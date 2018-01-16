### differencewith

滤除比较函数不返回的数组中的所有值`真正`. 

使用`array.filter()`和`array.findindex()`找到合适的值. 

```js
const differenceWith = (arr, val, comp) => arr.filter(a => val.findIndex(b => comp(a, b)) === -1);
```

```js
differenceWith([1, 1.2, 1.5, 3, 0], [1.9, 3, 0], (a, b) => Math.round(a) === Math.round(b)); // [1, 1.2]
```