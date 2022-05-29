---
layout: post
title: "The CONFIDENCE Constraint: A Step Towards Stochastic CP Solvers"
image: /images/2020-09-21-StochasticConstraint/chance.jpg
date: 2020-09-21
categories:
  - Papers
tags:
  - Constraint
  - Combinatorics
  - Stochastic Optimization
---

**Abstract:** We introduce the CONFIDENCE constraint, a chance constraint that ensures, with probability γ, that a set of variables are no smaller than random variables for which the probability distribution is given. This constraint is useful in stochastic optimization to ensure that a solution is robust to external random events. It allows to control the trade-off between optimizing the objective function and ensuring the satisfiability of the solution under random parameters. We present a filtering algorithm for this constraint with explanations. We apply the constraint to a case study, an industrial scheduling problem where tasks have random processing times due to possible breakdowns during their execution. We evaluate our solutions with simulations and show that this new constraint allows robust solutions in decent computation time.

[<img src="/Work/icons/pdf.png" width="25"/>](/Work/papers/CP2020ConfidenceConstraint.pdf)
[<img src="/Work/icons/link.png" width="25"/>](https://link.springer.com/chapter/10.1007/978-3-030-58475-7_44)
[<img src="/Work/icons/github.png" width="25"/>](https://github.com/AlexandreMercierAubin/Confidence-Constraint-CPAIOR2020)

## Video
<iframe width="560" height="315" style="display: block; margin: auto;" src="https://www.youtube.com/embed/UbolTOF_r8w" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Authors
Alexandre Mercier-Aubin, Ludwig Dumetz, Jonathan Gaudreault and Claude-Guy Quimper

## FAQ
The constraint offers a single solution that satisfies the risk thresholds with respect to probabilistic distributions. In the paper we used a Poisson distribution, although the algorithm is compatible with the distribution of your choice.
The constraint itself is not a policy, it will not adapt to a failed schedule. The Chance constraint should instead be considered as a fast filtering algorithm of risky solutions.

The risk of the first task causing a breakdown on a loom will most definitely create more problems (delays) than it happening for the last task. 
The delays ripple over a single loom, but also over the others because of resources starving. 
This is what we call the ripple effect. 
The chance constraint can be used to handle such cases as explained in the paper.


## Bibtex
```
@InProceedings{10.1007/978-3-030-58475-7_44,
author="Mercier-Aubin, Alexandre
and Dumetz, Ludwig
and Gaudreault, Jonathan
and Quimper, Claude-Guy",
editor="Simonis, Helmut",
title="The Confidence Constraint: A Step Towards Stochastic CP Solvers",
booktitle="Principles and Practice of Constraint Programming",
year="2020",
publisher="Springer International Publishing",
address="Cham",
pages="759--773",
abstract="We introduce the Confidence constraint, a chance constraint that ensures, with probability {\$}{\$}{\backslash}gamma {\$}{\$}, that a set of variables are no smaller than random variables for which the probability distribution is given. This constraint is useful in stochastic optimization to ensure that a solution is robust to external random events. It allows to control the trade-off between optimizing the objective function and ensuring the satisfiability of the solution under random parameters. We present a filtering algorithm for this constraint with explanations. We apply the constraint to a case study, an industrial scheduling problem where tasks have random processing times due to possible breakdowns during their execution. We evaluate our solutions with simulations and show that this new constraint allows robust solutions in decent computation time.",
isbn="978-3-030-58475-7"
}
```