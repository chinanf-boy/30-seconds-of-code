### escapehtml

转义字符串在html中使用. 

使用`与string.replace()`使用正则表达式匹配需要转义的字符,使用回调函数使用字典(对象)将每个字符实例替换为与其关联的转义字符. 

```js
const escapeHTML = str =>
  str.replace(
    /[&<>'"]/g,
    tag =>
      ({
        '&': '&amp;',
        '<': '&lt;',
        '>': '&gt;',
        "'": '&#39;',
        '"': '&quot;'
      }[tag] ƜƜ tag)
  );
```

```js
escapeHTML('<a href="#">Me & you</a>'); // '&lt;a href=&quot;#&quot;&gt;Me &amp; you&lt;/a&gt;'
```