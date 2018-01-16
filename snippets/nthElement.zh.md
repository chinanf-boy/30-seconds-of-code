### nthelement

返回数组的第n个元素. 

使用`array.slice()`得到一个包含第n个元素的数组. 如果索引超出范围,则返回`[]`. 第二个参数,`ñ`,得到数组的第一个元素. 

```js
const nthElement = (arr, n = 0) => (n > 0 ? arr.slice(n, n + 1) : arr.slice(n))[0];
```

```js
nthElement(['a', 'b', 'c'], 1); // 'b'
nthElement(['a', 'b', 'b'], -3); // 'a'
```