+++
date = '2022-09-02T15:44:10-04:00'
draft = false
title = 'Complex Analysis: Basics'
categories = 'Math'
ShowToc = true
tags = [ "Complex Analysis", "Basics" ]
+++
## Basic concepts of complex numbers

The **complex plane** $\mathbb{C}$ is the set of all numbers of the form $z = x + iy$, where $x,y \in \mathbb{R}$ and $i$ is the imaginary unit satisfying $i^2 = -1$.
The real part of $z$ is denoted $\operatorname{Re}(z) = x$ and the imaginary part $\operatorname{Im}(z) = y$.

We identify $\mathbb{C}$ with $\mathbb{R}^2$ via the correspondence $z = (x,y) \leftrightarrow x + iy$.

> [!info] Complex-valued function
> A **complex-valued function** on a set $U\subseteq C$ is a function $f:U\to \mathbb{C}$.

If $z = x + iy$ and $f(z) = u(x,y) + i v(x,y)$, then $u,v:\mathbb{R}^2 \to \mathbb{R}$ are called the **real part** and **imaginary part** of $f$, respectively.

## Topology in the complex plane

> [!info] Open set & Closed set (in the complex plane)
> A set $U\subseteq \mathbb{C}$ is **open** if for every $z_0 \in U$, there exists $\varepsilon>0$ such that the open disk $$D_\varepsilon(z_0)=\{z\in \mathbb{C}:|z-z_0|<\varepsilon\}$$ is contained in $U$.
> 
> A set $F\subseteq \mathbb{C}$ is **closed** if its complement $\mathbb{C}\setminus F$ is open.


**Definition (Region or domain).**
A **region** (or **domain**) is a nonempty open and connected subset of $\mathbb{C}$.

**Definition (Boundary and interior).**
Let $A \subseteq \mathbb{C}$. The **interior** of $A$ is the largest open set contained in $A$. The **boundary** $\partial A$ is the set of points $z \in \mathbb{C}$ such that every open disk centered at $z$ intersects both $A$ and $\mathbb{C} \setminus A$.

---

### **3. Limits, Continuity, and Differentiability**

**Definition (Limit of a complex function).**
Let $f:U \to \mathbb{C}$ and $z_0 \in U$ a limit point. We say that $f(z)$ has **limit $L$ as $z \to z_0$** if for every $\varepsilon > 0$, there exists $\delta > 0$ such that
$$0<|z-z_0|<\delta \implies |f(z)-L|<\varepsilon.$$

---

**Definition (Continuity).**
A function $f:U\to \mathbb{C}$ is **continuous** at $z_0\in U$ if
$$\lim_{z\to z_0}f(z)=f(z_0).$$
Equivalently, for every $\varepsilon > 0$, there exists $\delta > 0$ such that
$|z - z_0| < \delta \ \Rightarrow\ |f(z) - f(z_0)| < \varepsilon$.

> [!info] Complex differentiability

Let $f:U \to \mathbb{C}$, and $z_0 \in U$. We say that $f$ is **differentiable** at $z_0$ if the limit
$$f'(z_0)=\lim_{z\to z_0} \frac{f(z)-f(z_0)}{z-z_0}$$
exists. The value $f'(z_0)$ is called the **complex derivative** of $f$ at $z_0$.

> [!info] Holomorphic function
> Let $U\subseteq \mathbb{C}$ be an open set. A function $f:U\to \mathbb{C}$ is called **holomorphic** on $U$ if $f$ is complex differentiable at every point $z\in U$.
> 
> In particular, a function is called **entire** if it is holomorphic on $\mathbb{C}$.

> [!info] Complex conjugate  
> The complex conjugate of a complex number $z=a+bi$ is $a-bi$, denoted by $\overline{z}$.

> [!info] Modulus
> The **modulus/absolute value** of a complex number $z=a+bi$ is given by $|z|=\sqrt{a^2+b^2}$.

