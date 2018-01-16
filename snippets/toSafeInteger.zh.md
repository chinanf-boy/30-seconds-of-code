### tosafeinteger

将一个值转换为一个安全的整数. 

使用`math.max()`和`math.min()`找到最接近的安全值`math.round()`转换为一个整数. 

```js
const toSafeInteger = num =>
  Math.round(Math.max(Math.min(num, Number.MAX_SAFE_INTEGER), Number.MIN_SAFE_INTEGER));
```

```js
toSafeInteger('3.2'); // 3
toSafeInteger(Infinity); // 9007199254740991
```