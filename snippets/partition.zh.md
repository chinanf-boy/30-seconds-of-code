### 划分

根据所提供的函数对每个元素的真实性将元素分成两个数组. 

使用`array.reduce()`创建一个两个array.use的数组`的Array.push()`为其添加元素`FN`回报`真正`到第一个数组和元素`FN`回报`假`到第二个. 

```js
const partition = (arr, fn) =>
  arr.reduce(
    (acc, val, i, arr) => {
      acc[fn(val, i, arr) ? 0 : 1].push(val);
      return acc;
    },
    [[], []]
  );
```

```js
const users = [{ user: 'barney', age: 36, active: false }, { user: 'fred', age: 40, active: true }];
partition(users, o => o.active); // [[{ 'user': 'fred',    'age': 40, 'active': true }],[{ 'user': 'barney',  'age': 36, 'active': false }]]
```