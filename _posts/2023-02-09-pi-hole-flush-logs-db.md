---
title: How to clear all pi-hole logs
date: 2023-02-09 19:00
categories: [pi-hole]
tags: [ssh,logs]
---

***jfb-pihole***

Here's a quick way to create a new empty database.


```Shell
sudo service pihole-FTL stop
```
```shell
sudo rm /etc/pihole/pihole-FTL.db
```
```shell
sudo service pihole-FTL start
```

<https://www.reddit.com/r/pihole/comments/s7u6ca/comment/htcddvh/>