---
layout: post
title:  "如何在jupyter notebook中选择不同的conda环境(ipykernel)"
date:   2018-08-20 21:03:00 +0800
categories: jupyter-notebook
tags: jupyter-notebook conda
---

* content
{:toc}

首先激活对应的conda环境

    H:>activate tensorflow

在激活的环境中安装ipykernel
	
	(tensorflow)H:>conda install ipykernel

配置对应环境下的ipykernel

	H:>python -m ipykernel install --user --name tensorflow(环境名称) --display-name "tensorflow(在notebook中显示的环境名称)"

然后打开notebook

	H:>jupyter notebook

在kernel中就可以看到添加的conda环境了
![](http://ww1.sinaimg.cn/large/e3e031dfly1fugh8fqoe6j20nb0bvjs6.jpg)

参考链接：[https://ipython.readthedocs.io/en/stable/install/kernel_install.html#kernels-for-different-environments](https://ipython.readthedocs.io/en/stable/install/kernel_install.html#kernels-for-different-environments)