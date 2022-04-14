---
layout: post
title: "The CONFIDENCE Constraint: A Step Towards Stochastic CP Solvers"
date: 2020-09-07
categories: jekyll blogging
---

**Abstract:** Despite the significant progress made in scheduling in the
past years, industrial problems with several hundred tasks remain intractable
for some variants of the scheduling problems. We present techniques
that can be used to leverage the power of constraint programming
to solve an industrial problem with 800 non-preemptive tasks, 90
resources, and sequence-dependent setup times. Our method involves
solving the traveling salesperson problem (TSP) as a simplification of
the scheduling problem and using the simplified solution to guide the
branching heuristics. We also explore large neighborhood search. Experiments
conducted on a dataset provided by our partner from the textile
industry show that we obtain non-optimal but satisfactory solutions.

[<img src="https://alexandremercieraubin.com/MyWork/icons/pdf.png" width="25"/>](https://alexandremercieraubin.com/MyWork/papers/CP2020ConfidenceConstraint.pdf)
[<img src="https://alexandremercieraubin.com/MyWork/icons/link.png" width="25"/>](https://link.springer.com/chapter/10.1007/978-3-030-58475-7_44)

## Video
<iframe width="560" height="315" src="https://www.youtube.com/embed/UbolTOF_r8w" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Authors
Alexandre Mercier-Aubin, Ludwig Dumetz, Jonathan Gaudreault and Claude-Guy Quimper

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