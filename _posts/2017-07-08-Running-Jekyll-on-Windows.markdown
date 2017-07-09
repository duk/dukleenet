---
layout: post
title:  "Running Jekyll on Windows 10"
date:   2017-07-08 05:55:00 -07002
categories: learning
---

If you are using Windows 10, add these two to your Visual Studio Code settings. What it does it to swap out default powershell to Bash on Ubuntu on Windows. Now you and do whatever you want. 

{% highlight json %}
{
  "terminal.integrated.shell.windows": "C:\\WINDOWS\\Sysnative\\bash.exe",
  "terminal.integrated.shellArgs.windows": [
    "${workspaceRoot}",
    "--login"
  ]
}
{% endhighlight %}