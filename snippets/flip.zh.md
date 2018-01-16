### 翻动

flip将函数作为参数,然后将第一个参数作为最后一个参数. 

返回一个包含可变参数的闭包,然后拼接最后一个参数,使其成为第一个参数,然后应用其余参数. 

```js
const flip = fn => (...args) => fn(args.pop(), ...args);
```

```js
let a = { name: 'John Smith' };
let b = {};
const mergeFrom = flip(Object.assign);
let mergePerson = mergeFrom.bind(null, a);
mergePerson(b); // == b
b = {};
Object.assign(b, a); // == b
```