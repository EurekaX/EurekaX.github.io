---
title: HTTP 和 HTTPS 有什么区别？
updated: 2022-10-11T06:55:07.0000000+08:00
created: 2022-10-11T06:54:42.0000000+08:00
---

-   端口号：HTTP 默认是 80，HTTPS 默认是 443。
-   URL 前缀：HTTP 的 URL 前缀是[http://，HTTPS](http://，HTTPS) 的 URL 前缀是https://。
-   安全性和资源消耗： HTTP 协议运行在 TCP 之上，所有传输的内容都是明文，客户端和服务器端都无法验证对方的身份。HTTPS 是运行在 SSL/TLS 之上的 HTTP 协议，SSL/TLS 运行在 TCP 之上。所有传输的内容都经过加密，加密采用对称加密，但对称加密的密钥用服务器方的证书进行了非对称加密。所以说，HTTP 安全性没有 HTTPS 高，但是 HTTPS 比 HTTP 耗费更多服务器资源。
