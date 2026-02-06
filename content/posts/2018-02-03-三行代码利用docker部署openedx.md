---
title: 三行代码利用Docker部署OPENEDX
author: Natt
type: post
date: 2018-02-03T10:35:59+00:00
url: /6046.html
featured_image: /wp-content/uploads/2018/02/WX20180203-182848.png
nectar_blog_post_view_count:
  - 3537
categories:
  - 技术
  - 网络
tags:
  - docker
  - LMS
  - openedx
  - 技术

---
新部署一台 Ubuntu 14.04 的主机，SSH之后：

第一行代码，安装docker  
`curl -sSL https://get.daocloud.io/docker | sh`

&nbsp;

第二行代码，拉取镜像

`sudo docker pull wwj718/edx_cypress_docker:1.05`

&nbsp;

第三行代码，运行  
`sudo docker run -itd -p 80:80 -p 2022:22 -p 18010:18010 wwj718/edx_cypress_docker:1.05`

&nbsp;

参考：

`https://hub.docker.com/r/wwj718/edx_cypress_docker/`

`http://blog.just4fun.site/edx-cypress-cn-install-and-use.html`

`https://www.youtube.com/watch?v=24OiYPnTNv8`