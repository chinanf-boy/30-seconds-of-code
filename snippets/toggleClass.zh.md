### toggleclass

切换一个元素的类. 

使用`element.classlist.toggle()`为元素切换指定的类. 

```js
const toggleClass = (el, className) => el.classList.toggle(className);
```

```js
toggleClass(document.querySelector('p.special'), 'special'); // The paragraph will not have the 'special' class anymore
```