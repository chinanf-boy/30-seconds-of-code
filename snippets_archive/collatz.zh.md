### 在Collat​​z

应用collat​​z算法. 

如果`ñ`甚至是回报`n / 2个`. `否则,返回`3N + 1. 

```js
const collatz = n => (n % 2 == 0 ? n / 2 : 3 * n + 1);
```

```js
collatz(8); // 4
```