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

然后这个问题似乎是半年前就被注意到了，然后大概是从9月份有人反映连接不上github，一样的http400错误，我估计我现在才遇到是之前的授权一直没有到期，然后公司网站出现了bug，我就清空了一下浏览器的cache，结果各大网站都被sign out，然后这个授权也被清除了。

然而，发现有个聪明的网友，给了一个workaround[一个workaround](https://github.com/benweet/stackedit/issues/1755)：在弹出网页转到github授权界面的时候，在你点授权之前，F12打开console，输入下边的JS code：

    window.XMLHttpRequest =  class MyXMLHttpRequest extends window.XMLHttpRequest {
    open(...args){
    if(args[1].startsWith("https://api.github.com/user?access_token=")) {
      // apply fix as described by github
      // https://developer.github.com/changes/2020-02-10-deprecating-auth-through-query-param/#changes-to-make
  
      const segments = args[1].split("?");
      args[1] = segments[0]; // remove query params from url
      const token = segments[1].split("=")[1]; // save the token
      
      const ret = super.open(...args);
      
      this.setRequestHeader("Authorization", `token ${token}`); // set required header
      
      return ret;
    }
    else {
      return super.open(...args);
    }
    }
    }

<!--stackedit_data:
eyJoaXN0b3J5IjpbNDk5MzE2Nzg4XX0=
-->