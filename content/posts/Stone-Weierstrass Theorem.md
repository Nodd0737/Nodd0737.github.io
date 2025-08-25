+++
date = '2024-09-20T15:44:10-04:00'
draft = true
title = 'Stone-Weierstrass Theorem'
categories = 'Math'
+++

Given a topological space $X$, let $\mathcal{C}(X,\mathbb{R})$ denote the set of all continuous functions $f:X\to \mathbb{R}$. Recall this famous theorem in basic analysis:

> [!note] Weierstrass approximation theorem
> Let $f\in \mathcal{C}([a,b],\mathbb{R})$. Then for every $\varepsilon>0$, there exists a polynomial $p$ such that $$\sup_{x\in [a,b]} |f(x)-p(x)|<\varepsilon.$$
> In other words, if $\mathcal{P}$ denotes the set of all polynomials on $[a,b]$, then $\mathcal{P}$ is dense in $\mathcal{C}([a,b],\mathbb{R})$.

We now aim to generalize this theorem to compact Hausdorff spaces. Later on, we will also see a version that applies to locally compact Hausdorff (LCH) spaces.
## Preparations

The classical statement of the Stone-Weierstrass theorem involves several concepts that you may not have encountered before, so we need to introduce them first.

> [!info] Algebra
> 

> [!info] Subalgebra

> [!info] 

> [!note] Stone-Weierstrass theorem

Let $X$ be a compact Hausdorff space, and let $\mathcal{A} \subseteq C(X, \mathbb{R})$ be a subalgebra of the continuous real-valued functions on $X$ satisfying:
1. **Separates points**: For any $x, y \in X$ with $x \neq y$, there exists $f \in \mathcal{A}$ such that $f(x) \neq f(y)$.
2. **Contains constants**: The constant function $1$ is in $\mathcal{A}$.  

Then $\mathcal{A}$ is dense in $C(X,\mathbb{R})$ with respect to the uniform norm $\|f\|_\infty=\sup_{x\in X} |f(x)|$.  

**Complex version**: If $\mathcal{A} \subseteq C(X, \mathbb{C})$ is a subalgebra that separates points, contains constants, and is closed under complex conjugation ($f \in \mathcal{A} \implies \overline{f} \in \mathcal{A}$), then $\mathcal{A}$ is dense in $C(X, \mathbb{C})$.  