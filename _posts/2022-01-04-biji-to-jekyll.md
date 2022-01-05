---
title: "biji"
date: 2022-01-05T15:34:30-04:00
categories:
  - postman
tags:
  - 基础
  - 图片
---
### 什么是http协议？

1. 客户端和服务器传输数据的一种方式
2. 请求头【Host:   connection keepalive  Accept:    content-type  如果requestedWith为null，则为同步请求。如果requestedWith为XMLHttpRequest则为Ajax请求。 】，请求行，请求方式，请求地址，响应 statuscode 200  payload  cookie
![jpg](/assets/images/postman临时token设置.png)

### session token cookie 区别？
1. 都是服务器生成的
2. 【cookie存在客户端  sessionid存在服务器的内容   token  存在服务器数据库】

# 开发API“项目端口”“；例子：8111/yyc/doc.html”
### ?Postman   tests断言    状态断言  业务断言

1. 
2. 通过发送不完整数据/不正确参数来验证API的错误处理
3. 
参考 [postman官网文档](https://learning.postman.com/docs/writing-scripts/test-scripts/)

#### ！待提高！网页中存在验证码如何使用临时登录token测接口？ Params 里设置从浏览器F12拿到的临时token的value值 

## get、post请求区别？
1. get是通过网址？来传递参数的。不安全，主要是为了获取数据
2. post是通过表单form来传递参数的，提交数据

## post常用的请求参数有哪些？
1. form-data
2. json text javascript html xml
3. binary 二进制文件

## 数据参数化
timetamp
random
uid
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
3. cookie提取器




