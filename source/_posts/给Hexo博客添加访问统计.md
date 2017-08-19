---
title: 给Hexo博客添加访问统计
date: 2017-07-30 21:45:03
tags: [转载,学习笔记]
---

---
<font style="color: rgb(172,168,167)">注：转载请注明出处以及作者，违者必究。</font>

给博客新添加了访问统计，引入了不蒜子，参考原文[给Hexo博客添加访问统计](http://www.jianshu.com/p/8a8f880f40c0)。但是我发现了一个问题，博客显示的第一篇文章，在没有点进去的时候，阅读量会随着刷新次数增加，不知道算不算 bug。
下面是我从原文 copy 过来的：
### 1. 引入[不蒜子](http://busuanzi.ibruce.info/)

```html
<script async src="//dn-lbstatics.qbox.me/busuanzi/2.3/busuanzi.pure.mini.js"></script>
```
这段代码可以写在 footer.ejs 里或者 header.ejs 里或者 layout.ejs 里。
### 2. 添加站点访问量
<!-- more -->
通常站点的总访问量会显示在 footer 的位置，所以我们可以在 footer.ejs 里加上如下标签： 

```html
<span id="busuanzi_container_site_uv"> 
  本站访客数<span id="busuanzi_value_site_uv"></span>人次
</span>
```
计算访问量的方法有两种：
算法 a：pv 的方式，单个用户连续点击 n 篇文章，记录 n 次访问量。
算法 b：uv 的方式，单个用户连续点击 n 篇文章，只记录 1 次访客数。
我用的是 uv 的方式，大家自行选择即可。
### 3. 添加文章访问量

文章的访问量显示在文章里面，所以在 article.ejs 里加上文章访问量的标签：

```html
<span id="busuanzi_container_page_pv">
   本文总阅读量<span id="busuanzi_value_page_pv"></span>次
</span>
```
这个标签里的汉字可以自行修改，还可以给标签写上你想要的样式。

参考：[不蒜子|不如](http://ibruce.info/2015/04/04/busuanzi/)

### 4. 总结

1-3 都是原文摘抄啦。在实际里我还修改了一些样式。大概就是这样了。感觉不蒜子很好用啊～（除了那个 bug ）。