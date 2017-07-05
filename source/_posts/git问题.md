---
title: git问题
date: 2017-07-05 16:38:18
tags: [学习笔记,git]
---

### 问题描述1

<font style="color: rgb(172,168,167)">前很久的时候，上个月？？？给项目建了个仓库，方便我实验室电脑和自己电脑同步，然后遇到了一些问题（以前也这样过），所以mark下，提醒自己</font>

<code>$ git push origin master
The authenticity of host 'git.coding.net (XXX)' can't be established.
RSA key fingerprint is SHA256:jok3FH7q5LJ6qvE7iPNehBgXRw51ErE77S0Dn+Vg/Ik.
Are you sure you want to continue connecting (yes/no)? </code>

直接输入yes 就行
<!--more-->
[参考](https://coding.net/help/doc/git/ssh-key.html)


### 问题描述2

<code>! [rejected] master -> master (fetch first)
error: failed to push some refs to 'git@git.coding.net:xxx'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.</code>


原因是没有同步远程仓库
git pull origin master
同步一下

一般来说是成功的。但是我的报错了。原因是，我是两个不同的仓库。

<code>$ git pull origin master
From git.coding.net:xxx
 * branch master -> FETCH_HEAD
fatal: refusing to merge unrelated histories</code>

先前那句话后添加参数就可以了

git pull origin master --allow-unrelated-histories
搞定。

