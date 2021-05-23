---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "一个与三线共点有关的命题"
subtitle: ""
summary: "读高中时发现的，并给出了证明"
authors: [admin]
tags: ["三角形","三线共点","三点共线","射影几何"]
categories: ["平面几何"]
date: 2021-05-12T22:16:09+08:00
lastmod: 2021-05-12T22:16:09+08:00
featured: true
draft: true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "欧拉，所有人的老师"
  focal_point: "Smart"
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

## 准备

首先介绍两个射影几何方面的两个定理，这两个定理的我参考了《什么是数学》[<sup>1</sup>](#refer-anchor)这本书，下面会用的到：

> **_帕斯卡定理：_**
  如果一六边形的**顶点交替地位于**两条**直线**上，则**相对的边的交点**是**共线**的。

> **_布利安桑定理：_**
  如果一六边形的**边交替地通过**两个**点**，则**连接相对的顶点的边**是**共点**的。

## 两个命题及其证明

### 问题简述

{{< figure src="question.png" caption="问题背景图示"  width="75%" height="75%" >}}

如上图所示，作一个三角形$\Delta A_0 B_0 C_0$，分别从三角形各顶点$A_0$、$B_0$、$C_0$过三角形内一点$M$作直线交对边于点$A_1$、$B_1$、$C_1$，然后连接$A_1$、$B_1$、$C_1$这三个点得到一个新的三角形$\Delta A_1 B_1 C_1$，然后又产生了新的三个交点$A_2$、$B_2$、$C_2$，然后再连接这三个点又得到新的三角形$\Delta A_2 B_2 C_2$，按这样的步骤循环下去可以得到一个三角形序列$\left[ \Delta A_n B_n C_n \right]$


### 命题一

> 线段$A_0 B_2$、$A_2 B_0$、$M C_1$三线共点。

也就等价于证明下图中三个橙色的点共线。

{{< figure src="n=1.png" caption="定理一图示"  width="75%" height="75%" >}}

而这一点可以借助帕斯卡定理证明，而帕斯卡定理中需要指明的六边形各点1、2、3、4、5、6已经在图中标明，所以命题成立。

### 命题二

> 线段$A_0 B_{2k}$、$A_{2k} B_0$、$M C_1$三线共点，$k=1,2,3...$

针对这一命题可以借助数学归纳法来证明。

首先是$n=1$时，也就是命题一所描述的情况，所以此时命题二成立。

之后假设$n=k$时成立，借助此假设可以作出下图:

{{< figure src="n=k+.png" caption="n=k"  width="75%" height="75%" >}}

对于$n=k+1$的情况，也就是证明线段$C_{2k+1} C_{2k}$、$B_0 A_{2k+2}$、$A_0 B_{2k+2}$三线共点。

我们再借助布利安桑定理，在上图的基础上连接几条线段并取几个交点，具体作法如下图所示：

{{< figure src="n=k+1.png" caption="辅助线作法"  width="75%" height="75%" >}}

根据布利安桑定理，1、2、3、4、5、6为六边形的六个点，图中M,N点就是需要六边形各边交替通过的两个点，因此只需再证明1、6、N三点共线即可。

<div id = "refer-anchor"></div>

### 参考：


- [1] [什么是数学：对思想和方法的基本研究]()
