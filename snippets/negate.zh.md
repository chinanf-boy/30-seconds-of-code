### 否定

否定谓词功能. 

采用谓词函数并应用非运算符(`!`)与它的论据. 

```js
const negate = func => (...args) => !func(...args);
```

```js
[1, 2, 3, 4, 5, 6].filter(negate(n => n % 2 == 0)); // [ 1, 3, 5 ]
```