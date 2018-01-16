### httppost

做一个`岗位`请求传递的URL. 

使用[`XMLHttpRequest的`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/Using_XMLHttpRequest)web api来做一个`岗位`请求给定`网址`设置一个值`HTTP`请求标头`setrequestheader`方法`负载`事件,通过调用给定的`回电话`该`responseText的`处理`的onerror`事件,通过运行提供`呃`function.omit第三个参数,`数据`,不发送数据到提供的`网址`. 第四个观点,`呃`,将错误记录到控制台`错误`流默认情况下. 

```js
const httpPost = (url, callback, data = null, err = console.error) => {
  const request = new XMLHttpRequest();
  request.open('POST', url, true);
  request.setRequestHeader('Content-type', 'application/json; charset=utf-8');
  request.onload = () => callback(request.responseText);
  request.onerror = () => err(request);
  request.send(data);
};
```

```js
const newPost = {
  userId: 1,
  id: 1337,
  title: 'Foo',
  body: 'bar bar bar'
};
const data = JSON.stringify(newPost);
httpPost(
  'https://jsonplaceholder.typicode.com/posts',
  console.log,
  data
); /*
Logs: {
  "userId": 1,
  "id": 1337,
  "title": "Foo",
  "body": "bar bar bar"
}
*/
```