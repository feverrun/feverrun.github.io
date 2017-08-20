---
layout: title
title: travis 使用Travis自动化构建
date: 2017-07-19 22:41:43
tags:
	- travis
---

## 简介
持续集成：Continuous Integration,简称，CI，意思是在一个项目中，任何人对代码的修改，都会触发CI服务器自动对项目进行构建，自动运行测试，好处是随时发现问题。

## Travis CI 是什么？
Travis CI 是在线托管CI的服务，用Travis进行持续集成，不要自己搭建服务器。

## GitHub
Github 和 Travis CI 紧密相连

## 怎么用？
 1. 用github,登录Travis CI的网站 [Travis CI](https://travis-ci.org/)授权
 2. 选择代码库
 3. 对应github项目中,.travis.yml 文件的创建

## 使用感受
1. 在github中创建项目，我push本地的文件到github对应项目中，Travis CI察觉到我的项目的文件变了，立马开始构建， 感觉挺智能的。
2. 对git 的基本用法有了基本的认识
3. hexo 不推荐使用 travis，集成慢而且所有的东西都暴露了，不推荐，不如本地环境来的更快速，更实在。


 

