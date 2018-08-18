---
layout: post
title:  "编写Python脚本压缩远程notebook中的图片"
date:   2018-08-17 15:35:50 +0800
categories: python
tags: 压缩文件 远程下载
---


#使用zipfile模块

{% highlight python %}
import os, zipfile
rootdir=os.getcwd()
l=os.listdir(rootdir)		#获取当前路径下所有文件、文件夹

with zipfile.ZipFile('test.zip', mode='w') as zipf:
    for i in range(len(l)):
        path=os.path.join(rootdir,l[i])
        if os.path.isfile(path):	#如果是文件而不是目录则写入压缩文件
            zipf.write(l[i])
{% endhighlight %}

#在Coursera中上传此文件并运行

[![](https://s19.postimg.cc/ridvctynn/openfile.png)](https://s19.postimg.cc/image/ridvctynn/)

可以看到该目录下有许多图片文件，notebook只能勾选一个下载一个，不能批量下载，所以我们把改脚本上传到此目录中

[![image.png](https://s19.postimg.cc/nm0jgv8j7/image.png)](https://postimg.cc/image/3rehuqtbj/)

在notebook中新建一个cell，运行下面命令：

[![image.png](https://s19.postimg.cc/5vyuvuadv/image.png)](https://s19.postimg.cc/5vyuvuadv/)

就可以在images下生成一个test.zip文件，包括images下所有文件
，这样就可以只下载这个压缩文件，而不用一个一个点啦