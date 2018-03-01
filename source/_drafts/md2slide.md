categories: markdown
tags: slide reveal
title: 做一个简洁有力的slide
date: 2017/01/13 20:46:25
---

我觉得slide应该专注内容，而不是形式。后来发现有这么一种做slide的方式，我很是喜欢。


## 用markdown做slide
只需要用一行命令，就可以将你用markdown写成的内容转换成html格式的slide。

<!--more-->

## 工具

- markdown
- reveal.js
- pandoc

## 制作流程

- 用markdown编写slide内容；
- 用pandoc将markdown编写的文件转成html文件；命令如下
> pandoc -s --mathjax -i -t revealjs SLIDES -o example16d.html
- 将reveal.js文件夹与html文件放在同一个目录下。
- 用浏览器打开html文档即可演示slide。



## markdown转成slide的规则

目前并不确切知道，没有去看pandoc[源码](http://hackage.haskell.org/package/pandoc-1.19.1/docs/src/Text-Pandoc-Writers-HTML.html)。


## 工具获取
- pandoc
- reveal.js
