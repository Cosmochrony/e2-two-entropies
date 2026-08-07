This repository contains the source of the **Entanglement E2** Cosmochrony paper  
*Two Entanglement Entropies of the Conjugate Weil Pair: the Admissible Pair Sector and the Full Residual Rank*.

This paper separates two genuinely different entanglement entropies of the
closed conjugate Weil pair $\{c, q-c\}$ that the companion entanglement note
and the orthogonality paper E1 establish on two distinct projections, and
which carry different epistemic status. The separation is not cosmetic: the
two objects live on projections of different rank, have different physical
roles, and have different epistemic status.

## Central Question

> Which entanglement entropy of the conjugate Weil pair is the one determined
> by the admissible sector's own structure, and on what conditions does the
> residual-rank formula $S_{\mathrm{ent}}(n) = \log r_{\mathrm{pair}}(n)$ rest
> for general blocks?

## Two distinct objects

| Object | Projection | Rank | Status |
|---|---|---|---|
| Admissible pair sector $\mathcal{A}_c$ | $\Pi_q$ (rank-3 admissible) | 2 (after removing $e_0$) | Mean-zero unconditional; atomicity conditional on (H-rank); proto-state conditional on (H-rank) and (H-inv) |
| Residual fibre-level support | Full Gram--Schmidt basis | $r_{\mathrm{pair}}(n) = R_\infty - R(n)$, with $R_\infty = q$ | Unconditional for matched blocks; conditional otherwise |

The zero mode is always removed by admissibility (mean-zero lemma,
unconditional). **Spectral atomicity** itself (Q5a-O2 Proposition 4.1) --
that the rank-3 admissible projection is
$\mathrm{ran}(\Pi_q^{(c)}) = \mathrm{span}\{e_0, e_{\xi_c}, e_{q-\xi_c}\}$ --
is confirmed numerically to machine precision at the primes tested, but its
general analytical proof rests on O23's admissible-rank-exactly-three result,
which O23's own abstract states as conditional on the absence of additional
effective symmetries beyond Born--Infeld parity, within the scope of O18: an
explicit hypothesis here labelled **(H-rank)**. Under (H-rank), the
Born--Infeld parity pair $\{e_{\xi_c}, e_{q-\xi_c}\}$ is the two-dimensional
spin-$\tfrac12$ representation $V_{1/2}$.

## Core Results

### Theorem (Admissible pair entropy under (H-rank) and (H-inv))

Under **(H-rank)** and the further, independent explicit hypothesis
**(H-inv)** -- that the proto-state on $\mathcal{A}_c \otimes \mathcal{A}_c$
is invariant under the diagonal $2I$-action -- the proto-state is the
spin-$\tfrac12$ singlet
$$
|\Omega_c\rangle = \frac{1}{\sqrt{2}}\bigl(|\xi_c\rangle \otimes |q-\xi_c\rangle - |q-\xi_c\rangle \otimes |\xi_c\rangle\bigr),
$$
its reduced state is $\rho^{\mathrm{adm}}_c = \tfrac12 \mathbf{1}_2$, and
$$
S_{\mathrm{ent}}^{\mathrm{adm}} = \log 2.
$$
The proof uses spectral atomicity under (H-rank) (Q5a-O2), the unconditional
mean-zero lemma, and Q3's Theorem 3.2 (Schur's lemma via Clebsch--Gordan
$V_{1/2} \otimes V_{1/2} = V_0 \oplus V_1$, applied under (H-inv)). Neither
(H-rank) nor (H-inv) is derived from Born--Infeld indiscernibility, from
admissibility, or from any other principle in the present corpus; each is
stated as an explicit, undemonstrated hypothesis by the paper that introduces
it (O23 and Q3 respectively), and E2 imports both rather than deriving
either. The mean-zero lemma is unconditional regardless; the singlet
identification, and hence $\log 2$, holds for **general canonical blocks**
only **given both (H-rank) and (H-inv)**.

### Residual-rank entropy (status)

| Case | Status |
|---|---|
| Matched single-character blocks | **Proved** by E1 Theorem 7: $S_{\mathrm{ent}}(n) = \log r_{\mathrm{pair}}(n)$ unconditional -- the one unconditional result of this note |
| Independently sampled canonical blocks | **Conditional** on $[\mathrm{H}_{\mathrm{res}}]$ (residual admissibility indiscernibility) and on extending O17's equal-residual-dimension result beyond its own toy model to the real admissibility pipeline |
| Metaplectic dilation as bridge for $[\mathrm{H}_{\mathrm{res}}]$ | **Excluded** (acts between blocks, not within the residual support of a single block) |

The hypothesis $[\mathrm{H}_{\mathrm{res}}]$ has a status parallel to the
conditional hypotheses $[\mathrm{H\text{-}color}]$ and $[\mathrm{H\text{-}ext}]$
elsewhere in the programme.

## Position in the Programme

Constituent of the **entanglement sub-programme**
([ENT-Note](https://doi.org/10.5281/zenodo.20498835)). The result chain on
which the present note rests is:

- **Q5a-O2** ([Beau2026q5ao2](https://doi.org/10.5281/zenodo.19915951)): spectral atomicity (Proposition 4.1, conditional on (H-rank) via O23) and the mean-zero lemma (Lemma 3.1, unconditional);
- **O23** ([Beau2026a27](https://doi.org/10.5281/zenodo.19375136)): admissible rank exactly three, conditional on (H-rank) by O23's own statement;
- **O18** ([Beau2026a22](https://doi.org/10.5281/zenodo.19321413)): defines the scope within which (H-rank) is stated;
- **O17** ([Beau2026a21](https://doi.org/10.5281/zenodo.19299611)): equality of residual dimensions, within its own scalar toy model -- not yet shown to transfer to the real pipeline;
- **O31** ([Beau2026a35](https://doi.org/10.5281/zenodo.20030491)): the metaplectic dilation, excluded as a bridge for $[\mathrm{H}_{\mathrm{res}}]$;
- **E1** ([Beau2026ent1](https://doi.org/10.5281/zenodo.20499309)): universal admission orthogonality, matched-block flat Schmidt spectrum, and the open Schmidt-pairing question for general blocks;
- **Q3** ([Beau2026q3](https://doi.org/10.5281/zenodo.19979535)): the diagonal-invariance hypothesis (H-inv) and the unique-singlet theorem conditional on it (Theorem 3.2);
- **Foundation** ([Beau2026m](https://doi.org/10.5281/zenodo.19616329)): Axiom A3, used in the residual-flatness proof.

## Build

```bash
bash compile.sh
```

This runs `pdflatex → bibtex → pdflatex → pdflatex` on
`tex/EntanglementE2.tex` and produces `out/EntanglementE2.pdf`.
