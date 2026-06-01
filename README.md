This repository contains the source of the **Entanglement E2** Cosmochrony paper  
[*Two Entanglement Entropies of the Conjugate Weil Pair: the Admissible Pair Sector and the Full Residual Rank*](out/EntanglementE2.pdf).

This paper separates two genuinely different entanglement entropies of the
closed conjugate Weil pair $\{c, q-c\}$ that the companion entanglement note
and the orthogonality paper E1 establish on two distinct projections.
Conflating them produces an apparent tension between an unconditional $\log 2$
and a depth-dependent $\log r_{\mathrm{pair}}(n)$. The separation is not
cosmetic: the two objects live on projections of different rank, have different
physical roles, and have different epistemic status.

## Central Question

> Which entanglement entropy of the conjugate Weil pair is the one behind the
> Bell--Tsirelson sector, and on what conditions does the residual-rank
> formula $S_{\mathrm{ent}}(n) = \log r_{\mathrm{pair}}(n)$ rest for general
> blocks?

## Two distinct objects

| Object | Projection | Rank | Role |
|---|---|---|---|
| Admissible pair sector $\mathcal{A}_c$ | $\Pi_q$ (rank-3 admissible) | 2 (after removing $e_0$) | Spin-$\tfrac12$ singlet, Bell--Tsirelson |
| Residual fibre-level support | Full Gram--Schmidt basis | $r_{\mathrm{pair}}(n) = R_\infty - R(n)$, with $R_\infty = q$ | Pipeline-level contraction observable |

The first is fixed by **spectral atomicity** (O21 Proposition 4.1): the rank-3
admissible projection is
$\mathrm{ran}(\Pi_q^{(c)}) = \mathrm{span}\{e_0, e_{\xi_c}, e_{q-\xi_c}\}$;
after the mean-zero lemma removes $e_0$, the Born--Infeld parity pair
$\{e_{\xi_c}, e_{q-\xi_c}\}$ is the two-dimensional spin-$\tfrac12$
representation $V_{1/2}$.

## Core Results

### Theorem (Admissible pair entropy)

The proto-state on $\mathcal{A}_c \otimes \mathcal{A}_c$ is the spin-$\tfrac12$ singlet
$$
|\Omega_c\rangle = \frac{1}{\sqrt{2}}\bigl(|\xi_c\rangle \otimes |q-\xi_c\rangle - |q-\xi_c\rangle \otimes |\xi_c\rangle\bigr),
$$
its reduced state is $\rho^{\mathrm{adm}}_c = \tfrac12 \mathbf{1}_2$, and
$$
S_{\mathrm{ent}}^{\mathrm{adm}} = \log 2.
$$
The proof uses spectral atomicity (O21), the mean-zero lemma, and the singlet
identification from Q3 Theorem 4.1 (Born--Infeld indiscernibility +
Clebsch--Gordan $V_{1/2} \otimes V_{1/2} = V_0 \oplus V_1$). The statement
holds for **general canonical blocks**, unconditionally relative to the cited
upstream theorems.

### Residual-rank entropy (status)

| Case | Status |
|---|---|
| Matched single-character blocks | **Proved** by E1 Theorem 7: $S_{\mathrm{ent}}(n) = \log r_{\mathrm{pair}}(n)$ unconditional |
| Independently sampled canonical blocks | **Conditional** on $[\mathrm{H}_{\mathrm{res}}]$: residual admissibility indiscernibility |
| Metaplectic dilation as bridge for $[\mathrm{H}_{\mathrm{res}}]$ | **Excluded** (acts between blocks, not within the residual support of a single block) |

The hypothesis $[\mathrm{H}_{\mathrm{res}}]$ has a status parallel to the
conditional hypotheses $[\mathrm{H\text{-}color}]$ and $[\mathrm{H\text{-}ext}]$
elsewhere in the programme.

## Bell--Tsirelson connection

The entanglement that CHSH experiments measure is carried by the spin-$\tfrac12$
singlet. By the admissible pair theorem, this is exactly the admissible pair
sector with $S_{\mathrm{ent}}^{\mathrm{adm}} = \log 2$. The singlet correlator
$E(\hat a, \hat b) = -\hat a \cdot \hat b$ and the unconditional Tsirelson
bound $|S_{\mathrm{CHSH}}| \leq 2\sqrt{2}$ are derived from the same admissible
structure in Q1 (Theorem 2.14 and Corollary 2.16). The admissible pair entropy
is therefore the entanglement entropy of the state behind those results.

The full residual-rank entropy $S_{\mathrm{ent}}(n) = \log r_{\mathrm{pair}}(n)$
is a finer pipeline-level observable that tracks the contraction of the full
Gram--Schmidt span toward saturation. It is **not** the quantity measured by a
Bell experiment, and it should not be identified with the singlet entropy. The
two coincide only in the degenerate case $r_{\mathrm{pair}}(n) = 2$.

## Position in the Programme

Constituent of the **entanglement sub-programme**
([ENT-Note](https://doi.org/10.5281/zenodo.20498835)). The result chain on
which the present note rests is:

- **O21** ([Beau2026q5ao2](https://doi.org/...)): spectral atomicity (Proposition 4.1) and the mean-zero lemma (Lemma 3.1);
- **O29** ([Beau2026a33](https://doi.org/...)) and **O30** ([Beau2026a34](https://doi.org/...)): admissible rank exactly three, with the analytical backing of the rank-3 input;
- **O17** ([Beau2026a21](https://doi.org/...)): equality of conjugate pair residual dimensions;
- **E1** ([Beau2026ent1](https://doi.org/10.5281/zenodo.20499309)): universal admission orthogonality, matched-block flat Schmidt spectrum, and the open Schmidt-pairing question for general blocks;
- **Q3** ([Beau2026q3](https://doi.org/...)): Born--Infeld indiscernibility singlet identification (Theorem 4.1);
- **Q1** ([Beau2026q1](https://doi.org/...)): singlet correlator and the unconditional Tsirelson bound (Theorem 2.14, Corollary 2.16).

## Build

```bash
bash compile.sh
```

This runs `pdflatex → bibtex → pdflatex → pdflatex` on
`tex/EntanglementE2.tex` and produces `out/EntanglementE2.pdf`.
