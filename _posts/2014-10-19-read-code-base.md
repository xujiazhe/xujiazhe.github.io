---
layout: post
title:  "阅读代码的技巧(翻译)"
date:   2014-10-19 17:08:41 +0800
categories: work learn
tags: work learn
---


[翻译链接][1] to be continued

提高编程技能的一个方法是阅读优秀的代码. 为了让代码更可读,发展出来了一些技术诸如 SelfDocumentingCode和LiterateProgramming 然而,我们大多数时候不得不阅读一些达不到上述标准的代码. 有什么最好的方式来了解这些巨大的，非结构化的，由一堆人维护的，内部不一致，无文档的,我们还必须理解和吸收的 代码库?

**编译并运行程序**

当我们从内部学习它的时候,把程序跑起来,观察它的外部状态是有用的. 软件文档是有用的,但是不一定能准确描述程序的行为. 编译程序可以帮助你找到那些外部库被引用,那些编译链接选项是有效的等等.如果你能编出来一个调试版本的程序,你可以用调试器走进程序() 并且增加或者扩展软件的日志,来帮助你看到发生了什么.

**找到高层的逻辑**

从程序入口处开始(e.g. main() in C/C++/Java ), 找到程序是如何初始化,如何执行和退出的. 大多数的程序会有一个main循环,找到它(但是如果程序使用框架,main循环可能在那个框架里) 找到程序停止的条件,除了正常推出也包括不正常退出. 很多事件驱动的和面向对象设计的程序没有main,不过他们会有一些入口. (hint C++ 有些全局的类构造函数在main之前运行)

不一定总是这样,C64/C128平台的CEOS操作系统的软件被制定为为单一初始化路径. (在配置完自己的运行环境后,返回操作系统),然后不同的事件触发一系列callback. 从某种意义上说,GEOS应用就是叠加到了操作系统上去了. Indeed, any true event-driven style of programming closely, if not exactly, resembles this. What is the "main method" of a class? The constructor rarely is the most important method. By extension, an event driven program's initializer is rarely its most important callback.

画流程图 是的,我们都知道流程图是一种可怕的设计工具，但在分析程序流时他们可以是有用的。你不能记住所有的信息，那么在读代码时画一些流程图或状态图。不要遗漏分支.

**检查库调用**

如果应用程序调用了的外部库，检查库调用并请阅读这些函数的文档。（这可能是唯一你有的文档，所以好好利用它吧.)

**查找关键字**

使用您的编辑器的查找功能（或 grep） 在源码树中搜索你关心的关键词。例如，如果您想要找出如何及在何处该程序打开文件，搜索"open"或"file"。你可能会得到大量的结果，但这不是一件坏事 — — 挑重点的阅读也行。 对于 C/C++ 程序通常有用词是 "main", "abort", "exit", "catch", "throw", "fopen", "creat", "signal", "alarm", "socket", "fork", "select".

**利用代码理解工具**

一个出色的文本搜索工具提供一些功能，或还有一些更好的工具,可以分析源代码和查找引用，并生成图表，可以为为面向对象的代码解答下面的问题：

>此方法的调用者？
谁实现此接口或谁是这类的子类？
此类的超类是什么？
此类的实例哪里被创建、或作为参数传递或返回的？
此类重写超类的什么方法？
在此类的方法在哪里被多态的调用,即通过基类或接口？
引用 [理解和可视化的面向对象的代码][2] 第 5 节.

**打印代码**

Monitors can rarely beat the sheer textual capacity of an empty table on which a printout of the source code has been laid. You can see, at a glance, kilobytes of code. This aids tremendously in developing a "big picture" view of the code. 显示器很少能打败空表的纯粹文字能力，奠定了源代码的打印输出。你可以看一眼，看到千字节的代码。这极大地艾滋病在发展"大图"视图的代码。

**写单元测试**

它能证明你已经理解了这个代码要应该做什么,实际做了什么,并且你已经了解到它的局限性. 如果事先没有单元测试,在修改代码之前,你一定要加上一组单元测试.

**注释代码**

待续


  [1]: http://c2.com/cgi/wiki?TipsForReadingCode
  [2]: http://www.strath.ac.uk/science/computerinformationsciences/#EFoCS-33-98