---
layout: post
title: "Jython设置默认编码"
date: 2013-02-18 13:51
comments: true
categories: Jython
---
Jython项目对非ascii编码的支持不是很好，尤其是在windows环境。

但是需要用Jython做一些和Java配合的工作，又必须要能够在Windows环境工作。经过一番研究终于发现两个可行的方法。

在Win7命令行直接运行Jython 2.7a2是不行的，因为Jython默认是ascii编码，而Win7默认是GBK编码，更加悲剧的是JVM又不支持在Console使用GBK.

一个简单的解决方法：

	1	jython -C "utf-8"
看看默认编码：

	1	>>> import sys
	2	>>> sys.defaultencoding
	3	'ascii'
注意虽然系统默认编码还是ascii，但是已经可以正常的使用Shell了。因为JVM的默认编码已经改过了来了。

然后再执行下面这段代码：
	
	1	from org.python.core import codecs
	2	codecs.setDefaultEncoding('utf-8')

或者：
	
	1	import sys
	2	reload(sys)
	3	sys.setdefaultencoding('utf-8')

再检查下Jython的默认编码：

	1	>>> sys.defaultencoding
	2	'utf-8'
搞定。 