# GU321.COM

## 新人导航

### 文档

1. 阅读 : [doc.gu321.org](https://doc.gu321.org)
1. 源码 : [github.com/gu321/doc](https://github.com/gu321/doc)
1. 撰写: [www.gitbook.com/book/gu321/gu321/edit](https://www.gitbook.com/book/gu321/gu321/edit)

### 开发流程

采用fork+pull request开发模式，参见

* [《如何在github上fork一个项目来贡献代码以及同步原作者的修改》](http://www.cnblogs.com/rubylouvre/archive/2013/01/24/2874694.html)。


### 配置环境

#### WEB端


源码 [git.oschina.net/gu321/tz](http://git.oschina.net/gu321/tz)
配置文件 [git.oschina.net/gu321/tz_config](http://git.oschina.net/gu321/tz_config)

代码私有，请注册账号，告知管理员，申请只读权限。

普通开发者只有只读权限，代码改动请提交pull request。

所以，首先请fork源码，然后clone自己的源码。

源码目录关系如下


```
tz -> ~/tz 
tz_config -> ~/tz/cli/make/config/tz_config
```


clone 完毕后，请运行

```
~/tz/cli/make/config/tz_config/make.py

```


来生成初始化的配置文件 


```
~/tz/cli/make/config/tz_config/config.py

```

然后编辑配置config.py配置文件（可以考虑添加config.py到自己私人的代码库，防止丢失）

开发用的发信邮箱的配置参见teambition的文档[（文档链接）
](https://www.teambition.com/project/598a920df8ca884016a5a8bc/posts)

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

