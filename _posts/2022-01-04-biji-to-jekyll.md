---
title: "biji-postman"
date: 2022-01-05T15:34:30-04:00
categories:
  - postman
tags:
  - 基础
  - 图片
---
# Automation Test- master测试框架
1. 问题:(暂时未解决报错)
```python
// pip3 install -r requirements.txt产生
ERROR: Could not find a version that satisfies the requirement opencv-python==4.2.0.32
```
2. 内网: 
```python
// pip install pgmagick产生
reparing metadata (setup.py) ... error
  error: subprocess-exited-with-erro
```





### 什么是http协议？

1. 客户端和服务器传输数据的一种方式
2. 请求头【Host:   connection keepalive  Accept:    content-type  如果requestedWith为null，则为同步请求。如果requestedWith为XMLHttpRequest则为Ajax请求。 】，请求行，请求方式，请求地址，响应 statuscode 200  payload  cookie
![jpg](/assets/images/postman临时token设置.png)

### session token cookie 区别？
1. 都是服务器生成的
2. 【cookie存在客户端  sessionid存在服务器的内容   token  存在服务器数据库】

### 开发API“项目端口”“；例子：8111/yyc/doc.html”
### Postman_tests断言    状态断言  业务断言

1. Status code is 200 【状态码200】 
2. Response body Contanis string 断言返还结果包含字符串
3. Response body Json value check 对返还的json数据做检查
4. Response body is equat to a string 结果等于一个字符串
5. Response headers Content-Type header check 响应头里包含Content-type
6. Response time is less than 200ms
通过发送不完整数据/不正确参数来验证API的错误处理
参考 [postman官网文档](https://learning.postman.com/docs/writing-scripts/test-scripts/)

#### ！待提高！
1. 网页中实时加载的验证码如何，没有找到有用的解决方案
2. 

## get、post请求区别？
1. get是通过网址？来传递参数的。不安全，主要是为了获取数据
2. post是通过表单form来传递参数的，提交数据

## post常用的请求参数有哪些？
1. form-data
2. json text javascript html xml
3. binary 二进制文件

## 数据参数化
{{$timetamp}}
{{$random}}
{{$uid}}
## 全局变量如何设置/上一个接口的参数如何拿到？
1. json提取器
取 var data = JSON.parse(responseBody)
设置成全局 pm.globals.set("access_token",data.access_token)
用 {{access_token}}
延申：怎么拿深层的数据 {"code":0,"msg":"success","data":{"total":73,"list":[{"id":"1438030817535479
var data1 = data0.data
var data2 = data1.list
data2[0].id
2. 正则表达式
取  responseBody.match(new RegExp('"msg":"(.+?)",'))
设置成全局 pm.globals.set()
用{{msg}}
3. cookie提取器【实际测试不会使用】
postman.getResponseCookie

## token时效测试（需要逐步完善）
1. 登录后响应json里的expires_in（单位秒）
2. 一些登录返回接口并没有expires参数，所以如何测试程序登录后的在线时长
### 问答
1. 确认环境，排除其他因素，对应需求危害，如果不是特别等级很高的后期在跟进
2. 复现率低的BUG，最初记录它的时候详细描述，出现位置截图操作过程进行记录，不易复现备注，多轮回归测试进行复现，后期跟开发一起复现
3. 新项目测试：了解项目需求原型、业务逻辑、场景、设备是否跨平台、稳定性等、出计划、拿到测试地址根据测试计划用例，及时跟进需求变更，及时跟开发沟通问题，跟进问题，回归测试，及时汇报测试结果  测试报告
4. 了解现状/产品业务
5. cookie是浏览器缓存kv方式保存方便下一次访问使用
6. session是会话临时存在服务器里
7. token是用户标识访问授权，减少访问数据库对比账号密码次数
8. postman可设置环境、全局函数![jpg](/assets/images/postman环境.png)
9. 打包？
## Newman集成jenkins
1. 安装nodejs
2. 安装Newman
3. 安装Jenkins
4. 启动Jenkins http://localhost:8083(可使用安装时添加的端口)  
5. 解锁Jenkins （解锁钥匙在）
6. 创建命令运行postman脚本文件
7. 在结点配置nodejs和nmp的环境变量
```bash
"生成报告的插件"
npm install -g newman-reporter-html
"例如运行语句"
newman run "D:\J\渔业村.postman_collection.json" -g "D:\J\workspace.postman_globals.json" -e "D:\J\workspace.postman_globals.json" -r cli,html,json,junit --reporter-html-export "D:\j\report001.html"
```
