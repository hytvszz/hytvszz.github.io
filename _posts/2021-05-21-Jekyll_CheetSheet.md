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
{%  assign  openTag  =  '{%'  %}  {%  raw  %}`{% raw %} 大括号变量放这里 {%  endraw  %}{{  openTag  }} endraw %}{%  raw  %}  {%  endraw  %}



<!--stackedit_data:
eyJoaXN0b3J5IjpbLTI0MTE1ODc4NiwxMzc3NzExNzQ0LDg2ND
gwMzA1MSwtMjA5NTQ2NTY2LDQyNDAzMTc1NCwyMDgwMzg0OTU3
LDE3MjY0NTA1MDUsMTk0MTY2NjM1OSwtMzE4ODIwOTg5LC0xMz
UzMTg0MzM1LDE1Nzc0MTQ3OTIsLTIwMzcxNjI3MjgsLTIxMzE5
ODAwMTksLTExNzYyMzY1OTYsLTIxMTI4NTc1NjIsMzIyODk1OT
Y5LC03MjA4NjM0NDUsLTk4Mjk2OTcxNywxMTQwMTkwMzk4LC03
MjkzMjgzMTNdfQ==
-->