### 所用的时间

度量一个函数执行的时间. 

使用`console.time()`和`console.timeend()`来衡量开始和结束时间之间的差异,以确定回调执行多长时间. 

```js
const timeTaken = callback => {
  console.time('timeTaken');
  const r = callback();
  console.timeEnd('timeTaken');
  return r;
};
```

```js
timeTaken(() => Math.pow(2, 10)); // 1024, (logged): timeTaken: 0.02099609375ms
```