### 睡觉

延迟异步函数的执行. 

延迟执行的一部分`异步`功能,通过把它睡觉,返回一个`诺言`. 

```js
const sleep = ms => new Promise(resolve => setTimeout(resolve, ms));
```

```js
async function sleepyWork() {
  console.log("I'm going to sleep for 1 second.");
  await sleep(1000);
  console.log('I woke up after 1 second.');
}
```