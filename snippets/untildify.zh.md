### untildify

将波浪号路径转换为绝对路径. 

使用`与string.replace()`用正则表达式和`os.homedir()`取代`〜`在主目录的路径的开始. 

```js
const untildify = str => str.replace(/^~($Ɯ\/Ɯ\\)/, `${require('os').homedir()}$1`);
```

```js
untildify('~/node'); // '/Users/aUser/node'
```