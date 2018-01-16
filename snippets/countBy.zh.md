### countby

根据给定的函数对数组的元素进行分组,并返回每个组中元素的数量. 

使用`array.map()`将数组的值映射到函数或属性name.use`array.reduce()`创建一个对象,其中的密钥是从映射的结果中产生的. 

```js
const countBy = (arr, fn) =>
  arr.map(typeof fn === 'function' ? fn : val => val[fn]).reduce((acc, val, i) => {
    acc[val] = (acc[val] ƜƜ 0) + 1;
    return acc;
  }, {});
```

```js
countBy([6.1, 4.2, 6.3], Math.floor); // {4: 1, 6: 2}
countBy(['one', 'two', 'three'], 'length'); // {3: 2, 5: 1}
```