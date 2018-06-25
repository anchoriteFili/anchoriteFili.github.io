---
layout: post
#标题
title:  storyboard的创建及使用
#时间配置
date:   2018-05-23 18:39:31 +0800
#大类配置
categories: 知识
#小类配置
tag: swift
---
 
* content
{:toc}


### 相关链接
---

<a href="https://blog.csdn.net/u010105969/article/details/53942862" target="_blank">浅谈iOS中的WKWebView添加cookie</a><br> 

```swift
//MARK: 初始化wkwebview的cookie
    func wkWebcookie() {
        
        var jsStr = ""
        if let cookie = USER_DEFAULT.string(forKey: "Cookie") {
            jsStr = cookie.isEmpty ? "" : cookie
        }
        
        // 根据JS字符串初始化WKUserScript对象
        let userScript = WKUserScript(source: jsStr, injectionTime: .atDocumentStart, forMainFrameOnly: true)
        let userContentController = WKUserContentController()
        userContentController.addUserScript(userScript)
        
        // 根据生成的WKUserScript对象，初始化WKWebViewConfiguration
        let webConfiguration = WKWebViewConfiguration()
        webConfiguration.userContentController = userContentController
        
        wkweb = WKWebView(frame: .zero, configuration: webConfiguration)
    }
```