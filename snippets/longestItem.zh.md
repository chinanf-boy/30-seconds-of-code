### longestitem

采用任意数量的可迭代对象或对象`长度`财产和返回最长的一个. 

使用`中的Array.sort()`排序所有参数`长度`,返回第一个(最长的). 

```js
const longestItem = (...vals) => [...vals].sort((a, b) => b.length - a.length)[0];
```

```js
longestItem('this', 'is', 'a', 'testcase'); // 'testcase'
longestItem(...['a', 'ab', 'abc']); // 'abc'
longestItem(...['a', 'ab', 'abc'], 'abcd'); // 'abcd'
longestItem([1, 2, 3], [1, 2], [1, 2, 3, 4, 5]); // [1, 2, 3, 4, 5]
longestItem([1, 2, 3], 'foobar'); // 'foobar'
```