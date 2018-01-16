### indexofall

返回所有的索引`VAL`在一个数组中. `如果`VAL`从不发生,返回`\[]

. `使用`array.foreach()`循环元素和`的Array.push()存储匹配元素的索引. 返回索引数组. 

```js
const indexOfAll = (arr, val) => {
  const indices = [];
  arr.forEach((el, i) => el === val && indices.push(i));
  return indices;
};
```

```js
indexOfAll([1, 2, 3, 1, 2, 3], 1); // [0,3]
indexOfAll([1, 2, 3], 4); // []
```