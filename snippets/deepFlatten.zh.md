### deepflatten

深沉的阵列. 

使用递归.use`array.concat()`用一个空数组(`[]`)和传播运算符(`...`)来扁平化一个数组. 递归地扁平化每个元素是一个数组. 

```js
const deepFlatten = arr => [].concat(...arr.map(v => (Array.isArray(v) ? deepFlatten(v) : v)));
```

```js
deepFlatten([1, [2], [[3], 4], 5]); // [1,2,3,4,5]
```