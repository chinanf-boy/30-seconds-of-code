### FindLast中

返回提供的函数返回真值的最后一个元素. 

使用`array.filter()`去除其中的元素`FN`返回falsey值,`array.slice(-1)`得到最后一个. 

```js
const findLast = (arr, fn) => arr.filter(fn).slice(-1);
```

```js
findLast([1, 2, 3, 4], n => n % 2 === 1); // 3
```