---
layout: post
#标题
title:  SSZipArchive压缩三方的使用
#时间配置
date:   2018-04-18 14:45:31 +0800
#大类配置
categories: 知识
#小类配置
tag: object-c
---
  
* content
{:toc}

### 相关链接
---

* <a href="https://blog.csdn.net/zhengang007/article/details/51019479" target="_blank">SSZipArchive的使用详解和遇到的问题</a><br>
* <a href="https://github.com/ZipArchive/ZipArchive" target="_blank">github地址</a><br>


#### 基本使用

> 说明：此三方用于文件的压缩，object-c/swift都可以，使用前先导入 libz.tbd 库

**object-c使用**

```objc
// Create
[SSZipArchive createZipFileAtPath:zipPath withContentsOfDirectory:sampleDataPath];

// Unzip
[SSZipArchive unzipFileAtPath:zipPath toDestination:unzipPath];
```

**swift使用**

```swift
// Create
SSZipArchive.createZipFileAtPath(zipPath, withContentsOfDirectory: sampleDataPath)

// Unzip
SSZipArchive.unzipFileAtPath(zipPath, toDestination: unzipPath)
```