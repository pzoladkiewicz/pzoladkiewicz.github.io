---
title: Four commands to update Portainer
date: 2023-10-31 08:20
categories: [proxmox,docker]
tags: [tips,troubleshoot]
---

1.     docker stop portainer
2.     docker rm portainer
3.     docker pull portainer/portainer-ce:latest

4.     docker run -d -p 8000:8000 -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest