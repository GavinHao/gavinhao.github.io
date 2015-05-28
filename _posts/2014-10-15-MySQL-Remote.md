---
layout: post
title: "MySQL远程访问"
description: "MySQL远程访问"
category: MySQL
tags: MySQL
---
{% include JB/setup %}

# MySQL远程访问

在`MySQL`默认配置中是无法通过远程地址来访问的。今天遇到了这个问题在此记录下。

登陆`MySQL`:
	
	mysql -u root -p
	
执行一下语句:
	
	GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY 'passwd' WITH GRANT OPTION;
	
即可通过任意的远程地址和`root`用户来访问数据库了。

