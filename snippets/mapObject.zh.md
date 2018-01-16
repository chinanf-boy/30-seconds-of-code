### MapObject的

使用函数将数组的值映射到对象,其中键 - 值对由原始值作为键和映射值组成. 

使用匿名内部函数作用域来声明未定义的内存空间,使用闭包来存储返回值. `使用新的`排列将函数的映射存储在数据集上,使用逗号运算符返回第二个步骤,而不需要从一个上下文移动到另一个上下文(由于关闭和操作顺序). 

```js
const mapObject = (arr, fn) =>
  (a => (
    (a = [arr, arr.map(fn)]), a[0].reduce((acc, val, ind) => ((acc[val] = a[1][ind]), acc), {})
  ))();
```

```js
const squareIt = arr => mapObject(arr, a => a * a);
squareIt([1, 2, 3]); // { 1: 1, 2: 4, 3: 9 }
```