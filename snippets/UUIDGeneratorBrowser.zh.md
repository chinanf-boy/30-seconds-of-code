### uuidgeneratorbrowser

在浏览器中生成一个uuid. 

使用`加密`API生成一个UUID,符合[rfc4122](https://www.ietf.org/rfc/rfc4122.txt)版本4. 

```js
const UUIDGeneratorBrowser = () =>
  ([1e7] + -1e3 + -4e3 + -8e3 + -1e11).replace(/[018]/g, c =>
    (c ^ (crypto.getRandomValues(new Uint8Array(1))[0] & (15 >> (c / 4)))).toString(16)
  );
```

```js
UUIDGeneratorBrowser(); // '7982fcfe-5721-4632-bede-6000885be57d'
```