### initializearraywithvalues

用指定的值初始化和填充数组. 

使用`阵列(n)的`创建所需长度的数组,`填写(五)`以期望的价值填补它,你可以省略`VAL`使用默认值`0`. 

```js
const initializeArrayWithValues = (n, val = 0) => Array(n).fill(val);
```

```js
initializeArrayWithValues(5, 2); // [2,2,2,2,2]
```