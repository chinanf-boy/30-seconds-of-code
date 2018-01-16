### foreachright

从数组的最后一个元素开始,为每个数组元素执行一次提供的函数. 

使用`array.slice(0)`克隆给定的数组,`array.reverse()`扭转它和`array.foreach()`遍历倒排的数组. 

```js
const forEachRight = (arr, callback) =>
  arr
    .slice(0)
    .reverse()
    .forEach(callback);
```

```js
forEachRight([1, 2, 3, 4], val => console.log(val)); // '4', '3', '2', '1'
```