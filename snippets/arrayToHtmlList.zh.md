### arraytohtmllist

将给定的数组元素转换成`<LI>`标签并将其附加到给定ID的列表中. 

使用`array.map()`和`document.queryselector()`创建一个html标签列表. 

```js
const arrayToHtmlList = (arr, listID) =>
  arr.map(item => (document.querySelector('#' + listID).innerHTML += `<li>${item}</li>`));
```

```js
arrayToHtmlList(['item 1', 'item 2'], 'myListID');
```