### truthcheckcollection

检查谓词(第二个参数)是否对集合的所有元素(第一个参数)是真实的. 

使用`array.every()`检查每个通过的对象是否有指定的属性,如果它返回一个真值. 

```js
const truthCheckCollection = (collection, pre) => collection.every(obj => obj[pre]);
```

```js
truthCheckCollection([{ user: 'Tinky-Winky', sex: 'male' }, { user: 'Dipsy', sex: 'male' }], 'sex'); // true
```