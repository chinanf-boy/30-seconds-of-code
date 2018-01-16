### 选择

从一个对象中检索给定选择器指定的一组属性. 

使用`array.map()`对于每个选择器,`string.split( '')`分裂每个选择器和`array.reduce()`得到它所表示的价值. 

```js
const select = (from, ...selectors) =>
  [...selectors].map(s => s.split('.').reduce((prev, cur) => prev && prev[cur], from));
```

```js
const obj = { selector: { to: { val: 'val to select' } } };
select(obj, 'selector.to.val'); // ['val to select']
select(obj, 'selector.to.val', 'selector.to'); // ['val to select', { val: 'val to select' }]
```