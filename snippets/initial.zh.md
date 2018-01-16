### 初始

返回除最后一个数组外的所有元素. 

使用`arr.slice(0,-1)`返回数组的最后一个元素. 

```js
const initial = arr => arr.slice(0, -1);
```

```js
initial([1, 2, 3]); // [1,2]
```