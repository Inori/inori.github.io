---
title: Path Tracing 中 Russian Roulette 的期望
date: 2023-08-04 02:49:02
math: true
categories:
- Mathematics for Computer Graphics
tags:
- Math
---

### 简介
Path Tracing 的递归算法中要解决一个问题，就是光线不能无限反射，需要有一个停止的条件，一种方法就是使用俄罗斯轮盘赌，Russian Roulette (RR)，只有通过RR时才继续算反射，否则停止递归，这样即能避免无限递归，又能保证能量守恒。

### 结论
于是就引出一个问题，设RR通过概率概率是$p$，$p=0$不反射，$p=1$无限次反射，那么$0<p<1$对应多少次反射呢？也就是说得求出$p$的期望$E\left( p \right) $
这里先给出最终答案：
$$
E\left( p \right) =\frac{p}{\left( 1-p \right) ^2}
$$
也就是说，如果$p=0.5$，那么大体上会反射2次，$p=0.8$，大体上会反射20次

### 推导过程
{% asset_img p1.jpg p1 %}  
{% asset_img p2.jpg p2 %}  

### 相关资料
Games 101
https://www.bilibili.com/video/BV1X7411F744?t=3248.4&p=16


