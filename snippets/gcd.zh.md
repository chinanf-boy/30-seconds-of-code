### GCD

计算两个或更多数字/数组之间的最大公约数. 

内在`_gcd`函数使用recursion.base的情况是什么时候`ÿ`等于`0`. `在这种情况下,返回`X`其他的,返回gcd的`ÿ`和其余的部门`x / y的. 

```js
const gcd = (...arr) => {
  const _gcd = (x, y) => (!y ? x : gcd(y, x % y));
  return [...arr].reduce((a, b) => _gcd(a, b));
};
```

```js
gcd(8, 36); // 4
gcd(...[12, 8, 32]); // 4
```