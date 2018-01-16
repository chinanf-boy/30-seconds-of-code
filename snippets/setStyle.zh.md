### 的setStyle

为指定的元素设置一个css规则的值. 

使用`element.style`将指定元素的css规则的值设置为`VAL`. 

```js
const setStyle = (el, ruleName, val) => (el.style[ruleName] = val);
```

```js
setStyle(document.querySelector('p'), 'font-size', '20px'); // The first <p> element on the page will have a font-size of 20px
```