### 字谜

⚠️**警告**: 这个函数的执行时间随着每个字符呈指数增长. 

超过8到10个字符的任何东西都会导致浏览器挂起,因为它试图解决所有不同的组合. 

生成一个字符串的所有字符(包含重复). `对给定字符串中的每个字母使用递归,为其余字母创建所有的部分字母.use`array.map()`然后把这个字母和每个部分的字谜结合起来`array.reduce()`在一个数组中结合所有的字典. 基本情况是字符串`长度`等于`2`要么`1. 

```js
const anagrams = str => {
  if (str.length <= 2) return str.length === 2 ? [str, str[1] + str[0]] : [str];
  return str
    .split('')
    .reduce(
      (acc, letter, i) =>
        acc.concat(anagrams(str.slice(0, i) + str.slice(i + 1)).map(val => letter + val)),
      []
    );
};
```

```js
anagrams('abc'); // ['abc','acb','bac','bca','cab','cba']
```