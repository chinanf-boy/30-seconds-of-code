### readfilelines

返回指定文件的一行数组. 

使用`readfilesync`功能`FS`节点包创建一个`缓冲`从一个file.convert缓冲区到字符串使用`的toString(编码)`函数. 从文件的内容创建一个数组`分裂`一行一行的文件内容(每个`\ n`). 

```js
const fs = require('fs');
const readFileLines = filename =>
  fs
    .readFileSync(filename)
    .toString('UTF8')
    .split('\n');
```

```js
/*
contents of test.txt :
  line1
  line2
  line3
  ___________________________
*/
let arr = readFileLines('test.txt');
console.log(arr); // ['line1', 'line2', 'line3']
```