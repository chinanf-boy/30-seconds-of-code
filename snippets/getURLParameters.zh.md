### geturlparameters

返回一个包含当前url参数的对象. 

使用`string.match()`用适当的正则表达式来获得所有的键值对,`array.reduce()`将它们映射并组合成单个对象`location.search`作为适用于当前的理由`网址`. 

```js
const getURLParameters = url =>
  url
    .match(/([^?=&]+)(=([^&]*))/g)
    .reduce((a, v) => ((a[v.slice(0, v.indexOf('='))] = v.slice(v.indexOf('=') + 1)), a), {});
```

```js
getURLParameters('http://url.com/page?name=Adam&surname=Smith'); // {name: 'Adam', surname: 'Smith'}
```