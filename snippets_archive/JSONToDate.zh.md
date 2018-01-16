### jsontodate

将json对象转换为日期. 

使用`日期()`,将json格式的日期转换为可读的格式(`日/月/年`). 

```js
const JSONToDate = arr => {
  const dt = new Date(parseInt(arr.toString().substr(6)));
  return `${dt.getDate()}/${dt.getMonth() + 1}/${dt.getFullYear()}`;
};
```

```js
JSONToDate(/Date(1489525200000)/); // "14/3/2017"
```