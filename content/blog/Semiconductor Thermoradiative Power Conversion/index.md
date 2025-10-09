---
title: Semiconductor thermoradiative power conversion
summary: Reading Notes
date: 2024-09-30
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

## 前置知识

### 费米能级

定义：当处于绝对零度0K时，电子占据的最高能级。在费米能级以下的所有能级都被电子填满，能级以上的所有能级都是空的。

**费米—狄拉克分布**：当温度大于绝对零度时，可以通过费米-狄拉克分布描述电子占据能量为$E$的量子态概率。一般在费米能级处电子占据概论恒为1/2。其公式如下所示：
$$
f(E)=\frac{1}{1+e^{(E-E_F)/k_bT}}
$$
其中$E_F$为费米能级，$k_b$是玻尔兹曼常数，T为开式温度。

<img src=".\Fermi-Dirac distribution.jpg" />

<center style="font-size:14px"><p>Figure 2. Fermi-Dirac distribution. </p></center>

### Purcell效应(Deepseek解释)

**Purcell 效应** 指的是发光体（如原子、分子、量子点）的自发辐射速率可以通过其所处的**电磁环境**来改变和调控的现象。

简单来说，**一个发光体并不是以一个固定不变的速度发光，它发光的快慢取决于它周围的环境**。

#### 核心思想：

1. **自由空间中的发光**：一个孤立的原子在真空中发光时，其自发辐射速率是一个固定的固有值，由原子本身的属性决定。
2. **环境改变发光速率**：如果把这个原子放入一个特殊的电磁环境中（比如一个光学微腔、 near a metal nanoparticle， 或 inside a photonic crystal），它发光的速率就会改变。**速率增强**：如果发光体的发射频率与所在环境的某个电磁模式（如光学腔的共振模）频率匹配，并且模式体积很小，其自发辐射速率会**显著加快**。这是最常见的 Purcell 效应。**速率抑制**：反之，如果环境的电磁模式密度在发光频率处为零（例如在光子晶体的光子禁带中），自发辐射速率就会被**强烈抑制甚至完全阻止**。

#### 为什么会产生这种效应？

自发辐射过程并非完全是发光体自身的固有属性，它依赖于发光体与周围**真空涨落**的相互作用。所谓的“真空”并非空无一物，而是充满了能量极低且随机的电磁波动（虚光子）。这些涨落是促使激发态原子发生自发辐射的根源。

当你改变发光体周围的环境时（例如引入一个光学谐振腔），你实际上是在**重塑“真空”**——改变了该位置特定频率下的电磁模式密度（Local Density of States, LDOS）。

- **在谐振腔中**：在共振频率处，电磁模式密度大大增加，相当于给发光体提供了更多“辐射通道”，因此其辐射速率加快。
- **在光子禁带中**：电磁模式密度为零，发光体找不到可以辐射的通道，因此辐射被抑制。

## 热辐射二极管的工作原理

传统的热辐射发电器件热的流动从辐射物体$T_H$到发射表面$T_{EM}$再到大气温度$T_C$，满足$T_H >T_{EM}>T_C$，如图3的a所示。而如果使用窄带半导体作为热发射器件，可直接产生电能，如图3.b所示，其热关系满足$T_H=T_{EM}>T_C$。

<img src=".\Thermodynamic for thermoradiative devices.png" />

<center style="font-size:14px"><p>Figure 3. Thermodynamic energy (E), heat(Q) and entropy(S) flows for thermoradiative devices. </p></center>

## 光学增强热辐射

提高半导体热辐射二极管的发电效率的方法之一就是：用最少的发射体材料实现尽可能高的总外部发射。（因为Auger过程与体积成正比）所以光学手段来增强二极管的emission是很重要的。文中举例了四种比较有希望的方法。

### Optical thick devices

Index-matched lens

<img src=".\index-matched lens.png" style="zoom:50%;" />

<center style="font-size:14px"><p>Figure 4. Index-matched hemispherical lens.</p></center>

我的理解是这种做法：

1. 在源头上匹配了阻抗，使得红外辐射没有阻碍地进入透镜
2. 把半导体作为点光源，这种半球型的结构够有垂直表面的辐射，更容易发射到自由空间
3. 文章提到，这种方法将有效的光学区域增加了$n^2$倍； 将通过器件的平均路径长度提高了一个因子2倍，反射镜又将路径长度提高了2倍。所以总共增强了$n^2\times2\times 2 = 4n^2$

#### 如何超越这个增强的极限？(Deepseek对原文的理解)

+ 还提到上面这种增强是宽带发射情况下，如果光谱的带宽收到限制，发射增强效果会强于这个值。**如果你不要求增强所有颜色的光（宽带发射），而是只针对一个很窄的波长范围（限制光谱带宽），那么吸收/发射增强因子就有可能突破4n²这个经典极限**。

+ **为什么可以超越？** 4n²极限是针对*宽带*（所有波长）的统计平均极限。当只关心一个特定波长时，可以利用**光学共振效应**（如法布里-珀罗腔、光子晶体、等离子激元等）。这些共振结构可以在特定波长附近极大地局域和增强光场，使得该特定波长下的吸收和发射效率远高于宽带随机纹理结构的统计平均值。这本质上是**Purcell效应**的体现——通过改变光学态密度来显著增强发光速率。

### Randomly scattering back surface

这种方法，就是把玻璃的表面添加一些随机散射的纹理，使得光能够突破全反射，更容易外耦合到自由空间，缺点很明显，就是效率低下，外耦合效率没那么高。

<img src=".\Randomly scattering back surface.png" style="zoom:50%;" />

<center style="font-size:14px"><p>Figure 5. Random scattering texture surface.</p></center>

### Metasurface



------

<a id="1">[1]</a> Nielsen, Michael P., et al. "Semiconductor thermoradiative power conversion." *Nature Photonics* 18.11 (2024): 1137-1146.

