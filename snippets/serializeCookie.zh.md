### serializecookie

将一个cookie名称 - 值对序列化为一个set-cookie头字符串. 

使用模板文字和`encodeURIComponent方法()`创建适当的字符串. 

```js
const serializeCookie = (name, val) => `${encodeURIComponent(name)}=${encodeURIComponent(val)}`;
```

```js
serializeCookie('foo', 'bar'); // 'foo=bar'
```