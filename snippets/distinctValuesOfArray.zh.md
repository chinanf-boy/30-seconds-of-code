### distinctvaluesofarray

返回数组的所有不同值. 

使用es6`组`和`...休息`操作员放弃所有重复的值. 

```js
const distinctValuesOfArray = arr => [...new Set(arr)];
```

```js
distinctValuesOfArray([1, 2, 2, 3, 4, 4, 5]); // [1,2,3,4,5]
```