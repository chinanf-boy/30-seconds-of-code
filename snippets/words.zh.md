### 话

将给定的字符串转换为单词数组. 

使用`string.split()`与提供的模式(默认为非alpha作为正则表达式)转换为字符串数组. `使用`array.filter()删除任何空的strings.omit第二个参数使用默认的正则表达式. 

```js
const words = (str, pattern = /[^a-zA-Z-]+/) => str.split(pattern).filter(Boolean);
```

```js
words('I love javaScript!!'); // ["I", "love", "javaScript"]
words('python, javaScript & coffee'); // ["python", "javaScript", "coffee"]
```