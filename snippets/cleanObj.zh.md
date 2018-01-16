### cleanobj

删除除json对象指定的属性之外的任何属性. 

使用`object.keys()`方法来循环给定的json对象,并删除不包含在给定数组中的键. 如果您传递一个特殊的键,`childindicator`,它也将深入地将该功能应用于内部对象. 

```js
const cleanObj = (obj, keysToKeep = [], childIndicator) => {
  Object.keys(obj).forEach(key => {
    if (key === childIndicator) {
      cleanObj(obj[key], keysToKeep, childIndicator);
    } else if (!keysToKeep.includes(key)) {
      delete obj[key];
    }
  });
  return obj;
};
```

```js
const testObj = { a: 1, b: 2, children: { a: 1, b: 2 } };
cleanObj(testObj, ['a'], 'children'); // { a: 1, children : { a: 1}}
```