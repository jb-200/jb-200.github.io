---
title: "jmeter"
date: 2021-07-27T15:34:30-04:00
categories:
  - blog
tags:
  - jmeter
  - postman
---
## jmeter笔记

### 配置环境变量
```shell
%JMETER_HOME%\lib\ext\ApacheJMeter_core.jar;%JMETER_HOME%\lib\jorphan.jar;%JMETER_HOME%\lib\logkit-2.0.jar;
```
### 常见错误
```txt
Response message:Non HTTP response message: Illegal character found in host: '/'

解决办法：错误解决办法IP地址后不跟参数
```

### 用户登录:一次性登录 设置全局token

![jpg](/assets/images/jmeter用户登录.jpg)
```txt
获取上一请求的值,在下一请求中使用
```  
## postman

### 设置用户登录

```txt
在Headers设置Cookie token
```
![png](/assets/images/postman_ct.png)
### jmeter部署Linux服务器
1. 打开要上传文件目录下（jdk包、jmeter包）
2. 本地-->服务器
scp .文件名  （ssh登录配置的服务器名称） : 目录（服务器上目标路径）
3. 服务器--->本地
scp （ssh登录配置的服务器名称）:/home/.../...  C:/.../临时
4. 解压
 tar zxvf jdk-8u351-linux-i586.tar.gz
5.  配置环境变量
vi .bashrc
```python
#以下是jdk环境配置
export JAVA_HOME=/home/jb/jdk-19.0.1
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
export PATH=$JAVA_HOME/bin:$PATH:
#以下是jmeter环境配置
export JMETER_HOME=/home/jb/jmeter/apache-jmeter-5.5
export PATH=${JMETER_HOME}/bin:$PATH

#执行（注：生成的报告文件必须是不存在的，否则数据不会覆盖）
jmeter -n -f -t live_five.jmx -l live_five.jtl -j live_five.log
rm -rf live_five.jtl && jmeter -n -t live_five.jmx -l live_five.jtl
查询某状态的返回
grep code ./live_five.jtl | grep "已结束" | wc
```


