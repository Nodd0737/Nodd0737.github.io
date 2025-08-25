+++
date = '2023-03-09T15:44:10-04:00'
draft = false
title = 'Topological Spaces: Basics'
categories = 'Math'
ShowToc = true
tags = [ "General Topology", "Basics" ]
+++
## Basic definitions

> [!info] Topological space
> Given a nonempty set $X$, a collection $\mathcal{T}$ of subsets of $X$ is called a **topology** on $X$ if it satisfies the following conditions:
> - $X$ and $\emptyset$ are in $\mathcal{T}$.
> - The union of any collection of sets in $\mathcal{T}$ is also in $\mathcal{T}$.
> - The intersection of any finite number of sets in $\mathcal{T}$ is also in $\mathcal{T}$.
> 
> In this case, the pair $(X, \mathcal{T})$ is called a **topological space**.  
>> [!example] Examples
>> 1. Consider the set $X=\{a,b,c,d,e,f\}$. The collection $\mathcal{T}=\{X,\emptyset,\{a\},\{c,d\},\{a,c,d\},\{b,c,d,e,f\}\}$ is a topology on $X$.
>> 2. Given a nonempty set $X$, the **discrete topology** on $X$ is the topology consisting of all subsets of $X$. The **indiscrete**, or **trivial topology** on $X$ consists only of $\{X,\emptyset\}$.
>> 3. Every metric space is naturally a topological space. Specifically, given a metric space $(X,d)$, define $\mathcal{T}$ as the collection of subsets $U \subseteq X$ such that for every $x\in U$, there exists $r>0$ with $$B_r(x)=\{y\in X\mid d(x,y)< r\}\subseteq U.$$ This topology is called the **metric topology** induced by $d$ since it is constructed directly from the definition of open sets in a metric space.

A particular type of topology is important because it defines the topology on a subspace of a topological space.

> [!info] Subspace topology
> Given a topological space $(X,\mathcal{T})$ and a subset $Y\subset X$, the collection $\mathcal{T}_Y=\{U\cap Y\mid U\in \mathcal{T}\}$ forms a topology on $Y$, called the **subspace topology**. The resulting space $(Y,\mathcal{T}_Y)$ is a subspace of $(X,\mathcal{T})$.

> [!info] Open set & Closed set
> Let $(X,\mathcal{T})$ be a topological space.
> - A subset $U\subseteq X$ is an **open set** if it belongs to $\mathcal{T}$.
> - A subset $C\subseteq X$ is a **closed set** if its complement $X\setminus C$ is open.

> [!important] Open and closed sets are not mutually exclusive concepts. A set can be open but not closed, closed but not open, neither open nor closed, or both open and closed. Sets that are both open and closed are called *clopen* sets.

From now on, unless it may cause confusion, the topological space $(X,\mathcal{T})$ will be abbreviated as $X$.

> [!info] Open map & Closed map
> Let $f:X\to Y$ be a map between topological spaces.
> - $f$ is an **open map** if for every open set $U\subseteq X$, the image $f(U)\subseteq Y$ is open.
> - $f$ is an **closed map** if for every closed set $C\subseteq X$, the image $f(C)\subseteq Y$ is closed.

For convenience, many mathematical texts use the term "neighborhood". However, this term can be ambiguous. Below is a widely accepted definition.

> [!info] Neighborhood
> Given a topological space $X$, a **neighborhood** of a point $x\in X$ is a set $U\subset X$ that contains an open set $Y$ with $x\in Y$. In particular, if $U$ itself is open and contains $x$, then $U$ is called an **open neighborhood** of $x$.

> [!danger] Remark  
> The ambiguity arises because many authors use the term "neighborhood" to refer specifically to an open neighborhood. To ensure clarity, we will avoid this usage.

A set may have multiple topologies and we can compare them.

> [!info] Comparison of topologies
> Let $X$ be a nonempty set and $\mathcal{T}_1,\mathcal{T}_2$ topologies on $X$. If $\mathcal{T}_1\subseteq \mathcal{T}_2$, then we say that $\mathcal{T}_2$ is **finer/larger/stronger** than $\mathcal{T}_1$, and that $\mathcal{T}_1$ is **coarser/smaller/weaker** than $\mathcal{T}_2$. In particular, if $\mathcal{T}_1\subset \mathcal{T}_2$, then $\mathcal{T}_2$ is said to be **strictly finer** than $\mathcal{T}_1$, and similarly for the other terms.

It is easy to see that on an nonempty set, the discrete topology is the finest, and the trivial topology is the coarsest.
## Continuous map and homeomorphism

Before defining homeomorphisms, we first need to extend the notion of continuity to topological spaces.

> [!info] Continuous map
> A map $f:X\to Y$ between topological spaces is continuous if for every open set $V\subseteq Y$, its preimage $f^{-1}(V)$ is an open set in $X$.

> [!note] Gluing lemma
> Let $X=A\cup B$ be a topological space, where $A$ and $B$ are both open, or both closed, subsets of $X$. If $f:A\to Y$ and $g:B\to Y$ are continuous functions with $f(x)=g(x)$ for all $x\in A\cap B$, then the function $h:X\to Y$ defined by:  
> $$h(x)=\begin{cases}f(x), & \text{if } x\in A; \\ g(x), & \text{if } x\in B\end{cases}$$
> is also continuous.
> > [!success] Proof

> [!info] Limit of a sequence (in a topological space)
> Given a topological space $X$ and a sequence $\{x_n\}$ in $X$, an element $x \in X$ is called a limit of $\{x_n\}$ if for every open neighborhood $U$ of $x$, there exists $N\in \mathbb{N}$ such that $x_n\in U$ for all $n>N$. This is denoted by $x_n\to x$.

> [!info] Homeomorphism
> A bijective continuous map $f:X\to Y$ between topological spaces is called a **homeomorphism** if its inverse $f^{-1}:Y\to X$ is also continuous. In this case, $X$ and $Y$ are said to be **homeomorphic**, denoted by $X\cong Y$.

> [!info] Topological embedding
> A continuous map $f:X\to Y$ between topological spaces is called a **topological embedding** if $f$ is a homeomorphism onto its image $f(X)\subseteq Y$.