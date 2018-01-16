### createeventhub

创建一个pub / sub([发布 - 订阅](https://en.wikipedia.org/wiki/Publish%E2%80%93subscribe_pattern))事件中心与`发射`,`上`,和`离`方法. 

使用`的Object.create(空)`创造一个空洞`枢纽`不从属性继承的对象`Object.prototype中`. 对于`发射`,根据. 解析处理程序的数组`事件`参数,然后运行每一个`array.foreach()`通过传递数据作为参数`上`,为事件创建一个数组,如果它还不存在,则使用`的Array.push()`添加array.for的句柄`离`, 使用`array.findindex()`找到事件数组中的处理程序的索引并使用它将其删除`方法Array.splice()`. 

```js
const createEventHub = () => ({
  hub: Object.create(null),
  emit(event, data) {
    (this.hub[event] ƜƜ []).forEach(handler => handler(data));
  },
  on(event, handler) {
    if (!this.hub[event]) this.hub[event] = [];
    this.hub[event].push(handler);
  },
  off(event, handler) {
    const i = (this.hub[event] ƜƜ []).findIndex(h => h === handler);
    if (i > -1) this.hub[event].splice(i, 1);
  }
});
```

```js
const handler = data => console.log(data);
const hub = createEventHub();
let increment = 0;

// Subscribe: listen for different types of events
hub.on('message', handler);
hub.on('message', () => console.log('Message event fired'));
hub.on('increment', () => increment++);

// Publish: emit events to invoke all handlers subscribed to them, passing the data to them as an argument
hub.emit('message', 'hello world'); // logs 'hello world' and 'Message event fired'
hub.emit('message', { hello: 'world' }); // logs the object and 'Message event fired'
hub.emit('increment'); // `increment` variable is now 1

// Unsubscribe: stop a specific handler from listening to the 'message' event
hub.off('message', handler);
```