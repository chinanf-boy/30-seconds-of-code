### runpromisesinseries

运行一连串的承诺. 

使用`array.reduce()`创建一个承诺链,每个承诺在解决时都会返回下一个承诺. 

```js
const runPromisesInSeries = ps => ps.reduce((p, next) => p.then(next), Promise.resolve());
```

```js
const delay = d => new Promise(r => setTimeout(r, d));
runPromisesInSeries([() => delay(1000), () => delay(2000)]); // Executes each promise sequentially, taking a total of 3 seconds to complete
```