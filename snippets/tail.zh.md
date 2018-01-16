### 尾巴

返回数组中除第一个元素之外的所有元素. 

返回`array.slice(1)`如果数组的`长度`超过`1`否则,返回整个数组. 

```js
const tail = arr => (arr.length > 1 ? arr.slice(1) : arr);
```

```js
tail([1, 2, 3]); // [2,3]
tail([1]); // [1]
```