---
layout: post
title: "Jython加载Jar给JavaCode用"
date: 2013-02-18 13:48
comments: true
categories: Jython
---
上篇提到的把jar加入到Jython的sys.path里，只能解决Jython使用jar的问题。如果是Java代码要用Jar,例如使用Class.forName(xxxxx)，上述方法就不行了。

解决的方法是使用

  https://gist.github.com/4661588

  https://gist.github.com/4654376

里的方法. 