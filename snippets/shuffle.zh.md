### 拖曳

随机化一个数组的值的顺序,返回一个新的数组. 

使用[fisher-yates算法](https://github.com/chalarangelo/30-seconds-of-code#shuffle)重新排列数组的元素. 

```js
const shuffle = ([...arr]) => {
  let m = arr.length;
  while (m) {
    const i = Math.floor(Math.random() * m--);
    [arr[m], arr[i]] = [arr[i], arr[m]];
  }
  return arr;
};
```

```js
const foo = [1, 2, 3];
shuffle(foo); // [2,3,1], foo = [1,2,3]
```