### 离

从元素中移除一个事件监听器. 

使用`eventtarget.removeeventlistener()`从元素中删除事件侦听器. `省略第四个参数`OPTS`使用`假或者根据添加事件侦听器时使用的选项来指定它. 

```js
const off = (el, evt, fn, opts = false) => el.removeEventListener(evt, fn, opts);
```

```js
const fn = () => console.log('!');
document.body.addEventListener('click', fn);
off(document.body, 'click', fn); // no longer logs '!' upon clicking on the page
```