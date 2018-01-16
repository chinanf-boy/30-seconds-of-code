### initialize2darray

初始化一个给定的宽度和高度和值的二维数组. 

使用`array.map()`生成h行,其中每个行都是一个新的数组w,用值初始化. `如果没有提供该值,则默认为`空值. 

```js
const initialize2DArray = (w, h, val = null) =>
  Array.from({ length: h }).map(() => Array.from({ length: w }).fill(val));
```

```js
initialize2DArray(2, 2, 0); // [[0,0], [0,0]]
```