### 回文

回报`真正`如果给定的字符串是回文,`假`除此以外. 

转换字符串`string.tolowercase()`并使用`与string.replace()`从中删除非字母数字字符. 然后,`string.split( '')`成个人角色,`array.reverse()`,`的string.join( '')`并在转换之后与原始的非反转字符串进行比较`string.tolowercase()`. 

```js
const palindrome = str => {
  const s = str.toLowerCase().replace(/[\W_]/g, '');
  return (
    s ===
    s
      .split('')
      .reverse()
      .join('')
  );
};
```

```js
palindrome('taco cat'); // true
```