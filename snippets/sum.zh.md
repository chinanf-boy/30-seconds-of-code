### 和

返回两个或更多数字/数组的总和. 

使用`array.reduce()`将每个值添加到一个累加器,用一个值初始化`0`. 

```js
const sum = (...arr) => [...arr].reduce((acc, val) => acc + val, 0);
```

```js
sum(...[1, 2, 3, 4]); // 10
```