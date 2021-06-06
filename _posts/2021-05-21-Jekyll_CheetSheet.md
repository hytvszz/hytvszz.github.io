---
layout: post
title: "Jekyll CheetSheet (for github pages)"
date:   2021-05-21
tags: [IT]
language : English
comments: true
author: Zhen
toc: false
published: true
hidden: false
---
[中文官方文档点这里](http://jekyllcn.com/docs/templates/)
<!-- more -->

[CheetSheet点这里](https://gist.github.com/JJediny/a466eed62cee30ad45e2)

强行换行：在当前行结尾多加3个空格   
加入图片（1.后缀jpg或png不要写错；2.jpg或者png必须用小写）：    
`<p align="center"> <img src="{% raw %}{{ site.imageurl }}{% endraw %}/澳洲纪念币.jpg"> </p>`    
不让代码被渲染：mark他们为code   
不让双大括号被渲染：`{% raw %}{{ " {{ site.imageurl "}} }} {% endraw %}`或者
{%  assign  openTag  =  '{%'  %}  {%  raw  %} This is how you show the termination of the `{% raw %}` tag inside itself: {%  endraw  %}{{  openTag  }} endraw %}{%  raw  %} This content is back inside the {% raw %} block {%  endraw  %}



<!--stackedit_data:
eyJoaXN0b3J5IjpbMTM3NzcxMTc0NCw4NjQ4MDMwNTEsLTIwOT
U0NjU2Niw0MjQwMzE3NTQsMjA4MDM4NDk1NywxNzI2NDUwNTA1
LDE5NDE2NjYzNTksLTMxODgyMDk4OSwtMTM1MzE4NDMzNSwxNT
c3NDE0NzkyLC0yMDM3MTYyNzI4LC0yMTMxOTgwMDE5LC0xMTc2
MjM2NTk2LC0yMTEyODU3NTYyLDMyMjg5NTk2OSwtNzIwODYzND
Q1LC05ODI5Njk3MTcsMTE0MDE5MDM5OCwtNzI5MzI4MzEzXX0=

-->