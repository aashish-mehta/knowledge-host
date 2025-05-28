---
tags:
  - computer-science
---
NSGA-II is a well established Multi-objective [[Genetic Algorithm]]  for solving **multi-objective optimization** problems. It is based on genetic algorithms and includes efficient mechanisms to rank solutions and maintain diversity. ([[References#44]], [[References#45]])

---

## How it works

1. Initialize a random population.
2. Evaluate fitness based on all objectives.
3. Sort individuals into Pareto fronts using non-dominated sorting.
4. Calculate crowding distance to maintain diversity within each front.
5. Select parents using binary tournament selection (based on rank and distance).
6. Apply crossover and mutation to generate offspring.
7. Combine parent and offspring populations.
8. Select the next generation from the combined pool.
9. Repeat until a stopping condition is met (e.g., max generations).


---
## Notes

- **Multi-objective optimization**: Problems that involve optimizing two or more conflicting objectives.
- **[[Pareto Optimality|Pareto]] dominance**: A solution A dominates B if A is no worse in all objectives and better in at least one.
- **Pareto front**: The set of non-dominated (best trade-off) solutions.
