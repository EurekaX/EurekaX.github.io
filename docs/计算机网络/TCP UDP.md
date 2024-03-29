---
title: TCP UDP
updated: 2022-10-11T06:24:02.0000000+08:00
created: 2022-10-11T06:23:24.0000000+08:00
---

1.  是否面向连接：UDP 在传送数据之前不需要先建立连接。而 TCP 提供面向连接的服务，在传送数据之前必须先建立连接，数据传送结束后要释放连接。
2.  是否是可靠传输：远地主机在收到 UDP 报文后，不需要给出任何确认，并且不保证数据不丢失，不保证是否顺序到达。TCP 提供可靠的传输服务，TCP 在传递数据之前，会有三次握手来建立连接，而且在数据传递时，有确认、窗口、重传、拥塞控制机制。通过 TCP 连接传输的数据，无差错、不丢失、不重复、并且按序到达。
3.  是否有状态：这个和上面的“是否可靠传输”相对应。TCP 传输是有状态的，这个有状态说的是 TCP 会去记录自己发送消息的状态比如消息是否发送了、是否被接收了等等。为此 ，TCP 需要维持复杂的连接状态表。而 UDP 是无状态服务，简单来说就是不管发出去之后的事情了（这很渣男！）。
4.  传输效率：由于使用 TCP 进行传输的时候多了连接、确认、重传等机制，所以 TCP 的传输效率要比 UDP 低很多。
5.  传输形式： TCP 是面向字节流的，UDP 是面向报文的。
6.  首部开销：TCP 首部开销（20 ～ 60 字节）比 UDP 首部开销（8 字节）要大。
7.  是否提供广播或多播服务：TCP 只支持点对点通信，UDP 支持一对一、一对多、多对一、多对多；
