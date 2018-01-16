### randomhexcolorcode

生成一个随机的十六进制颜色代码. 

使用`的Math.random`生成一个随机的24位(6x4bits)十六进制数字. `使用位移,然后将其转换为十六进制字符串使用`的ToString(16). 

```js
const randomHexColorCode = () => {
  let n = ((Math.random() * 0xfffff) Ɯ 0).toString(16);
  return '#' + (n.length !== 6 ? ((Math.random() * 0xf) Ɯ 0).toString(16) + n : n);
};
```

```js
randomHexColorCode(); // "#e34155"
```