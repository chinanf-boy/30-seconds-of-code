### HTTPGET

做一个`得到`请求传递的URL. 

使用[`XMLHttpRequest的`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/Using_XMLHttpRequest)web api来做一个`得到`请求给定`网址`处理`负载`事件,通过调用给定的`回电话`该`responseText的`处理`的onerror`事件,通过运行提供`呃`function.omit第三个参数,`呃`,将错误记录到控制台`错误`流默认情况下. 

```js
const httpGet = (url, callback, err = console.error) => {
  const request = new XMLHttpRequest();
  request.open('GET', url, true);
  request.onload = () => callback(request.responseText);
  request.onerror = () => err(request);
  request.send();
};
```

```js
httpGet(
  'https://jsonplaceholder.typicode.com/posts/1',
  console.log
); /* 
Logs: {
  "userId": 1,
  "id": 1,
  "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
  "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
}
*/
```