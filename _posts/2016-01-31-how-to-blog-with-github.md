---
layout: post
title: 2016-01-31 - 怎么利用Github搭建个人博客
date: 2016-01-31
categories: blog
tags: [github,博客,jekyll]
description: 用Github + Jekyll搭建个人博客
---

##说明
Github Pages有以下几个优点：

* 轻量级的博客系统，没有麻烦的配置
* 使用标记语言，比如Markdown
* 无需自己搭建服务器
* 根据Github的限制，对应的每个站有300MB空间
* 可以绑定自己的域名

当然他也有缺点：

* 使用Jekyll模板系统，相当于静态页发布，适合博客，文档介绍等。
* 动态程序的部分相当局限，比如没有评论，不过还好我们有解决方案。
* 基于Git，很多东西需要动手，不像Wordpress有强大的后台

##步骤
总的来说，利用github搭建个人博客只需要三步:

1. 在github上建立一个名为xxx.github.io的库，这个xxx必须和你的账户名称一样
2. 将自己喜欢的jekyll喜欢的模板clone下来，并push到1步骤的库中，并修改下相应的配置
3. 绑定自己的个人域名，譬如`zuifeng.me`

##建立自己的xxx.github.io库
这里就略过了

##查找自己喜欢的jekyll模板
可以从这里找，[点我](https://github.com/jekyll/jekyll/wiki/Sites)

##绑定自己的域名
首先肯定的，需要自己购买一个域名，我反正是从阿里云万网购买的。

1. 购买域名，譬如 zuifeng.me
2. 在项目根目录下建立CNAME(注意是大写),内容为 zuifeng.me
3. 域名CNAME到xxx.github.io.(注意最后面还有一个点)，并A记录到`192.30.252.153`，这个ip可能会变，详情请[点击](https://help.github.com/articles/my-custom-domain-isn-t-working/)










