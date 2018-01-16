### httpsredirect

将页面重定向到https,如果它现在在http中. 

另外,按下后退按钮不会将其取回到历史记录中的http页面中. `使用`location.protocol`获得当前正在使用的协议. `如果不是https,请使用`location.replace()`用https版本的页面替换现有的页面. `使用`location.href得到完整的地址,与之分开string.split()并删除url的协议部分. 

```js
const httpsRedirect = () => {
  if (location.protocol !== 'https:') location.replace('https://' + location.href.split('//')[1]);
};
```

```js
httpsRedirect(); // If you are on http://mydomain.com, you are redirected to https://mydomain.com
```