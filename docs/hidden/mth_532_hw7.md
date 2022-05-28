---
layout: problemset_topology_munkres2e
title: Homework 7
parent: (hidden)
permalink: hidden/mth_532_hw7
nav_order: 1
---

* TOC
{:toc}

---

<div class='problem_stmt' markdown='1'>
### Problem 75.2
If $K$ is the Klein bottle, calculate $H_1(K)$ directly.

{: .no_toc}
Recall from Problem 74.3(a) that

$$\fundgroup(K,p) = \ket{a,b \st aba\inv b\inv = 1}$$

Define $p: G \to \quotient{G}{[G,G]}$ to be the natural projection homomorphism that sends any group $G$ to its abelianization.

Define $F = \ket{a,b \st \emptyset}$ to be free group on 2 generators and $N = \ket{aba\inv b}^F$ to be the normal closure of one generator in $F$.

By Corollary 75.2,

$$\begin{align*}
  p\paren{\fundgroup(K,p)}
    &= p\paren{\quotient{F}{N}} \\
    &\isom \quotient{p(F)}{p(N)} \\
    &= \quotient{p(\ket{a,b})}{\ket{p(aba\inv b)}} \\
    &= \quotient{\ket{p(a)} \oplus \ket{p(b)}}{\ket{2p(b)}} \\
    &\isom \Z \oplus \Z_2.
\end{align*}$$

<div class='problem_notes' markdown='1'>
[Here's](https://mathworld.wolfram.com/FundamentalGroup.html) the result from Wolfram Alpha. Note that direct sums and cartesian products are the same.
</div>

</div>

---

<div class='problem_stmt' markdown='1'>
### Problem 75.3(b)
Let $X$ be the quotient space obtained from an 8-sided polygonal region $P$ by pasting its edges together according to the labelling scheme $acadbcb\inv{}d$. Calculate $H_1(X)$.

{: .no_toc}
#### Proof.

By Seifert-van Kampen,

$$
  \fundgroup(X, x_0) = \ket{a,b,c,d \st acadbcb\inv d = 1}
$$

Define $p: G \to \quotient{G}{[G,G]}$ to be the natural projection homomorphism that sends any group $G$ to its abelianization.

Using Corollary 75.2, we get

$$\begin{align*}
  p(\ket{a,b,c,d \st \emptyset}) &\isom \Z^4 \\
  p(acadbcb\inv d) &= 2p(a) + 2p(c) + 2p(d)
\end{align*}$$

To simplify notation, let $z := p(z)$. Then, we have

$$
  H_1(X) = \quotient{
    \ket{a} \times \ket{b} \times \ket{c} \times \ket{d}
  }{
    \ket{2a+2c+2d}
  }
$$

We can re-parametrize our generating set by defining $e = a+c+d$. Since $e = a+c+d$ and $d = e-a-c$, $e$ is also a generator. Then, considering the generating set,

$$
  \ket{a,b,c,d} = \ket{a,b,c,a+b+d} = \ket{a,b,c,e}
$$

Therefore,

$$\begin{align*}
  H_1(X)
    &= \quotient{
        \ket{a} \times \ket{b} \times \ket{c} \times \ket{e}
      }{
        \ket{2e}
      } \\
    &= \Z \times \Z \times \Z \times \quotient{\Z}{2\Z}
\end{align*}$$


<div class='problem_notes' markdown='1'>
Note that $acadbcb\inv d \sim aabbccdd$ by arguments in Problem 77.3(d). [See here](https://math.stackexchange.com/questions/912928/homology-group-of-3-fold-sum-of-projective-planes) for an example of the re-parametrization.
</div>

</div>

---

<div class='problem_stmt' markdown='1'>
### Problem 77.3(d)
The proof of the classification theorem provides an algorithm for taking a proper labelling scheme for a polygonal region and reducing it to one of the four standard forms indicated in the theorem. The appropriate equivalences are the following.
{: .remove-bottom-margin}
1. $[y_0]a[y_1]a[y_2] \sim aa[y_0y_1\inv{}y_2]$.
2. $[y_0]aa\inv[y_1] \sim [y_0y_1]$ if $y_0y_1$ has length at least 4.
3. $w_0[y_1]a[y_2]b[y_3]a\inv[y_4]b\inv[y_5] \sim w_0aba\inv b\inv [y_1 y_4 y_3 y_2 y_5]$.
4. $w_0(cc)(aba\inv b\inv)w_1 \sim w_0 aa bb cc w_1$.
{: .lower-roman}

Using this algorithm, reduce

$$
 \text{(d) } abcd a\inv b\inv c\inv d\inv
$$

to one of the standard forms.

{: .no_toc}
#### Answer.

$$\begin{align*}
  abcd a\inv b\inv c\inv d\inv
  &\overset{(iii)}{\sim} ab a\inv b\inv cd c\inv d\inv
\end{align*}$$

This is of form (4) in Theorem 77.5, $(a_1b_1a_1\inv b_1\inv)\cdots(a_nb_na_n\inv b_n\inv)$ for $n \geq 1$.
</div>

---
