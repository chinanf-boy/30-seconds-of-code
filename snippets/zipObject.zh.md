### zipobject

给定一个有效的属性标识符和一个数组值的数组,返回一个将属性关联到值的对象. 

因为一个对象可以有未定义的值,但是没有未定义的属性指针,所以这个属性数组用来决定使用结果对象的结构`array.reduce()`. 

```js
const zipObject = (props, values) =>
  props.reduce((obj, prop, index) => ((obj[prop] = values[index]), obj), {});
```

```js
zipObject(['a', 'b', 'c'], [1, 2]); // {a: 1, b: 2, c: undefined}
zipObject(['a', 'b'], [1, 2, 3]); // {a: 1, b: 2}
```