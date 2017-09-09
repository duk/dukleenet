---
layout: post
title:  "Ubuntu Installation Tips" 
date:   2017-09-09 11:55:00 -07002
categories:  
---

When I installed Ubuntu 16.04 as a virtual machine, x-window was slow as fuck. Someone on stackoverflow said, it will never be as fast on a virtual machine. So a few days ago, I installed Ubuntu 16.04 as a dualboot. But it was still slow. Then I found out that you have to change graphic driver setting from generic X-Window to NVIDIA one. 

![Additional Driver](/images/nvidia.png)

After that, it was fast. 