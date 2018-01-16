### 拉

改变原始数组以滤除指定的值. 

使用`array.filter()`和`array.includes()`提取不需要的值`array.length = 0`通过将其长度重置为零来改变传入的数组`的Array.push()`重新填充它只有拉的值. 

_(对于不改变原始数组的片段,请参阅[`无`](#without))_

```js
const pull = (arr, ...args) => {
  let argState = Array.isArray(args[0]) ? args[0] : args;
  let pulled = arr.filter((v, i) => !argState.includes(v));
  arr.length = 0;
  pulled.forEach(v => arr.push(v));
};
```

```js
let myArray = ['a', 'b', 'c', 'a', 'b', 'c'];
pull(myArray, 'a', 'c'); // myArray = [ 'b', 'b' ]
```