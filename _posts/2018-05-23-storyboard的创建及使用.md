---
layout: post
#标题
title:  storyboard的创建及使用
#时间配置
date:   2018-05-23 18:03:31 +0800
#大类配置
categories: 知识
#小类配置
tag: swift 
---
 
* content
{:toc}


### 相关链接
---

* <a href="https://blog.csdn.net/hard_working1/article/details/50689217" target="_blank">Swift - 故事板storyboard的用法</a><br>



#### 1. 创建storyboard

#### 2. 向storyboard中拖拽UIViewController

#### 3. 创建一个UIViewController，并关联到storyboard中

![IMAGE]({{ site.img_url }}23A5FD5C75DEC1DA2B1E8B420B21B856.jpg)

![IMAGE]({{ site.img_url }}E90B4656464FC1FDAB294B1E3FEFADD8.jpg)

#### 4. 可以使用代码获取UIViewController

```swift
let rootViewController = UIStoryboard(name: "SHS", bundle: nil).instantiateViewController(withIdentifier: "SHSLogViewControllerID") as UIViewController
            window?.rootViewController = rootViewController

```