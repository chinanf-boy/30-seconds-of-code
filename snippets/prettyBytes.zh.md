### prettybytes

将字节数转换为可读的字符串. 

使用基于exponent.use访问单元的数组字典`number.toprecision()`将数字截断为一定数量的数字. 通过建立起来,返回经过验证的字符串,并考虑提供的选项以及是否为负数. 第二个参数,`精确`,要使用默认精度`3`digits.omit第三个参数,`addspace`,在数字和单位之间默认添加空格. 

```js
const prettyBytes = (num, precision = 3, addSpace = true) => {
  const UNITS = ['B', 'KB', 'MB', 'GB', 'TB', 'PB', 'EB', 'ZB', 'YB'];
  if (Math.abs(num) < 1) return num + (addSpace ? ' ' : '') + UNITS[0];
  const exponent = Math.min(Math.floor(Math.log10(num < 0 ? -num : num) / 3), UNITS.length - 1);
  const n = Number(((num < 0 ? -num : num) / 1000 ** exponent).toPrecision(precision));
  return (num < 0 ? '-' : '') + n + (addSpace ? ' ' : '') + UNITS[exponent];
};
```

```js
prettyBytes(1000); // "1 KB"
prettyBytes(-27145424323.5821, 5); // "-27.145 GB"
prettyBytes(123456789, 3, false); // "123MB"
```