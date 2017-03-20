---
layout: post
title:  "该博客的搭建"
date:    2016-02-18 20:17 +0800
categories: tech
tags: tech
---

以前用pelican搭在github上过，跟着[这个](http://www.lizherui.com/pages/2013/08/17/build_blog.html)教程走的  
pelican是静态博客生成器，自己写的markdown博客，用博客程序pelican把内容转换为静态内容在网上查看(没有后台的动态功能)  
pelican可以转换，可以实时 查看本地 博客文件 编写效果  

后来在阿里云主机上搭建过wordpress并且还有其开发环境，比较麻烦点，后来主机不想续费了，给冲掉了，哎~ 自己的博客的稳定靠谱呀。  

再后来选择用[github pages](https://pages.github.com/)功能，外加官网推荐的jekyll搭建的博客  

---------------  
我搭的是windows，本地安装整理比较麻烦。别人的教程写的很好[windows下搭建教程](http://corey600.github.io/blog/2013/02/28/use-github-and-octopress-create-blog/)

还有一些有趣的[jekyll主题](http://jekyllthemes.org/)

官网上和中文教程都有，不用多说

### 我想xujiazhe.com 和 www.xujiazhe.com 都能访问我的博客

#### 1 配置dns服务器里面的这两条记录。

![这里][5]

#### 2 在CNAME文件里面写下下面的内容

www.xujiazhe.com  
xujiazhe.com


### 我想用jetbrains的IDE来写博客

#### 1  为markdown文件类型添加一个后缀 md
 ![这里][1]

#### 2 添加一个博文的模板，创建md的时候就自动模板了。名字叫 Markdown File


{% highlight PHP %}
---
layout: post
title:  "#[[$Title$]]#"
date:    ${YEAR}-${MONTH}-${DAY} ${TIME} +0800
categories: #[[$CATEGORIES$]]#
---
{% endhighlight %}

用的是Apache Velocity模板语言

![这里][2]

#### 3 新建文件的时候选择Markdown File
![这里][3]

#### 4 新建效果，idea还有个预览插件
![这里][4]  
　　  
　　  

-------------
markdown尾行两个空格是段内换行

[1]:{{ site.url }}/images/1.png
[2]:{{ site.url }}/images/2.png
[3]:{{ site.url }}/images/3.png
[4]:{{ site.url }}/images/4.png
[5]:{{ site.url }}/images/5.png


