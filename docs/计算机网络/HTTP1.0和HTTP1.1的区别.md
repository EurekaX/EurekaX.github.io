---
title: HTTP/1.0和HTTP/1.1的区别
updated: 2022-10-12T15:44:02.0000000+08:00
created: 2022-10-12T15:31:50.0000000+08:00
---

HTTP/1.0和HTTP/1.1的区别：
（1）缓存处理：在HTTP1.0中主要使用header里的If-Modified-Since，Expires来做为缓存判断的标准，HTTP1.1则引入了更多的缓存控制策略，例如Entity tag，If-Unmodified-Since，If-Match，If-None-Match等更多可供选择的缓存头来控制缓存策略
（2）带宽优化及网络连接的使用：HTTP1.0中，存在一些浪费带宽的现象，例如：客户端只是需要某个对象的一部分，而服务器却将整个对象送过来了，并且不支持断点续传功能，HTTP1.1则在请求头引入了range头域，它允许只请求资源的某个部分，即返回码是206（Partial Content），方便了开发者自由的选择以便于充分利用带宽和连接
（3）错误通知的管理：在HTTP1.1中新增24个状态响应码，如409（Conflict）表示请求的资源与资源当前状态冲突；410（Gone）表示服务器上的某个资源被永久性的删除
（4）Host 头处理：在HTTP1.0中认为每台服务器都绑定一个唯一的IP地址，因此，请求消息中的URL并没有传递主机名（hostname）。但随着虚拟主机技术的发展，在一台物理服务器上可以存在多个虚拟主机（Multi-homed Web Servers），并且它们共享一个IP地址。HTTP1.1的请求消息和响应消息都应支持Host头域，且请求消息中如果没有Host头域会报告一个错误（400 Bad Request）
（5）长连接：HTTP 1.1支持持久连接（PersistentConnection）和请求的流水线（Pipelining）处理，在一个TCP连接上可以传送多个HTTP请求和响应，减少了建立和关闭连接的消耗和延迟，在HTTP1.1中默认开启Connection： keep-alive，弥补了HTTP1.0每次请求都要创建连接的缺点
