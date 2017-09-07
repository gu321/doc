# hg & git

## 导出hg或git中项目的方法

### GIT

Git项目：

使用Git项目的时候，我一般实现Clone出来，而后在Clone的地方使用archive。命令类似下面：



```
git archive master | tar -x -C /target/subfolder

```

如果我们需要变成压缩包可以这样：



```
git archive master | bzip2 >source.tar.bz2

```

### HG



```
hg archive /target/folder/subfolder/

```

这就是将项目全部导出到/target/folder/subfolder/目录下面。

