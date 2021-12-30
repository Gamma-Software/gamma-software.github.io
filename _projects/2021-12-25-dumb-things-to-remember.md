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

This must be removed

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

Bash
----

### Time your scripts

You can use the `time` command to easily get the execution time of a
script.\
For instance you want to know how long it takes to execute this command
`ls -l` simply write:

``` {.bash}
time ls -l
```

The result will be something like:

    real    0m0.038s
    user    0m0.000s
    sys     0m0.000s

More obvious one will be the command `sleep 1`, the result will be:

    real    0m1,003s
    user    0m0,001s
    sys     0m0,002s

### Time your python scripts

Python scripts can also be timed with the command `time`. For instance,
if you want to know how long it takes to execute this command
`python3 -c "import time; time.sleep(1)"` simply write:

``` {.bash}
time python3 -c "import time; time.sleep(1)"
```

The result will be something like:

``` {.bash}
real    0m1.003s
user    0m0.001s
sys     0m0.002s
```

### Make fun of executing a script

mpv audio\_file.wav &
<script>

You can also make a sound based on the success of failure of the script
as is...

You can also show an animation when the script successeed
