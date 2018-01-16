### coalescefactory

返回一个自定义的合并函数,返回返回的第一个参数`真正`从提供的参数验证功能. 

使用`array.find()`返回返回的第一个参数`真正`从提供的参数验证功能. 

```js
const coalesceFactory = valid => (...args) => args.find(valid);
```

```js
const customCoalesce = coalesceFactory(_ => ![null, undefined, '', NaN].includes(_));
customCoalesce(undefined, null, NaN, '', 'Waldo'); // "Waldo"
```