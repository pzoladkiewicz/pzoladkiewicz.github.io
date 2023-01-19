---
title: SSH into Proxmox LXC container
date: 2023-01-19 21:50
categories: [proxmox]
tags: [ssh,lxc]
---

To login to a container with username/password login open **sshd_config**

```
nano /etc/ssh/sshd_config
```

and change line
```
PermitRootLogin prohibit-password
```
to
```
PermitRootLogin yes
```
save changes, exit nano.   
Restart ssh service for the changes to take effect.
```
service ssh restart
```