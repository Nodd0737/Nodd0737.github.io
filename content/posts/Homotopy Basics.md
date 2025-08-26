+++
date = '2024-09-09T15:44:10-04:00'
draft = false
title = 'Homotopy: Basics'
categories = 'Math'
ShowToc = true
math = true
tags = [ "Algebraic Topology", "Basics" ]
+++

> [!info] Homotopy
> Let $f,g:X\to Y$ be continuous maps between topological spaces. A **homotopy** between $f$ and $g$ is a continuous map $H:X\times I\to Y$ satisfying $H(x,0)=f(x)$ and $H(x,1)=g(x)$ for all $x\in X$. In this case, $f$ and $g$ are said to be **homotopic**, denoted by $f\simeq g$.

Let $A$ be a subspace of $X$. If the homotopy $H$ described above satisfies $H(a,t)=f(a)=g(a)$ for all $a\in A$ and $t\in I$, we say that $f$ and $g$ are **homotopic relative to** $A$, denoted by $f\simeq g\; (\text{rel }A)$.

> [!danger] Note
> The homotopy is clearly an equivalence relation. The set of all maps homotopic to a given map $f$ is called the **homotopy class** of $f$, denoted by $[f]$.

The null-homotopy is a special case of homotopy.

> [!info] Null-homotopy
> A continuous map is **null-homotopic** if it's homotopic to a constant map.

> [!info] Contractibility
> A topological space is **contractible** if its identity map is null-homotopic.

> [!info] Homotopy equivalence  
> Given topological spaces $X$ and $Y$, if there exist continuous maps $f:X\to Y$ and $g:Y\to X$ such that  $g\circ f\simeq \text{id}_X$ and $f\circ g\simeq \text{id}_Y$, then $X$ and $Y$ are said to be **homotopy equivalent**, or to have the same **homotopy type**.

> [!info] Retract
> Given a topological space $X$, a subspace $A\subseteq X$ is a **retract** of $X$ if there exists a continuous map $r:X\to A$, called a **retraction**, such that $r(a)=a$ for all $a\in A$.

> [!info] Deformation retract
> Given a topological space $X$, a subspace $A\subset X$ is a **deformation retract** of $X$ if there exists a continuous map $H:X\times I\to X$, called a **deformation retraction**, such that
> - $H(x,0)=x$ for all $x\in X$,
> - $H(x,1)\in A$ for all $x\in X$,
> - $H(a,t)=a$ for all $a\in A$ and $t\in [0,1]$.

> [!abstract] Deformation retraction gives homotopy equivalence
> If a topological space $A$ is a deformation retract of another topological space $X$, then $A$ and $X$ are homotopy equivalent.