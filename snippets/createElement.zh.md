### 的createElement

从一个字符串创建一个元素(不附加到文档). 

如果给定的字符串包含多个元素,则只返回第一个. `使用`使用document.createElement()`创建一个新的元素`的innerHTML`到作为参数提供的字符串. `使用parentnode.firstelementchild返回字符串的元素版本. 

```js
const createElement = str => {
  const el = document.createElement('div');
  el.innerHTML = str;
  return el.firstElementChild;
};
```

```js
const el = createElement(
  `<div class="container">
    <p>Hello!</p>
  </div>`
);
console.log(el.className); // 'container'
```