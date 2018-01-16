### shallowclone

创建一个对象的浅层克隆. 

使用`object.assign()`和一个空的对象(`{}`)创建原始的浅层克隆. 

```js
const shallowClone = obj => Object.assign({}, obj);
```

```js
const a = { x: true, y: 1 };
const b = shallowClone(a); // a !== b
```