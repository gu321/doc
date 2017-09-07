# GU321.COM

## 新人导航

### 文档

1. 阅读 : [doc.gu321.org](https://doc.gu321.org)
1. 源码 : [github.com/gu321/doc](https://github.com/gu321/doc)
1. 撰写: [www.gitbook.com/book/gu321/gu321/edit](https://www.gitbook.com/book/gu321/gu321/edit)

### 代码

采用fork+pul request开发模式，参见

* [《如何在github上fork一个项目来贡献代码以及同步原作者的修改》](http://www.cnblogs.com/rubylouvre/archive/2013/01/24/2874694.html)。

#### 源码库

私有，请注册账号，告知管理员，申请只读权限。
普通开发者只有只读权限，代码改动请提交pull request。

网站 [git.oschina.net/gu321/tz](http://git.oschina.net/gu321/tz)

### 技术栈

#### 前端

* [jQuery](https://jquery.com/)
* [webpack](https://webpack.github.io/)
  * [入门Webpack，看这篇就够了](http://www.jianshu.com/p/42e11515c10f)
* [SCSS](http://sass-lang.com/)
  * [SASS用法指南](http://www.ruanyifeng.com/blog/2012/06/sass.html)
* [coffeescript](http://coffeescript.org/)
  * [coffeescript小书](https://read.douban.com/reader/ebook/198648/)
* [slm](https://github.com/slm-lang/slm)


#### 后端

* [python3](http://python.org/)
* [D语言](https://dlang.org/)     
  * [vibe.d](http://vibed.org/)
  
D语言用得较少，目前只用于自动补全的Trie树(并作为自动补全的webserver)。如遇到一些对性能要求高的场景，会考虑使用。
  
#### 数据库

* [PostgreSQL](https://www.postgresql.org/)
  * [PostgreSQL新手入门](http://www.ruanyifeng.com/blog/2013/12/getting_started_with_postgresql.html)
* [redis](https://redis.io/)      
  * [redis中文手册](http://redisdoc.com/)
* [pika](https://github.com/Qihoo360/pika/wiki)  

redis启动了2个实例，

其中cache实例被当为memcache用，设置了所有key按LRU轮换（不是持久的）。

另一个redis实例db，计划用于作为消息队列。

用户数据存储基本都是用的postgresql 。

pika是奇虎公司出品的兼容redis的硬盘数据库，目前主要是存储的一些爬虫抓过来的数据（就是如果丢了，重新爬一边就是了，无所谓）。

    
#### 运维
* [Caddy - The HTTP/2 Web Server with Automatic HTTPS](https://caddyserver.com/)
* Docker
  * [Docker 快速入门](http://z42.readthedocs.io/zh/latest/docker.html) 


#### 开发工具 \(仅供参考\)

* VIM 
  * [vim 快速入门](/h ttp://z42.readthedocs.io/zh/latest/devtools/vim.html)
  
#### 部署环境

参考基于腾讯云的一键不少脚本 cli/yun/init.sh
主机环境为centos7 ， 运行时环境基于docker

#TODO 补充完善如何个人部署，可以新开一个单独的文档。

#### 注意事项

代码库是GIT的，但是我是用HG-GIT。

HG是一个非常好用的代码控制工具（参见：[hg 简明教程](http://z42.readthedocs.io/zh/latest/devtools/hg.html) ），在通过hg alias设置命令别名后，操作GIT非常方便。

但是，毕竟HG不是主流的版本控制软件，GIT早有一统天下的趋势。

所以，大家可以自行选择，不强求统一。

但是请GIT的用户注意参考 .hgignore 设置 .gitignore 。

