### 回合

将数字四舍五入到指定的数字位数. 

使用`math.round()`和模板文字将数字四舍五入为指定的位数. 第二个参数,`小数点`舍入为一个整数. 

```js
const round = (n, decimals = 0) => Number(`${Math.round(`${n}e${decimals}`)}e-${decimals}`);
```

```js
round(1.005, 2); // 1.01
```