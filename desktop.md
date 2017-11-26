# P2P文件夹分享

## 项目需求、设计 - 一期


IP hash保存起点 hash保存终点
IP 



实现无中心服务器的P2P的文件夹分享。

分享的key
   目录清单
       每个文件切片的hash列表

文件hash的索引服务器（每个人保存以 xxxx 一部分以开头的hash，直到用完了自己的索引空间）
   
   我有哪些hash
   我知道别人有哪些hash
   
可以绑定自己的云服务器，进行镜像



https://www.paysapi.com/
这个可以用于绑定个人收款账户

1. 本机监听端口 IP % 1000 + 30000 
2. 连接之前访问过的服务器，看看是不是还活着
3. 查询拥有请求hash资源的服务器
4. 用户可以绑定一个自己的七牛云服务器做镜像
5. 文件使用自己的hash做一次xor加密，并切片为8M（[https://gist.github.com/revolunet/2412240](/revolunet/xor.py)）
6. 




## 资料

### P2P协议

* [磁力链接是如何实现下载的？](http://www.aneasystone.com/archives/2015/05/how-does-magnet-link-work.html)

* [IPFS：替代HTTP的分布式网络协议](http://www.infoq.com/cn/articles/ipfs)

* [zeronet:开放，自由，去中心化的网络](https://zeronet.io)


### 桌面端开发 


* [Electron 深度实践总结](https://changkun.us/archives/2017/03/217/)

* [一口气完成electron的入门学习](https://segmentfault.com/a/1190000006207600)

* [使用 Electron 将应用程序放入托盘](https://segmentfault.com/a/1190000008530265)

* [Electron API 演示(中文版)](https://github.com/demopark/electron-api-demos-Zh_CN)


* [用 Electron 打造 Win/Mac 应用，从「代码」到可下载的「安装包」，可能比你想得麻烦一点](https://segmentfault.com/a/1190000011908324)




