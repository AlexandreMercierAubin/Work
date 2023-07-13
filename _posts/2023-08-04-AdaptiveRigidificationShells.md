---
layout: post
title: "Adaptive Rigidification of Discrete Shells"
image: /images/2023-08-04-AdaptiveRigidificationShells/teaser.png
date: 2023-08-04
categories:
  - Papers
tags:
  - Constraint
  - Adaptive Rigidification
use_math: true
---
**Abstract:** We present a method to improve the computation time of thin shell simulations by using adaptive rigidification to reduce the number of degrees of freedom. Our method uses a discretization independent metric for bending rates, and we derive a membrane strain rate to curvature rate equivalence that permits the use of a common threshold.
To improve accuracy, we enhance the elastification oracle by considering both membrane and bending deformation to determine when to rigidify or elastify. Furthermore, we explore different approaches that are compatible with the previous work on adaptive rigidifcation and enhance the accuracy of the elastification on new contacts without increasing the computational overhead. Additionally, we propose a scaling approach that reduces the conditioning issues that arise from mixing rigid and elastic bodies in the same model.

[<img src="/Work/icons/pdf.png" width="25"/>](/Work/papers/SCA2023AdaptiveShells.pdf)
[<img src="/Work/icons/link.png" width="25"/>](https://doi.org/10.1145/3606932)
[<img src="/Work/icons/github.png" width="25"/>](https://github.com/AlexandreMercierAubin/AdaptiveRigidification2022)

## This page contains some placeholder information. The public repo will be available soon and installation process shall remain the same. For now I like the original adaptive rigidification repo.

## Installation
<iframe width="560" height="315" style="display: block; margin: auto;" src="https://www.youtube.com/embed/soxEZxP9zFc" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Full Presentation
<!--iframe width="560" height="315" style="display: block; margin: auto;" src="https://www.youtube.com/embed/mgxGp_U1H_I" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe-->

## Supplementals Video
<iframe width="560" height="315" style="display: block; margin: auto;" src="https://www.youtube.com/embed/JFHeRrgieLM" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Authors
Alexandre Mercier-Aubin, and Paul G. Kry

<!--
## Summarized Version
 Here is a summarized version of this paper. The pre-print can be downloaded using the link above.

### Mixing Rigids and Elastics
{% raw %}{::nomarkdown}
   <div>
	When a portion of the elastic mesh is made rigid, we store the positions of vertices making up the rigid body in the rigid body frame.  Letting $r_i$ for $i \in \mathcal{R}$ be the rigid vertex positions in coordinates of the rigid body frame, we can compute the positions and velocities of these vertices in the world frame as $x_i = R \, r_i + p$  and $\dot{x}_i = - (R r_i) \times \omega + v$.  This second expression can be written instead as a matrix product,
	$$
	\begin{align}
	\dot{x}_i = 
		\underbrace{
	\begin{bmatrix} I & - (R \, r_i)^\times \end{bmatrix}
	}_{\Gamma_i}
	\begin{bmatrix} v \\ \omega \end{bmatrix},
	%\phi
	\end{align}
	$$
	where $(\cdot)^\times$ denotes construction of the 3-by-3 cross product operator.  Furthermore, we can now write the velocity of all vertices in the finite element model as a product of a matrix $G$ with velocities of our active (elastic and rigid) degrees of freedom, $\dot{x}_\mathsf{A}$,   
	$$
	\begin{equation}
	\dot{x} = 
	\underbrace{
	\begin{bmatrix}
	 I & 0 \\
	 0 & \Gamma
	 \end{bmatrix}}_{G}
	\underbrace{
	 \begin{bmatrix}
	 \dot{x}_\mathcal{A} \\
	 \phi
	 \end{bmatrix}}_{\dot{x}_\mathsf{A}}.
	\end{equation}
	$$
 </div>
{:/}{% endraw %}

### Rigidification

If the rotationally invariant Green strain tensor $E=\frac{1}{2}(F^TF-I)$ remains constant for a period of time, then we allow the element to become rigid.  
For time step $k$, we compute the strain rate using finite difference 
{% raw %}
   <div>
		$$
		\begin{align}
			\dot{E}_k= \frac{E_k - E_{k-1}}{h},
		\end{align}
		$$
		ignoring rotation by comparing strain in material space.
		Selecting a threshold for rigidification is not difficult, and is largely a question choosing a trade-off between error and speed. However, a large threshold will lead to large errors; a good choice is crucial so as not to generate visual artifacts.
	</div>
{% endraw %}

{:style="text-align:center;"}
<figure>
  <img src="{{ '/images/2022-08-08-AdaptiveRigidification/rigidBody.png' | absolute_url }}" alt="" width="250">
  <figcaption></figcaption>
  <style>
    figure figcaption {
    text-align: center;
    }
  </style>
</figure>

We use an adjacency graph for tetrahedral elements with shared faces (or with shared edges for triangle elements in 2D simulations). Each connected component forms a rigid body in our simulation.

{:style="text-align:center;"}
<figure>
  <img src="{{ '/images/2022-08-08-AdaptiveRigidification/BFS.png' | absolute_url }}" alt="" width="250">
  <figcaption></figcaption>
  <style>
    figure figcaption {
    text-align: center;
    }
  </style>
</figure>

There are two possibilities to handle the case where rigid
bodies share a vertex. One can add hinge constraints;
this will slow down the time integration. We instead
choose to make our BFS greedy, the first rigid element to
touch a vertex (edge in 3D) claims it. Note that when this
case happens, the neighboring elements often rigidify on
the next frame.

{:style="text-align:center;"}
<figure>
  <img src="{{ '/images/2022-08-08-AdaptiveRigidification/HingeAvoidance.png' | absolute_url }}" alt="" width="350">
  <figcaption>Orange regions show rigid bodies. If the red
triangle is a rigid candidate, it must not become part of body
B as the red adjacent vertex already belongs to body A.</figcaption>
  <style>
    figure figcaption {
    text-align: center;
    }
  </style>
</figure>

### Elastification
Consider an oracle that determines which elements
should elastify. We propose a single preconditioned
conjugate gradient iteration to approximate the strain
rate, which we compare to an elastification threshold.
The propagation of the information is critical to
generate good elastification behavior. Preconditioning
is essential, otherwise each iteration only propagates
information between neighbours following the sparsity
structure of the system.

Incomplete Cholesky factorization is a good choice because the forward and backward substitution provides an excellent opportunity for an impulse at one vertex to influence $\dot{x}_\text{approx}$ at distant vertices, even with only one iteration of conjugate gradient


### Local rigidification

{:style="text-align:center;"}
<figure>
  <img src="{{ '/images/2022-08-08-AdaptiveRigidification/octopus.png' | absolute_url }}" alt="" width="250">
  <figcaption>An octopus ready to be cooked with its tentacles
still dangling.</figcaption>
  <style>
    figure figcaption {
    text-align: center;
    }
  </style>
</figure>

Our technique works like sleeping on static bodies, yet it really shines in scenes with local deformation. This effectively reduces the size of the system to solve from $3n$ vertices to exactly 6 degrees of freedom for a rigidified chunk of the models. As the time to solve is dependent on the degrees of freedom in the full system, this significantly reduces the computation time of the simulation.
-->
#### See our paper for more details and results
[code](https://github.com/AlexandreMercierAubin/AdaptiveRigidification2022)

## Bibtex TODO: change it with the actual articleno once released
```
@proceedings{10.1145/3528223.3530124,
author = {Mercier-Aubin, Alexandre and Kry, Paul G.},
title = {Adaptive Rigidification of Discrete Shells},
year = {2023},
issue_date = {August 2023},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
volume = {6},
number = {2},
url = {https://dl.acm.org/doi/abs/10.1145/3528223.3530124},
doi = {10.1145/3606932},
abstract = {We present a method to improve the computation time of thin shell simulations by using adaptive rigidification to reduce the number of degrees of freedom. Our method uses a discretization independent metric for bending rates, and we derive a membrane strain rate to curvature rate equivalence that permits the use of a common threshold.
To improve accuracy, we enhance the elastification oracle by considering both membrane and bending deformation to determine when to rigidify or elastify. Furthermore, we explore different approaches that are compatible with the previous work on adaptive rigidifcation and enhance the accuracy of the elastification on new contacts without increasing the computational overhead. Additionally, we propose a scaling approach that reduces the conditioning issues that arise from mixing rigid and elastic bodies in the same model.},
journal = {ACM Comput. Graph. Interact. Tech.},
month = {Aug},
articleno = {1},
numpages = {17},
keywords = {cloth, shells, adaptive simulation, rigid bodies, finite element}
}
```