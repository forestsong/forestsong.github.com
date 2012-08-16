---
layout: post
title: "Progress and Issues with jekyll"
description: ""
category: 
tags: []
---
{% include JB/setup %}

##进展

删掉了之前不能删除的post

**解决方法**

1. 删掉本地repo的working directory
2. 用github的客户端把remote的repo clone到本地 forestsong.github.com目录
3. 重新使用如下命令删除需要删除的文件
	
	git -rm ./_posts/filename.md
	


##问题
1. 用如下命令可以创建中文title的blog，但是只能一天创建一个中文post，因为默认的文件名都一样
	
	rake post title="中文标题的blog"
	
	和
	
	rake post title=“测试一下”
	
	生成的post文件名都一样，所以会产生如下提示
	
	
	./_posts/2012-08-16-.md already exists. Do you want to overwrite? yn y
	
2. 勉强创建的中文post，又无法删除，提示如下（update，应该是没有提交，所以remote repo上其实根本没有这个文件）

	fatal: pathspec '_posts/2012-08-16-1.md' did not match any files
	
3. 可以用如下方法删除这些文件

	rm 2012-08-16-1.md 
	
	