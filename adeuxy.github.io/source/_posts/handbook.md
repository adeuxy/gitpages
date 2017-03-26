---
title: handbook
date: 2017-03-26 14:19:21
tags: linux
---

###### 查看端口和连接信息
``` bash
netstat -ntlp
```
<!-- more -->

###### 列出占用端口进程
``` bash
lsof -i :8080
```
###### 查看iptables状态
``` bash
/etc/init.d/iptables status
```
###### 添加8080端口
``` bash
/sbin/iptables -I INPUT -p tcp --dport 8080 -j ACCEPT
/etc/rc.d/init.d/iptables save
/etc/init.d/iptables restart
```
###### 按日期动态命名日志文件
``` bash
/`date "+%F"`.`date "+%H-%M-%S"`.`date "+%N"` 2>&1
```
