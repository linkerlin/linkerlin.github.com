---
layout: post
title: "Jython动态加载Jar"
date: 2013-02-18 13:49
comments: true
categories: Jython
---
 用Jython做单元测试Java项目的时候，需要能动态的从Jar包里load类。

以下是一个简单的方法：

	import sys
	sys.path+=["./extlibs/servlet-api-2.5.jar"]
	from javax.servlet.http import *
第二行是关键，只要你能找到Jar的位置，就不愁加载不起来哈。 