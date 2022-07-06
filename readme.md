##JavaWebTest
    扩展：请你谈谈网站是如何进行访问的？
    答：输入一个域名；回车
    检查本机的C:\Windows\System32\drivers\etc\hosts配置文件下有没有这个域名映射；
    有：直接返回对应的ip地址，这个地址中，有我们需要访问的web程序，可以直接访问    
    127.0.0.1 www.qinjiang.com
    没有：去DNS服务器找，找到的话就返回，找不到就返回找不到；
    可以配置一下环境变量（可选性）
***
    扩展：一个完整的HTTP请求过程是如何的？
    连接：https://blog.csdn.net/u013777975/article/details/80496121?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522165698929916781683975172%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=165698929916781683975172&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_ecpm_v1~rank_v31_ecpm-5-80496121-null-null.142%5ev30%5econtrol,185%5ev2%5econtrol&utm_term=%E4%B8%80%E4%B8%AA%E5%AE%8C%E6%95%B4%E7%9A%84%E7%BD%91%E7%BB%9C%E8%AF%B7%E6%B1%82%E8%BF%87%E7%A8%8B&spm=1018.2226.3001.4187
***
    扩展：什么是HTTP/HTTPS协议？
    HTTP：
    超文本传输协议（HTTP，HyperText Transfer Protocol）是互联网上应用最为广泛的一种网络协议。设计 HTTP 最初的目的是为了提供一种发布和接收 
    HTML 页面的方法。它可以使浏览器更加高效。HTTP 协议是以明文方式发送信息的，如果黑客截取了 Web 浏览器和服务器之间的传输报文，就可以直接获得其
    中的信息。
    HTTP/1.0：客户端可以与web服务器连接后，只能获得一个web资源，断开连接
    HTTP/1.1：客户端可以与web服务器连接后，可以获得多个web资源。
    HTTP 原理：
    ①  客户端的浏览器首先要通过网络与服务器建立连接，该连接是通过 TCP 来完成的，一般 TCP 连接的端口号是80。 建立连接后，客户机发送一个请求给服务器，
    请求方式的格式为：统一资源标识符（URI）、协议版本号，后边是 MIME 信息包括请求修饰符、客户机信息和许可内容。
    ②  服务器接到请求后，给予相应的响应信息，其格式为一个状态行，包括信息的协议版本号、一个成功或错误的代码，后边是 MIME 信息包括服务器信息、
    实体信息和可能的内容。
    ____________________________________________________________________________________________________________________________
    HTTPS：
    是以安全为目标的 HTTP 通道，是 HTTP 的安全版。HTTPS 的安全基础是 SSL。SSL 协议位于 TCP/IP 协议与各种应用层协议之间，为数据通讯提供安全支持。
    SSL 协议可分为两层：SSL 记录协议（SSL Record Protocol），它建立在可靠的传输协议（如TCP）之上，为高层协议提供数据封装、压缩、加密等基本功能的支持。
    SSL 握手协议（SSL Handshake Protocol），它建立在 SSL 记录协议之上，用于在实际的数据传输开始前，通讯双方进行身份认证、协商加密算法、交换加密密钥等。
    HTTPS 设计目标：
    (1) 数据保密性
    (2) 数据完整性
    (3) 身份校验安全性
    Http和Https的区别：
    1、HTTPS  协议需要到 CA （Certificate Authority，证书颁发机构）申请证书，一般免费证书较少，因而需要一定费用。
    (以前的网易官网是http，而网易邮箱是 https 。)
    2、HTTP 是超文本传输协议，信息是明文传输，HTTPS 则是具有安全性的 SSL 加密传输协议。
    3、HTTP 和 HTTPS 使用的是完全不同的连接方式，用的端口也不一样，前者是80，后者是443。
    4、HTTP 的连接很简单，是无状态的。HTTPS 协议是由 SSL+HTTP 协议构建的可进行加密传输、身份认证的网络协议，比 HTTP 协议安全。
    (无状态的意思是其数据包的发送、传输和接收都是相互独立的。无连接的意思是指通信双方都不长久的维持对方的任何信息。)
***
    扩展：请求概念？
    1.请求行
    请求行中的请求方式：GET
    请求方式：Get,Post,HEAD,DELETE,PUT,TRACT.…
    get：请求能够携带的参数比较少，大小有限制，会在浏览器的URL地址栏显示数据内容，不安全，但高效
    post:请求能够携带的参数没有限制，大小没有限制，不会在浏览器的URL地址栏显示数据内容，安全，但不高效。
    2.消息头
    Accept：告诉浏览器，它所支持的数据类型
    Accept-Encoding：支持哪种编码格式  GBK   UTF-8   GB2312  ISO8859-1
    Accept-Language：告诉浏览器，它的语言环境
    Cache-Control：缓存控制
    Connection：告诉浏览器，请求完成是断开还是保持连接
    HOST：主机..../.
***
    扩展：响应概念？
    1.响应体
    Accept：告诉浏览器，它所支持的数据类型
    Accept-Encoding：支持哪种编码格式  GBK   UTF-8   GB2312  ISO8859-1
    Accept-Language：告诉浏览器，它的语言环境
    Cache-Control：缓存控制
    Connection：告诉浏览器，请求完成是断开还是保持连接
    HOST：主机..../.
    Refresh：告诉客户端，多久刷新一次；
    Location：让网页重新定位；
    2.响应状态码
    200：请求响应成功200
    3xx:请求重定向·重定向：你重新到我给你新位置去；
    4xx:找不到资源404·资源不存在；
    5xx:服务器代码错误 500 502:网关错误
***
    扩展：localStorage和sessionStorage和cookie的区别？
    参考资料：https://blog.csdn.net/weixin_42246997/article/details/102796076?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522165701006516781818749529%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=165701006516781818749529&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-102796076-null-null.142^v30^control,185^v2^control&utm_term=localstorage%E5%92%8Csessionstorage&spm=1018.2226.3001.4187
    1.首先localStorage和sessionStorage是HTML5新加入的特性，以键值对的形式存储。
    2.localStorage生命周期是永久，除非主动清除localStorage信息，否则这些信息将永远存在。存放数据大小为一般为5MB,
      而且它仅在客户端（即浏览器）中保存，不参与和服务器的通信。
    3.sessionStorage 属性允许你访问一个，对应当前源的 session Storage 对象。它与 localStorage 相似，不同之处在于 
      localStorage 里面存储的数据没有过期时间设置，而存储在 sessionStorage 里面的数据在页面会话结束时会被清除
    4. cookie是客户端与服务器端进行会话使用的一个能够在浏览器本地化存储的技术。简言之，cookie是服务器端发给客户端的文本文件；目的是用于辨别用户身份。







