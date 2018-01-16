### splitlines

将多行字符串拆分成一行数组. 

使用`string.split()`和一个正则表达式来匹配换行符并创建一个数组. 

```js
const splitLines = str => str.split(/\r?\n/);
```

```js
splitLines('This\nis a\nmultiline\nstring.\n'); // ['This', 'is a', 'multiline', 'string.' , '']
```