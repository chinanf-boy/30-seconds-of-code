### removevowels

返回a中的所有元音`海峡`取而代之`REPL`. 

使用`与string.replace()`用正则表达式来替换所有的元音`海峡`.omot`REPL`使用默认值`""`. 

```js
const removeVowels = (str, repl = '') => str.replace(/[aeiou]/gi,repl);
```

```js
removeVowels("foobAr"); // "fbr"
removeVowels("foobAr","*"); // "f**b*r"
```