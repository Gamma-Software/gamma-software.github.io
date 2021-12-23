---
categories:
  - projects
tags:
  - content
  - css
  - edge case
  - lists
  - markup
  - projects
  - code
title: Dumb things to remember
---

Dumb Things to Remember
=======================

This repository list all the dumb things that I encoutered and must be
noted on a notepad (this is actually the notepad)

Docker
------

### DNS

I installed on my server a DNS resolver. The docker engine parameter
must be updated to add the ip of the dns server. In the
*/etc/docker/daemon.json* file.

``` {.json}
{
  "dns": ["192.168.1.34", "8.8.8.8"]
}
```

### Store the docker images on another partition

Just override the data-root parameter in */etc/docker/daemon.json*

``` {.json}
{
  "data-root": "/mnt/data/docker_images"
}
```
