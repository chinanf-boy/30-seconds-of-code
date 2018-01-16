### 无

过滤出具有指定值之一的数组元素. 

使用`array.filter()`创建一个数组排除(使用`!array.includes()`)所有给定的值. 

_(用于改变原始数组的细节请参阅[`拉`](#pull))_

```js
const without = (arr, ...args) => arr.filter(v => !args.includes(v));
```

```js
without([2, 1, 2, 3], 1, 2); // [3]
```