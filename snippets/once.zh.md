### 一旦

确保函数只被调用一次. 

利用封闭,使用一面旗帜,`叫`,并将其设置为`真正`一旦函数第一次被调用,防止它被再次调用. `为了让功能有其自身的功能`这个`上下文改变了(比如在一个事件监听器中),`功能`关键字必须被使用,并且所提供的函数必须具有应用的上下文. 允许使用其余的/传播的函数提供任意数量的参数`...)运营商. 

```js
const once = fn => {
  let called = false;
  return function(...args) {
    if (called) return;
    called = true;
    return fn.apply(this, args);
  };
};
```

```js
const startApp = function(event) {
  console.log(this, event); // document.body, MouseEvent
};
document.body.addEventListener('click', once(startApp)); // only runs `startApp` once upon click
```