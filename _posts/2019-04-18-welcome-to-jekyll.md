---
title: "welcome"
date: 2019-04-18T15:34:30-04:00
categories:
  - blog
tags:
  - Jekyll
  - update
---
git笔记


```ruby
从开发分支合并到主分支  然后先更新在提交
Git add .
Git commit -m ""
Git push origin master
git pull 拉取
Git tree 查看结果树
Ssh tx 链接远程
切换分支 git checkout
Git branch -vv 查看分支的所有状态
git merge 合并分支
Git branch -d 删除
来自 <https://git-scm.com/book/zh/v2/Git-%E5%88%86%E6%94%AF-%E5%8F%98%E5%9F%BA> 
#=> prints 'Hi, Tom' to STDOUT.
```
---
测试笔记


```ruby
	1. 数据库，表格形成乘积的大表，先筛选最大程度减少数据
	2. 数据库 表外键以ID存储内存占用小
	3. Git版本回退，版本控制，查看每次存储之间的变化
  4. 测试注意界面表单分页数据
#=> prints 'Hi, Tom' to STDOUT.
```
---
python笔记


```ruby
	• Webdriver   启动器  下载并且防止启动器的位置：  放置到python的主目录下
	• 错误提示：“ssion not created: This version of ChromeDriver only supports Chrome version 88”webdriver 启动器版本需要下载最新版本/浏览器需要降级
	• 新窗口 跳转元素定位 窗口      switch_to.window(browser.window_handles[1])    窗口从0 开始计数
	• 

	• 元素定位
//input[@class='el-input__inner'])[2]

	• select元素下拉框
Select() # 实例化Select
.select_by_index(1)  # 选择第二项选项：o1
.select_by_value("o2")  # 选择value="o2"的项
.select_by_visible_text("o3")  # 选择text="o3"的值，即在下拉时我们可以看到的文本
	• 非select下拉框
下拉直接点击选择定位的元素

	• 解决   element not interactable交互报错
本地Jenkins端口号 8088
C:\Windows\system32\config\systemprofile\AppData\Local\Jenkins\.jenkins\secrets\initialAdminPassword
	• Iframe 内部元素获取        driver.switch_to.frame(id)/name   有唯一的id/name



#=> prints 'Hi, Tom' to STDOUT.
```

---
jmeter笔记


```ruby
%JMETER_HOME%\lib\ext\ApacheJMeter_core.jar;%JMETER_HOME%\lib\jorphan.jar;%JMETER_HOME%\lib\logkit-2.0.jar;

Response message:Non HTTP response message: Illegal character found in host: '/'
错误解决办法IP地址后不跟参数
用户登录:一次性登录  设置全局token


#=> prints 'Hi, Tom' to STDOUT.
```


Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
