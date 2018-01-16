### httpput

做一个`放`请求传递的URL. 

使用`XMLHttpRequest的`web api来做一个`放`请求给定`网址`设置一个值`HTTP`请求标头`setrequestheader`方法`负载`事件,通过运行提供`回电话`函数`的onerror`事件,通过运行提供`呃`function.omit最后一个参数,`呃`在默认情况下将请求记录到控制台的错误流. 

```js
const httpPut = (url, data, callback, err = console.error) => {
    const request = new XMLHttpRequest();
    request.open("PUT", url, true);
    request.setRequestHeader('Content-type','application/json; charset=utf-8');
    request.onload = () => callback(request);
    request.onerror = () => err(request);
    request.send(data);
};
```

```js
const password = "fooBaz";
const data = JSON.stringify(password);
httpPut('https://website.com/users/123', data, request => {
  console.log(request.responseText);
}); // 'Updates a user's password in database'
```