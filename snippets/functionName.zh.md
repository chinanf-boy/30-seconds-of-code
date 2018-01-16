### functionname

记录一个函数的名字. 

使用`console.debug()`和`名称`传入的方法的属性将方法的名称记录到`调试`控制台的通道. 

```js
const functionName = fn => (console.debug(fn.name), fn);
```

```js
functionName(Math.max); // max (logged in debug channel of console)
```