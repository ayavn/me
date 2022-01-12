---
title: (Regex) Detect urls in string
toc: true
branch: master
categories: [dart, flutter, regex, regex-url, etect-url-in-string]
badges: true
comments: true
description: Working both http and https protocol
layout: post
---

Easy done:

```
(http|ftp|https):\/\/([\w_-]+(?:(?:\.[\w_-]+)+))([\w.,@?^=%&:\/~+#-]*[\w@?^=%&\/~+#-])
```
