1、定义 什么是WebSocket

```javascript
WebSocket是一个持久化的网络通信协议，可以在单个TCP连接上进行全双工通讯,没有Request（请求）和 response（响应）的概念，两者地位完全平等，连接一旦建立，客户端和服务端之间可以进行双向数据传输
```

2、HTTP

```
Http是一个非持久的协议，客户端想知道服务端的处理进度只能通过不停地使用ajax进行轮询或者采用long poll的方式来，但是前者对服务器压力大，后者则会因为一直等待response造成阻塞

Http1.1默认开启了keep-alive长连接保持了这个TCP通道使得在一个Http连接中，可以发送多个request，接收多个response，而且这个response也是被动的，不能主动发起

websocket虽然是独立于HTTP的一种协议，但是websocket必须依赖 HTTP 协议进行一次握手(在握手阶段是一样的)，握手成功后，数据就直接从 TCP通道传输，与 HTTP 无关了，可以理解为两者有交集，但是并不是全部。

socket也被称为套接字，与HTTP和WebSocket不一样，socket不是协议，它是在程序层面上对传输层协议（TCP/IP）的接口封装，一个能够提供端对端的通信的调用接口（API）

```

![image-20201014112005428](C:\Users\25771\AppData\Roaming\Typora\typora-user-images\image-20201014112005428.png)