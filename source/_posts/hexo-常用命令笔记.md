---
title: hexo 命令笔记
date: 2017-02-23 16:38:56
tags: [学习笔记,hexo]
---

<font style="color: rgb(172,168,167)">题外话：积累了很久的。一直没写，没push。太懒了TAT</font>
### 服务器

hexo server  #启动服务预览 Hexo 会监视文件变动并自动更新
hexo server -s  #静态模式
hexo server -p 5000  #更改端口
hexo server -i 192.168.1.1  #自定义 IP

### 文章相关
<!--more-->

hexo n "我的博客" == hexo new "我的博客" #新建文章
hexo p == hexo publish
hexo g == hexo generate #生成静态文件
hexo d == hexo deploy #部署

hexo c ==hexo clean  #清除缓存

### 监视文件变动

hexo generate --watch #监视文件变动

参考文献： [hexo常用命令笔记](https://segmentfault.com/a/1190000002632530)

<!--more-->