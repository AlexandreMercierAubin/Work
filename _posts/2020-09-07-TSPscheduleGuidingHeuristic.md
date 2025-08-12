---
layout: post
title: "Leveraging Constraint Scheduling: A Case Study
to the Textile Industry"
image: 
  path: /images/2020-09-07-TSPscheduleGuidingHeuristic/machineTextile.jpg
  thumbnail: /images/2020-09-07-TSPscheduleGuidingHeuristic/machineTextile.jpg
date: 2020-09-07
categories:
  - Papers
tags:
  - Traveling Salesman Problem
  - Constraint
  - Combinatorics
---

Warmstart your solve with a faster TSP solution.

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

[<img src="/Work/icons/pdf.png" width="25"/>](/Work/papers/CPAIOR2020TspSchedule.pdf)
[<img src="/Work/icons/link.png" width="25"/>](https://link.springer.com/chapter/10.1007/978-3-030-58942-4_22)

## Video
<iframe width="560" height="315" style="display: block; margin: auto;" src="https://www.youtube.com/embed/dC72_1jTPGs" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Authors
Alexandre Mercier-Aubin, Jonathan Gaudreault and Claude-Guy Quimper

## Copyrights and Data
Sadly Claude-Guy is still in the process of releasing the code for this paper. 
We will hopefully be able to provide it at some point, but this is out of my hands at the moment.

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