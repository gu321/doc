导出hg或git中项目的方法
原来在SVN中，我们可以使用svn export非常简单的导出项目，然而在Git或hg的项目中，我找遍了，也没有找到有export的选项。那我们应该如何导出网上的开源项目呢？

Git项目：

使用Git项目的时候，我一般实现Clone出来，而后在Clone的地方使用archive。命令类似下面：

code
1
git archive master | tar -x -C /target/subfolder
如果我们需要变成压缩包可以这样：

code
1
git archive master | bzip2 >source.tar.bz2
当然，导成zip压缩包可能在Windows下会更流行些：

code
1
git archive --format zip --output /full/path/to/zipfile.zip master
如果你还有不太清楚的，可以在git的命令行下使用查看帮助：

code
1
git help archive
hg：

方法类似了，只是命令稍微有些不同：

code
1
hg clone --verbose -- https://project-source-home/ /target/folder/
路由到Clone出来的目录里面，使用下面的命令：

code
1
hg archive /target/folder/subfolder/
这就是将Clone里面的项目全部导出到/target/folder/subfolder/目录下面。

更具体的，也可以参见帮助：

code
1
hg help archive
