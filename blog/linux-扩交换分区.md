---
layout: posts
date: 2018-12-27 00:38:36
title: linux扩swap
categories: linux
tags: 
- linux
comments: true
---

### linux扩充swap
    linux扩充swap 1GB

#### 查看当前swap：
```shell
free -m
```


#### 增加swap:
```shell
    dd if=/dev/zero of=/swapfile bs=1M count=1024
    mkswap /swapfile
    swapon /swapfile
```

#### 自动挂载：
```shell
cat /etc/fstab
/swapfile                                 swap                    swap    defaults        0 0
```

#### 查看扩充后：
```shell
free -m
```



~~完~~
