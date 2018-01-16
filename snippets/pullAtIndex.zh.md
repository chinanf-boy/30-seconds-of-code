### pullatindex

改变原始数组以滤除指定索引处的值. 

使用`array.filter()`和`array.includes()`提取不需要的值`array.length = 0`通过将其长度重置为零来改变传入的数组`的Array.push()`重新填充它只有拉的values.use`的Array.push()`跟踪拉值

```js
const pullAtIndex = (arr, pullArr) => {
  let removed = [];
  let pulled = arr
    .map((v, i) => (pullArr.includes(i) ? removed.push(v) : v))
    .filter((v, i) => !pullArr.includes(i));
  arr.length = 0;
  pulled.forEach(v => arr.push(v));
  return removed;
};
```

```js
let myArray = ['a', 'b', 'c', 'd'];
let pulled = pullAtIndex(myArray, [1, 3]); // myArray = [ 'a', 'c' ] , pulled = [ 'b', 'd' ]
```