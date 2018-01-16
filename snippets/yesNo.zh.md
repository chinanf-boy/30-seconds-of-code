### YESNO

回报`真正`如果字符串是`ÿ`/`是`要么`假`如果字符串是`ñ`/`没有`. 

使用`regexp.test()`检查字符串是否评估为`Y /是的`要么`N /无`. 第二个参数,`高清`将默认答案设置为`没有`. 

```js
const yesNo = (val, def = false) =>
  /^(yƜyes)$/i.test(val) ? true : /^(nƜno)$/i.test(val) ? false : def;
```

```js
yesNo('Y'); // true
yesNo('yes'); // true
yesNo('No'); // false
yesNo('Foo', true); // true
```