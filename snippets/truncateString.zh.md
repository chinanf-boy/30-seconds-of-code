### truncatestring

截断一个字符串到指定的长度. 

确定字符串的`长度`大于`NUM`. 将字符串截断为所需的长度`'...'`追加到最后或原始字符串. 

```js
const truncateString = (str, num) =>
  str.length > num ? str.slice(0, num > 3 ? num - 3 : num) + '...' : str;
```

```js
truncateString('boomerang', 7); // 'boom...'
```