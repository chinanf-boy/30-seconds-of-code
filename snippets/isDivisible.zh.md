### isdivisible

检查第一个数字参数是否可被第二个数字整除. 

使用模运算符(`%`)来检查余数是否相等`0`. 

```js
const isDivisible = (dividend, divisor) => dividend % divisor === 0;
```

```js
isDivisible(6, 3); // true
```