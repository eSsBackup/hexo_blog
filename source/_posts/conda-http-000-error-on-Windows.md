---
title: conda encounter http000 error on Windows
date: 2019-03-13 20:52:02
tags:
---

##
When I tried to install Python package to a new created conda environment on my Windows 10 tablet, conda returns error as below.

"CondaHTTPError: HTTP None None for url <https://repo.continuum.io/pkgs/free/win-64/repodata.json.bz2><br>Elapsed: None<br><br>An HTTP error occurred when trying to retrieve this URL.<br>HTTP errors are often intermittent, and a simple retry will get you on your way.<br>ConnectTimeout(MaxRetryError("HTTPSConnectionPool(host='repo.continuum.io', port=443): Max retries exceeded with url: /pkgs/free/win-64/repodata.json.bz2 (Caused by ConnectTimeoutError(<requests.packages.urllib3.connection.VerifiedHTTPSConnection object at 0x0000000005E606A0>, 'Connection to repo.continuum.io timed out. (connect timeout=9.15)'))",),)<br>Navigator Error #2760"

After I googled it, I got several solutions. Some said it was caused by Python, in which there is no ssl compiled. But my conda and conda-installed python worked well once. If the problem is caused by not compiled ssl module in Python, it should not been working at first. 
And some said the pip package should been updated to the latest version. But here comes a question, if I can't use pip or conda to install new package, I can't use pip or conda to update either. 
As a victim of GFW in China, I was inspired by a comment at github, which said that the same problem can be solved by adding proxy server section in .condarc. After I add scripts below to .condarc(which located in C:\Users\YourUserName\), conda commands works well on my system.
```yaml
proxy_servers:
    http: http://127.0.0.1:1088
    https: https://127.0.0.1:1088
```

PS: On Windows, I use v2rayN and socks5 protocol as ladder, and use privoxy as http-forward to handle http and https request.