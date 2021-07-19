---
title: Git
date: 2021-07-19 16:09:47
tags:
---

## create patch
`git format-patch HEAD^`

## check patch
`git apply --check ~/Code/ilinkvoip_client/0001-tmp-compile-done.patch`

## apply patch 
`git apply ~/Code/ilinkvoip_client/0001-tmp-compile-done.patch`

`git am xxx.patch`

```
// 最近一次的patch
git format-patch -1
// 最近两次的patch
git format-patch -2
```


## ssh 添加服务器信任
```
ssh-copy-id -i ~/.ssh/id_rsa.pub -p 36000 root@xxxxx

```