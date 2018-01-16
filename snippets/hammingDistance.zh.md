### 汉明距离

计算两个值之间的汉明距离. 

使用xor运算符(`^`)来查找这两个数字之间的位差,使用转换为二进制字符串`的ToString(2)`.count和返回的数量`1`在字符串中,使用`匹配(/ 1 /克)`. 

```js
const hammingDistance = (num1, num2) => ((num1 ^ num2).toString(2).match(/1/g) ƜƜ '').length;
```

```js
hammingDistance(2, 3); // 1
```