---
title: Semiconductor thermoradiative power conversion
summary: Reading Notes
date: 2025-09-07
math: true
authors:
  - admin
tags:
  - Notes
image:
  caption: 'Thermoradiative power generation'
---

## 文章大纲

文章发表于Nature Photonics，2024年10月，由澳大利亚新南威尔士大学的Nicholas J. Ekins-Daukes(NED)教授主导的**综述型论文**。

该论文综述了热辐射二极管在辐射受限、存在非辐射两种情况下的工作原理。讨论了现有的方法局限性和夜间发电性能提升的机遇。<a href="#1">[1]</a>

<img src=".\article overview.png" />

<center style="font-size:14px"><p>Figure 1. Article overview. </p></center>

## 热辐射二极管的工作原理

​	在单色光情况下，像的复振幅$U_i$可以用物像复振幅$U_o$的叠加积分表示：
$$
U_i(u,v) = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} U_o(\xi,\eta) h(u,v;\xi,\eta) d\xi d\eta
$$

其中$u,v$是像平面的坐标，$\xi,\eta$是物平面坐标，$h(u,v;\xi,\eta)$为系统的**脉冲响应函数**，其物理意义是：物平面点$(\xi,\eta)$的一个脉冲信号经过该系统后在像平面的点$(u,v)$产生的响应，其傅里叶变换$H(g_x,g_y;f_x,f_y)$为**相干传递函数CTF**。上述式子如果在一个空不变系统中，则可以理解为一个卷积：
$$
U_i(u,v)=U_o(\xi,\eta)\bigotimes h(u,v;\xi,\eta)
$$




------

<a id="1">[1]</a> Nielsen, Michael P., et al. "Semiconductor thermoradiative power conversion." *Nature Photonics* 18.11 (2024): 1137-1146.
