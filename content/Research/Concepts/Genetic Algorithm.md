---
tags:
  - glossary
  - computer-science
---
Genetic Algorithms work on the mechanism of natural selection, where several initial guesses are passed through a [[Fitness Function]] to determine how well they meet requirements.

The most promising guesses are combined to produce new, slightly different (or 'mutated') guesses. The best (elite) guesses survive to the next generation, and some of the new estimates are formed by combining the elite guesses. These are called crossover guesses.

The remaining estimates are mutated by introducing a random change ([[References#43]]).

The new estimates are passed through the fitness function again, and the process is repeated until a [[Termination Condition]] is met, and the best solution is retrieved.

![[genetic-algorithm-structure.png | center | desc]] The general structure of a genetic algorithm ([[References#42]])

The effectiveness of a genetic algorithm can be determined by its [[Pareto Optimality]] 