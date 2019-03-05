---
title: Use hexo to maintain your own static blog
author: Esmidth
date: 2019-03-05 17:45:55
tags:
---


## Intro
hexo is designed to generate and deploy static page on github as customized blog, developed with Node.js.
To satisfy my demand for blogging, I use hexo to deploy my markdown notes on github.com. Here comes my manual.

## Register and Init project on Github.com

## Installation
As my daily used OS are Windows and Linux, I choose to install node.js on WSL, which makes the installation procedure works well for Linux user.
- ### Node.js
    ```bash
    sudo apt install npm
    ```
- ### Hexo
    change directory to where your project is located first, and install hexo
    ```bash
    npm install hexo
    npm install hexo-deployer-git
    ```

## Init 

to init hexo project, change directory to project directory and type

```bash
hexo init
```

## Create new post, page or draft
Create new article
```bash
hexo new <type> <title>
```
## Generate and Deploy
- ### Generate new static render
    ```bash
    hexo g
    ```
- ### Deploy article to github
    ```bash
    hexo d
    ```
