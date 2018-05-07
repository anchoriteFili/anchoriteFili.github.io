---
layout: post
#标题
title:  wordpress建站(本地服务器版本)
#时间配置
date:   2018-05-02 11:26:31 +0800
#大类配置
categories: 知识
#小类配置
tag: wordpress
---
 
* content
{:toc}


### 相关链接
---

* <a href="https://www.zhihu.com/question/28276750" target="_blank">在Wordpress中如何使用MarkDown编辑博文？</a><br>
* <a href="https://codex.wordpress.org/zh-cn:安装_WordPress#.E8.91.97.E5.90.8D.E7.9A.845.E5.88.86.E5.AE.89.E8.A3.85" target="_blank">五分钟安装教程</a><br>
* <a href="https://jingyan.baidu.com/article/b0b63dbf1523cb4a4930705f.html" target="_blank">wordpress 建站教程</a><br>
* <a href="https://cn.wordpress.org/txt-download/" target="_blank">wordpress下载页面</a><br>
* <a href="https://cn.wordpress.org/switching/" target="_blank">轻松将您的WordPress切换为中文</a><br>
* <a href="https://cn.wordpress.org/wordpress-4.9.4-zh_CN.zip" target="_blank">WordPress 4.9.4下载链接</a><br>
* <a href="https://cn.wordpress.org/wordpress-4.9.4-zh_CN.tar.gz" target="_blank">下载.tar.gz — 8.7 MB</a><br>

**安装或使用WordPress的问题，请查看相关文档。**
* <a href="http://wordpress.org/" target="_blank">WordPress.org</a><br>
* <a href="http://zh-cn.forums.wordpress.org/" target="_blank">WordPress中文论坛</a><br>
* <a href="http://codex.wordpress.org/zh-cn:Main_Page" target="_blank">WordPress中文文档</a><br>

### 配置过程
---

> **注意：**可直接根据下载的压缩包中的readme.html文件进行使用。

#### 服务器环境要求
---
* PHP 5.2.4或更新版本
* MySQL 5.0或更新版本
* Apache mod_rewrite模块（可选，用于支持“固定链接”和“站点网络”功能）

> 下载压缩包到本地，解压缩，双击解开的文件夹中的readme.html文件，即可查看WordPress的介绍、安装，和升级方法。在您将程序文件上传至服务器相应目录后，安装过程只需5分钟。

> 已经在使用WordPress英文版本的用户，无需重新安装，也可<a href="https://cn.wordpress.org/switching/" target="_blank">轻松将您的WordPress切换为中文</a><br>。若您有特殊需要，亦可使用<a href="https://i18n.svn.wordpress.org/zh_CN/" target="_blank">SVN</a><br> checkout所需的po和mo文件。简体中文WordPress压缩包是基于<a href="https://core.svn.wordpress.org/" target="_blank">英文SVN源</a><br>自动构建的。


#### 一、下载wordpress

* <a href="https://cn.wordpress.org/wordpress-4.9.4-zh_CN.zip" target="_blank">WordPress 4.9.4下载链接</a><br>
* <a href="https://cn.wordpress.org/wordpress-4.9.4-zh_CN.tar.gz" target="_blank">下载.tar.gz — 8.7 MB</a><br>

![IMAGE]({{ site.img_url }}90DC2F3D263EF4934D3BE45D5D8203BD.jpg)

#### 二、如果有本地服务器，将下载wordpress文件夹放入本地服务器并运行

`1. 将文件放入本地服务器文件夹`

![IMAGE]({{ site.img_url }}9C1B30C93A6445384D89918CDEB79372.jpg)

`2. 运行本地服务器`

![IMAGE]({{ site.img_url }}B5CBF2E4DCE33F6DEF9EBA96D76F40DC.jpg)

`3. 配置本地数据库`

* 打开本地数据库
![IMAGE]({{ site.img_url }}3872576FF7B874F5D695A84C21EC37C9.jpg)
* 使用 Sequel Pro 链接本地数据库
![Snip20180307_8.png]({{ site.img_url }}C30F8E62B40F08A2EF06C0CA06CC6340.png)
* 创建wordpress数据库
![IMAGE]({{ site.img_url }}B069A9AE55AE7D41E42831CCF3DD4B68.jpg)
![IMAGE]({{ site.img_url }}00884E5E943EE40E30BA70442F978BCC.jpg)
![IMAGE]({{ site.img_url }}258841B5500B238C288E3AD0B72CF433.jpg)

`4. 设置数据库`

![IMAGE]({{ site.img_url }}89325F37B0D3D6814BC491A4F239D617.jpg)

**配置数据库基本信息**

![IMAGE]({{ site.img_url }}F63EDBC85D2E16D7683308A3519FF5B9.jpg)

![IMAGE]({{ site.img_url }}63AEEA81FE97177AF1F2F4C2B82326BA.jpg)

`5. 使用WordPress五分钟安装程序`

`密码：M#dLpuDiDpTsh&GwU0`

![IMAGE]({{ site.img_url }}CC28239A54F08AB77C2236B97ACEAC2C.jpg)

![IMAGE]({{ site.img_url }}3BAE473A2EA862D8D381F2E27DAA9B0B.jpg)

![IMAGE]({{ site.img_url }}E302E76FD1282C70B87CAB4C23DB37FD.jpg)

`6. 点击登录，进入管理页面`

![IMAGE]({{ site.img_url }}460BBACDDB7C75ED2A29C992E4C08DDD.jpg)



#### 下面就是自己搞着玩儿了
---

>> 哈哈哈哈