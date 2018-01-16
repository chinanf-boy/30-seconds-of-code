### chainasync

链异步功能. 

循环遍历包含异步事件的函数数组,调用`下一个`当每个异步事件已经完成时. 

```js
const chainAsync = fns => {
  let curr = 0;
  const next = () => fns[curr++](next);
  next();
};
```

```js
chainAsync([
  next => {
    console.log('0 seconds');
    setTimeout(next, 1000);
  },
  next => {
    console.log('1 second');
  }
]);
```