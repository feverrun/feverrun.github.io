---
layout: title
title: 域名www与不带www的区别
date: 2017-07-18 22:41:43
tags:
	- domain
---


## 遇到问题 
访问feverrun.top 可以正常访问
访问www.feverrun.top 无法正常访问


## 郁闷中
这是为什么呢？几秒钟。。。


## 简单认识域名
  www.feverrun.top，aaa.feverrun.top，bbb.feverrun.top 
  同为feverrun.top 这个域名的二级域名
  feverrun.top 这个域名为根域名

<!-- more -->

## 解决方法
1. 我们从域名服务商提供的后台域名解析那里设置域名解析，需要分别解析@和www(@是根，www是子)
2. 最好用301重定向，访问www.feverrun.top 转向 feverrun.top


## 小结
 1. 我只在乎，主要解决有无www,照样访问网站的问题，目的达到。
 
 2. 1中的方法，可行分开解析，搜索引擎抓取网页的时候，会把这两个地址，分别解析，会影响SEO,可做301

 3. 这里不做深究
 

