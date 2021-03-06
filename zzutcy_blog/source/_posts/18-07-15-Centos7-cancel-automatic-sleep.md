---
layout: post
title: Centos 7桌面版取消自动休眠
date: 2018-07-15 20:26:08
comments: true
tags:
    - Centos7
    - 坑
categories:
    - 笔记
---

![Centsos](https://ws3.sinaimg.cn/large/006tNbRwly1fwbl2n48qej30go08rgm6.jpg)


* 作为一个刚接触Linux的新手，用实验室闲置的服务安装的Centos 7 来提供内网的文件服务。然后在寝室美滋滋的用SSH进行远程操作.

* 理想很美好但是现实很残酷，最近发现服务器有时候会莫名其妙的 **无响应** 等到了实验室才猛然发现原来系统是自动休眠了，经过一番搜索找到了解决方案 在这里分享一下

<!-- more -->

```bash
vim /etc/X11/xorg.conf		# 这个文件原来是没有的，这算是新建了一个文件

# 添加以下内容

Section "ServerFlags"
		Option "BlankTime"   "0"
        Option "StandbyTime" "0"
        Option "SuspendTime" "0"
        Option "OffTime"     "0"
EndSection

Section "Monitor"
        Option "DPMS" "false"
EndSection
```

* 然后重启服务器，不太这些配置的意思，但至少没再发生原来的情况了，以后是肯定要学习一下 xorg.conf 的详细配置。
这个文件好像不能出什么错误，否则系统可能会起不来，所以配置的时候要 **格外小心！**。


---
### 文章作者:[糖醋鱼](http://zzutcy.top)

### 版权声明:转载请注明来自[糖醋鱼的博客](http://zzutcy.top)
---