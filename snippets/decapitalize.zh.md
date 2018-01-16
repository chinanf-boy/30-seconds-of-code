### decapitalize

将字符串的第一个字母去除. 

使用数组解构和`string.tolowercase()`给首字母去封顶,`...休息`在第一个字母后再获取字符数组`array.join( '')`使它再次成为一个字符串`upperrest`参数保持字符串的其余部分不变,或者将其设置为`真正`转换为大写. 

```js
const decapitalize = ([first, ...rest], upperRest = false) =>
  first.toLowerCase() + (upperRest ? rest.join('').toUpperCase() : rest.join(''));
```

```js
decapitalize('FooBar'); // 'fooBar'
decapitalize('FooBar', true); // 'fOOBAR'
```