---
layout: post
title: "Adaptive Rigidification of Discrete Shells"
image: 
  path: /images/2023-08-04-AdaptiveRigidificationShells/teaser.png
  thumbnail: /images/2023-08-04-AdaptiveRigidificationShells/teaser.png
date: 2023-08-05
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

Methods like remeshing target mostly flat regions of shells. We excel at coarsening curves.

**Abstract:** We present a method to improve the computation time of thin shell simulations by using adaptive rigidification to reduce the number of degrees of freedom. Our method uses a discretization independent metric for bending rates, and we derive a membrane strain rate to curvature rate equivalence that permits the use of a common threshold.
To improve accuracy, we enhance the elastification oracle by considering both membrane and bending deformation to determine when to rigidify or elastify. Furthermore, we explore different approaches that are compatible with the previous work on adaptive rigidifcation and enhance the accuracy of the elastification on new contacts without increasing the computational overhead. Additionally, we propose a scaling approach that reduces the conditioning issues that arise from mixing rigid and elastic bodies in the same model.

[<img src="/Work/icons/pdf.png" width="25"/>](/Work/papers/SCA2023AdaptiveShells.pdf)
[<img src="/Work/icons/link.png" width="25"/>](https://doi.org/10.1145/3606932)
[<img src="/Work/icons/github.png" width="25"/>](https://github.com/AlexandreMercierAubin/AdaptiveRigidificationShells2023)


## Installation
<iframe width="560" height="315" style="display: block; margin: auto;" src="https://www.youtube.com/embed/soxEZxP9zFc" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Full Presentation
<iframe width="560" height="315" style="display: block; margin: auto;" src="https://www.youtube.com/embed/oMPXLxo2W9c" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Supplemental Video
<iframe width="560" height="315" style="display: block; margin: auto;" src="https://www.youtube.com/embed/JFHeRrgieLM" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Authors
Alexandre Mercier-Aubin, and Paul G. Kry

## Embedded paper
 <embed width="560" height="315" style="display: block; margin: auto;" src="/Work/papers/SCA2023AdaptiveShells.pdf" type="application/pdf" />

#### Github link
[click here for the code if you missed the two github buttons](https://github.com/AlexandreMercierAubin/AdaptiveRigidificationShells2023)

## Bibtex
```
@article{ARDS,
author = {Mercier-Aubin, Alexandre and Kry, Paul G.},
title = {Adaptive Rigidification of Discrete Shells},
year = {2023},
issue_date = {August 2023},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
volume = {6},
number = {3},
url = {https://doi.org/10.1145/3606932},
doi = {10.1145/3606932},
abstract = {We present a method to improve the computation time of thin shell simulations by using adaptive rigidification to reduce the number of degrees of freedom. Our method uses a discretization independent metric for bending rates, and we derive a membrane strain rate to curvature rate equivalence that permits the use of a common threshold. To improve accuracy, we enhance the elastification oracle by considering both membrane and bending deformation to determine when to rigidify or elastify. Furthermore, we explore different approaches that are compatible with the previous work on adaptive rigidifcation and enhance the accuracy of the elastification on new contacts without increasing the computational overhead. Additionally, we propose a scaling approach that reduces the conditioning issues that arise from mixing rigid and elastic bodies in the same model.},
journal = {Proc. ACM Comput. Graph. Interact. Tech.},
month = {aug},
articleno = {39},
numpages = {17},
keywords = {cloth, finite element, rigid bodies, adaptive simulation, shells}
}
```
