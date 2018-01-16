### 利用

大写字符串的第一个字母. 

使用数组解构和`string.touppercase()`首字母大写,`...休息`在第一个字母后再获取字符数组`array.join( '')`使它再次成为一个字符串`lowerrest`参数保持字符串的其余部分不变,或者将其设置为`真正`转换为小写. 

```js
const capitalize = ([first, ...rest], lowerRest = false) =>
  first.toUpperCase() + (lowerRest ? rest.join('').toLowerCase() : rest.join(''));
```

```js
capitalize('fooBar'); // 'FooBar'
capitalize('fooBar', true); // 'Foobar'
```