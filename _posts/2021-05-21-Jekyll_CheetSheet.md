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
不让双大括号被渲染：{% raw %}{{ site.imageurl }}{% endraw %} 或者 {{ "{{ site.imageurl "}} }} 


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIwOTU0NjU2Niw0MjQwMzE3NTQsMjA4MD
M4NDk1NywxNzI2NDUwNTA1LDE5NDE2NjYzNTksLTMxODgyMDk4
OSwtMTM1MzE4NDMzNSwxNTc3NDE0NzkyLC0yMDM3MTYyNzI4LC
0yMTMxOTgwMDE5LC0xMTc2MjM2NTk2LC0yMTEyODU3NTYyLDMy
Mjg5NTk2OSwtNzIwODYzNDQ1LC05ODI5Njk3MTcsMTE0MDE5MD
M5OCwtNzI5MzI4MzEzXX0=
-->