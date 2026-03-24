---
layout: post
title: 顺手给blog的VPS装个SSR
author: Natt
date: 2023-01-11T07:49:34+00:00
aliases: ["/6553.html"]
image: "/wp-content/uploads/2023/01/20230111154148.jpg"
description: ""
categories:
  - "艺术设计"
tags:
  - "机场"
  - "小鸡"
  - "代码"
  - "续费"

---


对我来说，那个啥就是水和空气  
一般情况下，现在都在用大机场了，稳定性自然比自己弄个小鸡更好，并且还能为孩子的Disney+和Nintendo Service Online 服务提供必要的便利。

但，为了防止一不小心的机场不稳而无法那个啥，甚至是机场流量到了忘了续费等情况，一个备用小鸡还是必要的。

感谢互联网，几行代码就能完成，这里记录一下，方便自己后续

安装环境以及teddysun的一键SSR代码 ↓  
`apt-get update -y && apt-get install wget -y && apt-get install curl -y`  
`wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh`  
`chmod +x shadowsocks-all.sh`  
`./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log`

安装BBR加速 ↓  
`wget -N --no-check-certificate "https://gist.github.com/zeruns/a0ec603f20d1b86de6a774a8ba27588f/raw/4f9957ae23f5efb2bb7c57a198ae2cffebfb1c56/tcp.sh" && chmod +x tcp.sh && ./tcp.sh`  
`./tcp.sh`

最后，别忘了开防火墙对应的SSR端口，重启，完事。