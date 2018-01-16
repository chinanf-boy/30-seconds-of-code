### luhncheck

的执行情况[luhn算法](https://en.wikipedia.org/wiki/Luhn_algorithm)用于验证各种标识号码,如信用卡号码,imei号码,国家提供商标识号码等. 

使用`string.split( '')`,`array.reverse()`和`array.map()`与...结合`parseInt函数()`获得一个digits.use数组`方法Array.splice(0,1)`获取最后一位数字`array.reduce()`来实现luhn算法`真正`如果`和`可以被整除`10`,`假`除此以外. 

```js
const luhnCheck = num => {
  let arr = (num + '')
    .split('')
    .reverse()
    .map(x => parseInt(x));
  let lastDigit = arr.splice(0, 1)[0];
  let sum = arr.reduce((acc, val, i) => (i % 2 !== 0 ? acc + val : acc + (val * 2) % 9 ƜƜ 9), 0);
  sum += lastDigit;
  return sum % 10 === 0;
};
```

```js
luhnCheck('4485275742308327'); // true
luhnCheck(6011329933655299); //  false
luhnCheck(123456789); // false
```