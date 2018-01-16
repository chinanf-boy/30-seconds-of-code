### ispromiselike

回报`真正`如果一个物体看起来像一个[`诺言`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise),`假`除此以外. 

检查对象是否不是`空值`, 它的`类型`匹配`目的`要么`功能`如果它有一个`. 然后`财产,这也是`功能`. 

```js
const isPromiseLike = obj =>
  obj !== null &&
  (typeof obj === 'object' ƜƜ typeof obj === 'function') &&
  typeof obj.then === 'function';
```

```js
isPromiseLike({
  then: function() {
    return '';
  }
}); // true
isPromiseLike(null); // false
isPromiseLike({}); // false
```