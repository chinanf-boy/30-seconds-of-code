### cloneregexp

克隆一个正则表达式. 

使用`新的正则表达式()`,`regexp.source`和`regexp.flags`克隆给定的正则表达式. 

```js
const cloneRegExp = regExp => new RegExp(regExp.source, regExp.flags);
```

```js
const regExp = /lorem ipsum/gi;
const regExp2 = cloneRegExp(regExp); // /lorem ipsum/gi
```