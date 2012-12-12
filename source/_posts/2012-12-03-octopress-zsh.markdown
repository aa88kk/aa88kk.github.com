---
layout: post
title: "octopress 与 oh-my-zsh不兼容的问题"
date: 2012-12-03 16:35
comments: true
categories: zsh,octopress
---

octopress在zsh下使用rake new_post['...']命令操作时会报'no matchs found' 错误，可修改zsh环境配置，或在方括号前加上转义符,如下:

    rake new_post\['...'\]
