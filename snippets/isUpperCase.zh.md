### isuppercase

检查一个字符串是否为大写. 

将给定的字符串转换为大写,使用`string.touppercase()`并与原来的比较. 

```js
const isUpperCase = str => str === str.toUpperCase();
```

```js
isUpperCase('ABC'); // true
isLowerCase('A3@$'); // true
isLowerCase('aB4'); // false
```