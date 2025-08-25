+++
date = '2024-06-08T15:44:10-04:00'
draft = true
title = 'Metrizability and Classical Results of Urysohn and Tietze'
categories = 'Math'
+++

> [!note] Urysohn's lemma
> A topological space $X$ is normal if and only if for any two disjoint closed sets $A,B\subset X$, there exists a continuous function $f:X\to [0,1]$ such that $f(a)=0$ for all $a\in A$ and $f(b)=0$ for all $b\in B$.
> > [!success] Proof

> [!info] Metrizable space
> A topological space $X$ is **metrizable** if its topology is induced by some metric $d$ on $X$.

> [!important] A metrizable space is not merely similar to a metric space. It is topologically identical to a metric space, though the specific metric may not be specified.

> [!note] Urysohn metrization theorem
> A topological space is metrizable if and only if it is Hausdorff, regular and second-countable.
> > [!success] Proof
> > 

> [!note] Tietze extension theorem
> Let $X$ be a normal space and $A\subseteq X$ a closed subset. If $f:A\to \mathbb{R}$ is continuous, then there exists a continuous extension $\tilde{f}:X\to \mathbb{R}$ such that $\tilde{f}|_A=f$.
