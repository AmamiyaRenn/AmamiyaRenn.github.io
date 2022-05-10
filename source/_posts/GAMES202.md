---
title: GAMES202
tags:
  - 图形学
  - GAMES202
categories:
  - 图形学
  - GAMES202
description: GAMES202一些笔记与踩坑
keywords: "图形学, GAMES202"
abbrlink: 40691
date: 2022-05-09 09:48:19
cover: https://cdn.jsdelivr.net/gh/AmamiyaRenn/cloudimg@master/SAO5.jpg
---

# 踩坑

1. 模型渲染不出来
   1. git clone three.js
   2. 把 homework 中的 MTLLoader、OBJLoader、OribitControls 用上面下载的文件进行替代
   3. 把下载的源码中的 three.min.js 放入 lib
   4. 修改 index.html 中`<script src="lib/three.js" defer></script>`
      1. 改为`<script src="lib/three.min.js" defer></script>`

# 重难点

## ShadowMap

1. 硬阴影
   1. 渲染步骤
      1. 以光源视角渲染场景
         1. 生成 z-buffer，命名为 shadowMap
      2. 以相机视角渲染场景
         1. 对于任意一个 fragment（此处简单理解为像素），通过它的世界坐标和光源视角的 MVP 矩阵，可以算出光源视角下的对应的深度 d(shadowMCoord.z)与 z-buffer 的对应 UV 值（shadowCoord.xy）
         2. 通过 shadowCoord.xy 查询对应的 shadowMap 上的深度 s
         3. 如果 d<=s，则可被光源看见，从而不在阴影中
