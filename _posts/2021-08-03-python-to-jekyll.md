---
title: "python-json"
date: 2021-07-27T15:34:30-04:00
categories:
  - blog
tags:
  - notes
  - notes
---
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
????????????????
strip()
返回字符串的剪裁版本
