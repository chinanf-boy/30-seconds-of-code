### bytesize

以字节为单位返回字符串的长度. 

将给定的字符串转换为[`BLOB`目的](https://developer.mozilla.org/en-US/docs/Web/API/Blob)并找到它`尺寸`. 

```js
const byteSize = str => new Blob([str]).size;
```

```js
byteSize('😀'); // 4
byteSize('Hello World'); // 11
```