### sortcharactersinstring

按字母顺序排列字符串中的字符. 

使用扩展运算符(`...`)`中的Array.sort()`和`string.localecompare()`排序中的字符`海峡`,使用重组`的string.join( '')`. 

```js
const sortCharactersInString = str => [...str].sort((a, b) => a.localeCompare(b)).join('');
```

```js
sortCharactersInString('cabbage'); // 'aabbceg'
```