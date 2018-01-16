### jsontofile

写一个json对象到一个文件. 

使用`fs.writefile()`,模板文字和`json.stringify()`写一个`JSON`反对`以.json`文件. 

```js
const fs = require('fs');
const JSONToFile = (obj, filename) =>
  fs.writeFile(`${filename}.json`, JSON.stringify(obj, null, 2));
```

```js
JSONToFile({ test: 'is passed' }, 'testJsonFile'); // writes the object to 'testJsonFile.json'
```