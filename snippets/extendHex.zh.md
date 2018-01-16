### extendhex

将3位数的颜色代码扩展为6位数的颜色代码. 

使用`array.map()`,`string.split()`和`array.join()`加入映射数组,将3位rgb注释的十六进制颜色代码转换为6位数形式. `array.slice()`是用来删除`#`从字符串开始,因为它被添加一次. 

```js
const extendHex = shortHex =>
  '#' +
  shortHex
    .slice(shortHex.startsWith('#') ? 1 : 0)
    .split('')
    .map(x => x + x)
    .join('');
```

```js
extendHex('#03f'); // '#0033ff'
extendHex('05a'); // '#0055aa'
```