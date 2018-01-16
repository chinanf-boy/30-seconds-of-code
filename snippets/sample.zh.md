### 样品

从数组中返回一个随机元素. 

使用`的Math.random()`生成一个随机数,乘以`长度`并使用它将其四舍五入到最接近的整数`math.floor()`这个方法也适用于字符串. 

```js
const sample = arr => arr[Math.floor(Math.random() * arr.length)];
```

```js
sample([3, 7, 9, 11]); // 9
```