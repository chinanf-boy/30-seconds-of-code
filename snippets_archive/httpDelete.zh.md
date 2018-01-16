### httpdelete

做一个`删除`请求传递的URL. 

使用`XMLHttpRequest的`web api来做一个`删除`请求给定`网址`处理`负载`事件,通过运行提供`回电话`函数`的onerror`事件,通过运行提供`呃`function.omit第三个参数,`呃`在默认情况下将请求记录到控制台的错误流. 

```js
const httpDelete = (url, callback, err = console.error) => {
  const request = new XMLHttpRequest();
  request.open("DELETE", url, true);
  request.onload = () => callback(request);
  request.onerror = () => err(request);
  request.send();
};
```

```js
httpDelete('https://website.com/users/123', request => {
  console.log(request.responseText);
}); // 'Deletes a user from the database'
```