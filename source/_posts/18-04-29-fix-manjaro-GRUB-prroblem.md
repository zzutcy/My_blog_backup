---
layout: post
title: 安装manjaro 出现GRUB 恢复模式的解读办法
date: 2018-04-29 10:20:54
comments: true
tags:
    - Manjaro
    - GRUB
categories:
    - 笔记
---

![Manjaro grub](https://ws1.sinaimg.cn/large/006tNbRwly1fwbm24toatj311y0lc3zu.jpg)

### 今天看到manjaro 更新了新版 而且大佬们都乐于推荐manjaro 于是就 想着 尝试一下！

<!-- more -->

殊不知 这次在我那破本子上的一次尝试 让我看到了我本子装Linux的希望  让我有了准备折腾一番 大干一场的 冲动！！！！

在这我总结一下我这次折腾 所遇到的坑

**❂首先是 BIOS设置**
**BIOS UEFI启动 并且把 安全启动关闭！！！**

**❂然后是 制作安装镜像启动盘**
也许你会问 这有什么难得。 对当时我也是这样想的 但是在和 平时进行相同操作时 却四处碰壁。 进入了所谓的 GRUB  恢复模式！ 没错 你猜对了 我当时一脸蒙蔽！ 在经过一番google 后，找到了元凶！那就是 镜像写入方式有问题！！！ **需要以DD模式写入！**

这里推荐一款 开源 ！！ 好用！！ 强大！！ 并且能够在WIN下实现DD模式写入ISO 镜像的软件 他就是 RUFUS！ 体积非常小 ！

在以DD模式写入过后 终于能顺利的进行安装了！

（我还以为是我安装的时候 出现了问题 重装了 5，6 次！！！ 鱼儿 哭死在厕所里！）

希望 这个能对你有所帮助！


---
### 文章作者:[糖醋鱼](http://zzutcy.top)

### 版权声明:转载请注明来自[糖醋鱼的博客](http://zzutcy.top)
---