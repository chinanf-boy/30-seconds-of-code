### pullatvalue

改变原始数组以滤除指定的值. 

返回删除的元素. `使用`array.filter()`和`array.includes()`提取不需要的值`array.length = 0`通过将其长度重置为零来改变传入的数组`的Array.push()`重新填充它只有拉的values.use`的Array.push()跟踪拉值

```js
const pullAtValue = (arr, pullArr) => {
  let removed = [],
    pushToRemove = arr.forEach((v, i) => (pullArr.includes(v) ? removed.push(v) : v)),
    mutateTo = arr.filter((v, i) => !pullArr.includes(v));
  arr.length = 0;
  mutateTo.forEach(v => arr.push(v));
  return removed;
};
```

```js
let myArray = ['a', 'b', 'c', 'd'];
let pulled = pullAtValue(myArray, ['b', 'd']); // myArray = [ 'a', 'c' ] , pulled = [ 'b', 'd' ]
```