---
layout: problemset_topology_munkres2e
title: Homework 8
parent: (hidden)
permalink: hidden/mth_532_hw8
nav_order: 1
---

* TOC
{:toc}

---

<div class='problem_stmt' markdown='1'>
### Problem 77.3(g)
The proof of the classification theorem provides an algorithm for taking a proper labelling scheme for a polygonal region and reducing it to one of the four standard forms indicated in the theorem. The appropriate equivalences are the following.
{: .remove-bottom-margin}
1. $[y_0]a[y_1]a[y_2] \sim aa[y_0y_1\inv{}y_2]$.
2. $[y_0]aa\inv[y_1] \sim [y_0y_1]$ if $y_0y_1$ has length at least 4.
3. $w_0[y_1]a[y_2]b[y_3]a\inv[y_4]b\inv[y_5] \sim w_0aba\inv b\inv [y_1 y_4 y_3 y_2 y_5]$.
4. $w_0(cc)(aba\inv b\inv)w_1 \sim w_0 aa bb cc w_1$.
{: .lower-roman}

Using this algorithm, reduce

$$
 \text{(g) } abcdabdc
$$

to one of the standard forms.


{: .no_toc}
#### Answer.

$$\begin{align*}
  abcdabdc
  &\overset{(i)}{\sim} aa d\inv c\inv b\inv b d c \\
  &\overset{(ii)}{\sim} aa d\inv c\inv d c \\
  &\overset{(iv)}{\sim} aa d\inv d\inv c\inv c\inv \\
  &\overset{\text{relabel}}{\sim} aabbcc.
\end{align*}$$

The given labelling scheme is of the third form in the classification theorem.

</div>

---

<div class='problem_stmt' markdown='1'>
### Problem 77.4
Let $w$ be a proper labelling scheme for a 10-sided polygonal region. If $w$ is of projective type, which is the list of spaces in Theorem 77.5 can it represent? What if $w$ is of torus type?

{: .no_toc}
#### Part (1).

Assume that $w$ is of the torus type. Then, cancellations are allowed since we can label two adjacent sides as $qq\inv$. For simpler notation, we'll omit the cancelled letters.

By Theorem 77.5, there are 3 possibilities up to isomorphism following forms (1) and (4):
{: .remove-bottom-margin}
1. $aa\inv bb\inv$ representing $S^2$,
2. $aba\inv b\inv$ representing $T$,
3. $(aba\inv b\inv)(cdc\inv d\inv)$ representing $T_2$.

{: .no_toc}
#### Part (2).

Now, assume that $w$ is of the projective type. Observe that cancellation of sides is still allowed. Then, by Theorem 77.5, there are 5 possibilities up to isomorphism following forms (2) and (4).
{: .remove-bottom-margin}
1. $abab$ representing $P$,
2. $aabb$ representing $P_2$,
3. $aabbcc$ representing $P_3$,
4. $aabbccdd$ representing $P_4$,
5. $aabbccddee$ representing $P_5$.


</div>

---

<div class='problem_stmt' markdown='1'>
### Problem 78.1(a)
What space is indicated by each of the following labelling schemes for a collection of four triangular regions?

$$
\text{(a) } abc, dae, bef, cdf
$$

{: .no_toc}
#### Answer.

Gluing the triangles together (also considering the orientation of the sides), we get

![glued triangle](/assets/images_hw/mth_532_hw8_triangle.jpg){: width='250px'}

Then, we get the labelling scheme

$$\begin{align*}
  cde\inv cd\inv e\inv
  &\overset{(i)}{\sim} cced\inv d\inv e\inv \\
  &\overset{(i)}{\sim} d\inv d\inv cc e e\inv \\
  &\overset{(ii)}{\sim} d\inv d\inv cc \\
  &\overset{\text{relabel}}{\sim} aabb
\end{align*}$$

representing the surface $P_2$

</div>

---
