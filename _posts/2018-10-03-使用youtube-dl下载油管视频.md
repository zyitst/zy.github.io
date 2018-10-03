---
layout: post
title:  "使用youtube-dl下载油管视频"
date:   2018-08-20 21:03:00 +0800
categories: 资源下载
tags: 资源下载 youtube
---

* content
{:toc}

在下面这个网址下载youtube-dl工具

http://rg3.github.io/youtube-dl/

如无法访问请移步

链接: [https://pan.baidu.com/s/1pVSDNvepC1cDup0FIE_Esw](https://pan.baidu.com/s/1pVSDNvepC1cDup0FIE_Esw) 提取码: 6ixt




将youtube-dl.exe的路径加入到PATH环境变量中

> 开启cmd，输入

	youtube-dl -u test123@abc.com https://www.youtube.com/playlist?list=PLfYUBJiXbdtSyktd8A_x0JNd6lxDcZE96 --playlist-start 9 --playlist-end 12

其中-u后面为你的youtube账户名，后面的链接为你想要下载视频URL或播放列表的URL，这里我使用的是播放列表，因为我想要下载这一个系列的视频。后面的

	playlist-start 9 --playlist-end 12

是我想下载列表中9到12集的视频。因为之前我下载过一次，到第九个视频失败了。

附截图![](http://ww1.sinaimg.cn/large/e3e031dfly1fvvdogx7mtj20r70krjry.jpg)

另外由于自己听力不是特别好，有些地方不借助字幕还是听不太懂，因此google到一个下载youtube字幕的网站[https://downsub.com/](https://downsub.com/)。直接把要下载字幕的视频URL链接复制进去就能下载啦！很好很强大~

![](http://ww1.sinaimg.cn/large/e3e031dfly1fvvfajfu9lj211y0kkq70.jpg)