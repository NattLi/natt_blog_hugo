---
title: 更换DeepIn 系统源至 Aliyun 以实现加速
author: Natt
type: post
date: 2018-01-15T14:45:42+00:00
url: /6026.html
featured_image: /wp-content/uploads/2018/01/deepin.png
nectar_blog_post_view_count:
  - 1977
categories:
  - 技术
tags:
  - DeepIn

---
由于一些原因需要用到Linux，为了简单安装的 DeepIn 15.5, 一切顺利但是后续通过终端安装一些服务的时候卡如死狗啊。于是将源更换至aliyun，速度飙升至跑满带宽。

&nbsp;

记录一下过程：

    sudo gedit  /etc/apt/sources.list
    
    将 http://packages.deepin.com/ 
    替换为 http://mirrors.aliyun.com/
    
    然后：
    

    sudo apt-get update
    刷新即可