---
layout: page
title: About
permalink: /about/
---

My name is Duk and I build websites for a living. I am currently focusing on UX part of things; JavaScript and CSS in general. I am well versed with 
most UI frameworks. I guess you can label me as "full stack developer." 

In the past, I've worked with .NET stack and Java stack at various companies.

This site is hosted at Amazon AWS.

I use Jekyll for the site and deploy to S3 bucket using aws command line like this.

{% highlight shell %}
sudo apt install aws
aws configure --profile duk
aws s3 cp ~/duklee.net/_site s3://duklee.net --recursive --profile duk --region us-west-1
{% endhighlight %}

Here are the domain names that I own. Hopefully I do something with them in near future.

1. [Nextdoor Chefs](https://nextdoorchefs.com)
2. [Work Openly](https://workopenly.com)
3. [Happy Developer](https://happydeveloper.com)