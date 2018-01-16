### SBDM

将输入字符串散列为整数. 

使用`string.split( '')`和`array.reduce()`创建输入字符串的散列,利用位移. 

```js
const sdbm = str => {
  let arr = str.split('');
  return arr.reduce(
    (hashCode, currentVal) =>
      (hashCode = currentVal.charCodeAt(0) + (hashCode << 6) + (hashCode << 16) - hashCode),
    0
  );
};
```

```js
sdbm('name'); // -3521204949
```