# 技术栈

## 前端

* [jQuery](https://jquery.com/)
* [webpack](https://webpack.github.io/)
    * [入门Webpack，看这篇就够了](http://www.jianshu.com/p/42e11515c10f)
* [SCSS](http://sass-lang.com/)
    * [SASS用法指南](http://www.ruanyifeng.com/blog/2012/06/sass.html)
* [coffeescript](http://coffeescript.org/)
    * [coffeescript小书](https://read.douban.com/reader/ebook/198648/)
* [slm](https://github.com/slm-lang/slm)
* [websocket](http://www.ruanyifeng.com/blog/2017/05/websocket.html)

## API

* [hapi.js](https://hapijs.com/)
    * [hapi.js在国内用的不多,我来稍微安利一下]( http://t.cn/RpLef0w)
* [websockets/ws](https://github.com/websockets/ws)

## 后端

* [python3](http://python.org/)
* [D语言](https://dlang.org/)
    
    * [vibe.d](http://vibed.org/)

    D语言用得较少，目前只用于自动补全的Trie树(并作为自动补全的webserver)。如遇到一些对性能要求高的场景，会考虑使用。

## 数据库

* [PostgreSQL](https://www.postgresql.org/)
    * [PostgreSQL新手入门](http://www.ruanyifeng.com/blog/2013/12/getting_started_with_postgresql.html)
* [redis](https://redis.io/)
    * [redis中文手册](http://redisdoc.com/)
* [pika](https://github.com/Qihoo360/pika/wiki)

redis启动了2个实例，

其中cache实例被当为memcache用，设置了所有key按LRU轮换（不是持久的）。

另一个redis实例db，计划用于实时消息队列（如聊天、股票行情）。

用户数据存储基本都是用的postgresql 。

pika是奇虎公司出品的兼容redis的硬盘数据库，目前主要是存储的一些爬虫抓过来的数据（就是如果丢了，重新爬一边就是了，无所谓）。

#### 运维
* [Caddy - 自动配置https的服务器](https://caddyserver.com/)
* Docker
    * [Docker 快速入门](http://z42.readthedocs.io/zh/latest/docker.html)
* [supervisor - 进程守护](http://t.cn/RGmuP0g)


#### 开发工具 \(仅供参考\)

* VIM
    * [vim 快速入门](http://z42.readthedocs.io/zh/latest/devtools/vim.html)