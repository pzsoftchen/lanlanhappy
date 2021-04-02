---
layout: post
title:  "Mac安装HomeBrew和HomeBrew-Cask"
date:   2020-02-02 10:12:33 +0800
categories: NOTE
---


<div align=center>
<img src="../assets/img/2020-02-02-01.png">
</div>

## Mac安装HomeBrew和HomeBrew-Cask

> 这两天在家为我的Mac安装HomeBrew和HomeBrew Cask，原本以为这应该是件很简单的事，没曾想断断续续折腾了两天，期间遇到了太多稀奇古怪的问题，Google了大半天，也尝试了很多种安装办法，终于安装成功，以此记录期间遇到的各种问题。

## 基础环境
- 操作系统为Mac OS X 10.15.3 Catalina或更高版本
- 已安装版本管理工具Git（Mac OS X 10.7 Lion已经预安装）
- 已安装Xcode开发工具
- 已安装JDK8
- 开启蓝灯专业版本翻墙

## 安装过程中遇到的各类问题
### 问题1
执行完官网安装命令后，出现如下问题
```shell
curl: (7) Failed to connect to raw.githubusercontent.com port 443: Connection refused
```
### 问题2
```shell
Homebrew installation on Mac OS X Failed to connect to raw.githubusercontent.com port 443
```
### 问题3
```shell
error: RPC failed; curl 56 LibreSSL SSL_read: SSL_ERROR_SYSCALL, errno 54
	fatal: The remote end hung up unexpectedly
	fatal: early EOF
	fatal: index-pack failed
	Failed during: git fetch origin master:refs/remotes/origin/master --tags --force
```
### 问题4
```shell
error: RPC failed; curl 18 transfer closed with outstanding read data remaining
	fatal: The remote end hung up unexpectedly
	fatal: early EOF
	fatal: index-pack failed
	Failed during: git fetch origin master:refs/remotes/origin/master --tags --force
```
以上问题的遇到过程以及期间的尝试的解决手段，在这里就不再详细说明，安装过程一路坎坷，可以说几乎网上能搜到的问题我都碰了个遍；如果你也遇到以上这些问题中的某一个或某几个，可以参考后面我后面安装成功的正确姿势。

### 最终正确的安装办法
> 核心的问题还是“墙”的问题，因为整个安装过程我开启了蓝灯翻墙（我购买的是专业版本的服务），错误的认为我碰到的问题并不是由于“墙”导致的，所以一直再尝试解决遇到的问题，我在解决问题的过程中却碰到了越来越多的问题，花费了非常多的时间去尝试和摸索。

正确的安装办法主要参考了以下几篇文章，核心思路是先要将镜像设置为国内提供的站点

这里不再进行转载，贴上链接，供参考：
- <a href="https://juejin.im/post/5c738bacf265da2deb6aaf97" target="_blank">Mac HomeBrew国内镜像安装方法</a>
- <a href="https://juejin.im/post/5cd2a50e518825356d54b847" target="_blank">HomeBrew和HomeBrew Cask的安装和使用</a>
- <a href="https://lug.ustc.edu.cn/wiki/mirrors/help/brew.git" target="_blank">中科大源</a>
- <a href="https://mirror.tuna.tsinghua.edu.cn/help/homebrew/" target="_blank">清华大学的源</a>
- <a href="https://brew.sh/" target="_blank">官方安装文档</a>
