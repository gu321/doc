# 配置环境 - WEB


* 源码 [git.oschina.net/gu321/tz](http://git.oschina.net/gu321/tz)
* 配置文件 [git.oschina.net/gu321/tz_config](http://git.oschina.net/gu321/tz_config)

代码私有，请注册账号，告知管理员，申请只读权限。

普通开发者只有只读权限，代码改动请提交pull request。



## 部署线上服务器

数据库和caddy都运行在主机上，应用进程运行在容器内。

线上完整环境配置请参考基于腾讯云的一键部署脚本 

[cli/yun/init.sh](http://git.oschina.net/gu321/tz/blob/master/cli/yun/init.sh)

主机环境为centos7 ， 运行时环境基于docker ubuntu

本机可以创建一个类似如下的脚本方便直接登录远程的docker


ssh_docker.sh

```
SH="ssh -t -l root gu321"
exec $SH docker exec -it gu321 timeout 24h bash -c "su\ -\ ol"
```

其中，每次连接貌似都是创建一个bash进程（退出的时候也不会消失），加上timeout是为了防止bash进程越来越多。


## 部署个人开发环境

首先需要启动数据库和caddy

#TODO@碧海潮生 : 参考线上部署脚本 http://git.oschina.net/gu321/tz/blob/master/cli/yun/init_centos.sh  ，补充完善如何进行个人开发环境的部署

因为线上环境的postgresql是用的腾讯云的数据库，所以，开发环境需要自己启动一个postgresql 。

参考 [cli/yun/psql/init.sh](http://git.oschina.net/gu321/tz/blob/master/cli/yun/psql/init.sh) 脚本，初始化postgresql数据库。

然后 [daocloud.io](https://dashboard.daocloud.io/orgs/vcwatch/build-flows/bba47cb4-13d4-4720-8790-f9926aa7eeb9)上有构建好的容器，申请访问权限后，参考线上环境部署脚本pull启动即可。

接着，生成配置文件

**首先请fork源码，然后clone自己的源码**。

源码库-文件目录的对应关系如下

```
tz -> ~/tz
tz_config -> ~/tz/cli/make/config/tz_config
```


clone 后，请运行

```
~/tz/cli/make/config/tz_config/make.py

```


来生成初始化的配置文件


```
~/tz/cli/make/config/tz_config/config.py

```


编辑配置config.py配置文件。

其中CDN可以留空，USER为当前LINUX用户的用户名。

域名因为启用了https，需要一个真实的域名指向你的线上开发服务器。

国内没备案的域名，http会被不时的阻断，需要https才能用线上服务器调试。

```
CONFIG.HOST = "你自己的域名"
CONFIG.HOST_BG = "bg.%s"%CONFIG.HOST

```

配置文件中

```
CONFIG.DNSPOD.ID
CONFIG.DNSPOD.SECRET
```

[请点此访问DNSPORD安全中心](https://www.dnspod.cn/console/user/security)获取（域名的NAMESERVER请用DNSPOD）



开发用的发信邮箱的配置参见[tz_config配置说明](http://git.oschina.net/gu321/tz_config/blob/master/README.md)

**最后，请记得添加config.py到自己fork之后的私人代码库，防止丢失**

完成配置后，如果数据库准备就绪，运行


```
./cli/once/install.sh
```


就可以自动初始化开发环境了。

之后，启动 



```
./dev 

```


就可以进入开发调试了！


