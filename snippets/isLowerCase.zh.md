### islowercase

检查一个字符串是否小写. 

将给定的字符串转换为小写,使用`string.tolowercase()`并与原来的比较. 

```js
const isLowerCase = str => str === str.toLowerCase();
```

```js
isLowerCase('abc'); // true
isLowerCase('a3@$'); // true
isLowerCase('Ab4'); // false
```