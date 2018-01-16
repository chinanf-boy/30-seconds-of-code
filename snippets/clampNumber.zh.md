### clampnumber

夹子`NUM`在由边界值规定的包含范围内`一个`和`b`. 

如果`NUM`属于范围之内,归还`NUM`. 另外,返回范围内最近的数字. 

```js
const clampNumber = (num, a, b) => Math.max(Math.min(num, Math.max(a, b)), Math.min(a, b));
```

```js
clampNumber(2, 3, 5); // 3
clampNumber(1, -1, -5); // -1
```