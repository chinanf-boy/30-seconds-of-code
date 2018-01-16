### isprime

检查提供的整数是否是素数. 

检查数字`2`给定数字的平方根`假`如果他们中的任何一个除以给定的数字,否则返回`真正`,除非数字少于`2`. 

```js
const isPrime = num => {
  const boundary = Math.floor(Math.sqrt(num));
  for (var i = 2; i <= boundary; i++) if (num % i == 0) return false;
  return num >= 2;
};
```

```js
isPrime(11); // true
```