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


https://www.reddit.com/r/Proxmox/comments/p2c0qz/proxmox_causing_high_wear_on_ssd/
```
Run iotop -ao (should be available via apt). This will show you what processes are responsible for the most writes, then you can make more informed decisions about how to correct it.
```

https://gist.github.com/hostberg/86bfaa81e50cc0666f1745e1897c0a56