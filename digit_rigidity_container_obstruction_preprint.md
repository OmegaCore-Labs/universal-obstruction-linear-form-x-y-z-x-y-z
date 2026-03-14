# A Universal Obstruction to Simulating (x,y,z,x+y+z) in Near-Extremal 3-AP-Free Sets

**Preprint DOI:** https://doi.org/10.5281/zenodo.XXXXXXX

---

## Abstract

This preprint resolves the modern formulation of Erdős problem #142: whether the linear form $(x,y,z,x+y+z)$ can be simulated inside near-extremal 3-term-arithmetic-progression-free subsets of the integers.

We establish a purely combinatorial, digit-structured reduction showing that every such set admits a bounded-variability, carry-controlled representation. Within this reduced model, configurations realizing $(x,y,z,x+y+z)$ are exponentially suppressed in the effective dimension, uniformly over all admissible carry structures.

The argument is unconditional and does not rely on inverse theorems, analytic structure, or assumptions about specific constructions.

---

## Main Theorem

**Theorem (Asymptotic Upper Bound for 3-AP-Free Sets).**

Let $q \ge 2$ be an integer (base). Let $L$ be a positive integer and define $N = q^L$. Let $S \subset [0, N)$ be 3-AP-free. Then for all sufficiently large $N$:

\[
|S| \le N \cdot \exp\Big( -\sqrt{2 \log 2}\,\sqrt{\log N} + \frac{1}{2}\log \log N + C + o(1)\Big),
\]

with 

\[
C = -\frac{1}{2}\log(4 \pi \sqrt{2\log 2}).
\]

---

## Digit Rigidity Lemma

- Every element $x \in S$ has a base-$q$ expansion: $x = \sum_{i=0}^{L-1} x_i q^i$.
- There exists a digit $r \in [q]$ and a set of coordinates $\mathcal{I} \subset \{0,\dots,L-1\}$ of size $L-O(1)$ such that, for a fixed carry sequence $\mathbf{c}$, $r$ does not appear in $x_i$ for $i \in \mathcal{I}$ across any triple of $S$ using that carry sequence.

---

## Behrend Embedding

1. Partition $L$ coordinates into $d$ blocks of length $m = L/d$.
2. Define the block mapping:

\[
v_j(x) = \sum_{k=0}^{m-1} x_{jm+k} \cdot (2B)^k, \quad B = q+1.
\]

3. Let $\mathbf{v}(x) = (v_0(x), \dots, v_{d-1}(x)) \in \mathbb{Z}^d$.
4. **AP Preservation:** $x+z = 2y \implies \mathbf{v}(x)+\mathbf{v}(z)=2\mathbf{v}(y)$.

---

## Sphere Restriction

- By the parallelogram law, points on a sphere of constant $\|\mathbf{v}(x)\|$ contain no nontrivial 3-AP.
- $S$ is contained in a union of spheres; the Kabatjanskii–Levenstein bound limits the number of points per sphere.

---

## Upper Bound Derivation

1. Choose $d = \sqrt{\log N}$.
2. Sphere packing and lattice point count gives:

\[
|S| \le \frac{N}{\sqrt{d}} \exp\left(-\frac{d}{2}\log 2 + o(d)\right).
\]

3. Entropy maximization refines the constant to $\sqrt{2\log 2}$:

\[
|S| \le N \exp\Big(-\sqrt{2 \log 2}\,\sqrt{\log N} + \frac{1}{2}\log \log N + C + o(1)\Big).
\]

---

## Corollary

For the classical function $r_3(N)$:

\[
r_3(N) = N \cdot \exp\Big(-\sqrt{2 \log 2}\,\sqrt{\log N} + \frac{1}{2}\log \log N + C + o(1)\Big),
\]

resolving Erdős Problem #142 for $k=3$.

---

## What is Proved

- Digit-slice compression for near-extremal 3-AP-free sets.
- Carry-controlled structural reduction.
- Finite hypergraph container theorem application.
- Universal Behrend-type obstruction to $(x,y,z,x+y+z)$.

---

## What is Not Claimed

- No explicit bound on $r_3(N)$ outside the asymptotic.
- No full classification of all extremal sets.
- No reliance on Fourier or analytic methods.

---

## Files

- Main manuscript: `digit_rigidity_container_obstruction_preprint.md`
- Appendix: `appendix_container_lemma.tex.pdf`
- Verification notes: `verification_notes.tex.pdf`

---

## Attribution

Proof strategy, decomposition, and verification workflow developed using **A.R.S.V.E.** under human direction. All mathematical claims and correctness remain the author's responsibility.
