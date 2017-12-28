---
layout: post
#一个项目多个target的创建
title: 一个项目多个target的创建
#时间配置
date:   2017-12-22 14:44:00 +0800
#大类配置
categories: xcode功能
#小类配置
tag: xcode
---

* content
{:toc}

### 引用链接
* [iOS同一项目多个Target的快速实现方法 - 两种使用场景详解](http://www.cnblogs.com/yajunLi/p/6001132.html)<br>

## 场景一： 一个项目配置多个环境
-------------------
1> 在tagets中直接添加Duplicate

![1.png](resources/56E922EF9D61781DEF6302B564EE8075.png =283x203)

2> 添加target并重新命名为runtimeOC

![2.png](resources/939AB2C76B30E8123E1907B571659945.png =169x163)

3> 修改Schemes中的名字

![3.png](resources/819E95EC397554D84E3471CDA7666A36.png =364x261)<br>
![4.png](resources/605D40DBECAC47AA5DA1153930DEB5D3.png =746x405)

4> 将自动生成的plist重新命名 -> 删除 -> 重新加载进入标记

![5.png](resources/CA7F8564C885212532A25BF4187F1D9B.png =271x277)
![6.png](resources/5BB5605807D45E6675C45A23B4C7B790.png =426x367)
![7.png](resources/1F4A65D9A2D6D9B508F8DCAB745AEDAB.png =530x128)
![8.png](resources/0D22EB7A40B844B0F70007A69BA38194.png =466x181)
![9.png](resources/1EDD18E8A80DB5772046230DB7D1EB33.png =717x420)
![10.png](resources/6A1C05E092F358B229E923EAB7E5702D.png =852x353)

5> 在项目中定义特定的宏作为区分（OC用macros，swift用swift_flag）
![11.png](resources/F6047094060E6FCB1C59C56A23E9150E.png =852x338)
![12.png](resources/4A4E45FA5403CE37D6DDDA3DBA099096.png =1146x686)

swift在swift_flag中添加宏，并且宏必须是字符串，每个宏都要用"-D"隔开，否则失效

![13.png](resources/AA5DBBB0D9879ED8E71B1409B6BBDD8A.png =870x383)
![14.png](resources/39F75F7246B9B488D69342550706E09B.png =1136x745)

## 场景二： 项目中直接创建一个整体项目target(相当于另外一个项目)
-------------------
![15.png](resources/FDDEBC27CE2A2980751516073767F54B.png =605x317)
![16.png](resources/85EDF5490394BF10CEB4AEDE4158DB98.png =730x521)