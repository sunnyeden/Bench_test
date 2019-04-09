### apachebench压力测试（apache）

#### 只要安装了apache，会自带ab压力测试
```
ab -c 10 -n 100 http://www.tanwan.com/
```

> **-c是指并发数**

> **-n是指请求总数**

#### 请求结果

```
Server Software:        nginx/1.10.2           #服务器类型
Server Hostname:        www.jiangliang738.cn   #域名
Server Port:            80					   #端口

Document Path:          /					   #根目录
Document Length:        10 bytes

Concurrency Level:      10
Time taken for tests:   2.677 seconds          #测试时间
Complete requests:      100                    #完成的请求数量
Failed requests:        0                      #失败的请求
Total transferred:      17200 bytes
HTML transferred:       1000 bytes
Requests per second:    37.36 [#/sec] (mean)
Time per request:       267.700 [ms] (mean)
Time per request:       26.770 [ms] (mean, across all concurrent requests)
Transfer rate:          6.27 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        7   26 140.0     10    1411
Processing:    11  231 414.8     93    1650
Waiting:       11  196 412.7     68    1637
Total:         20  257 434.9    104    1666

Percentage of the requests served within a certain time (ms)
  50%    104       #50%的请求处理时间在1毫秒左右
  66%    140
  75%    146
  80%    152
  90%   1516
  95%   1538
  98%   1548
  99%   1666
 100%   1666 (longest request)
```

> **主要看Failed requests，不为0说明网站超过负荷了**