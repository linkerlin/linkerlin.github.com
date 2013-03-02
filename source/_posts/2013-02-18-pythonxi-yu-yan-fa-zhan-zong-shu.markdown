---
layout: post
title: "Python系语言发展综述"
date: 2013-02-18 13:53
comments: true
categories: Python
---
Python系语言经过多年的发展，衍生出多个版本。其中：

#### CPython 
也就是通常说的Python。这个版本在3.x系列发展的时候遇到困难，由于设计上的失误，很多开源组件还是坚持在2.5+版本。这种情况，在3.x系列不发生巨大改变的情况下，不会改变。

#### Cython 
由于人工智能和数学的需要，更快的数值计算需求催生了Cython。Cython的优势：代码可以从Python转换到C/CPP，从而保护了源码并且提高了CPU密集性的计算的性能。

#### PyPy 
从欧盟拿了不少资助，发展的很好。RPython是其核心的简化的Python方言。性能提升来自JIT编译器。但是，PyPy在兼容性上做不到Cython那样的无缝融合到标准CPython环境。从而，很少有人使用，基本是玩具。

#### mypy 
一个刚起步的方言，画了一个很大的饼。

#### shedskin 
一个务实的Python到C++编译器，不能100%兼容，但是可以独立运行。同样是玩具。

#### Jython 
兼容度极高，但是面向Java环境，不适合需要使用C扩展的情况。

#### IronPython 
微软系的东西，不解释。 