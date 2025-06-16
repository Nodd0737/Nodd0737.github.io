+++
date = '2024-06-15T15:44:10-04:00'
draft = true
title = 'Compactness II'
categories = 'Math'
+++

> [!warning] Prerequisite
## Other Compactness

> [!info] Definition: sequential compactness  
> A topological space $X$ is called **sequentially compact** if every sequence in $X$ has a convergent subsequence whose limit is in $X$.

> [!info] Definition: countable compactness
> A topological space $X$ is called **countably compact** if every countable open cover of $X$ has a finite subcover.

> [!info] Definition: limit point compactness
> A topological space $X$ is called **limit point compact** if every infinite subset of $X$ has a limit point in $X$.
## Relationship between different compactness

> [!abstract] Proposition
> 1. Every compact space is countably compact.
> 2. Every sequentially compact space is countably compact.
> 3. Every countably compact space is limit point compact.

> [!success] Proof
> 1. Trivial. Compactness implies countable compactness by definition.
> 2. Suppose $X$ is sequentially compact. Assume, for contradiction, that there exists a countable open cover $\mathcal{U}=\{U_n:n\in \mathbb{N}\}$ of $X$ that admits no finite subcover. Then for each $n\in \mathbb{N}$, the finite union $U_1\cup U_2\cup \cdots\cup U_n$ is a proper subset of $X$. Based on this, we can construct a sequence $\{x_n\}$ in $X$ by choosing points $x_n\in X\setminus (U_1\cup U_2\cup \cdots\cup U_n)$. Since $X$ is sequential compact, there exists a subsequence $\{x_{n_k}\}$ converging to some point $x\in X$.
> $\mathcal{U}$ covers $X$, so there exists an index $m$ for which $x\in U_m$. Since $U_m$ is open and $x_{n_k}\to x$, there exists $K\in \mathbb{N}$ such that for all $k>K$, $x_{n_k}\in U_m$. However, by the construction of the sequence, if $n_k>m$, then $x_{n_k}\notin U_m$, which leads to a contradiction. Hence, the assumption is false, implying that $X$ should be countably compact.
> 3. Suppose $X$ is countably compact and let $A\subset X$ be an infinite set. Assume, for contradiction, that $A$ has no limit point in $X$. Then for each $a\in A$ there exists an open neighborhood $U_a$ of $a$ such that $U_a\cap A=\{a\}$. Since $A$ is infinite, we can extract a countably infinite subset $B\subset A$. 
> Consider the countable collection of sets $\mathcal{U}=\{U_b:b\in B\}\cup \{X \setminus B\}$. Note that $\mathcal{U}$ is the union of open sets and contains $X$, so it's an open cover of $X$. Since $X$ is countably compact, there exists a finite subcover of $\mathcal{U}$. However, a finite subcollection of $\{U_b:b\in B\}$ covers only finitely many points of $B$, and $X\setminus B$ covers no point of $B$. Thus, any finite subcover of $\mathcal{U}$ cannot cover $B\subset X$, which leads to a contradiction. Hence, the assumption is false, implying that $X$ should be limit point compact.

When the underlying space has certain properties, open cover compactness and sequential compactness become equivalent. This is the case, for example, in metric spaces, which are central to analysis.

> [!abstract] Equivalence of compactness in metric spaces
> Given a metric space $(X,d)$, the following statements are equivalent:
> 1. $X$ is compact.
> 2. $X$ is sequentially compact.
> 3. $X$ is countably compact.
> 4. $X$ is limit point compact.
> 5. $X$ is complete and totally bounded.

$\mathbb{R}^n$ is a special case of metric spaces, so the proposition above naturally works on it. In fact, both of the following theorems, which are very important in fundamental analysis, are only part of this proposition.

> [!note] Bolzano-Weierstrass theorem
> Every bounded sequence in $\mathbb{R}^n$ has a convergent subsequence.

> [!note] Heine-Borel theorem
> A subset of $\mathbb{R}^n$ is compact if and only if it is closed and bounded.