# 配置环境


#### WEB端


* 源码 [git.oschina.net/gu321/tz](http://git.oschina.net/gu321/tz)
* 配置文件 [git.oschina.net/gu321/tz_config](http://git.oschina.net/gu321/tz_config)

代码私有，请注册账号，告知管理员，申请只读权限。

普通开发者只有只读权限，代码改动请提交pull request。

所以，**首先请fork源码，然后clone自己的源码**。

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


./cli/once/install.sh


#TODO 补充完善如何个人部署。
