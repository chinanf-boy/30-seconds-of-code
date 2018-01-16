### capitalizeeveryword

大写字符串中每个单词的第一个字母. 

使用`与string.replace()`匹配每个单词的第一个字符`string.touppercase()`将其资本化. 

```js
const capitalizeEveryWord = str => str.replace(/\b[a-z]/g, char => char.toUpperCase());
```

```js
capitalizeEveryWord('hello world!'); // 'Hello World!'
```