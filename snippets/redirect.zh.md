### 重定向

重定向到指定的网址. 

使用`window.location.href`要么`window.location.replace()`重定向到`网址`. 传递第二个参数来模拟链接点击(`真正`- 默认)或http重定向`假`). 

```js
const redirect = (url, asLink = true) =>
  asLink ? (window.location.href = url) : window.location.replace(url);
```

```js
redirect('https://google.com');
```