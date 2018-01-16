### 合并

返回第一个非空/未定义的参数. 

使用`array.find()`返回第一个非`空值`/`未定义`论据. 

```js
const coalesce = (...args) => args.find(_ => ![undefined, null].includes(_));
```

```js
coalesce(null, undefined, '', NaN, 'Waldo'); // ""
```