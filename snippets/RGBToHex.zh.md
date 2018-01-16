### rgbtohex

将rgb组件的值转换为颜色代码. 

使用按位左移运算符将给定的rgb参数转换为十六进制字符串(`<<`)和`的ToString(16)`, 然后`string.padstart(6, '0')`得到一个6位的十六进制值. 

```js
const RGBToHex = (r, g, b) => ((r << 16) + (g << 8) + b).toString(16).padStart(6, '0');
```

```js
RGBToHex(255, 165, 1); // 'ffa501'
```