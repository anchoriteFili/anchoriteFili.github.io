---
layout: post
#标题
title:  WKWebView点击_blank链接不跳转
#时间配置
date:   2018-06-08 15:01:31 +0800
#大类配置
categories: 知识
#小类配置
tag: swift
---
 
* content
{:toc}
 

**相关链接：**

<a href="https://www.jianshu.com/p/60ba6aeb0c42" target="_blank">关于WKWebView 加载网页 点击link不会跳转的解决方案</a><br>

```swift
-(void)webView:(WKWebView *)webView decidePolicyForNavigationAction:(WKNavigationAction *)navigationAction decisionHandler:(void (^)(WKNavigationActionPolicy))decisionHandler
{
    //如果是跳转一个新页面
    if (navigationAction.targetFrame == nil) {
        [webView loadRequest:navigationAction.request];
    }
   
    decisionHandler(WKNavigationActionPolicyAllow);
}
```