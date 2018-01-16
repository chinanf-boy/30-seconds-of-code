### 撰写

执行从右到左的功能组合. 

使用`array.reduce()`执行从右到左的函数组合. 最后(最右边的)函数可以接受一个或多个参数;其余的功能必须是一元的. 

```js
const compose = (...fns) => fns.reduce((f, g) => (...args) => f(g(...args)));
```

```js
const add5 = x => x + 5;
const multiply = (x, y) => x * y;
const multiplyAndAdd5 = compose(add5, multiply);
multiplyAndAdd5(5, 2); // 15
```