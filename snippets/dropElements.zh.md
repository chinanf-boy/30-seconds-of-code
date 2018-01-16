### dropelements

删除数组中的元素,直到传递的函数返回`真正`. 

返回数组中的其余元素. `循环遍历数组,使用`array.slice()`删除数组的第一个元素,直到函数的返回值为止`真正回收剩余的元素. 

```js
const dropElements = (arr, func) => {
  while (arr.length > 0 && !func(arr[0])) arr = arr.slice(1);
  return arr;
};
```

```js
dropElements([1, 2, 3, 4], n => n >= 3); // [3,4]
```