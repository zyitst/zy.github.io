---
layout: post
title:  "编写Python脚本压缩远程notebook中的图片"
date:   2018-11-04 15:35:50 +0800
categories: python
tags: 压缩文件 远程下载
---


之前倒腾了好久好不容易装上了cuda9.2,后来不知为何脑残运行了`sudo apt install nvidia-cuda-toolkit`,呼啦下载了一大堆，结果就在电脑上同时存在两个版本的cuda，一个9.2是之前安装好的，一个10.0是运行了那条命令安装的。

在网上搜索发现，在`/usr/local/`文件夹下多了一个`cuda`符号链接文件，同时多了一个`cuda-10.0`，原来的`cuda-9.2`还在。打开`cuda`链接，发现指向`cuda-10.0`。于是乎想出这么个馊注意...




将`cuda`链接删除，重新建立一个`cuda`链接指向`cuda-9.2`

10月份忙找工作和狗屁毕设，经过了一段时间没碰ubuntu系统，回来发现`nvcc`命令不好使了！！！回想之前装cuda的过程，想到可能是环境变量的问题（参考[NVIDIA文档](https://docs.nvidia.com/cuda/cuda-installation-guide-linux/index.html#environment-setup)），于是想到把`/usr/local/cuda/bin/`添加到环境变量。

- export PATH=/usr/local/cuda/bin/${PATH:+:${PATH}}

