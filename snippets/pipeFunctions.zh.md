### pipefunctions

执行从左到右的功能组合. 

使用`array.reduce()`与传播运算符(`...`)执行从左到右的函数组合. 第一个(最左边的)函数可以接受一个或多个参数;其余的功能必须是一元的. 

```js
const pipeFunctions = (...fns) => fns.reduce((f, g) => (...args) => g(f(...args)));
```

```js
const add5 = x => x + 5;
const multiply = (x, y) => x * y;
const multiplyAndAdd5 = pipeFunctions(multiply, add5);
multiplyAndAdd5(5, 2); // 15
```