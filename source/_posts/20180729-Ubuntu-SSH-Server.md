---
title: Ubuntu 18.04 Desktop SSH Server Config
date: 2018-07-29 13:06:47
tags:
---

- 安装openssh-server

  ```bash
  sudo apt install openssh-server
  ```
- 查看ssh服务是否已经运行
  ```bash
  ps -e | grep ssh
  ```
- 重启ssh服务
  ```bash
  service sshd restart
  ```