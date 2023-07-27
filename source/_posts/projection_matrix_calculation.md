---
title: 投影矩阵的推导过程
date: 2023-07-25 01:23:51
math: true
categories:
- Mathematics for Computer Graphics
tags:
- Math
---

目标如下图所示，把View Space的坐标映射到Clip Space: 

{% asset_img map.png 空间映射 %}                                         
 
这里先做一些前置说明：
设View Space (也可以叫做Eye Space)里的点坐标为 $\left( x_e, y_e, z_e, 1 \right) $
设Clip Space 里的点坐标为 $\left( x_c, y_c, z_c, w_c \right) $
设 NDC Space 里点的坐标为 $\left( x_n, y_n, z_n, 1 \right) $

同时不考虑viewport非中心对称的情况 (非中心对称时$x_e$和$x_c$并非线性关系)

以下为推导过程：

{% asset_img proc1.jpg proc1 %}
{% asset_img proc2.jpg proc2 %}
{% asset_img proc3.jpg proc3 %}

<br/> 
<br/>

同时观察$z_e$和$z_n$之前的映射关系:
{% asset_img proc4.jpg proc4 %}

<br/> 
<br/>

画个函数图像，绿色和红色$(n,f)$取值分别为 (1, 3), (1, 100):
{% asset_img z_map.jpg z_map %} 

从图上可以看出：
相同$f$值的情况下，$z_e$越接近远平面，其变化引起$z_n$的变化越不明显
相同$z_e$值的情况下，$f$越小，变化率(导数)越大 
这个特性和z-fighting相关，因为$f$较大的情况下，$z_e$的微小变动几乎不会引起$z_n$的变化

这里想到一点，就是depth buffer里存储的是perspective divide之后的z值，所以early depth test发生在
perspective divide之后