**Definition (Complex conjugate).**
The **complex conjugate** of $z = x + iy$ is defined by
$$
\overline{z} = x - iy.
$$

**Definition (Modulus).**
The **modulus** (or absolute value) of $z = x + iy$ is defined by
$$
|z| = \sqrt{x^2 + y^2}.
$$

**Definition (Polar form).**
Every nonzero $z \in \mathbb{C}$ can be written as

$$
z = r e^{i\theta},\quad \text{where } r = |z| > 0,\ \theta = \arg(z) \in \mathbb{R}.
$$

The function $\arg(z)$ is multivalued unless a branch is specified.

**Definition (Path or curve).**
A **path** (or **curve**) in $\mathbb{C}$ is a continuous function $\gamma:[a,b]\to \mathbb{C}$.

* It is **piecewise smooth** if it is differentiable except at finitely many points and has piecewise continuous derivative.
* It is **closed** if $\gamma(a) = \gamma(b)$.
* It is **simple** if $\gamma$ is injective except possibly at endpoints.

Let $f:U\to \mathbb{C}$ be continuous, and let $\gamma:[a,b]\to U$ be a piecewise smooth path. The integral of $f$ along $\gamma$ is defined by
$$\int_\gamma f(z)\,dz:=\int_a^b f(\gamma(t))\gamma'(t)\,dt.$$

### **1. Cauchy’s Integral Theorem**

**Theorem (Cauchy’s Integral Theorem — simple version).**

Let $U \subseteq \mathbb{C}$ be an open set, and let $f:U\to \mathbb{C}$ be holomorphic. Let $\gamma$ be a closed, piecewise smooth path contained in $U$ that is **null-homotopic** (i.e., can be continuously deformed to a point within $U$). Then: $$\int_\gamma f(z)\,dz=0.$$
**Remarks:**
- The precise formulation often requires $U$ to be **simply connected**.
- This is the foundation for the deep relationship between complex differentiation and integration.

### **2. Cauchy’s Integral Formula**

**Theorem (Cauchy’s Integral Formula).**

Let $f$ be holomorphic on an open set $U \subseteq \mathbb{C}$, and suppose that $\overline{D_r(z_0)} \subseteq U$ for some $r > 0$. Then for every $z \in D_r(z_0)$,

$$

f(z) = \frac{1}{2\pi i} \int_{\partial D_r(z_0)} \frac{f(\zeta)}{\zeta - z} , d\zeta.

$$

- The integral is taken counterclockwise along the boundary of the disk.
- This formula allows evaluation of the value of a holomorphic function using only its boundary values.

**Theorem (Morera’s Theorem).**

Let $f:U \to \mathbb{C}$ be a continuous function on an open set $U \subseteq \mathbb{C}$. If for every closed, piecewise smooth path $\gamma$ in $U$,

$$

\int_\gamma f(z),dz = 0,

$$

then $f$ is **holomorphic** on $U$.

This is the converse of Cauchy’s theorem under the assumption of continuity.

---

### **4. Holomorphic Functions are Infinitely Differentiable**

If $f$ is holomorphic on an open set $U \subseteq \mathbb{C}$, then $f$ is **infinitely differentiable** on $U$.

Moreover, the derivatives can be expressed as:

$$

f^{(n)}(z) = \frac{n!}{2\pi i} \int_{\partial D} \frac{f(\zeta)}{(\zeta - z)^{n+1}},d\zeta,

$$

where $D$ is a closed disk around $z$ contained in $U$.

This means that holomorphic functions are **real-analytic**, and even more: they are **complex-analytic**.

> [!info] Taylor series (in the complex plane)
> Let $f$ be a holomorphic function in an open disk $D_r(z_0)\subseteq \mathbb{C}$. Then for all $z\in D_r(z_0)$, $$f(z)=\sum_{n=0}^\infty \frac{f^{(n)}(z_0)}{n!} (z-z_0)^n.$$