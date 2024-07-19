---
layout: post
title: "Adaptive Rigidification of Discrete Shells"
image: /images/2023-08-04-AdaptiveRigidificationShells/teaser.png
date: 2024-07-19
categories:
  - Papers
tags:
  - Simulation
  - Finite Element
  - Contact
  - Approximations
  - Adaptive Rigidification
  - Shells
use_math: true
---
**Abstract:** We present a novel multi-layer method for extended position-based dynamics that exploits a sequence of reduced models consisting of rigid and elastic parts to speed up convergence. Taking inspiration from concepts like adaptive rigidification and long-range constraints, we automatically generate different rigid bodies at each layer based on the current strain rate. During the solve, the rigid bodies provide coupling between progressively less distant vertices during layer iterations, and therefore the fully elastic iterations at the final layer start from a lower residual error. Our layered approach likewise helps with the treatment of contact, where the mixed solves of both rigid and elastic in the layers permit fast propagation of impacts. We show several experiments that guide the selection of parameters of the solver, including the number of layers, the iterations per layers, as well as the choice of rigid patterns. Overall, our results show lower compute times for achieving a desired residual reduction across a variety of simulation models and scenarios.

Accepted for publication at SCA 2024. Here is the preprint. I will update the page as we get closer to the conference (August).
[<img src="/Work/icons/pdf.png" width="25"/>](/Work/papers/SCA2024MultiLayerXPBD.pdf)

## Authors
Alexandre Mercier-Aubin, and Paul G. Kry

## Embedded paper
 <embed width="560" height="315" style="display: block; margin: auto;" src="/Work/papers/SCA2024MultiLayerXPBD.pdf" type="application/pdf" />
