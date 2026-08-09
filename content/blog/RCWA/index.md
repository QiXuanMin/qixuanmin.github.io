---
title: Rigorous Coupled-Wave Analysis
summary: RCWA
date: 2026-08-02
math: true
authors:
  - admin
tags:
  - Notes
image:
  caption: 'Rigorous Coupled-Wave Analysis'
---

## Overview of RCWA

1. Determine the eigenmodes of each layer by Fourier expansion of the material distribution;
2. Calculate the in-out relation and coupling coefficients of single layer with eigenmodes and the electromagnetic boundary condition;
3. Calculate overall layers by the Redheffer star product;
4. Recover Electromagnetic fields with input light source, global in-out-relation, and coupling coefficients.

<img src=".\rcwa flowchart.png" />

<center style="font-size:14px"><p>Figure 1. Flowchart of RCWA. </p></center>



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

<a id="1">[1]</a> Kim, Changhyun, and Byoungho Lee. "TORCWA: GPU-accelerated Fourier modal method and gradient-based optimization for metasurface design." *Computer Physics Communications* 282 (2023): 108552.
