### 显示

显示了所有指定的元素. 

使用扩展运算符(`...`)和`array.foreach()`清除`显示`属性指定的每个元素. 

```js
const show = (...el) => [...el].forEach(e => (e.style.display = ''));
```

```js
show(...document.querySelectorAll('img')); // Shows all <img> elements on the page
```