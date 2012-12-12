---
layout: post
title: "如何将github上的octopress更新到本地"
date: 2012-12-03 15:58
comments: true
categories: zsh,octopress,git,github
---

octopress网站文档里只是描述如何从零开始创建发布，但有时候我们需要从github上更新到另外一台机器，而不是重新安装.

    git clone -b source git@github.com:aa88kk/aa88kk.github.com.git ./octopress
    cd octopress
    git clone git@github.com:aa88kk/aa88kk.github.com.git ./_deploy

其实就记住2点，source分支对应octopress目录.master分支，对应octopress下的_deploy目录,就可以随便用git操作了.
