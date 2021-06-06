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
不让双大括号被渲染："{% raw %"}{{ site.imageurl }}{% endraw %} 或者 {% raw %}{{ " {{ site.imageurl "}} }} {% endraw %}


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTU2NDA5MzgwNSwtMjA5NTQ2NTY2LDQyND
AzMTc1NCwyMDgwMzg0OTU3LDE3MjY0NTA1MDUsMTk0MTY2NjM1
OSwtMzE4ODIwOTg5LC0xMzUzMTg0MzM1LDE1Nzc0MTQ3OTIsLT
IwMzcxNjI3MjgsLTIxMzE5ODAwMTksLTExNzYyMzY1OTYsLTIx
MTI4NTc1NjIsMzIyODk1OTY5LC03MjA4NjM0NDUsLTk4Mjk2OT
cxNywxMTQwMTkwMzk4LC03MjkzMjgzMTNdfQ==
-->