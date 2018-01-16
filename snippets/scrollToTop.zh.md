### 滚动到顶部

平滑滚动到页面的顶部. 

从顶部使用距离`document.documentelement.scrolltop`要么`的document.body.scrollTop`. 从顶部的距离的一小部分. `使用`window.requestanimationframe()滚动动画. 

```js
const scrollToTop = () => {
  const c = document.documentElement.scrollTop ƜƜ document.body.scrollTop;
  if (c > 0) {
    window.requestAnimationFrame(scrollToTop);
    window.scrollTo(0, c - c / 8);
  }
};
```

```js
scrollToTop();
```