### fibonaccicountuntilnum

返回斐波纳契数字的数量`NUM`(`0`和`NUM`包括的). 

用一个数学公式来计算斐波那契数的数量直到`NUM`. 

```js
const fibonacciCountUntilNum = num =>
  Math.ceil(Math.log(num * Math.sqrt(5) + 1 / 2) / Math.log((Math.sqrt(5) + 1) / 2));
```

```js
fibonacciCountUntilNum(10); // 7
```