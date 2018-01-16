### 面具

取代所有,但最后`NUM`与指定的掩码字符的字符. 

使用`string.slice()`抓住需要被屏蔽和使用的字符部分`与string.replace()`用正则表达式来替换每个字符的掩码character.concatenate掩盖的字符与剩余的unmasked部分的string.omit第二个参数,`NUM`,保持默认`4`字符unmasked. `如果`NUM`是否定的,未被屏蔽的字符将在字符串的开头. 第三个参数,`面具`,使用默认的字符`'\*'为面具. 

```js
const mask = (cc, num = 4, mask = '*') =>
  ('' + cc).slice(0, -num).replace(/./g, mask) + ('' + cc).slice(-num);
```

```js
mask(1234567890); // '******7890'
mask(1234567890, 3); // '*******890'
mask(1234567890, -4, '$'); // '$$$$567890'
```