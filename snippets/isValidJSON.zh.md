### isvalidjson

检查提供的参数是否是有效的json. 

使用`JSON.parse()来`和a`试着抓`块来检查提供的参数是否是有效的json. 

```js
const isValidJSON = obj => {
  try {
    JSON.parse(obj);
    return true;
  } catch (e) {
    return false;
  }
};
```

```js
isValidJSON('{"name":"Adam","age":20}'); // true
isValidJSON('{"name":"Adam",age:"20"}'); // false
isValidJSON(null); // true
```