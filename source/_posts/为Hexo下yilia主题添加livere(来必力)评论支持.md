---
layout: t
title: 为Hexo下yilia主题添加livere(来必力)评论支持
date: 2017-07-15 11:51:00
tags:
	- yilia
toc: true
---
在使用yilia主题后，想添加评论功能，然而主题自带的第三方评论对我来说都用不了，多说关了，网易云跟帖也关了，畅言必须进行域名备案，github page使用不了。在这种情况下，只能使用下livere。	
## 注册 livere
livere 有两个版本：

- City 版： 是一款适合所有人使用的免费版本

- Premium 版：是一款能够帮助企业实现自动化管理的多功能收费版本

## 添加livere插件
首先在yilia主题的 _config.yml 文件中添加如下配置：

``` 	
livere: true
```
<!--more-->
然后\layout_partial\post目录下添加livere.ejs，把livere安装代码复制进去，文件内容如下，其中data-uid就是你自己的data-uid。

```
<!-- 来必力City版安装代码 -->
<div id="lv-container" data-id="city" data-uid="your data-uid">
<script type="text/javascript">
	(function(d, s) {
     var j, e = d.getElementsByTagName(s)[0];
     if (typeof LivereTower === 'function') { return; }
     j = d.createElement(s);
     j.src = 'https://cdn-city.livere.com/js/embed.dist.js';
     j.async = true;
     e.parentNode.insertBefore(j, e);
 })(document, 'script');
</script>
<noscript>为正常使用来必力评论功能请激活JavaScript</noscript>
</div>
<!-- City版安装代码已完成 -->
```

最后在layout_partial\article.ejs中<% if (!index && post.comments){ %>后面添加如下代码：

```
<% if (theme.livere){ %>
<%- partial('post/livere', {
    key: post.slug,
    title: post.title,
    url: config.url+url_for(post.path)
  }) %>
<% } %>
```

至此，为yilia主题添加livere评论插件完成。




