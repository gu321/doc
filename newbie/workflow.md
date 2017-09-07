# 开发流程


开发流程采用fork+pull request开发模式，参见

* [《如何在github上fork一个项目来贡献代码以及同步原作者的修改》](http://www.cnblogs.com/rubylouvre/archive/2013/01/24/2874694.html)。


## 注意事项

代码库是GIT的，但是我是用HG-GIT。

HG是一个非常好用的代码控制工具（参见：[hg 简明教程](http://z42.readthedocs.io/zh/latest/devtools/hg.html) ），在通过hg alias设置命令别名后，操作GIT非常方便。

但是，毕竟HG不是主流的版本控制软件，GIT早有一统天下的趋势。

所以，大家可以自行选择，不强求统一。

但是请GIT的用户注意参考 .hgignore 设置 .gitignore 。