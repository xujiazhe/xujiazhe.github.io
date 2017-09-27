---
layout: post
title:  "springboot java web开发工程师效率"
date:   2017-09-27 17:08:41 +0800
categories: work
tags: work
---



### 基础好工具

	idea
	iterm2 和 oh-my-zsh
	git



### 热加载

java web项目每次重启时间成本太大.
编程有一个过程很重要, 就是试验, 在一次次试验中探索, 积累素材优化调整程序模型.

单元热加载
   改动文件后, 编译该单元 -> **可能** 会触发热加载该模块.  (  build -> Recompile '.....java'   )

 + ##### idea IDE支持

   - Run

     ​	没有编译后reload功能

   - Debug

     ​	reload the recompile的class. 最好用



 + ##### 引入SpringBoot Devtools

     - Run
       ​编译一次 自动组装加载一次. 慢.
     - Debug
       ​idea 提示加载, 程序自动加载.
```XML
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-devtools</artifactId>
    <optional>true</optional>
</dependency>
```
​       相关文档   [devtools](https://docs.spring.io/spring-boot/docs/current/reference/html/using-boot-devtools.html);  [hot swap 83](https://docs.spring.io/spring-boot/docs/current/reference/html/howto-hotswapping.html);  [hot swap 84](https://docs.spring.io/spring-boot/docs/current-SNAPSHOT/reference/)


 + ##### JRebel IDE插件

     - JRebel Run 该应用    
         ​	重编该单元, 自动加载
       - JRebel debug 方式启动该应用
         ​	JRebel自动加载, idea也提示加载.




### Code Review 工具 upsource

upsource 是 jetbrains 公司出的一个CR 工具, upsource 支持zip和docker安装.

- 安装docker     macos安装docker [教程](https://yeasy.gitbooks.io/docker_practice/content/install/mac.html); centos安装docker 教程就在上面;

- docker安装upsource    docker pull jetbrains/upsource:[2017.2.2307](https://hub.docker.com/r/jetbrains/upsource/tags/)  找最新版本哦.  [其他仓库的结果](https://store.docker.com/search?q=upsource&source=community&type=image) : [结果1](https://store.docker.com/community/images/esycat/upsource) ; [结果2](https://store.docker.com/community/images/jetbrains/upsource)

- 启动步骤, [官网](https://www.jetbrains.com/help/upsource/docker-installation.html); [文档2](https://hub.docker.com/r/jetbrains/upsource/)

- idea IDE可以安装upsource插件看到 comment.

  gitlab 也可以review. gitlab web页面 摁下 ? , 弹出页面快捷键提示窗.




### 调试

​    断点条件

​    断点提前返回

​    回帧重入

​    Drop Frame	这个不是一个快捷键，而是一个 Debug 面板上的按钮。该按钮可以用来退回到当前停住的断点的上一层方法上，可以让过掉的断点重新来过




