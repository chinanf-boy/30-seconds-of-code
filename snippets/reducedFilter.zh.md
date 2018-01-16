### reducedfilter

过滤基于条件的对象数组,同时也过滤未指定的键. 

使用`array.filter()`根据谓词过滤数组`FN`以便它返回条件返回真值的对象. `在过滤的数组上,使用`array.map()`使用返回新的对象`array.reduce()`过滤掉没有提供的键`按键论据. 

```js
const reducedFilter = (data, keys, fn) =>
  data.filter(fn).map(el =>
    keys.reduce((acc, key) => {
      acc[key] = el[key];
      return acc;
    }, {})
  );
```

```js
const data = [
  {
    id: 1,
    name: 'john',
    age: 24
  },
  {
    id: 2,
    name: 'mike',
    age: 50
  }
];

reducedFilter(data, ['id', 'name'], item => item.age > 24); // [{ id: 2, name: 'mike'}]
```