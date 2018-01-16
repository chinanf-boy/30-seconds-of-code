### 采样大小

得到`ñ`随机元素的唯一键从`排列`达到大小`排列`. 

用数组洗牌数组[fisher-yates算法](https://github.com/chalarangelo/30-seconds-of-code#shuffle). 使用`array.slice()`获得第一名`ñ`elements.omit第二个参数,`ñ`从数组中随机获取一个元素. 

```js
const sampleSize = ([...arr], n = 1) => {
  let m = arr.length;
  while (m) {
    const i = Math.floor(Math.random() * m--);
    [arr[m], arr[i]] = [arr[i], arr[m]];
  }
  return arr.slice(0, n);
};
```

```js
sampleSize([1, 2, 3], 2); // [3,1]
sampleSize([1, 2, 3], 4); // [2,3,1]
```