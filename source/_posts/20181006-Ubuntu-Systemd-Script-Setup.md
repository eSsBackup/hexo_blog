---
title: Ubuntu KMS Service Systemd Script Setup
date: 2018-10-26 13:08:20
tags:
---

- .pid files, located in the /var/run/, gives the process a certain pid number the locate the process while the process is running. And the pid numbers are in plain text forms in the files.

- want a bash script running with the system booting up.
  - In "[Unit]" section, add "After" and "Wants" attribute to satisfy dependency.
  - In "[Service]" section
    - set "Type=oneshot", which is used to run bash script.
    - set "ExecStart" equals the script location and command used to send to script.
    - set "RemainAfterExit=yes",to remain the process status after the script ends.
  - in "[Install]" section,set "WantedBy=multi-user.target".

- Powershell command on Windows to activate VOL version Windows and Office

  - ```powershell
    cd /d "%SystemRoot%\system32"
    slmgr /skms 你的KMS服务端主机的IP或者域名
    slmgr /ato
    slmgr /xpr
    ```