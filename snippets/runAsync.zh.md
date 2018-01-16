### runasync

在一个单独的线程中使用a运行一个函数[网络工作者](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers),允许长时间运行的功能不阻止用户界面. 

创建一个新的`工人`用一个`BLOB`对象url,其内容应该是所提供函数的字符串化版本. 立即发布调用函数的返回值. 返回一个promise,`的onMessage`和`的onerror`事件和解决从工作人员回来的数据,或抛出一个错误. 

```js
const runAsync = fn => {
  const blob = `var fn = ${fn.toString()}; postMessage(fn());`;
  const worker = new Worker(
    URL.createObjectURL(new Blob([blob]), {
      type: 'application/javascript; charset=utf-8'
    })
  );
  return new Promise((res, rej) => {
    worker.onmessage = ({ data }) => {
      res(data), worker.terminate();
    };
    worker.onerror = err => {
      rej(err), worker.terminate();
    };
  });
};
```

```js
const longRunningFunction = () => {
  let result = 0;
  for (let i = 0; i < 1000; i++) {
    for (let j = 0; j < 700; j++) {
      for (let k = 0; k < 300; k++) {
        result = result + i + j + k;
      }
    }
  }
  return result;
};
/*
  NOTE: Since the function is running in a different context, closures are not supported.
  The function supplied to `runAsync` gets stringified, so everything becomes literal.
  All variables and functions must be defined inside.
*/
runAsync(longRunningFunction).then(console.log); // 209685000000
runAsync(() => 10 ** 3).then(console.log); // 1000
let outsideVariable = 50;
runAsync(() => typeof outsideVariable).then(console.log); // 'undefined'
```