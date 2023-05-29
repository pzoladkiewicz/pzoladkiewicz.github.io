---
title: How to fix problem with accessing Proxmox Web GUI
date: 2023-05-29 10:50
categories: [proxmox]
tags: [tips,troubleshoot]
---

Everytime you change network adapter there is good chance proxmox will rename adapter's name. What you need to do is 

- first check new names using
```shell
ip a
```
- then change it in 

```shell
nano /etc/network/interfaces
```

- and reboot or systemctl restart networking.


[source: Softlution](https://www.youtube.com/watch?v=jxW2it3v8Ps)