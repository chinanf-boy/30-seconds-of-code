### 调用getScrollPosition

返回当前页面的滚动位置. 

使用`pagexoffset`和`pageyoffset`如果他们被定义,否则`scrollleft`和`scrollTop的`你可以省略`埃尔`使用默认值`窗口`. 

```js
const getScrollPosition = (el = window) => ({
  x: el.pageXOffset !== undefined ? el.pageXOffset : el.scrollLeft,
  y: el.pageYOffset !== undefined ? el.pageYOffset : el.scrollTop
});
```

```js
getScrollPosition(); // {x: 0, y: 200}
```