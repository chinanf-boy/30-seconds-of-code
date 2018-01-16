### reversestring

反转一个字符串. 

使用扩展运算符(`...`)和`array.reverse()`以反转string.combine字符中的字符顺序来获取一个字符串`的string.join( '')`. 

```js
const reverseString = str => [...str].reverse().join('');
```

```js
reverseString('foobar'); // 'raboof'
```