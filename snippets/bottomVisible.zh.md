### bottomvisible

回报`真正`如果页面底部可见,`假`除此以外. 

使用`scrolly`,`scrollHeight属性`和`clientheight`以确定页面的底部是否可见. 

```js
const bottomVisible = () =>
  document.documentElement.clientHeight + window.scrollY >=
  (document.documentElement.scrollHeight ƜƜ document.documentElement.clientHeight);
```

```js
bottomVisible(); // true
```