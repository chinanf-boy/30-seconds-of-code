### 去掉

从给定函数返回的数组中移除元素`假`. 

使用`array.filter()`找到返回真值的数组元素`array.reduce()`使用删除元素`方法Array.splice()`.the`FUNC`被调用三个参数(`值,索引,数组`). 

```js
const remove = (arr, func) =>
  Array.isArray(arr)
    ? arr.filter(func).reduce((acc, val) => {
        arr.splice(arr.indexOf(val), 1);
        return acc.concat(val);
      }, [])
    : [];
```

```js
remove([1, 2, 3, 4], n => n % 2 == 0); // [2, 4]
```