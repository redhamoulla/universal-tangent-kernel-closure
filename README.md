# Universal Tangent-Kernel Closure in Two-Factor Linear Networks, and Its Failure Beyond

[![Build paper](https://github.com/redhamoulla/universal-tangent-kernel-closure/actions/workflows/materialize-paper.yml/badge.svg)](https://github.com/redhamoulla/universal-tangent-kernel-closure/actions/workflows/materialize-paper.yml)

This repository contains the theoretical note by **Redha Moulla — AXIA, France** on exact finite-width tangent-kernel closure in linear networks.

## Main result

For the scalar-output two-factor linear network

\[
f=XW^\top a, \qquad G=XX^\top,
\]

gradient flow projects exactly onto the joint prediction–kernel state \((f,K)\):

\[
\dot f=-Kr,
\qquad
\dot K=-(Gr)f^\top-f(Gr)^\top-2(f^\top r)G.
\]

The closure holds for arbitrary hidden width, input dimension, finite dataset, differentiable loss, and parameter state. It is independent of the balancing leaf and is driven by \((f,r)\), rather than directly by \(K\).

For scalar deep-linear networks, the paper derives

\[
\dot e_k=-2fr(d-k+1)e_{k-1},
\qquad
K=e_{d-1},
\qquad
\dot K=-4fr\,e_{d-2}.
\]

Universal closure holds at two factors. From three factors onward, kernel velocity depends on information varying along regular fibers with fixed output and fixed tangent kernel. Conditioning on the conserved balancing leaf restores exact closure.

## Paper

- [`paper/universal_tangent_kernel_closure.pdf`](paper/universal_tangent_kernel_closure.pdf) — compiled paper
- [`paper/universal_tangent_kernel_closure.tex`](paper/universal_tangent_kernel_closure.tex) — LaTeX source
- [`paper/references.bib`](paper/references.bib) — bibliography

## Build locally

```bash
cd paper
latexmk -pdf universal_tangent_kernel_closure.tex
```

The checked-in PDF is rebuilt from the LaTeX source by GitHub Actions.

## Author

**Redha Moulla**  
AXIA, France
