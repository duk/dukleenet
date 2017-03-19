---
layout: post
title:  "How to learn UI"
date:   2016-09-28 00:54:24 -0700
categories: css
---

I will be talking about how I will master UI (html, CSS, JavaScript) and you should too. This is something I came up with. But the original idea has been around for awhile. 

The bottom line is you need to memorize as much as possible. And you should use "chunking" to make them "memorizable." Think of it as lego pieces. Once 
you have that in your brain, it gets easier. What you need to do is to put them together to build bigger blocks.

For example, do not memorize CSS attributes indivisually. Instead, memorize css set.

{% highlight css %}
padding: 0 8px; /* don't do this */
{% endhighlight %}

instead,

{% highlight css %}
/* snippet from  https://www.w3schools.com/howto/howto_js_popup.asp */
/* Popup container */
.popup {
    position: relative;
    display: inline-block;
    cursor: pointer;
}
{% endhighlight %}

Now, you know what to do to create popup type style. Once you have that block in your head, you can then be creative with it. But make a block as 
lean a possible. You don't want to add color to a popup; that's a matter of customization.

What I am currently doing is to go through [W3 How To][w3-how-to], and try to memorize everything that's on it. For example, memorize how to make
animated button.first

{% highlight css %}
/* https://www.w3schools.com/howto/tryit.asp?filename=tryhow_css_buttons_animate3 */
.button {
  padding: 15px 25px;
  font-size: 24px;
  text-align: center;
  cursor: pointer;
  outline: none;
  color: #fff;
  background-color: #4CAF50;
  border: none;
  border-radius: 15px;
  box-shadow: 0 9px #999;
}

.button:hover {background-color: #3e8e41}

.button:active {
  background-color: #3e8e41;
  box-shadow: 0 5px #666;
  transform: translateY(4px);
}

{% endhighlight %}

[w3-how-to]: https://www.w3schools.com/howto/default.asp
