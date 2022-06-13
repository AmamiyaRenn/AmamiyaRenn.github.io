---
title: C++的内存管理基础
tags:
  - C/C++
  - 技术笔记
abbrlink: 19090
date: 2022-05-25 21:14:57
categories:
  - 程序语言
  - C/C++
cover: https://cdn.jsdelivr.net/gh/AmamiyaRenn/cloudimg@master/p5_1.jpg
description: 最近写 C++主控代码时对 C++的内存管理方法产生了一些好奇，于是学习了一下其中的一些基础，特此记录
keywords:
  - 程序语言
  - C/C++
---

# 参考资料

{% btn 'https://cloud.tencent.com/developer/article/1062982', 从4行代码看右值引用,far fa-hand-point-right,blue larger %}
{% btn 'https://blog.csdn.net/qq_30272539/article/details/81390900', 函数返回值为引用左值和右值问题,far fa-hand-point-right,blue larger %}
{% btn 'https://aprilnavi.github.io/2021/04/26/c++(%E5%9F%BA%E7%A1%80%E9%83%A8%E5%88%86)/', c++(基础部分),far fa-hand-point-right,blue larger %}
{% btn 'https://aprilnavi.github.io/2021/05/06/c++(%E8%BF%9B%E9%98%B6%E9%83%A8%E5%88%86)/', c++(进阶部分),far fa-hand-point-right,blue larger %}
{% btn 'https://zhuanlan.zhihu.com/p/150555165', 现代 C++：一文读懂智能指针,far fa-hand-point-right,blue larger %}

# 指针

非严格的讲：
**内存地址**或叫**地址**，即某表达式或数据存在与计算机存储器中的位置，一个唯一的地址有一个唯一的地址数据如`0x2EF0`
**左值**(lvalue)即能对表达式取地址的值，例如`int i = 10`中的`i`。
**右值**(rvalue)即不能对表达式取地址的值，例如`10`,`"Hello World!"`,`0x2EF0`，非引用的函数返回值等；当右值出现时，计算机会先开一个对应类型的临时值，当该行码结束时计算机会把右值销毁
**指针**(pointer)即存储着被指对象的内存地址的左值
**赋值**(Assignment)定义完成以后再赋值（不管在定义的时候有没有赋值）即赋值
**初始化**(Initialization)即在定义的同时进行赋值；初始化只能有一次，赋值可以有多次

此处给出例子

```C++
int b = 10;
int* a = &b;
```

第一行通过一个右值`10`初始化了一个`int`类型的左值`b`
第二行通过一个取址符`&`完成了对左值`b`的取地址的操作，然后地址值作为右值被赋值给了`int*`（`int`类型指针）类型的左值`a`

考虑这行代码

```C++
*a = 5;
```

这行代码通过`*`规定`*a`即为`b`这个地址中的内容，所以这行代码把`5`赋值给了`b`
通过这行代码，`b`的内容被改为了`5`

# 引用

**引用**(reference)即对某表达式的别名
**左值引用**即对能被取地址的表达式的别名
**右值引用**即对不能被取地址的表达式的别名

{% note purple 'fa-solid fa-plus' simple %}

通过右值引用的声明，右值又“重获新生”，其生命周期与右值引用类型变量的生命周期一样长，只要该变量还活着，该右值临时量将会一直存活下去

{% endnote %}

---

未完待续
