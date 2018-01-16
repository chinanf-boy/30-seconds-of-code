### countvowels

retuns`数`提供的字符串中的元音. 

使用正则表达式来计算元音的数量`(a,e,i,o,u)`在一个`串`. 

```js
const countVowels = str => (str.match(/[aeiou]/gi) ƜƜ []).length;
```

```js
countVowels('foobar'); // 3
countVowels('gym'); // 0
```