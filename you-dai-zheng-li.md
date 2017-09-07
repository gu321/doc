* DOCKER构建 https://daocloud.io


## 配置环境

配置环境 

0. python版本是3.6
1. 软链接 src/py/tz 到 python 目录下的 site-packages
2. 运行 cli/7z/unpack.py 解码配置文件
4. cli/install.sh

## 主机初始化

### 腾讯云
* cli/yun/init.sh : 初始化腾讯云主机(域名设置为gu321，ssh登录)
* cli/yun/ssh.sh : ssh登录云主机中的docker

### 数据库导入

* cli/backup/psql ./table_load.sh

## 数据初始化

### 汇率数据

1. 运行 src/py/spider/rate/run.sh 导入招行的汇率

### 股票数据

进入目录 src/py/spider

1. 运行 stock.py 导入雪球的股票列表
2. 运行 report/stock2com.py 找到是股票的股票代码
3. 运行  price/price_hk_us.py 导入美股、港股的价格
4. 抓取A股的股价&除权分红 src/py/spider/stock/price/dividend_cn.py

### 自动补全


运行 src/py/autocomplete/autocomplete_json.py 生成股票json数据（定时任务） 



### 使用说明

* 数据库密码参见 cli/make/config/dev.py
* python postgresql 数据库的使用参见 src/py/example/postgresql.py
* 运行 ./dev 启动调务

## 调试技巧



### 编译pika 

make 加上参数 -Wno-error ， 不要把警告当错误 

rocksdb下面文件如果有编译错误，可以加上#include <functional>

/tmp/pika/pika/third/rocksdb/util/thread_local.h
/tmp/pika/pika/third/rocksdb/util/posix_logger.h
