### 复制到剪贴板

将一个字符串复制到剪贴板. `仅作为用户行为的结果(即,`点击

事件监听器). `创建一个新的`&lt;textarea>的`元素,使用提供的数据填充它,并将其添加到html document.use`selection.getrangeat()`存储选择的范围(如果有的话).use`document.execcommand( '复制')`复制到剪贴板. 删除`&lt;textarea>的`元素从html文档中最终使用`选择(). 的AddRange()恢复原来的选定范围(如果有的话). 

```js
const copyToClipboard = str => {
  const el = document.createElement('textarea');
  el.value = str;
  el.setAttribute('readonly', '');
  el.style.position = 'absolute';
  el.style.left = '-9999px';
  document.body.appendChild(el);
  const selected =
    document.getSelection().rangeCount > 0 ? document.getSelection().getRangeAt(0) : false;
  el.select();
  document.execCommand('copy');
  document.body.removeChild(el);
  if (selected) {
    document.getSelection().removeAllRanges();
    document.getSelection().addRange(selected);
  }
};
```

```js
copyToClipboard('Lorem ipsum'); // 'Lorem ipsum' copied to clipboard.
```