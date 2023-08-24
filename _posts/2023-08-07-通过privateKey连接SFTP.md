---
layout: post
title: "通过privateKey连接SFTP"
date:   2023-08-07
tags: [IT]
language : Chinese
comments: true
author: Zhen
toc: false
published: true
hidden: false
---
`SessionOptions sessionOptions = new SessionOptions { Protocol = Protocol.Sftp, HostName = "b2btest.myer.com.au", PortNumber = 980, UserName = "evolve", //PrivateKeyPassphrase = "", SshHostKeyFingerprint = "LKcrHlDXpe9Nlr2QayQID4U4U0FKLKpYAwV4PkQSrik", SshPrivateKeyPath = Path.Combine(Directory.GetCurrentDirectory(), "myer.ppk"), };`

**passphrase**, not set, choose empty, can ignore.

**fingerprint**, tried my own fingerprint when generate key pair:

J556EDT42c/Te7kDL+ZaGQm4fxX1Pv9WjUhHnfyTQP0

not working,

get it from the error when running the code:

WinSCP.SessionRemoteException: 'Host key does not match configured key fingerprint "J556EDT42c/Te7kDL+ZaGQm4fxX1Pv9WjUhHnfyTQPO"!  
**Host key fingerprint is ssh-rsa 1024 LKcrHlDXpe9Nlr2QayQID4U4U0FKLKpYAwV4PkQSrik.**

`SshPrivateKeyPath` : generate client public/private key pari by

[![](https://www.jscape.com/hubfs/JSCAPE%20%E2%80%94%20Icon%20%E2%80%94%20Blue@4x.png)Setting Up SFTP Public Key Authentication On The Command Line | JSCAPE](https://www.jscape.com/blog/setting-up-sftp-public-key-authentication-command-line)

then send myer the public key to validate, using my own private key id_rsa

not working as the format error, the error got from running code: OpenSSH SSH-2 private key (new format)

need to convert to xxxx.ppk format

**download Putty, find puttygen after install, load private key file, save private key as myer.ppk**

![](blob:https://theevolvedgroup.atlassian.net/6b57f571-2384-4d14-91b7-3c23012d170a#media-blob-url=true&id=ccb4ddcc-ce98-464e-90c4-b95e06f6c3c3&collection=&contextId=39505&height=572&width=792&alt=)

when writing file, myer server does not support edit timestamp

[![](https://winscp.net/favicon.ico)Upload of file .. was successful, but error occurred while setting the permissions and/or timestamp. If the problem persists, turn off setting permissions or preserving timestamp. Alternatively you can turn on ‘Ignore permission errors’ option. :: WinSCP](https://winscp.net/eng/docs/message_preserve_time_perm)

。。。。。。。。。。
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjA0MTY0OTI0NCwtMTY5MDk4OTcxNCwtMT
g0ODU3MjU4Nl19
-->