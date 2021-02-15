---
description: 一个非官方的湖科大教务系统 API 文档。
---

# 湖南科技大学强智教务系统  API 文档

{% hint style="success" %}
有任何讨论意见，可以前往 [Github 的 Issues](https://github.com/hjthjthjt/HNUST-QZ-API/issues) 中讨论，或[博客文章](https://jakting.com/archives/hnust-qz-api.html)评论区讨论。

此文档地址：[https://kdjw.docs.jakting.com/](https://kdjw.docs.jakting.com/)
{% endhint %}

{% hint style="info" %}
**请务必在阅读前，先查看** [**【必读】FAQ**](https://kdjw.docs.jakting.com/faq)**，因未阅读导致的问题请自己负责。**
{% endhint %}

{% hint style="danger" %}
这并不是一个官方文档，强智和学校**随时**可能改 API 导致文档失效。
{% endhint %}

学校换了个新的系统，虽然还是憨批强智。

新版的 PC 版强智本身是支持 API 的，但学校似乎没买，因此无法使用，访问 API 会直接跳转回首页。

不过因为在微信端引入了教务系统，使得现在有机会去找到对应的 API 了（好耶

![](.gitbook/assets/image.png)

此文档是我对一部分 API 的归纳，**并非官方文档。**

虽然要毕业了不过如果能帮到后来人的话就最好了（

首先，从微信企业号处很轻易地得到移动端教务系统的地址：

[http://kdfw.hnust.edu.cn/bbxy/\#/](http://kdfw.hnust.edu.cn/bbxy/#/)

样式上看得出来是 Vue.js，那一般是前后端分离，API 的 **BASE\_URL** 很好找

{% hint style="info" %}
 http://kdfw.hnust.edu.cn/bbxyhd
{% endhint %}

文档中所有的东西都以此地址为 **BASE\_URL**。

剩余部分请参考目录中的对应文档。

