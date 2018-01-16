### hasflags

检查当前进程的参数是否包含指定的标志. 

使用`array.every()`和`array.includes()`检查是否`process.argv`包含所有指定的标志. 使用正则表达式来测试指定的标志是否带有前缀`-`要么`-`并相应地加上前缀. 

```js
const hasFlags = (...flags) =>
  flags.every(flag => process.argv.includes(/^-{1,2}/.test(flag) ? flag : '--' + flag));
```

```js
// node myScript.js -s --test --cool=true
hasFlags('-s'); // true
hasFlags('--test', 'cool=true', '-s'); // true
hasFlags('special'); // false
```