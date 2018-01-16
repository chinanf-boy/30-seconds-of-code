### 功能

从一个对象的自身(和可选继承的)枚举属性返回一个函数属性名称的数组. 

使用`object.keys(OBJ)`迭代对象自己的属性`遗传`是`真正`, 使用`object.get.prototypeof(OBJ)`也得到对象的继承properties.use`array.filter()`只保留那些属性是functions.omit第二个参数,`遗传`,默认情况下不包括继承的属性. 

```js
const functions = (obj, inherited = false) =>
  (inherited
    ? [...Object.keys(obj), ...Object.keys(Object.getPrototypeOf(obj))]
    : Object.keys(obj)
  ).filter(key => typeof obj[key] === 'function');
```

```js
function Foo() {
  this.a = () => 1;
  this.b = () => 2;
}
Foo.prototype.c = () => 3;
functions(new Foo()); // ['a', 'b']
functions(new Foo(), true); // ['a', 'b', 'c']
```