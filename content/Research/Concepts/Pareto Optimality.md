---
tags:
  - computer-science
  - glossary
aliases:
  - Pareto Efficiency
  - Pareto Frontier
  - Pareto Optimal
---
A solution is considered Pareto optimal if **no other solution can improve one objective without worsening at least one other** [[References#47]].

---

## Notes

- **Dominated solution**: A solution is dominated if another solution is better in all objectives or equal in some and better in at least one.
- **Non-dominated solution**: Not dominated by any other in the population; considered Pareto optimal.
- **Pareto front**: The set of all non-dominated solutions. These represent the best trade-offs.

---

## Example

Imagine optimizing a design for **cost** and **performance**:

| Design | Cost ↓ | Performance ↑ | Dominated? |
|--------|--------|----------------|------------|
| A      | 100    | 70             | No         |
| B      | 90     | 60             | No         |
| C      | 120    | 80             | No         |
| D      | 100    | 50             | Yes (by A) |

Design D is **dominated** by A (same cost, worse performance), so it's not Pareto optimal.

---

## Related Notes

- [[NSGA-II]]
- [[SPEA2DSE]]
- [[Genetic Algorithm]]
