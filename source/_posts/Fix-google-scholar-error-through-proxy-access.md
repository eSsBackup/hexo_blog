---
title: Fix google scholar error through proxy
date: 2019-03-21 18:00:53
tags:
---

## Description

While using v2ray proxy to access google scholar, there is always a problem that a warming from Google says Google Scholar is accessed through proxy and proxy accessing is not permitted by Google.

## Solution

modify hosts file on proxy server at "/etc/hosts/"
add hosts below to the files

```bash
2404:6800:4008:c06::be scholar.google.com
2404:6800:4008:c06::be scholar.google.com.hk
2404:6800:4008:c06::be scholar.google.com.tw
2401:3800:4001:10::101f scholar.google.cn #www.google.cn
```