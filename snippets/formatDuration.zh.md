### formatduration

返回给定毫秒数的可读格式. 

划分`女士`用适当的值来获得适当的值`天`,`小时`,`分钟`,`第二`和`毫秒`. 使用`object.entries()`同`array.filter()`只保留非零值`array.map()`为每个值创建字符串,适当地复数化`string.join(',')`将这些值组合成一个字符串. 

```js
const formatDuration = ms => {
  if (ms < 0) ms = -ms;
  const time = {
    day: Math.floor(ms / 86400000),
    hour: Math.floor(ms / 3600000) % 24,
    minute: Math.floor(ms / 60000) % 60,
    second: Math.floor(ms / 1000) % 60,
    millisecond: Math.floor(ms) % 1000
  };
  return Object.entries(time)
    .filter(val => val[1] !== 0)
    .map(val => val[1] + ' ' + (val[1] !== 1 ? val[0] + 's' : val[0]))
    .join(', ');
};
```

```js
formatDuration(1001); // '1 second, 1 millisecond'
formatDuration(34325055574); // '397 days, 6 hours, 44 minutes, 15 seconds, 574 milliseconds'
```