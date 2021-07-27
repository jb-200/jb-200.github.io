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

