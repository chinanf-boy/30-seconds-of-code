### uuidgeneratornode

在node.js中生成一个uuid

使用`加密`API生成一个UUID,符合[rfc4122](https://www.ietf.org/rfc/rfc4122.txt)版本4. 

```js
const crypto = require('crypto');
const UUIDGeneratorNode = () =>
  ([1e7] + -1e3 + -4e3 + -8e3 + -1e11).replace(/[018]/g, c =>
    (c ^ (crypto.randomBytes(1)[0] & (15 >> (c / 4)))).toString(16)
  );
```

```js
UUIDGeneratorNode(); // '79c7c136-60ee-40a2-beb2-856f1feabefc'
```