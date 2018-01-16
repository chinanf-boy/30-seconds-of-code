### hasclass

回报`真正`如果元素具有指定的类,`假`除此以外. 

使用`element.classlist.contains()`检查元素是否具有指定的类. 

```js
const hasClass = (el, className) => el.classList.contains(className);
```

```js
hasClass(document.querySelector('p.special'), 'special'); // true
```