### 隐藏

隐藏指定的所有元素. 

使用扩展运算符(`...`)和`array.foreach()`申请`显示: 无`到每个指定的元素. 

```js
const hide = (...el) => [...el].forEach(e => (e.style.display = 'none'));
```

```js
hide(...document.querySelectorAll('img')); // Hides all <img> elements on the page
```