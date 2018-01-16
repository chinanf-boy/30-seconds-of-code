### elementisvisibleinviewport

回报`真正`如果指定的元素在视口中可见,`假`除此以外. 

使用`element.getboundingclientrect()`和`window.inner(宽度Ɯ高度)`valuesto确定给定的元素是否在viewport中可见. 第二个参数确定元素是否完全可见,或者指定`真正`以确定是否部分可见. 

```js
const elementIsVisibleInViewport = (el, partiallyVisible = false) => {
  const { top, left, bottom, right } = el.getBoundingClientRect();
  const { innerHeight, innerWidth } = window;
  return partiallyVisible
    ? ((top > 0 && top < innerHeight) ƜƜ (bottom > 0 && bottom < innerHeight)) &&
        ((left > 0 && left < innerWidth) ƜƜ (right > 0 && right < innerWidth))
    : top >= 0 && left >= 0 && bottom <= innerHeight && right <= innerWidth;
};
```

```js
// e.g. 100x100 viewport and a 10x10px element at position {top: -1, left: 0, bottom: 9, right: 10}
elementIsVisibleInViewport(el); // false - (not fully visible)
elementIsVisibleInViewport(el, true); // true - (partially visible)
```