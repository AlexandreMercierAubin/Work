---
layout: post
title: "Real-Time Triangle-SDF Continuous Collision Detection"
image: 
  path: /images/SCA2025ShurikenTeaser.png
  thumbnail: /images/SCA2025ShurikenTeaser.png
date: 2025-08-08
categories:
  - Papers
tags:
  - Collisions 
  - Real-time
  - Physics-based
  - Signed Distance Field
use_math: true
---
**Abstract:** We introduce an efficient solution to the problem of continuous collision detection (CCD) between triangle geometry and signed distance fields (SDFs). We formulate the triangle-SDF collision problem as a novel spatio-temporal local optimization that solves for the first time of impact between a triangle and an SDF isosurface. Our method offers improved robustness over point sampling methods, and outperforms recent triangle-SDF discrete collision detection (DCD) algorithms. Furthermore, a novel method for adaptively refining the potential collision points on large triangles is proposed for robust triangle-SDF collision detection with coarse meshes. This enables the use of reduced geometry for efficient simulations. We demonstrate the benefits of our approach by comparing to state-of-the-art algorithms for triangle-SDF collision detection, and showcase its effectiveness through simulations involving complex collision scenarios.

[<img src="/Work/icons/pdf.png" width="25"/>](/Work/papers/SCA25_TriSDF_ccd.pdf)
[<img src="/Work/icons/link.png" width="25"/>](https://dl.acm.org/doi/abs/10.1145/3747862)

## Award
This paper was awarded a best paper honorable mention at SCA 2025.

## Supplemental Video
<iframe width="560" height="315" style="display: block; margin: auto;" src="https://www.youtube.com/embed/RMd3nsqH3S4?si=9BPaqtO0vjiLNZ4w" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Authors
Joël Pelletier-Guénette, Alexandre Mercier-Aubin, Sheldon Andrews

## Embedded paper
 <embed width="560" height="315" style="display: block; margin: auto;" src="/Work/papers/SCA25_TriSDF_ccd.pdf" type="application/pdf" />

## Bibtex
```
@article{trisdfccd2025,
    author = {Pelletier-Guénette, Joël and Mercier-Aubin, Alexandre and Andrews, Sheldon},
    title = {Real-Time Triangle-SDF Continuous Collision Detection},
    year = {2025},
    journal = {Proceedings of the ACM on Computer Graphics and Interactive Techniques},
    volume = {8},
    number = {4},
    series = {SCA ‘25}
    doi = {10.1145/3747862}
}
```