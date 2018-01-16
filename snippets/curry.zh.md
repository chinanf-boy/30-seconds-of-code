### 咖喱

咖喱功能. 

使用递归. 如果提供的参数数量(`ARGS`)就足够了,调用传递函数`FN`. 另外,返回一个curried函数`FN`如果你想要一个接受可变数目参数的函数(一个可变参数函数,例如,`math.min()`),您可以选择将参数个数传递给第二个参数`元数`. 

```js
const curry = (fn, arity = fn.length, ...args) =>
  arity <= args.length ? fn(...args) : curry.bind(null, fn, arity, ...args);
```

```js
curry(Math.pow)(2)(10); // 1024
curry(Math.min, 3)(10)(50)(2); // 2
```