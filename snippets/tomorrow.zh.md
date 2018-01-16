### 明天

导致明天的date.use的字符串表示`新日期()`拿到今天的日子`86400000`秒(24小时),使用`date.toisostring()`将日期对象转换为字符串. 

```js
const tomorrow = () => new Date(new Date().getTime() + 86400000).toISOString().split('T')[0];
```

```js
tomorrow(); // 2017-12-27 (if current date is 2017-12-26)
```