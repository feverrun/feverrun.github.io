---
layout: t
title: Next下添加Algolia搜索遇到的坑
date: 2017-07-15 11:51:00
tags:
	- next
categories: next
---

## 当前环境
    hexo 3.3.8
    next 5.1.2
## 官网已集成algolia搜索
实现方法如下
**下面这个要注意：**
在站点配置文件加入如下代码:
```    
	algolia:
	  applicationID: 'applicationID'
	  apiKey: 'apiKey'
	  adminApiKey: 'adminApiKey'
	  indexName: 'indexName'
	  chunkSize: 5000
```
<!-- more -->
## hexo algolia 报错
1. 站点配置文件algolia那里，缺少对fields的配置
2. 站点配置文件appID 那里,配置名称有误

## 最终站点配置文件修改如下：
```
algolia:
  appId: 'applicationID'
  applicationID: 'applicationID'
  apiKey: 'apiKey'
  adminApiKey: 'adminApiKey'
  indexName: 'indexName'
  chunkSize: 5000
  fields:
     - title
     - slug
     - path
     - content:strip
```
## 最终主题配置文件修改如下
```
algolia_search:
  enable: true
  hits:
    per_page: 10
  labels:
    input_placeholder: "输入关键字"
    hits_empty: "没有找到与 ${query} 相关的内容"
    hits_stats: "${hits}条相关记录, 共耗时 ${time} ms"
```

## 就此问题得到解决
>这里的集成，我是被坑了一次