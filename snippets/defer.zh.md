### 延缓

延迟调用一个函数,直到当前的调用栈被清除. 

使用`的setTimeout()`以1ms的超时时间向浏览器事件队列添加新事件,并允许渲染引擎完成其工作. `使用传播(`...)运算符为该函数提供任意数量的参数. 

```js
const defer = (fn, ...args) => setTimeout(fn, 1, ...args);
```

```js
// Example A:
defer(console.log, 'a'), console.log('b'); // logs 'b' then 'a'

// Example B:
document.querySelector('#someElement').innerHTML = 'Hello';
longRunningFunction(); //Browser will not update the HTML until this has finished
defer(longRunningFunction); // Browser will update the HTML then run the function
```