---
layout: post
title: 基于Jekyll 的github pages blog 如何绑定独立域名
author: Natt
date: 2018-01-19T06:02:27+00:00
aliases: ["/6035.html"]
image: "/wp-content/uploads/2018/01/jekyll-logo.png"
description: ""
categories:
  - "技术"
tags:
  - "域名"
  - "绑定"
  - "记录"
  - "配置"

---


自己建立了一个 Jekyll 的博客做测试，刚才解决了域名绑定，记录一下。

思路来自：http://playingfingers.com/2016/03/26/build-a-blog/#section-2 ，只是他写的比较长，很吓人。于是我写个简单点的：

&nbsp;

步骤一，配置域名

<img loading="lazy" decoding="async" class="alignnone size-full wp-image-6036" src="/wp-content/uploads/2018/01/Snip20180119_2.png" alt="" width="733" height="395" srcset="/wp-content/uploads/2018/01/Snip20180119_2.png 733w, /wp-content/uploads/2018/01/Snip20180119_2-450x242.png 450w, /wp-content/uploads/2018/01/Snip20180119_2-600x323.png 600w, /wp-content/uploads/2018/01/Snip20180119_2-300x162.png 300w" sizes="auto, (max-width: 733px) 100vw, 733px" /> 

&nbsp;

如上图，用A记录解析你希望的二级域名，如输入www，或blog，记录值填写 github 的ip地址 192.30.252.153 即可。或者去<a href="https://help.github.com/articles/troubleshooting-custom-domains/#dns-configuration-errors" target="_blank" rel="noopener">这个网页</a>查看ip.

&nbsp;

步骤二，添加一个CNAME文件

<img loading="lazy" decoding="async" class="alignnone size-full wp-image-6038" src="/wp-content/uploads/2018/01/Snip20180119_3.png" alt="" width="346" height="68" srcset="/wp-content/uploads/2018/01/Snip20180119_3.png 346w, /wp-content/uploads/2018/01/Snip20180119_3-300x59.png 300w" sizes="auto, (max-width: 346px) 100vw, 346px" /> 

在网站根目录新建一个 CNAME 文件，无后缀名，打开后填入你配置的域名，保存即可。

注意，只写域名，不要加入 http:// 之类的多余内容。

&nbsp;

&nbsp;

以上配置好后，commit + push，最多等几分钟，即可实现绑定+访问。