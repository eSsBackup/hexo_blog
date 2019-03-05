---
title: Ubuntu 18.04 ShadowsocksR Config
date: 2018-07-02 13:03:48
tags:
---

- copy bash script from remote server ssr3
```bash
scp root@ssr3:~/shadowsocksR.sh ~/
```
- run script as roots

```bash
sudo bash ~/shadowsocksR.sh
```
- modify server IP & port in json config file
```bash
sudo vi /etc/shadowsocks.json
```
- modify init file; Change "BIN" from "server.py" to "local.py"
```bash
sudo vi /etc/init.d/shadowsocks
```
- update run from startup
```bash
sudo update-rc.d shadowsocks defaults
```
- add proxy to terminal
```bash
export https_proxy=http://127.0.0.1:1086
export http_proxy=$https_proxy
```
