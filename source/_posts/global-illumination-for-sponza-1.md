---
title: '[Global illumination for Sponza][1] 搭建环境'
date: 2023-09-17 02:13:12
categories:
- Global Illumination
tags:
- CG
- GI
---

### Start
为了学习图形学相关的算法，打算用经典的Sponza场景自己实现GI，GI算法不只一种，而且经常是几种结合使用，所以我计划写个系列博客，记录一下学习过程中遇到的困难，非教学向。

### Nvidia Falcor
开始的时候其实是打算用Vulkan从最底层写起的，[框架](https://github.com/Inori/GowVulkanSamples)都写好了。

不过从之前的经验来看，从最底层写起其实是很花时间的，要手动处理资源绑定、ImageLayout转换、barrier等等细节的东西，而且一但有某个细节出错，往往很难调试，会浪费更多时间。

一个偶然的机会发现了Nvidia出了个[Falcor](https://github.com/Inori/Falcor)渲染框架，试了一下发现这玩意真是不错，抽象做的非常好，不用关心底层vulkan dx api的细节，资源绑定和传递都非常容易。而且复杂度适中，比自己调用Vulkan复杂，但是远比UE简单，可以很轻松就能理解框架代码。

Falcor自带了很多现成的Rander Pass，不过我不打算使用，毕竟是出于学习目的，用现成的没有任何意义。我打算只用Falcor资源加载、绑定、传递部分的代码，其它算法、shader全部手写。

### Sponza Demo
研究了一会，可以正常加载场景了，先blinn-phong搞起：

{% asset_img sponza.jpg Sponza %}  