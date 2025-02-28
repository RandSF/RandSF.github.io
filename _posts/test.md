---
layout: post
title: Do Carmo Note Chpt1
date: 2015-10-20 11:12:00-0400
description: an example of a blog post with some math
tags: math
categories: sample-posts
related_posts: false
---

some concepts:

$\R^3$, it is just a space. For two points $p, q\in\R^3$, we can build a vector $q-p$ that has origin at $p$. A set of such vectors is the **_tangent space of $\R^3$ at $p$_**, denoted as $\R^3_p$. And $\R^3_0$ is the "3D vector space" we always talk about. Lets take it as an example.

**_Vector Field_** $v$: Informally, $v$ is a **map** that assigns a vector in $\R^n_p$ to each point $p\in\R^n$. Notice that the vector $v(p)$ lies in different tangent spaces. For example, an **Electric Field** has different vectors at different points. We can write $v$ as

$$
v(p)=\sum_{i=1}^na_i(p)e_i
$$

![an electric field from wiki](https://upload.wikimedia.org/wikipedia/commons/thumb/3/37/VFPt_image_charge_plane_horizontal.svg/250px-VFPt_image_charge_plane_horizontal.svg.png)

where $e_i$ are the canonical basis of $\R^n_0$.

**_Dual Space_** $\left(R^n_p\right)^* $: the basis of it is $(dx_i)_p$, where $x_i:\R^n\mapsto\R$ takes the $i$-th coordinate of the point. That is $x_i(p)=p_i$.Then $(dx_i)_p$ takes the coordinate of the points in $\R^n_p$, it is the translation of $x_i$, similar to $e_i$ and $(e_i)_p$. Easily we can see set $\{(dx_i)_p\}$ is the dual basis of $\{(e_i)_p\}$.

**_an Exterior Form of degree 1_** ( a **_field of linear form_**) $\omega$: Informally, it assigns elements in $(\R^n)_p$ for each $p\in\R^n$. Or it simple replace $e_i$ in $v(p)$ with $(dx_i)p$.

**_an Exterior Form of degree 2_** : Informally, it is the bilinear dual of $\R^n_p\times\R^n_p$. And it is **alternate**. The set of it is $\Lambda^2(\R^n_p)^*$. For $\varphi_1, \varphi_2\in(\R^n_p)^*$, we have

$$
(\varphi_1\wedge\varphi_2)(v_1, v_2):=\det\left(\left[\begin{matrix}
\varphi_1(v_1)&\varphi_1(v_2)\\
\varphi_2(v_1)&\varphi_2(v_2)\\
\end{matrix}\right]\right)=\det(\varphi_i(v_j))
$$

and $\varphi_1\wedge\varphi_2\in\Lambda^2(\R^n_p)^*$. Expand the above equation, we can guess that$(dx_i\wedge dx_j)_p, i<j$ is a basis for $\Lambda^2(\R^n_p)^*$.

Generally, we have **_Proposition 1_**:

$$
\{
(dx_{i_1}\wedge\dots\wedge dx_{i_k})_p, \
i_1<i_2<\dots<i_k, \
i_j\in\{1,\dots,n\}
\}
$$

is the basis of $\Lambda^k(\R^n_k)^*$.

Hint to proof: proof **linear independence** by 1. applying the function $(dx_{i_1}\wedge\dots\wedge dx_{i_k})_p$ to $(e_{j_1},\dots,e_{j_k})$ (with different permutation of $i$). 2. for all $f\in\Lambda^k(\R^n_p)^*$, $f$ is a linear combination of the set.

For any exterior form $\omega$, we can write:

$$
\omega=\sum a_Idx_I
$$

where $I$ is the $k$-upla $(i_1,\dots,i_k),\ i_1<\dots<i_k$

**_Exterior product_** $\wedge$: it can be used to combined two forms, if $\omega$ is a $k$-form and $\varphi$ is a $s$-form, then $\omega\wedge\varphi$ is a ($k+s$)-form.

**_Proposition 2_** (properties of $\wedge$):

- Associative law: $(\omega\wedge\varphi)\wedge\theta=\omega\wedge(\varphi\wedge\theta)$
- Commutative law: $(\omega\wedge\varphi)=(-1)^{ks}(\varphi\wedge\omega)$ (imaging reversing the columns of a matrix)
- Distributive law: $\omega\wedge(\varphi+\theta)=\omega\wedge\varphi+\omega\wedge\theta$

**_convention between two spaces_**:

- $f:\R^n\mapsto\R^m$, $f^*:\Lambda^k(\R^m_p)^*\mapsto\Lambda^k(\R^n_p)^*$

- $\omega, \varphi\in\Lambda^k(\R^m_p)^*$, we have

  $$
  (f^*\omega)(p)(v_1,\dots,v_k)=\omega(f(p))(df_p(v_1), \dots,df_p(v_k))
  $$

  where $df_p:\R^n_p\mapsto\R^m_{f(p)}$.

- $g: \R^m\mapsto\R$ ($0$-form)

Then we have **_Proposition 3_**:

1. f
