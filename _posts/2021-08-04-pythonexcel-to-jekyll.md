---
title: "excel-python"
date: 2021-08-04T15:34:30-04:00
categories:
  - excel
tags:
  - python
  - excel
---
# 读写文件
```python
# r 读
#  w 写入空文件
#   a  在原文件的基础上加
# 如果执行后没报错并且文件未写入查看文件权限
open(filename, 'r',encoding='utf-8', errors='ignore')

```
# 换行循环

```python
for i in range(2):
    	for j in range(3):
            for k in range(4):
                string = "{},{},{}\n".format(i, j, k)
                with open("a.csv",'a') as file:
                    file.write(string)
```
![jpg](/assets/images/循环.png)

# 拆分单元格显示

```python
for i in range(2):
	i_string = str(i)
	for j in range(3):
		j_string = str(j)
		for k in range(4):
			k_string = str(k)
			string = "{},{},{}\n".format(i_string, j_string, k_string)
			i_string = ''
			j_string = ''
			k_string = ''
			with open("a.csv",'a') as file:
				file.write(string)
```     
![jpg](/assets/images/拆分.png)