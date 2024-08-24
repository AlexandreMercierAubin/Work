---
layout: post
title: "A Multi-Layer Solver for XPBD"
image: /images/2024-08-21-MultiLayerXPBD/TeaserPills.png
date: 2024-07-19
categories:
  - Papers
tags:
  - XPBD
  - Rigid Bodies
  - Contact
  - Soft Bodies
  - Multigrid
use_math: true
---
**Abstract:** We present a novel multi-layer method for extended position-based dynamics that exploits a sequence of reduced models consisting of rigid and elastic parts to speed up convergence. Taking inspiration from concepts like adaptive rigidification and long-range constraints, we automatically generate different rigid bodies at each layer based on the current strain rate. During the solve, the rigid bodies provide coupling between progressively less distant vertices during layer iterations, and therefore the fully elastic iterations at the final layer start from a lower residual error. Our layered approach likewise helps with the treatment of contact, where the mixed solves of both rigid and elastic in the layers permit fast propagation of impacts. We show several experiments that guide the selection of parameters of the solver, including the number of layers, the iterations per layers, as well as the choice of rigid patterns. Overall, our results show lower compute times for achieving a desired residual reduction across a variety of simulation models and scenarios.

The DOI is not ative yet, but here is the preprint
[<img src="/Work/icons/pdf.png" width="25"/>](/Work/papers/SCA2024MultiLayerXPBD.pdf)
[<img src="/Work/icons/link.png" width="25"/>](https://www.doi.org/10.1111/cgf.15186)
[<img src="/Work/icons/github.png" width="25"/>](https://github.com/AlexandreMercierAubin/MultiLayerSolver2024)

## Full Presentation
To be released soon after the conference

## Supplemental Video
<iframe width="560" height="315" style="display: block; margin: auto;" src="https://www.youtube.com/embed/JXlFrHPCJ-0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Authors
Alexandre Mercier-Aubin, and Paul G. Kry

## Embedded paper
 <embed width="560" height="315" style="display: block; margin: auto;" src="/Work/papers/SCA2024MultiLayerXPBD.pdf" type="application/pdf" />

#### Github link
[click here for the code if you missed the two github buttons](https://github.com/AlexandreMercierAubin/MultiLayerSolver2024)

## Bibtex
```
@article{MLXPBD,
journal = {Computer Graphics Forum},
title = {A Multi-layer Solver for XPBD},
author = {Mercier-Aubin, Alexandre and Kry, Paul G.},
year = {2024},
publisher = {The Eurographics Association and John Wiley & Sons Ltd.},
ISSN = {1467-8659},
DOI = {10.1111/cgf.15186}
}
```