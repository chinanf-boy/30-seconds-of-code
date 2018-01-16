### GetStyle为

返回指定元素的css规则的值. 

使用`window.getcomputedstyle()`获取指定元素的css规则的值. 

```js
const getStyle = (el, ruleName) => getComputedStyle(el)[ruleName];
```

```js
getStyle(document.querySelector('p'), 'font-size'); // '16px'
```