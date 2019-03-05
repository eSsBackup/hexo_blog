---
title: Standard Procedure of Server Setup
date: 2019-01-28 12:47:38
tags:
---

1. ### Upload ssh-key and disable password login
   - modify system hosts file to identify server
        - C:\Windows\System32\drivers\etc (Windows 7 or later)
        - /etc/hosts (Linux)
   - copy files contained ssh authroized keys to server
        ``` bash
        scp authorized_keys root@server_ip:~/.ssh
        ```
2. ### Install v2ray
      - download v2ray and install
        ```bash
        bash <(wget http://install.direct/go.sh)
        ```
      - change server configuration
        ```bash
        scp server_config.json root@server_ip:/etc/v2ray/config.json
        ```
3. ### Install shadowsocksR && enable bbr
      - download ShadowsocksR
      - install ShadowsocksR
4. ### Install utility such as htop, screenfetch, etc
      - contained in ShadowsocksR install script
5. ### Install kms service
      - download one_key_install script
      - move ctrl script to somewhere
      - set up systemctl using kms.service
      - (optional) using supervisor to mantain kms service
6. ### Install Denyhost or Fail2ban
      - using apt to install denyhost
      - whitelist my own ip address
7. ### Restart server