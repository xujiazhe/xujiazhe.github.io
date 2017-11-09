---
layout: post
title:  "macos 一些中文包"
date:   2017-11-01 17:08:41 +0800
categories: work
tags: work
---



## man page显示中文

```shell

# 1, 下载 编译 安装 man中文包

### git clone https://github.com/man-pages-zh/manpages-zh  #可以参与翻译, 多做贡献哦

wget  https://codeload.github.com/man-pages-zh/manpages-zh/zip/master -O manpages-zh-master.zip
unzip manpages-zh-master.zip && cd manpages-zh-master

brew install autoconf  automake  python3  opencc
autoreconf --install --force
./configure --disable-zhtw
make
sudo make install


# 2, 安装 排版 系统

brew install homebrew/dupes/groff
brew link homebrew/dupes/groff


# 修改配置

vim ~/.zshrc
  alias cman=’man -M /usr/local/share/man/zh_CN’

sudo vim /etc/man.conf
  # 搜索NROFF，替换为
    NROFF preconv -e utf8 | /usr/local/bin/groff -Wall -mtty-char -Tutf8 -mandoc -c
  # 搜索PAGER，替换为
    PAGER /usr/bin/less -isR
```

参考

    https://lamjack.github.io/2017/mac-install-chinese-man-doc/
    http://www.cnblogs.com/wujinhong/p/7251376.html
    https://github.com/man-pages-zh/manpages-zh



## vim帮助文档中文

```shell
https://github.com/yianwillis/vimcdoc
```



