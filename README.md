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
| Admissible pair sector $\mathcal{A}_c$ | $\Pi_q$ (rank-3 admissible) | 2 (after removing $e_0$) | Structure unconditional; proto-state conditional on (H-inv) |
| Residual fibre-level support | Full Gram--Schmidt basis | $r_{\mathrm{pair}}(n) = R_\infty - R(n)$, with $R_\infty = q$ | Unconditional for matched blocks; conditional otherwise |

The admissible sector's structure is fixed by **spectral atomicity** (Q5a-O2
Proposition 4.1): the rank-3 admissible projection is
$\mathrm{ran}(\Pi_q^{(c)}) = \mathrm{span}\{e_0, e_{\xi_c}, e_{q-\xi_c}\}$;
after the mean-zero lemma removes $e_0$, the Born--Infeld parity pair
$\{e_{\xi_c}, e_{q-\xi_c}\}$ is the two-dimensional spin-$\tfrac12$
representation $V_{1/2}$. This part is unconditional.

## Core Results

### Theorem (Admissible pair entropy under (H-inv))

Under the explicit hypothesis **(H-inv)** -- that the proto-state on
$\mathcal{A}_c \otimes \mathcal{A}_c$ is invariant under the diagonal $2I$-action --
the proto-state is the spin-$\tfrac12$ singlet
$$
|\Omega_c\rangle = \frac{1}{\sqrt{2}}\bigl(|\xi_c\rangle \otimes |q-\xi_c\rangle - |q-\xi_c\rangle \otimes |\xi_c\rangle\bigr),
$$
its reduced state is $\rho^{\mathrm{adm}}_c = \tfrac12 \mathbf{1}_2$, and
$$
S_{\mathrm{ent}}^{\mathrm{adm}} = \log 2.
$$
The proof uses spectral atomicity (Q5a-O2), the mean-zero lemma, and Q3's
Theorem 3.2 (Schur's lemma via Clebsch--Gordan $V_{1/2} \otimes V_{1/2} = V_0
\oplus V_1$, applied under (H-inv)). (H-inv) is stated by Q3 as an explicit,
undemonstrated hypothesis, not derived there from Born--Infeld
indiscernibility, from admissibility, or from any other principle; whether a
physically admissible proto-state must satisfy (H-inv) is a separate, open
question. The atomicity of the sector itself, and the elimination of the zero
mode, are unconditional; the singlet identification, and hence $\log 2$, holds
for **general canonical blocks** only **given (H-inv)**.

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

- **Q5a-O2** ([Beau2026q5ao2](https://doi.org/10.5281/zenodo.19915951)): spectral atomicity (Proposition 4.1) and the mean-zero lemma (Lemma 3.1);
- **O23** ([Beau2026a27](https://doi.org/10.5281/zenodo.19375136)): admissible rank exactly three;
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
