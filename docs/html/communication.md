在浏览器中，多个标签页之间的通信是很有限的，主要有以下几种方式：

1. 使用 Cookie：可以通过 cookie 在不同标签页之间进行信息的传递。

```
// 写入cookie
document.cookie = "name=ChatAi";

// 在另一个标签页读取
var cookieValue = document.cookie.replace(/(?:(?:^|.*;\s*)name\s*\=\s*([^;]*).*$)|^.*$/, "$1");
```

2. 使用 localStorage：可以使用 localStorage 在不同标签页之间进行信息的共享。

```
// 在一个标签页写入数据到localStorage中
localStorage.setItem('name', 'ChatAi');

// 在另一个标签页读取数据
var name = localStorage.getItem('name');
```

3. 使用 BroadcastChannel API：该 API 提供了一种发布/订阅的机制，可以允许多个标签页之间进行实时通信。

```
// 创建一个新的BroadcastChannel
const myChannel = new BroadcastChannel('my_channel');

// 在一个标签页发送消息
myChannel.postMessage('Hello from ChatAi!');

// 在另一个标签页接受消息
myChannel.onmessage = function(event) {
  console.log('Received a message from ChatAi:', event.data);
};
```

需要注意的是，BroadcastChannel API 不是所有浏览器都支持的。
