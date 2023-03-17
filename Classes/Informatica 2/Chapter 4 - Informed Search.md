17-03-2023
---
# Chapter 4 - Informed Search
## Search Heuristics
A heuristic is:
- A function that *estimates* how close a state is to a goal
- Designed for a particular search problem
- Examples: Manhattan distance, Euclidian distance for pathing

## Greedy Search
Example: Pathing on a graph representing a map with cities and roads as nodes and edges
- Expand the node that seems closest
- What can go wrong?

Strategy: expand a node that you think is closest to a goal state
- Heuristic: estimate distance to nearest goal for each state

A common case:
- Best-first takes you straight to the goal

Worst case:
- Like a badly-guided DFS

## A* Search
Combining UCS and Greedy
- Uniform-cost orders by path cost, or *backward cost* $g(n)$
- Greedy orders by goal proximity, or *forward cost* $h(n)$
- A* orders by the sum $f(n) = g(n) + h(n)$

### When should A* terminate?
Should we stop when we enqueue a goal?
- No. Only stop when we dequeue a goal are we sure that it is the least-cost path

### Is A* optimal?
Only whith a good heuristic. A bad heuristic can misrepresent the real cost and cause A* to choose a non-optimal path.

#### Idea: Admissibility
**Estimates should be less than actual costs.**

Inadmissible (pessimistic) heuristics break optimally by trapping good plans on the fringe

Admissible (optimistic) heuristics slow down bad plans but never outweigh the costs

A heuristic *h* is admissible if $$0 \le h(n) \le h^*(n)$$
where $h^*(n)$ is the true cost to a nearest goal

Example:
- Navigating a maze using air distance: real cost will always be higher or same as the heuristic, as there likely are walls

Coming up with admissible heuristics es most of what's involved with using A* in practice

## Optimality of A* Search: Blocking
Assume:
- A is an optimal goal node
- B is a suboptimal goal node
- h is admissible

Claim:
- A will exit the fringe before B

Proof:
- Imagine B is on the fringe
- Some ancestor *n* of A is on the fringe too (maybe even A)
- Claim: *n* will be expanded before B
	1. $f(n) \le f(A)$
	2. $f(A) < f(B)$
	3. *n* expands before B
- All ancestors of A expand before B
- $\therefore$ all ancestors of A and even A itself exit the fringe before B

## Properties of A*
- A* expands mainly towards the goal, but does hedge its bets to ensure optimality
	- Think elliptic search space, where UCS has a circular search space

## Applications of A*
- Video games
- Routing algorithms
- Route planning
- etc.

## Creating Admissible Heuristics
Most of the work in solving hard search problems optimally is in coming up with admissible heuristics.

Often, admissible heuristics are solutions to *relaxed problems*, where new actions are available

Inadmissible heuristics are often useful too

How about using the actual cost as a heuristic?
- Calculation is expensive
- This is what UCS already does