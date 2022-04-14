---
layout: post
title: "Leveraging Constraint Scheduling: A Case Study
to the Textile Industry"
date: 2020-09-21
categories: jekyll blogging
---

**Abstract:** We introduce the CONFIDENCE constraint, a chance constraint that ensures, with probability γ, that a set of variables are no smaller than random variables for which the probability distribution is given. This constraint is useful in stochastic optimization to ensure that a solution is robust to external random events. It allows to control the trade-off between optimizing the objective function and ensuring the satisfiability of the solution under random parameters. We present a filtering algorithm for this constraint with explanations. We apply the constraint to a case study, an industrial scheduling problem where tasks have random processing times due to possible breakdowns during their execution. We evaluate our solutions with simulations and show that this new constraint allows robust solutions in decent computation time.

[<img src="https://alexandremercieraubin.com/MyWork/icons/pdf.png" width="25"/>](https://alexandremercieraubin.com/MyWork/papers/CPAIOR2020TspSchedule.pdf)
[<img src="https://alexandremercieraubin.com/MyWork/icons/link.png" width="25"/>](https://link.springer.com/chapter/10.1007/978-3-030-58942-4_22)

## Video
<iframe width="560" height="315" src="https://www.youtube.com/embed/dC72_1jTPGs" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Authors
Alexandre Mercier-Aubin, Jonathan Gaudreault and Claude-Guy Quimper

## Bibtex
```
@InProceedings{10.1007/978-3-030-58942-4_22,
author="Mercier-Aubin, Alexandre
and Gaudreault, Jonathan
and Quimper, Claude-Guy",
editor="Hebrard, Emmanuel
and Musliu, Nysret",
title="Leveraging Constraint Scheduling: A Case Study to the Textile Industry",
booktitle="Integration of Constraint Programming, Artificial Intelligence, and Operations Research",
year="2020",
publisher="Springer International Publishing",
address="Cham",
pages="334--346",
abstract="Despite the significant progress made in scheduling in the past years, industrial problems with several hundred tasks remain intractable for some variants of the scheduling problems. We present techniques that can be used to leverage the power of constraint programming to solve an industrial problem with 800 non-preemptive tasks, 90 resources, and sequence-dependent setup times. Our method involves solving the traveling salesperson problem (TSP) as a simplification of the scheduling problem and using the simplified solution to guide the branching heuristics. We also explore large neighborhood search. Experiments conducted on a dataset provided by our partner from the textile industry show that we obtain non-optimal but satisfactory solutions.",
isbn="978-3-030-58942-4"
}
```