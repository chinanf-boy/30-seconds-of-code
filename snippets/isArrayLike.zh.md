### isarraylike

检查提供的参数是否类似于数组(即可迭代). 

使用扩展运算符(`...`)来检查提供的参数是否可迭代`试着抓`块和逗号运算符(`,`)返回适当的值. 

```js
const isArrayLike = val => {
  try {
    return [...val], true;
  } catch (e) {
    return false;
  }
};
```

```js
isArrayLike(document.querySelectorAll('.className')); // true
isArrayLike('abc'); // true
isArrayLike(null); // false
```