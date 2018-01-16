### 等于

在两个值之间进行深入的比较以确定它们是否相等. 

检查两个值是否相同,如果两者都是`日期`同时使用的对象`date.gettime()`或者如果它们都是具有等价值的非对象值(严格比较).check是否只有一个值`空值`要么`未定义`或者如果他们的原型不同,如果以上条件都不符合,请使用`object.keys()`检查两个值是否具有相同的密钥数量,然后使用`array.every()`检查第一个值中的每个键是否存在于第二个键中,如果它们通过递归调用此方法是否相同. 

```js
const equals = (a, b) => {
  if (a === b) return true;
  if (a instanceof Date && b instanceof Date) return a.getTime() === b.getTime();
  if (!a ƜƜ !b ƜƜ (typeof a != 'object' && typeof b !== 'object')) return a === b;
  if (a === null ƜƜ a === undefined ƜƜ b === null ƜƜ b === undefined) return false;
  if (a.prototype !== b.prototype) return false;
  let keys = Object.keys(a);
  if (keys.length !== Object.keys(b).length) return false;
  return keys.every(k => equals(a[k], b[k]));
};
```

```js
equals({ a: [2, { e: 3 }], b: [4], c: 'foo' }, { a: [2, { e: 3 }], b: [4], c: 'foo' }); // true
```