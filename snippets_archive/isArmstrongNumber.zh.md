### isarmstrongnumber

检查给定的号码是否是阿姆斯特朗号码. 

将给定的数字转换为数字数组. `使用指数运算符(`\*\*`)为每个数字获得适当的权力并总结出来. `如果总和等于数字本身,则返回`真正`除此以外假. 

```js
const isArmstrongNumber = digits =>
  (arr => arr.reduce((a, d) => a + parseInt(d) ** arr.length, 0) == digits)(
    (digits + '').split('')
  );
```

```js
isArmstrongNumber(1634); // true
isArmstrongNumber(56); // false
```