---
title: "git-pyhon测试"
date: 2019-04-18T15:34:30-04:00
categories:
  - blog
tags:
  - git
  - python
---

## git笔记

从开发分支合并到主分支  然后先更新在提交

```bash
Git add .
Git commit -m ""
Git push origin master
git pull # 拉取
Git tree # 查看结果树
Ssh tx # 链接远程
git checkout # 切换分支 
Git branch -vv # 查看分支的所有状态
git merge # 合并分支
Git branch -d # 删除
```

来自 [git官网](https://git-scm.com/book/zh/v2/Git-%E5%88%86%E6%94%AF-%E5%8F%98%E5%9F%BA)

## 测试笔记

1. 数据库，表格形成乘积的大表，先筛选最大程度减少数据
2. 数据库 表外键以ID存储内存占用小
3. Git版本回退，版本控制，查看每次存储之间的变化
4. 测试注意界面表单分页数据

## python笔记

1. Webdriver   启动器  下载并且防止启动器的位置：  放置到python的主目录下
2. 错误提示：“ssion not created: This version of ChromeDriver only supports Chrome version 88”webdriver 启动器版本需要下载最新版本/浏览器需要降级
3. 新窗口 跳转元素定位 窗口

```python
switch_to.window(browser.window_handles[1]) # 窗口从 0 开始计数
```

4. 元素定位:

```python
input[@class='el-input__inner'])[2]
```
5. select元素下拉框

```python
Select() # 实例化Select
.select_by_index(1)  # 选择第二项选项：o1
.select_by_value("o2")  # 选择value="o2"的项
.select_by_visible_text("o3")  # 选择text="o3"的值，即在下拉时我们可以看到的文本
```
6. 非select下拉框

下拉直接点击选择定位的元素

7. 解决**element not interactable**交互报错
本地Jenkins端口号 8088

```txt
C:\Windows\system32\config\systemprofile\AppData\Local\Jenkins\.jenkins\secrets\initialAdminPassword
```

8. Iframe 内部元素获取

```python
driver.switch_to.frame(id)/name # 有唯一的id/name
```



