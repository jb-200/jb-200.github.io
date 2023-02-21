---
title: "python-json"
date: 2021-07-27T15:34:30-04:00
categories:
  - blog
tags:
  - notes
  - notes
---

```bash


Json模块提供了四个功能：dumps、dump、loads、load
json.dumps(): 对json进行编码，把数据类型转换成字符串。
json.dump():对json进行编码， 把数据类型转换成字符串，并存储在文件中。
json.loads(): 对json进行解码，把字符串转换成数据类型 。
json.load(): 把文件打开，对json进行解码，从字符串转换成数据类型。
参考[stackoverflow](https://stackoverflow.com/questions/45964731/how-to-parse-hierarchy-based-on-indents-with-python)

pickle.dump(obj, file[, protocol])
序列化对象，并将结果数据流写入到文件对象中。参数protocol是序列化模式，默认值为0，表示以文本的形式序列化。protocol的值还可以是1或2，表示以二进制的形式序列化
pickle.load(file)
　　反序列化对象。将文件中的数据解析为一个Python对象。
cell()
固定的行跟列
strip()
返回字符串的剪裁版本
```

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




