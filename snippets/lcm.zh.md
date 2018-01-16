### LCM

返回两个或更多数字的最小公倍数. 

使用最大公约数(gcd)公式和事实`lcm(x,y)= x * y / gcd(x,y)`确定最小公倍数. gcd公式使用递归. 

```js
const lcm = (...arr) => {
  const gcd = (x, y) => (!y ? x : gcd(y, x % y));
  const _lcm = (x, y) => x * y / gcd(x, y);
  return [...arr].reduce((a, b) => _lcm(a, b));
};
```

```js
lcm(12, 7); // 84
lcm(...[1, 3, 4, 5]); // 60
```