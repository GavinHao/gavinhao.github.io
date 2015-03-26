---
layout: post
title: "利用JekyllBootstrap快速搭建基于Github的博客"
description: "利用jekyllBootstrap快速搭建Github的博客"
category: 博客
tags: [博客,Github]
---
{% include JB/setup %}

# 所需环境

1. ruby
2. jekyll
3. Git
4. Github帐号

这部分内容google有很多解决方案，我就不一一赘述了。安装好这几个软件和一个Github帐号就可搭建自己的博客了。

# 快速创建

首先需要在Github上建立和你自己的用户名同名的仓库：`username.github.io`,然后在本地切换到你自己的工作目录。通过在命令行运行这几行命令：

    git clone https://github.com/plusjade/jekyllbootstrap username.github.io
	cd username.github.io
	git remote set-url origin http://github.com/username/username.github.io 
	#username全部替换为你自己的用户名
	git add .
	git commit -m "create the blog"
	git push origin master

十分钟后访问`username.github.io`就可直接看到你的最基本的博客了。

#定制博客
通过修改_config.yml:
	
	title : 你的博客名称
	author :
  		name : 你的名字
  		email : 你的邮箱
  		github : 你的github

jekyllbootstrap已经为你配置好分类、归档、标签以及disqus的功能，当然disqus需要自己配置`_config.yml`中的comments部分，更改short\_name为你自己的short\_name。

当然你也可在jekyll官网上查看文档，进行更进一步的配置，自定义。

#第一篇博客

在目录`_posts/`下通过`year-month-day-name.md`的名字创建文章后，在文章头部添加以下格式的代码：

	---
	layout: post
	title: "利用JekyllBootstrap快速搭建基于Github的博客"
	description: "利用jekyllBootstrap快速搭建Github的博客"
	category: 博客
	tags: [博客,Github]
	---
	{% include JB/setup %}

推送到Github中：

	git add .
	git commint -m "post my first blog"
	git push origin master

过会就可在username.github.io中看到你的第一篇博客了。