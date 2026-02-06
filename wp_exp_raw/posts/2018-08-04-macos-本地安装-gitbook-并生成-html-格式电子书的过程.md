---
title: macOS 本地安装 gitbook 并生成 html 格式电子书的过程
author: Natt
type: post
date: 2018-08-04T08:55:28+00:00
url: /6166.html
featured_image: /wp-content/uploads/2018/08/gitbook.png
nectar_blog_post_view_count:
  - 2194
amp_status:
  - enabled
categories:
  - 技术
tags:
  - gitbook
  - gitbook教程
  - MAC
  - MACOS

---
第一步：安装node.js

https://nodejs.org/en/download/

第二步：第二步：安装gitbook

npm install gitbook-cli -g  
或者  
sudo npm install gitbook-cli -g

第三步：初始化  
记得选择目标文件夹，然后：  
gitbook init

第四步：粘入内容  
将md文件都拷入目标文件夹

第五步：生成  
gitbook build

第六步：上传  
将 _book 文件夹传到网站服务器，即可