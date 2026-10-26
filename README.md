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
| Admissible pair sector $\mathcal{A}_c$ | Hypothesised atomic triple (rank 3) | 2 (parity-pair component) | Carrier conditional on (H-carrier); proto-state conditional on (H-carrier) and (H-inv) |
| Residual fibre-level support | Full Gram--Schmidt basis | $r_{\mathrm{pair}}(n) = R_\infty - R(n)$, with $R_\infty = q$ | Matched blocks: proved under a supplied purity of the joint state, which E1 does not derive; conditional otherwise |

The admissible pair carrier is fixed by an explicit two-clause hypothesis, **(H-carrier)**:
(i) the admissible sector of each factor is the atomic Fourier triple
$\mathrm{ran}(\Pi_q^{(c)}) = \mathrm{span}\{e_0, e_{\xi_c}, e_{q-\xi_c}\}$; (ii) its parity-pair
component carries the spin-$\tfrac12$ module $V_{1/2}$ of the binary group acting in (H-inv)
(the natural swap on the pair plane has eigenvalues $\pm 1$ while $-1 \in 2I$ must act as
$-\mathbf{1}$, so the module identification is a genuine assumption).
It is structurally motivated -- every selected Gram--Schmidt direction of the
pre-saturation pipeline is a pure Fourier mode (Q5a-O2, Propositions 3.1--3.2;
equivalently E1's orthogonality result), and conjugate frequencies enter as
parity partners -- but not derived: the rank-three threshold $\Sigma_c(n_3)=3$
is a supplied selection rule (O23), the pipeline's three-coordinate reduction
is a truncation from which no rank can be read (Q5a-O2, Proposition 4.1), no
mean-zero theorem removes the zero mode (the passage to the pair sector is part
of the sector definition), and the archived support-size diagnostics are not
reproducible and include a delocalised case ($q=61$, pair $c=2$).
Under (H-carrier), the conjugate-frequency pair $\{e_{\xi_c}, e_{q-\xi_c}\}$ carries
the two-dimensional spin-$\tfrac12$ representation $V_{1/2}$.

## Core Results

### Theorem (Admissible pair entropy under (H-carrier) and (H-inv))

Under **(H-carrier)** and the further, independent explicit hypothesis
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
The proof uses the (H-carrier) pair sector and Q3's Theorem 3.2 (Schur's
lemma via Clebsch--Gordan $V_{1/2} \otimes V_{1/2} = V_0 \oplus V_1$, applied
under (H-inv)). Neither (H-carrier) nor (H-inv) is derived from Born--Infeld
structure, from admissibility, or from any other principle in the present
corpus; (H-carrier) is stated by E2 itself, (H-inv) by Q3, and E2 imports the
latter rather than deriving it. The singlet identification, and hence
$\log 2$, holds for **general canonical blocks** only **given both
(H-carrier) and (H-inv)**.

### Residual-rank entropy (status)

| Case | Status |
|---|---|
| Matched single-character blocks | **Proved** by E1 Theorem 7 under a supplied purity of the joint state, which E1 does not derive: $S_{\mathrm{ent}}(n) = \log r_{\mathrm{pair}}(n)$ |
| Independently sampled canonical blocks | **Conditional** on the same supplied purity, on $[\mathrm{H}_{\mathrm{res}}]$ (residual admissibility indiscernibility) and on extending O17's equal-residual-dimension result beyond its own toy model to the real admissibility pipeline |
| Metaplectic dilation as bridge for $[\mathrm{H}_{\mathrm{res}}]$ | **Excluded** (acts between blocks, not within the residual support of a single block) |

The hypothesis $[\mathrm{H}_{\mathrm{res}}]$ has a status parallel to the
conditional hypotheses $[\mathrm{H\text{-}color}]$ and $[\mathrm{H\text{-}ext}]$
elsewhere in the programme.

## Position in the Programme

Constituent of the **entanglement sub-programme**
([ENT-Note](https://doi.org/10.5281/zenodo.20498835)). The result chain on
which the present note rests is:

- **Q5a-O2** ([Beau2026q5ao2](https://doi.org/10.5281/zenodo.19915951)): pure Fourier modes of the pre-saturation pipeline (Propositions 3.1--3.2) and the truncation status of the three-coordinate reduction (Proposition 4.1), which motivate (H-carrier) without deriving it;
- **O23** ([Beau2026a27](https://doi.org/10.5281/zenodo.19375136)): the adjoint-dimension theorem for a supplied spinor carrier; the threshold $\Sigma_c(n_3)=3$ is a supplied selection rule, both bridges open;
- **O18** ([Beau2026a22](https://doi.org/10.5281/zenodo.19321413)): Born--Infeld parity covariance (even-order responses preserved, odd-order reversed) and the open fibre-identification problem within which any carrier selection would have to be posed;
- **O17** ([Beau2026a21](https://doi.org/10.5281/zenodo.19299611)): equality of residual dimensions, within its own scalar toy model -- not yet shown to transfer to the real pipeline;
- **O31** ([Beau2026a35](https://doi.org/10.5281/zenodo.20030491)): the metaplectic dilation, excluded as a bridge for $[\mathrm{H}_{\mathrm{res}}]$;
- **E1** ([Beau2026ent1](https://doi.org/10.5281/zenodo.20499309)): universal admission orthogonality, matched-block flat Schmidt spectrum, and the open Schmidt-pairing question for general blocks;
- **Q3** ([Beau2026q3](https://doi.org/10.5281/zenodo.19979535)): the diagonal-invariance hypothesis (H-inv) and the unique-singlet theorem conditional on it (Theorem 3.2);
- **Foundation** ([Beau2026m](https://doi.org/10.5281/zenodo.19616329)): Axiom A3 and its non-factorisability lemma, which holds only under an additional sector reading of A3, not
  derived; the residual-flatness proof uses that reading through (H-res).

## Build

```bash
bash compile.sh
```

This runs `pdflatex → bibtex → pdflatex → pdflatex` on
`tex/EntanglementE2.tex` and produces `out/EntanglementE2.pdf`.
