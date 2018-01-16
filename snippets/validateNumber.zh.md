### validatenumber

回报`真正`如果给定的值是一个数字,`假`除此以外. 

使用`!isnan()`与...结合`parsefloat()`检查参数是否是一个数字`ISFINITE()`检查数量是否有限`数()`检查强制是否成立. 

```js
const validateNumber = n => !isNaN(parseFloat(n)) && isFinite(n) && Number(n) == n;
```

```js
validateNumber('10'); // true
```