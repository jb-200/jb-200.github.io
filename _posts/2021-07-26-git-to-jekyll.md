---
title: "git-python测试"
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
git init --bare #服务器创建可上传库
git clone tx:/“路径” #克隆服务器库
注意：服务器上bare仓库不能直接查看必须clone才能查看

git设置缩写命令
.gitconfig
[alias]
        co = checkout
        br = branch
        ci = commit
        st = status -s
        tree = log --oneline --all --graph
        treeb = log --oneline --graph --branches
        treet = log --oneline --graph --tags
        diffc = diff --cached
        mg = merge
        mgg = merge -
        coo = checkout -
        amend = commit --amend --reuse-message=HEAD

code
```

来自 [git官网](https://git-scm.com/book/zh/v2/Git-%E5%88%86%E6%94%AF-%E5%8F%98%E5%9F%BA)

### git代码链接个人服务器
```txt
注意:查看个人服务器备份学习代码是否已上传???
```
### ssh登录相关
***
命令行工具推荐 Windows PowerShell   快捷键win+r   wt
服务器链接快捷工具推荐：PuTTY
ssh root@12.12.12    链接服务器

ssh免密登录配置
pwd 查看当前目录
ssh-keygen  生成密匙
ssh 127.0.0.1
将公钥上传    
方法1，scp拷贝到服务器追加到.ssh/aythorized_keys       scp -P跟密码或者跟 -f .ssh/id_rsa.pub root@11111/home/.ssh (-P port  指定ssh端口)
方法2 cat ~/.ssh/id_rsa.pub   复制本地公钥
.ssh/authorized_keys    
ssh免密登录 - 跨越&尘世 - 博客园 (cnblogs.com)
注意：
chmod
.ssh 目录权限是700    文件authorized_keys私钥的权限是600
C：/用户/.ssh/下存储私钥
config文件配置快捷链接名称
***

## Git相关问题

1. 数据库，表格形成乘积的大表，先筛选最大程度减少数据
2. 数据库 表外键以ID存储内存占用小
3. Git版本回退，版本控制，查看每次存储之间的变化
4. 测试注意界面表单分页数据


