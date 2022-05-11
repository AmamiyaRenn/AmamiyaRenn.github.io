---
title: git使用经验与使用教程
tags:
  - git
  - 技术笔记
  - VSCode
categories:
  - 技术笔记
  - git
cover: "https://cdn.jsdelivr.net/gh/AmamiyaRenn/cloudimg@master/Shojo in Room.jpg"
description: git 是一个分布式版本控制软件，是你代码的后悔药；git 配合功能强大的 VSCode，简直就是如虎添翼
keywords: "git, VSCode, 技术笔记"
abbrlink: 40411
date: 2022-05-11 10:26:07
---

互联网逛多了，深感真正有切实操作价值的教程挺少，很大部分都是 copy 他人文章还不标注转载，所以在本文我会把一些真正帮到我的文章列出，并附上一些我个人的经验

# 如何使用git

## 安装

不会还有人没下git吧，不会吧 😥
如果你是{%label Linux orange%}系统，直接`sudo apt-get install git`就可以了
如果你是{%label Windows blue%}系统，最简单的下载方式是打开你的 windows terminal 中的 powershell7 通过 winget 安装: `winget install -e --id Git.Git`
什么你还没有 windows terminal 和 Powershell7? 赶快去 Microsoft Store 下吧
{% note purple 'fa-solid fa-plus' simple %}

关于`winget`支持的安装，可以查询{% btn 'https://winget.run/',winget.run,far fa-hand-point-right,blue  %}，同时 winget 如果没有也可以在这里下载安装

{% endnote %}

## 使用

下文比较全面的介绍了什么是git，如何配置与使用git，如何在IDE（如 Jetbrains系和 VSCode）中使用git
{% btn 'https://www.zhihu.com/question/20866683/answer/2247525158',如何优雅地使用Git？,far fa-hand-point-right,blue larger %}

## 无法链接到github?

有两种办法
{%label 办法一 green%}: 不用GitHub, 改用Gitee
但是明显不靠谱是吧, 毕竟上Github是现代人基本修养
{%label 办法二 green%}: 给终端开代理

1. 首先, 你得有个代理
   先下载`clash`来挂梯子(我不推荐qv2ray, 因为我没试成功 😥, 且clash 是跨平台的),{% btn 'https://github.com/Fndroid/clash_for_windows_pkg/releases',此处下载clash_for_windows_pkg 发行版,far fa-hand-point-right,blue  %}, 如果登不上那你需要挂个梯子, 那么问题来了, 本来下 clash 就是为了挂梯子, 现在和我说要先挂梯子才能下clash...我只能说可以上gitee上看看能不能下到, 要么就自己找资源吧
   关于clash的操作我推荐这个回答{% btn 'https://www.zhihu.com/question/480431059/answer/2240507461',clash下载,far fa-hand-point-right,blue%}和这个回答{% btn 'https://www.zhihu.com/question/432847922/answer/2328447514',请问有没有大神知道Clash for Android URL配置怎么弄啊?,far fa-hand-point-right,blue%}
2. 然后, 给终端开代理
   {% tabs TerminalAgent %}

<!-- tab Linux @fab fa-linux-->

如果你是{%label Linux orange%}系统, 则设置中设置手动网络代理->在http 和 https选项加入 clash 的 port号码, 如7890->打开你的终端, `sudo gedit ~/.bashrc`(如果你用zsh则`sudo gedit ~/.zshrc`(其他的话看你用什么shell))->末尾写入`export http_proxy="http://localhost:port" `和`export https_proxy="https://localhost:port"`

<!-- endtab -->

<!-- tab Windows @fab fa-windows-->

如果你是{%label Windows blue%}系统, 可以参考这一篇{% btn 'https://blog.csdn.net/YZ930035683/article/details/102075969',给 Windows 的终端配置代理,far fa-hand-point-right,blue%}

<!-- endtab -->

{% endtabs %}
然后你就可以愉快的使用git了!
如果VSCode的`git push`功能出现`fatal 443链接错误`了, 就可以直接在终端中输入指令来`push`

