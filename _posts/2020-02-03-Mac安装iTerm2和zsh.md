---
layout: post
title:  "Mac安装iTerm2和zsh"
date:   2020-02-03 11:22:13 +0800
categories: NOTE
---

## Mac安装iTerm2和zsh

> 安装过程，采用 brew 安装，如不支持brew，请参考该链接安装：<a href="http://www.happycoding.cool/blog/blog/Mac%E5%AE%89%E8%A3%85HomeBrew%E5%92%8CHomeBrew-Cask.html" target="_blank">Homebrew安装过程</a>

### 安装iTerm2
brew cask install iTerm2

### 安装zsh
brew install zsh

### 安装oh-my-zsh

#### 方式一
```shell
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
#### 方式二
```shell
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```
以上两种方法都可能会出现，安装源无法访问的情况，此时可以采用如下安装办法
#### 方式三
1. 将安装脚本下载到本地
2. 执行 sh install.sh 进行安装

### 配置主题

<a href="https://github.com/ohmyzsh/ohmyzsh/wiki/Themes" target="_blank">查看支持的主题列表</a>
目录：~/.oh-my-zsh/themes
主题配置：
- 编辑： ～/.zshrc
- 找到属性：ZSH_THEME
- 如：配置主题 pygmalion：ZSH_THEME="pygmalion"

#### 配置插件
<a href="https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins" target="_blank">查看支持的插件列表</a>
目录：~/.oh-my-zsh/plugins

#### 插件配置

- 编辑： ～/.zshrc
- 找到属性：plugins
- 配置属性，系统已经默认了git，可根据需要从插件列表中选择需要的插件进行配置

如：
```shell
plugins=(git gradle mvn extract sublime zsh-autosuggestions zsh-syntax-highlighting)
```
#### 介绍几个常用插件

oh-my-zsh 自带插件
- git/gradle/mvn 
这三个就不用过多介绍
- extract 
功能强大的解压插件，所有类型的文件解压通过一个命令x全搞定，再也不需要去记tar后面到底是哪几个参数了
比如： x backup-001.tar.gz 或者 x temp-file.zip
- sublime
如果你电脑上装有Sublime，可以方便的在Zsh终端中调用Sublime打开文件，比如输入 st README.md 就可以调用机器上安装的Sublime Text打开当前目录的README.md文件进行编辑操作
#### 扩展插件
zsh-autosuggestions/zsh-syntax-highlighting
这两个是扩展插件，需要额外进行安装，其功能是命令行提示以及语法高亮显示

```shell
zsh-autosuggestions 安装
git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions

zsh-syntax-highlighting 安装
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

### 参考资料
- <a href="https://iterm2.com/" target="_blank">iterm2</a>
- <a href="https://ohmyz.sh/" target="_blank">ohmyz</a>
- <a href="https://xiaozhou.net/learn-the-command-line-iterm-and-zsh-2017-06-23.html" target="_blank">iTerm与Zsh</a>
