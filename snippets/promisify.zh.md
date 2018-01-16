### promisify

转换一个异步函数来返回一个promise. 

使用currying来返回一个函数`诺言`即调用原始函数`...休息`运算符传入所有参数. 

_在节点8+中,您可以使用[`util.promisify`](https://nodejs.org/api/util.html#util_util_promisify_original)_

```js
const promisify = func => (...args) =>
  new Promise((resolve, reject) =>
    func(...args, (err, result) => (err ? reject(err) : resolve(result)))
  );
```

```js
const delay = promisify((d, cb) => setTimeout(cb, d));
delay(2000).then(() => console.log('Hi!')); // // Promise resolves after 2s
```