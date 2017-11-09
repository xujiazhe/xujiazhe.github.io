---
layout: post
title:  "Spring Boot官方文档 41.测试"
date:    2019-05-25 0:16 +0800
published: false
categories: Tech
tags: Tech Java Test
---

### 41. 测试  

Spring Boot为应用测试 提供了一些工具和注解. 有两个模块提供测试支持;spring-boot-test包含核心部件, spring-boot-test-autoconfigure 为测试提供auto-configuration支持.  
多数开发者使用 spring-boot-starter-test 启动模板, 其包含那两个测试模块和其他有用的库(JUnit, Assert, Hamcrest等)  

#### 14.1 测试依赖(Test scope dependencies)  

如果你使用那个测试 启动模板, 你会发现这些库.  
JUnit, Java程序测试的实际标准库.  
Spring Test & Spring Boot Test, SpringBoot程序的工具箱和集成测试.  
AssertJ, 一个好用的断言库.  
Hamcrest, 一个匹配器对象包(也可以说是约束和谓词)  
Mockito, Java Mock框架  
JSONassert, 一个JSON断言库  
JsonPath, JSON的XPath库  

Spring Boot默认使用Mockito1.x版本. 如果你想用2.x版本也是可以的.  
我们在写测试的时候我们平时发现好用的库. 如果你觉得这些不符合你的需求,你可以添加额外的依赖.  

#### 41.2 测试Spring应用  

依赖注入的一大好处就是让你的代码单元测试变得简单. 你可以直接用new初始化一些对象,甚至不用涉及Spring. 你可以使用mock对象而不是实际的依赖.  
你常常超出"单元测试", 开始"继承测试",(这个过程中常用到Spring的ApplicationContext). 不用部署或者连接其他的基础设施 就可以开始集成测试.  
Spring Framework有一个专用的测试模块用来集成测试. 你可以声明一个对org.springframework:spring-test, 或者用spring-boot-starter-test 启动模板来包含它.  
如果你以前没有用过spring-test模块, 你可以从阅读Spring Boot的相关参考文档开始.

#### 41.3 测试Spring Boot应用  

一个Spring Boot应用就是一个Spring ApplicationContext, 所以测试它 和你平时用vanilla Spring context做的没什么两样. 有一个需要注意的就是外部属性, 日志和其他的仅在SpringApplication创建的时候安装到context中的功能.  

Spring Boot提供的注解@SpringBootTest 和 spring-test的注解@ContextConfiguration 一样, 为你提供Spring Boot功能.这些注解的功能是通过创建在你测试中使用的ApplicationContext通过SpringApplication.  
你可以使用@SpringBootTest的webEnvironment属性来深度定制你的tests运行.  

MOCK --- 加载一个WebApplicationContext并提供mock的servlet环境. 当用这个注解的时候, 嵌入的servlet容器不会启动. 如果servlet APIs在类目录里没找到, 这个模式会会退到创建一个常规的non-web ApplicationContext. Can be used in conjunction with @AutoConfigureMockMvc for MockMvc-based testing of your application.


