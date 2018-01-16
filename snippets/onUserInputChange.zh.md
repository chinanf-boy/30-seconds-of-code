### onuserinputchange

每当用户输入类型更改时运行回调`老鼠`要么`触摸`). 

用于根据输入设备启用/禁用代码. `这个过程是动态的,并与混合设备(例如触摸屏手提电脑)一起工作. `使用两个事件监听器. `承担`老鼠`最初输入并绑定一个`touchstart`事件监听器到文档. `上`touchstart`,添加一个`鼠标移动`事件监听器连续听两次鼠标移动事件在20ms内发射,使用performance.now()在这些情况下,将输入类型作为参数运行回调. 

```js
const onUserInputChange = callback => {
  let type = 'mouse',
    lastTime = 0;
  const mousemoveHandler = () => {
    const now = performance.now();
    if (now - lastTime < 20)
      (type = 'mouse'), callback(type), document.removeEventListener('mousemove', mousemoveHandler);
    lastTime = now;
  };
  document.addEventListener('touchstart', () => {
    if (type === 'touch') return;
    (type = 'touch'), callback(type), document.addEventListener('mousemove', mousemoveHandler);
  });
};
```

```js
onUserInputChange(type => {
  console.log('The user is now using', type, 'as an input method.');
});
```