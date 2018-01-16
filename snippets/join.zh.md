### 加入

将数组的所有元素连接成一个字符串并返回这个字符串. 

使用分隔符和结束分隔符. `使用`array.reduce()`把元素组合成一个string.omit第二个参数,`分隔器`,使用默认的分隔符`''`. 第三个参数,`结束`,使用相同的值`分隔器默认. 

```js
const join = (arr, separator = ',', end = separator) =>
  arr.reduce(
    (acc, val, i) =>
      i == arr.length - 2
        ? acc + val + end
        : i == arr.length - 1 ? acc + val : acc + val + separator,
    ''
  );
```

```js
join(['pen', 'pineapple', 'apple', 'pen'], ',', '&'); // "pen,pineapple,apple&pen"
join(['pen', 'pineapple', 'apple', 'pen'], ','); // "pen,pineapple,apple,pen"
join(['pen', 'pineapple', 'apple', 'pen']); // "pen,pineapple,apple,pen"
```