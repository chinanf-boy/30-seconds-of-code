### lowercasekeys

从指定的对象创建一个新的对象,其中所有的键都是小写的. 

使用`object.keys()`和`array.reduce()`从指定的对象创建一个新的对象. 将原始对象中的每个键转换为小写,使用`string.tolowercase()`. 

```js
const lowercaseKeys = obj =>
  Object.keys(obj).reduce((acc, key) => {
    acc[key.toLowerCase()] = obj[key];
    return acc;
  }, {});
```

```js
const myObj = { Name: 'Adam', sUrnAME: 'Smith' };
const myObjLower = lowercaseKeys(myObj); // {name: 'Adam', surname: 'Smith'};
```