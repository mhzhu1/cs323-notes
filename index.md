---
layout: post
title: Contents
---

These notes are based on Stanford [CS323](http://cs.stanford.edu/~ermon/cs323/index.html), taught by [Stefano Ermon](http://cs.stanford.edu/~ermon/), and have been written by Michael Zhu. The notes are still under construction! If you find any typos or can contribute to help make the notes better, please let us know, or submit a pull request with your fixes to our [Github repository](https://github.com/ermongroup/cs323-notes).

This course is a graduate level introduction to automated reasoning techniques and their applications, covering logical and probabilistic approaches. Topics include: logical and probabilistic foundations, backtracking strategies and algorithms behind modern SAT solvers, stochastic local search and Markov Chain Monte Carlo algorithms, classes of reasoning tasks and reductions, and applications.


## Logical Reasoning

1. [Representation - propositional logic](logic/representation/): Definitions: syntax, semantics, knowledge base. Satisfiability: inference reduces to satisfiability, conjunctive normal form.
2. [Inference - SAT solvers](logic/inference/): Brute force, early stopping, unit resolution, DPLL algorithm, conflict-driven clause learning, engineering considerations. Special cases of SAT problems: Horn SAT and 2-SAT.
3. [Inference - random walk SAT solvers](logic/random_walk/): Random walk algorithm for 2-SAT: review of Markov chains, algorithm, analysis of algorithm. Random walk algorithm for 3-SAT. Other variants.


## Probabilistic Reasoning
