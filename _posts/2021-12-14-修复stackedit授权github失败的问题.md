---
layout: post
title: "修复stackedit授权github失败的问题"
date:   2021-12-10
tags: [IT]
language : Chinese
comments: true
author: Zhen
toc: false
published: true
hidden: false
---
出去一趟回来发现blog的后台编辑器stackedit登录不了github了，弹出来了http400的错误。

查了一下是因为github更新了第三方授权的API token格式还是什么的。然后stackedit的管理员一直没有merge[热心网友的这个fix](https://github.com/benweet/stackedit/pull/1724)。

然后这个问题似乎是半年前就发生了，不知道
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0OTczMTQzNDddfQ==
-->