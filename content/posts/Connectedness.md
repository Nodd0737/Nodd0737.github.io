+++
date = '2024-08-04T15:44:10-04:00'
draft = true
title = "Connectedness"
categories = 'Math'
ShowToc = true
tags = [ "General Topology" ]
+++
## Connectedness

> [!info] Connected space
> A topological space is **disconnected** if it can be expressed as the union of two disjoint, nonempty open subsets. Otherwise, it is **connected**.

> [!abstract] The continuous image of a connected space is connected
> Let $X$ and $Y$ be topological spaces and $f:X\to Y$ a continuous map. If $X$ is connected, then $f(X)$ is connected in $Y$.
>> [!success] Proof

> [!idea] Homeomorphism preserves connectedness
> Let $X$ and $Y$ be topological spaces and $f:X\to Y$ a homeomorphism. If $X$ is connected, then $Y$ is also connected.

> [!abstract] Equivalent characterizations of connectedness
> For a topological space $X$, the following statements are equivalent:
> 
> $(a)$ $X$ is disconnected.
> 
> $(b)$ $X$ can be expressed as the union of two disjoint, nonempty closed subsets.
> 
> $(c)$ $X$ has at least one nontrivial clopen subset.
> 
> $(d)$ There exists a continuous surjection $f:X\to \{0,1\}$.
> > [!success] Proof
> > Let $X=A\cup B$, where $A$ and $B$ are disjoint, nonempty open subsets of $X$.
> > 
> > $(a)\implies (b)$: Note that $A=X\setminus B$ is closed, and likewise $B=X\setminus A$ is closed. This expresses $X$ as the union of two disjoint, nonempty closed sets.
> > 
> > $(b)\implies (c)$: We know that $A$ (and $B$) are both open and closed. Thus, $X$ has at least one nontrivial clopen subset.
> > 
> > $(c)\implies (d)$: Let $C\subset X$ be clopen, and then $X\setminus C$ is also clopen. Define
> > $$f(x)=\begin{cases}0 & \text{if } x\in C, \\ 1 & \text{if } x\in X \setminus C.\end{cases}$$
> > Now $f$ is a surjection with $f^{-1}(\{0\})=C$ and $f^{-1}(\{1\})=X\setminus C$. Since $\{0\}$ and $\{1\}$ are open in the discrete space $\{0,1\}$, $f$ is continuous.
> > 
> > $(d)\implies (a)$: 

> [!info] Totally disconnected space

A topological space $X$ is **totally disconnected** if its connected components are all singletons. Equivalently:
- For any two distinct points $x,y\in X$, there exists a separation $X = U \sqcup V$ (where $U$ and $V$ are disjoint open sets) with $x \in U$ and $y \in V$.  

**Examples:**  
1. The Cantor set (with the subspace topology from $\mathbb{R}$).  
2. The space $\mathbb{Q}$ of rationals (with the Euclidean topology).  
3. Any discrete space.

Relation to Totally Disconnected Spaces:
- A space can be neither (e.g., $\mathbb{Q}$) or one but not the other (e.g., the Cantor set is totally disconnected but not arcwise connected).
## Path-Connectedness

> [!info] Path
> A **path** in a topological space $X$ is a continuous map $f:[0,1]\to X$. The point $f(0)$ is called the **initial point**, and $f(1)$ is the **final point**.
> 
> In particular, a **loop** is a path with $f(0)=f(1)$.

From now on, we will use $I$ to denote the unit interval $[0,1]$.

> [!info] Path-Connected space
> A topological space $X$ is **path-connected** if for any two points $x,y\in X$, there exists a path $f:I\to X$ with $f(0)=x$ and $f(1)=y$.

> [!abstract] Path-connectedness implies connectedness
> Every path-connected space is connected.
>> [!success] Proof
>> Assume, for contradiction, that there exists a path-connected topological space $X$ which is not connected. Then there exist two non-empty, disjoint open subsets $U$ and $V$ of $X$ such that $X=U\cup V$. Since $X$ is path-connected, for any $x\in U$ and $y\in V$, there exists a continuous path $f:I\to X$ such that $f(0)=x$ and $f(1)=y$.
>> Because $U,V$ are open in $X$ and $f$ is continuous, the preimages $f^{-1}(U)$ and $f^{-1}(V)$ are open in $I$. It's clear that these sets are nonempty, disjoint, and satisfy $I=f^{-1}(U)\cup f^{-1}(V)$. This contradicts the fact that $I$ is connected.
>> Therefore, the initial assumption is false, and we conclude that every path-connected space is connected.

> [!info] Locally path-connected space

> [!info] Connected component
> Let $X$ be a topological space and $x\in X$ a point. The **connected component** of $x\in X$ is the maximal connected subset of $X$ containing $x$.
## Exercises

> [!question] Problem 1
> A topological space $X$ is **arcwise connected** if for any two points $x,y\in X$, there exists a topological embedding $f:[0,1]\to X$ with $f(0)=x$ and $f(1)=y$.
> 
> Show that a Hausdorff space is arcwise connected if and only if it is path-connected.