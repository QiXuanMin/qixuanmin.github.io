---
title: Coherent Imaging
summary: Imaging Theory
date: 2021-09-01
math: true
authors:
  - admin
tags:
  - Notes
image:
  caption: 'Coherent wave propagation'
---

## 阿贝成像模型

​	阿贝的成像模型比较原始，灵感来自于双缝干涉和惠更斯原理，他认为：光照射在物体上，根据惠更斯原理，物体作为一个次级波源继续传播，物光经过透镜后在透镜的后焦面上发生了第一次干涉，这些焦斑继续传播，在成像面上发生了第二次干涉从而产生了图像。<a href="#1">[1]</a> Figure 1很好的诠释了Abbe的理论，物体为一个多级次的光栅，经过透镜后光栅的每个级次在焦面汇聚。

<img src=".\abbe imaging theory.png" />

<center style="font-size:14px"><p>Figure 1. Abbe Theory of image formation by diffraction and interference. </p></center>

根据Abbe的理论，一个复杂的物体所产生的衍射分量中，只有一部分贝有限的入射光瞳截取（相对低频的分量），而未被截取的是高频分量。

## 相干成像理论

​	在单色光情况下，像的复振幅$U_i$可以用物像复振幅$U_o$的叠加积分表示：
$$
U_i(u,v) = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} U_o(\xi,\eta) h(u,v;\xi,\eta) d\xi d\eta
$$

其中$u,v$是像平面的坐标，$\xi,\eta$是物平面坐标，$h(u,v;\xi,\eta)$为系统的**脉冲响应函数**，其物理意义是：物平面点$(\xi,\eta)$的一个脉冲信号经过该系统后在像平面的点$(u,v)$产生的响应，其傅里叶变换$H(g_x,g_y;f_x,f_y)$为**相干传递函数CTF**。上述式子如果在一个空不变系统中，则可以理解为一个卷积：
$$
U_i(u,v)=U_o(\xi,\eta)\bigotimes h(u,v;\xi,\eta)
$$




------

<a id="1">[1]</a> Gross, H. ed., 2005. *Handbook of optical systems* (Vol. 1, pp. 41-58). Weinheim: Wiley-Vch.
