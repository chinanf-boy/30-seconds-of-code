### 阶乘

计算一个数的阶乘. 

使用递归.if`ñ`小于或等于`1`,返回`1`. 其他,退货的产品`ñ`和阶乘`n  -  1`. 如果发生异常`ñ`是一个负数. 

```js
const factorial = n =>
  n < 0
    ? (() => {
        throw new TypeError('Negative numbers are not allowed!');
      })()
    : n <= 1 ? 1 : n * factorial(n - 1);
```

```js
factorial(6); // 720
```