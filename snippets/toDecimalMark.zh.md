### todecimalmark

使用`的toLocaleString()`将浮点运算转换为[小数点](https://en.wikipedia.org/wiki/Decimal_mark)形成. 它使一个逗号分隔的字符串从一个数字. 

```js
const toDecimalMark = num => num.toLocaleString('en-US');
```

```js
toDecimalMark(12305030388.9087); // "12,305,030,388.909"
```