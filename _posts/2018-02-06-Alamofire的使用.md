---
layout: post
#标题
title:  Alamofire的使用
#时间配置
date:   2018-02-06 15:32:31 +0800
#大类配置
categories: 知识
#小类配置
tag: swift
---

* content
{:toc}
 

**git地址：** [https://github.com/Alamofire/Alamofire](https://github.com/Alamofire/Alamofire) <br>

> 简介：swift版的afnetworking，用于网络接口的申请

```swift
    /*  接口post请求
     *  url: 传过来的url
     *  param: 传过来的接口参数
     *  complete：接口返回的参数
     */
    class func post(url: String?, param: Parameters, complete: @escaping (_ result: [String: Any]) -> Void ) -> Void {
        
        // 如果发过来的链接长度为空，则直接返回，不做任何反应
        guard let urlString = url, strlen(url) > 0 else {
            return
        }
        
        Alamofire.request(urlString, method: .post, parameters: param, encoding: JSONEncoding.default).responseJSON { (response) in
            
            print("request ********** \(String(describing: response.request))")
            
            switch(response.result) {
            case .success(_):
                if let Json = response.result.value{
                    
                    // 将数据转化为字典
                    if let dic = try? JSONSerialization.jsonObject(with: response.data!, options: JSONSerialization.ReadingOptions.allowFragments) as! [String: Any] {
                        
                        print("请求数据 ********** \(dic)")
                        // 如果code为0，则表示请求成功
                        if dic["code"] as! Int == 0 {
                            complete(dic["data"] as! [String : Any])
                        } else {
                            print("请求数据失败********* \(String(describing: response))")
                        }
                    }
                }
                break
                
            case .failure(_):
                print("请求网络失败")
                break
            }
        }
    }
    
    
    /// 带有头的网络请求
    ///
    /// - Parameters:
    ///   - url: 请求链接
    ///   - param: 请求参数
    ///   - headers: 请求头
    ///   - complete: 请求后的结果
    class func post(url: String?, param: Parameters, headers: HTTPHeaders, complete: @escaping (_ result: [String: Any]) -> Void ) -> Void {
        
        // 如果发过来的链接长度为空，则直接返回，不做任何反应
        guard let urlString = url, strlen(url) > 0 else {
            return
        }
        
        Alamofire.request(urlString, method: .post, parameters: param, encoding: JSONEncoding.default, headers: headers).responseJSON { (response) in
            
            switch(response.result) {
                case .success(_):
                    if let Json = response.result.value{
                        print("请求的网路数据 ****** :\(Json) ")
                        
                        // 将数据转化为字典
                        if let dic = try? JSONSerialization.jsonObject(with: response.data!, options: JSONSerialization.ReadingOptions.allowFragments) as! [String: Any] {
                            
                            print("请求数据 ********** \(dic)")
                            // 如果code为0，则表示请求成功
                            if dic["code"] as! Int == 0 {
                                complete(dic["data"] as! [String : Any])
                            } else {
                                print("请求数据失败********* \(response)")
                            }
                        }
                    }
                    break
                
                case .failure(_):
                    print("请求网络失败")
                    break
            }
        }
    }
```