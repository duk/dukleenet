---
layout: post
title:  "How to get Infinite Loader wth Table using React Virtualized"
date:   2017-08-01 03:53:00 -07002
categories: reactjs
---

Pulled my hair for a couple of days on this one. The key point is to use `cellDataGetter` in Column. And make sure rowData is not undefined.

<script src="https://gist.github.com/duk/ea41fb76985c258604bcd7ebc0f32500.js"></script>