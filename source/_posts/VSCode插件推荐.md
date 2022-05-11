---
title: VSCode插件推荐
tags:
  - 技术笔记
  - VSCode
  - IDE
categories:
  - IDE
  - VSCode
abbrlink: 45037
date: 2022-05-10 14:40:51
cover: https://cdn.jsdelivr.net/gh/AmamiyaRenn/cloudimg@master/telephone_booth.jpg
description: 记录了一些可以显著增强VSCode的插件，不得不说VSCode真的非常强大且高颜值，前提是会配置
keywords: "IDE, VSCode"
---

如果你还没下载 VSCode 的话请
{% btn 'https://code.visualstudio.com/', 此处进入 VSCode 官网下载VSCode,far fa-hand-point-right,blue larger %}

{% note pink 'fas fa-laptop-code' simple %}

VSCode 的灵魂当然就是众多的功能强大的插件了，下面我会介绍一些常用的插件以供参考

{% endnote %}

# 美化

{% note blue 'fas fa-bullhorn' simple %}
众所周知，**编程的技术水平和编辑器的颜值成正比**
{% endnote %}

此处是我美化的结果

![VSCode美化效果](https://cdn.jsdelivr.net/gh/AmamiyaRenn/cloudimg@master/VSCode_Beautify.png)

{% tabs Beautify %}

<!-- tab 中文用户界面 @fas fa-image -->

一键汉化请装`Chinese (Simplified) (简体中文) Language Pack`

<!-- endtab -->

<!-- tab 编辑器主题 @fas fa-language" -->

推荐一款美观同时对背景图友好的主题——`One Dark Pro`
安装完成后按`F1`输入`theme`调整颜色主题为`One Dark Pro Darker`，并在插件的拓展设置中把勾都打上

<!-- endtab -->

<!-- tab 背景图 @fas fa-atom -->

背景图插件我只推荐`backgound-cover`
{% note red 'fa-solid fa-circle-exclamation' simple %}
如果插件配置好后却没有显示，而且也没出现`code 已经损坏`的提示，说明你没有用管理员身份打开 VSCode。
对于{% label Windows blue %}用户，请执行`Visual Studio Code图标 -> 鼠标右键 -> 属性 -> 兼容性 -> 以管理员身份运行此程序打勾`
对于{% label Linux orange %}，请在终端键入`sudo chown -R $(whoami) /usr/share/code`
想要消除`code 已经损坏`的提示，可以安装`Fix VSCode Checksums`插件，或者直接对该提示执行`不再显示`
{% endnote %}

<!-- endtab -->

<!-- tab 文件图标 @fas fa-icons -->

简约美观的图标——`vscode-icons`

<!-- endtab -->

<!-- tab 代码括号 @fas fa-chevron-left-->

括号全白，看的头大，能不能拯救一下？
能！只需要安装`Bracket Pair Colorizer 2`，即可享受花花绿绿的括号

<!-- endtab -->

<!-- tab 输入时粒子效果 @fas fa-bolt-->

`Power Mode`的配置与效果请看
{% btn 'https://blog.csdn.net/muzilanlan/article/details/81509374', 写代码的时候体验狂拽酷炫的效果, far fa-hand-point-right,blue purple %}

<!-- endtab -->

{% endtabs %}

---

# Markdown

VSCode 的正确运用方式是：写 `Markdown`！
那怎么才能有丝滑的`Markdown`体验呢，请参考下方链接进行配置
{% btn 'https://zhuanlan.zhihu.com/p/442554652', 再见 Typora！5 分钟从 Typora 迁移到 VScode！,far fa-hand-point-right,blue larger %}
配置好后该怎么写`Markdown`文档呢，请参考这一篇
{% btn 'https://zhuanlan.zhihu.com/p/149479119', Markdown学习向整理,far fa-hand-point-right,blue larger %}
同时我推荐{%label Markmap green%}这个插件，它可以从你的 markdown 文件自动生成对应思维导图形式的预览
更多的操作可以参考
{% btn 'https://zhuanlan.zhihu.com/p/496083303', 第 6 期、写作：基于 VS Code 的 Markdown 写作技术栈,far fa-hand-point-right,blue larger %}

---

# 程序语言

{% note blue 'fas fa-bullhorn' simple %}
众所周知，**没装程序语言插件支持的 VSCode 和记事本没区别**
{% endnote %}

{% tabs ProgramingLanguage %}

<!-- tab C/C++ @fa-solid fa-c -->

C/C++ 插件请安装`C/C++ Extension Pack`

<!-- endtab -->

<!-- tab Python @fab fa-python -->

Python 插件请安装`Python`和`autoDocstring`

<!-- endtab -->

<!-- tab Matlab -->

Matlab 插件请安装`Matlab Extension Pack`

<!-- endtab -->

{% endtabs %}

---

# 提高生产力！

{% note blue 'fa-regular fa-circle-question' simple %}
代码{% label 写的慢 red %}，代码{% label 写不爽 red %}，代码自己写了{% label 自己都不想看 red %}怎么办？
**好消息！好消息！这是有救的！**，只需要安装如下插件，即可大大加强 VSCode 的生产力
{% endnote %}

{% tabs CodeProductivity %}

<!-- tab git @fa-brands fa-git-alt -->

git 插件请安装`Git Extension Pack`
有人会问：{%label git我不会用怎么办😫 red%}
其实可以去学一学，不是特别难
如果有空的话我更新这一篇文章或者开一篇新文章，专门讲一讲 git 的基本操作和怎么在 VSCode 中愉快的使用 git

<!-- endtab -->

<!-- tab Header @fas fa-marker -->

`KoroFileHeader`可以一键生成头部注释和函数注释，不过需要做一定的配置
{% btn 'https://blog.csdn.net/zhumizhumi/article/details/91446572', VSCode 自动生成文件头部注释和函数注释, far fa-hand-point-right,blue purple %}

<!-- endtab -->

<!-- tab 文档格式化 @fa-solid fa-bars-staggered-->

文档一键格式化可以使用`Prettier`
但是这个插件不是对所有的语言都支持，事实上，支持的还蛮少的
对于`Python`，可以参考这个文章
{% btn 'https://blog.csdn.net/Pythonlaowan/article/details/99205649', 10分钟教你用YAPF让Python代码瞬间从丑陋变漂亮, far fa-hand-point-right,blue purple %}

<!-- endtab -->

<!-- tab 路径提示 @fa-brands fa-stackpath-->

`Path Intellisense`可以在键入路径时自动提供提示

<!-- endtab -->

<!-- tab 代码自动补全 @fa-solid fa-brain -->

代码中总是有一堆重复，比如变量重复，代码行重复，甚至是代码块重复，能不能让 AI 帮我们忙呢？
这是可以的，只需要安装`Tabnine`即可享受
{% note purple 'fa-solid fa-plus' simple %}

关于代码自动补全，目前出了一个还在内测的用嘴自动写代码工具`Github Copilot`可以关注一下

{% endnote %}

<!-- endtab -->

<!-- tab Todo Tree @fa-regular fa-circle-check-->

`Todo Tree`可以在 VSCode 左侧栏提供一个以树形结构显示 Todo 的图标

<!-- endtab -->

{% endtabs %}

{% note red 'fa-solid fa-face-frown' simple %}

有人会问，明明我已经用了这些插件为什么还会出现如上问题？
我的评价是：{%label 先提高代码水平吧😋 pink%}

{% endnote %}
