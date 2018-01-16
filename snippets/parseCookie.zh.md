### parsecookie

解析一个http cookie头字符串并返回所有cookie名称 - 值对的对象. 

使用`string.split( ';')`将键值对彼此分开`array.map()`和`string.split( '=')`在每个pair中分隔键值`array.reduce()`和`decodeuricomponent()`用所有的键值对创建一个对象. 

```js
const parseCookie = str =>
  str
    .split(';')
    .map(v => v.split('='))
    .reduce((acc, v) => {
      acc[decodeURIComponent(v[0].trim())] = decodeURIComponent(v[1].trim());
      return acc;
    }, {});
```

```js
parseCookie('foo=bar; equation=E%3Dmc%5E2'); // { foo: 'bar', equation: 'E=mc^2' }
```