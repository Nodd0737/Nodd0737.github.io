+++
date = '2022-12-28T15:44:10-04:00'
draft = false
title = "Rings and Fields: Basics"
categories = 'Math'
ShowToc = true
tags = [ "Abstract Algebra", "Basics" ]
+++

Since we already have a background in group theory, we can move quickly through some basic definitions and propositions about rings and fields. However, it's worth noting that while rings and fields build upon group structures, their study involves fundamentally different concepts and methods compared to group theory.
## Basic definitions related to rings

> [!info] Ring
> A **ring** is a set $R$ together with two binary operations, addition $(+)$ and multiplication $(\cdot)$, such that for all $a,b,c\in R$:
> - $(R,+)$ is an abelian group with identity element $0$.
> - Multiplication is associative, that is, $(a\cdot b)\cdot c=a\cdot(b\cdot c)$.
> - The distributivity laws hold, that is, $a\cdot(b+c)=a\cdot b+a\cdot c$ and $(b+c)\cdot a=b\cdot a+c\cdot a$.
> 
> In particular:
> - $R$ is called **commutative** if $a\cdot b=b\cdot a$ for all $a,b\in R$.
> - $R$ is said to be a **ring with unity** or **unital ring** if there exists an element $1\neq 0$ such that $1\cdot a=a\cdot 1=a$ for all $a\in R$.

> [!info] Subring
> A **subring** of a ring $R$ is a subset $S\subseteq R$ that is itself a ring under the same operations.

> [!info] Ring homomorphism & Ring isomorphism
> A map $\phi:R\to S$ between rings $R$ and $S$ is a **ring homomorphism** if for all $a,b\in R$:
> - $\phi(a+b)=\phi(a)+\phi(b)$.
> - $\phi(a\cdot b)=\phi(a)\cdot \phi(b)$.
> 
> If $R$ and $S$ are unital, then $\phi(1_R)=1_S$.
> 
> A bijective ring homomorphism is a **ring isomorphism**.

> [!info] Zero divisor
> Given a ring $R$, a nonzero element 

> [!info] Integral domain
> An **integral domain** is a commutative ring with unity that has no zero divisors.

Let $R$ be a ring. A nonzero element $a\in R$ is a **zero divisor** if there exists a nonzero $b\in R$ such that
$$
ab = 0 \quad \text{or} \quad ba = 0.
$$

In a **commutative** ring, these are equivalent.


## Basic definitions related to fields

When studying vector spaces, some instructors prefer to be rigorous and list the full definition of a field, while others choose to avoid this and simply state that $\mathbb{F}$ is either $\mathbb{R}$ or $\mathbb{C}$. Here, we will define a field based on the concepts of groups and rings.

> [!info] Field
> A **field** is a set $F$ together with two binary operations, addition $(+)$ and multiplication $(\cdot)$, such that:
> - $(F,+)$ is an abelian group with identity element $0$.
> - $(F\setminus \{0\},\cdot)$ is an abelian group with unity $1$.
> - The distributivity laws hold, that is, $a\cdot(b+c)=a\cdot b+a\cdot c$ and $(b+c)\cdot a=b\cdot a+c\cdot a$ for all $a,b,c\in F$.

> [!important] More concisely, a field is a commutative ring with unity in which every nonzero element has a multiplicative inverse.

> [!info] Subfield
> A **subfield** of a field $F$ is a subset $K\subseteq F$ that is itself a field under the same operations.

Every field is an integral domain.

A **field extension** $F\subseteq E$ is an inclusion of fields (where $F$ is a subfield of $E$). The **degree** of the extension, $[E : F]$, is the dimension of $E$ as an $F$-vector space.  

**Example:** $[\mathbb{C}:\mathbb{R}]=2$.  
#### **3. Characteristic**
The **characteristic** of a field $F$, denoted $\text{char}(F)$, is the smallest positive integer $p$ such that $p \cdot 1 = 0$. If no such $p$ exists, $\text{char}(F) = 0$.  

**Examples:**  
- $\text{char}(\mathbb{Q}) = 0$.  
- $\text{char}(\mathbb{F}_p) = p$ (where $\mathbb{F}_p = \mathbb{Z}/p\mathbb{Z}$).  
#### **4. Prime Field**
The **prime field** of $F$ is its smallest subfield:  
- If $\text{char}(F) = 0$, the prime field is $\mathbb{Q}$.  
- If $\text{char}(F) = p$, the prime field is $\mathbb{F}_p$.
