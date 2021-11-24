---
title: Hexo博客搭建和Github部署
top: false
cover: false
toc: true
mathjax: false
date: 2021-11-24 11:37:12
password:
summary:
tags: [Hexo]
categories: [博客搭建]
---
Hexo是一款开源的非常方便好用的博客框架, 与Github Pages结合可以实现完全免费的博客建站, 本文记录我的博客的搭建流程, 供大家参考.

> 我是在Ubuntu18.04 LTS Desktop环境进行的搭建, 本文命令示例也以此系统为基础介绍.

## 本地环境安装

### 安装Git和Nodejs

1. 安装Git

由于博客项目有在多终端上编辑的需求, 本身部署到GitPages上也有需求, 所以需要先安装Git.
Ubuntu安装:

``` bash
$ sudo apt install git-all
```

检查是否安装成功:
``` bash
$ git --version
```

其他平台如Mac可以通过XCode Command Line Tools安装, Windows平台下可以下载可执行文件进行安装. 参考官方[Git安装文档](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

2. 安装Nodejs

比较熟悉的小伙伴可以用nvm或n来进行node的安装, 本文只介绍最基础的安装方式. (建议安装13及以上版本, 我的版本是v16.13.0)
从NodeSource安装:

``` bash
# 将NodeSource签名添加到系统, 如果需要其他版本可以改成 setup_{需要的版本号}
$ curl -sL https://deb.nodesource.com/setup_16.x | sudo -E bash -

# apt安装
$ sudo apt install nodejs

# 检查版本确认安装成功
$ node --version

# 同时查看npm版本
$ npm --version
```

### 安装Hexo客户端

接下来安装hexo命令行客户端, 一行命令搞定
``` bash
$ sudo npm install -g hexo-cli
```
安装后可以通过查看版本号确认安装是否成功
``` bash
$ hexo -v
```
我的安装版本是 hexo: 5.4.0, hexo-cli: 4.3.0

### 新建博客目录

### 本地预览

## GitHub配置

### 新建项目和GitPages配置

### ssh密钥配置

## 尝试发布

## 代码同步