---
toc: true
layout: post
description: Disable indexing Xcode
categories: [indexing, xcode]
title: Disable indexing Xcode
---
# Disable indexing Xcode

Stopping xcode from indexing
Just run this command in the terminal to turn off Indexing:

```shell
defaults write com.apple.dt.XCode IDEIndexDisable 1
```

To turn it back on, run this:

```shell
defaults write com.apple.dt.XCode IDEIndexDisable 0
```
