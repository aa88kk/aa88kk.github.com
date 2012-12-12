---
layout: post
title: "在MacVim上安装taglist插件"
date: 2012-12-05 17:21
comments: true
categories: vim, macos
---

taglist几乎是程序员必备的vim插件，在macos上安装taglist时，很可能会因为命令冲突而导致安装失败。

在macvim中使用taglist插件时,如果出现错误：

    Taglist: Failed to generate tags for /Users/liujie/Documents/nodetest/server/server.js
    ctags: illegal option -- -^@usage: ctags [-BFadtuwvx] [-f tagsfile] file ...^@

则说明ctags命令冲突。taglist使用的是Exuberant ctags, 和系统所带的ctags(/usr/bin/ctags)不是同一个程序. 假定Exuberant Ctags安装在/usr/local/bin目录下，要在vimrc文件中增加配置：

    Tlist_Ctags_Cmd = “/usr/local/bin/ctags”
