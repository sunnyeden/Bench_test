### webbench压力测试（Linux）

#### 安装webbench
```
wget http://www.ha97.com/code/webbench-1.5.tar.gz
```
```
tar zxvf webbench-1.5.tar.gz
```
```
cd webbench-1.5
```
```
make && make install
```

#### 编译错误解决方法


```
mkdir -m 644 -p /usr/local/man/man1
```

```
yum install ctags 
```

#### webbench使用方法
```
webbench -c 1000 -t 30 http://www.tanwan.com/
```

> ### -c是指并发数

> ### -t是指请求时间

#### 请求结果
```
Speed=24920 pages/min, 21037312 bytes/sec.
Requests: 24833 susceed, 87 failed.
```

> ### 主要看是否有失败数，有的话说明网站超过负荷了