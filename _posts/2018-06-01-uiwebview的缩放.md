---
layout: post
#标题
title:  uiwebview的缩放
#时间配置
date:   2018-06-01 11:06:31 +0800
#大类配置
categories: 知识
#小类配置
tag: object-c
---
 
* content
{:toc}

#### 1. 添加相关代理

```objc
<UIScrollViewDelegate, UIWebViewDelegate> 
webView.scrollView.delegate = self; 
```
 
#### 4. 设置相关代理

```objc
- (UIView *)viewForZoomingInScrollView:(UIScrollView *)scrollView { 
   return nil; 
} 
```