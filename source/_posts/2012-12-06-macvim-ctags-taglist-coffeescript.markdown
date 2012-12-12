---
layout: post
title: "让taglist支持coffee sctript"
date: 2012-12-06 14:23
comments: true
categories: vim,coffeescript
---


由于tags原生程序并不支持CoffeeScript，需要先进行配置.

1.生成并编辑~/.ctags文件，增加内容如下

    --langdef=CoffeeScript
    --langmap=CoffeeScript:.coffee
    --regex-CoffeeScript=/(^|=[ \t])*class ([A-Za-z]+\.)*([A-Za-z]+)( extends [A-Za-z.]+)?$/\3/c,class/
    --regex-CoffeeScript=/^[ \t]*(module\.)?(exports\.)?@?([A-Za-z.]+)[ \t]*:.*[-=]>.*$/\3/m,method/
    --regex-CoffeeScript=/^[ \t]*(module\.)?(exports\.)?([A-Za-z.]+)[ \t]*=.*[-=]>.*$/\3/f,function/

2.编辑~/.vimrc，增加内容:
    
    let tlist_coffee_settings = 'CoffeeScript;c:class;m:method;f:function'



注:

    os  : Mac OS X
    vim : MacVim
    ctags : Exuberant ctags

