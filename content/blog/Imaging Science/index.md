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

阿贝的成像模型比较原始，灵感来自于双缝干涉和惠更斯原理，他认为：光照射在物体上，根据惠更斯原理，物体作为一个次级波源继续传播，物光经过透镜后在透镜的后焦面上发生了第一次干涉，这些焦斑继续传播，在成像面上发生了第二次干涉从而产生了图像。<a href="#1">[1]</a>

<img src=".\abbe imaging theory.png" />

<center style="font-size:14px"><p>Figure 1. Abbe Theory of image formation by diffraction and interference. </p></center>

根据Abbe的理论，一个复杂的物体所产生的衍射分量中，只有一部分贝有限的入射光瞳截取（相对低频的分量），而未被截取的是高频分量。总的来说就是把衍射现象来自于入射光瞳。
$$
U_i(x,y) = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} U_o(\xi,\eta) h(x-\xi, y-\eta) d\xi d\eta
$$











<a id="1">[1]</a> Gross, H. ed., 2005. *Handbook of optical systems* (Vol. 1, pp. 41-58). Weinheim: Wiley-Vch.
