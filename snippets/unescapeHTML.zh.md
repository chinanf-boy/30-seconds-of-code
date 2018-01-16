### unescapehtml

unescapes逃脱了html字符. 

使用`与string.replace()`使用正则表达式匹配需要未转义的字符,使用回调函数使用字典(对象)将每个转义字符实例替换为与其相关联的非转义字符. 

```js
const unescapeHTML = str =>
  str.replace(
    /&amp;Ɯ&lt;Ɯ&gt;Ɯ&#39;Ɯ&quot;/g,
    tag =>
      ({
        '&amp;': '&',
        '&lt;': '<',
        '&gt;': '>',
        '&#39;': "'",
        '&quot;': '"'
      }[tag] ƜƜ tag)
  );
```

```js
unescapeHTML('&lt;a href=&quot;#&quot;&gt;Me &amp; you&lt;/a&gt;'); // '<a href="#">Me & you</a>'
```