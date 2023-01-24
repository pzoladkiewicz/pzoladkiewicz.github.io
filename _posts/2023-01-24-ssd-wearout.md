---
title: How to prevent SSD wearout
date: 2023-01-22 21:50
categories: [proxmox]
tags: [ssd,tips]
---

https://www.reddit.com/r/Proxmox/comments/soix8n/ssd_wear_out_59_after_six_months/


```
If you don't have several servers and don't need high availability, then disable theese services:

systemctl stop corosync pve-ha-crm pve-ha-lrm

systemctl disable corosync pve-ha-crm pve-ha-lrm

Crm and lrm constantly write to disks, and as someone stated above - eat SSDs for breakfast.
```

```
disable HA service if you not use
```

```
Double check that Trim is enabled on the drive.
```