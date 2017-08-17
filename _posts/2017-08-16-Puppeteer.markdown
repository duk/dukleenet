---
layout: post
title:  "Puppeteer"
date:   2017-08-16 22:47:00 -07002
categories: technology
---

When you install [Puppeteer](https://github.com/GoogleChrome/puppeteer#puppeteer--) on Windows. Make sure you do it in normal "Command Prompt", not in "Node.js Command Prompt." npm install pulls linux chrome instead of window chrome in node.js command prompt.

Also on Ubuntu server, I had to install bunch of dependencies.

``` bash
sudo apt install libpangocairo-1.0 libx11-xcb1 libxcomposite1 libxcursor1 libxdamage1 libxi6 libxtst6 libnss3 libcups2 libxrandr2 libgconf-2-4 libasound2 libatk1.0-0 libgtk-3-0
```