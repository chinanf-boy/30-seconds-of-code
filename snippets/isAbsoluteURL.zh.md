### isabsoluteurl

回报`真正`如果给定的字符串是一个绝对的url,`假`除此以外. 

使用正则表达式来测试字符串是否是绝对url. 

```js
const isAbsoluteURL = str => /^[a-z][a-z0-9+.-]*:/.test(str);
```

```js
isAbsoluteURL('https://google.com'); // true
isAbsoluteURL('ftp://www.myserver.net'); // true
isAbsoluteURL('/foo/bar'); // false
```