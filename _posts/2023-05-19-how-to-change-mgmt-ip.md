---
title: How to change management interface and IP
date: 2023-05-19 09:09
categories: [proxmox]
tags: [tips]
---

You can manually change the IP address in 
```shell
nano /etc/network/interfaces
```
and reboot or systemctl restart networking.



in addition to editing '/etc/network/interfaces' you also need to make sure that the hostname resolves to the new ip-address - this is usually done by entering/changing the entry in
```shell
nano /etc/hosts
```