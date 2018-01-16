### escaperegexp

转义字符串以在正则表达式中使用. 

使用`与string.replace()`逃避特殊字符. 

```js
const escapeRegExp = str => str.replace(/[.*+?^${}()Ɯ[\]\\]/g, '\\$&');
```

```js
escapeRegExp('(test)'); // \\(test\\)
```