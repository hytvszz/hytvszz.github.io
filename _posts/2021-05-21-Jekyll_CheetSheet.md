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
不让双大括号被渲染：`{% raw %}{{ " {{ site.imageurl "}} }} {% endraw %}`或者`{% raw %}`    



<!--stackedit_data:
eyJoaXN0b3J5IjpbODY0ODAzMDUxLC0yMDk1NDY1NjYsNDI0MD
MxNzU0LDIwODAzODQ5NTcsMTcyNjQ1MDUwNSwxOTQxNjY2MzU5
LC0zMTg4MjA5ODksLTEzNTMxODQzMzUsMTU3NzQxNDc5MiwtMj
AzNzE2MjcyOCwtMjEzMTk4MDAxOSwtMTE3NjIzNjU5NiwtMjEx
Mjg1NzU2MiwzMjI4OTU5NjksLTcyMDg2MzQ0NSwtOTgyOTY5Nz
E3LDExNDAxOTAzOTgsLTcyOTMyODMxM119
-->