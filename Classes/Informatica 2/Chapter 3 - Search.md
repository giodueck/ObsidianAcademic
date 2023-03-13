10-03-2023
---
# Chapter 3 - Search

## Agents that plan ahead

### Reflex agents
- Choose action based on current perception (and maybe memory)
- Does not consider future consequences of actions
- *Consider how the world currently is*

Not always a good solution. Still, there are situations where a reflex agent is rational

### Planning agents
- Ask "what if?"
- Decisions base on *hypothesized* consequences of actions
- Must have model of how the world evolves based on actions
- Must formulate a goal (test)
- *Consider how the world would be*

Optimal vs. complete planning
Planning vs. replanning

## Search problems

A Search problem consists of:
- A state space
- A successor function (with actions, costs)
- A start state and a goal test

A solution is a sequence of actions (a plan) which transforms the start state to a goal state

### What is in a State Space?
The *world state* includes every last detail of the environment

A *search state* keeps only the details needed for planning (abstraction)

Example: Pacman
Problem: Pathing
- States: (x, y) location
- Actions: N, S, W, E
- Successor: update location only
- Goal test: is (x, y) = END

Problem: Eat all dots
- States: {(x, y), dot booleans}
- Actions: NSEW
- Successor: update location and possibly dot booleans
- Goal test: all booleans false

#### State space sizes
World state:
- Agent positions: 120
- Food count: 30
- Ghost positions: 12
- Number of ghosts: 2
- Agent facing: NSEW

How many:
- World states?
	$120 \times 2^{30} \times 12^2 \times 4$
- States for pathing?
	$120$
- States for eat-all-dots?
	$120 \times 2^{30}$

### State space graph
The state space can be represented as a directed graph where each state occurs once.
Rarely actually built in memory, it's too big. But is a useful idea when exploring the state space.

#### Search Trees
Root: start state
Branches/children: possible futures, neighbor states

Characteristics:
- A "what if" tree of plans and their outcomes
- The start state is the root node
- Children correspond successor states
- Nodes show states, but correspond to *plans* that achieve those states. $\therefore$ states can appear repeatedly
- **For most problems we can never actually build the whole tree**
	We construct on demand and as little as possible

##### General Tree search
Important ideas:
- Fringe
- Expansion
- Exploration

Main question: which fringe nodes to explore?

## Search algorithms
Properties:
- Complete: guaranteed to find solution if one exists?
- Optimal: Guaranteed to find the least-cost path?
- Time complexity?
- Space complexity?
- Cartoon of a seach tree:
	- b is the branching factor
	- m is the maximum depth
	- solutions at various depths
- Number of nodes in entire tree?
	- $1 + b + b^2 + ... + b^m = O(b^m)$

### Depth-First Search

Strategy: expand a deeperst node first
Implementation: Fringe is a LIFO stack

Properties:
- What nodes does DFS expand?
	- Some left prefix of the tree
	- Could process the whole tree (e.g. no solution found)
	- if m is finite, takes time $O(b^m)$
- How much space does the fringe take?
	- Only has siblings on path to root, so $O(bm)$
- Is it complete?
	- m could be infinite, so only if we prevent cycles (more later)
- Is it optimal?
	- No, it finds the "leftmost" solution, regardless of depth or cost

### Breadth-First Search

Strategy: expand the shallowest node first
Implementation: Fringe is a FIFO queue

Properties:
- What nodes does BFS expand?
	- Processes all nodes above shallowest solution
	- Let depth of shallowest solution be s
	- Search takes time $O(b^s)$
- How much space does the fringe take?
	- Has roughly the last tier, so $O(b^s)$
- Is it complete?
	- s must be finite if a solution exists, so yes
- Is it optimal?
	- Only if costs are all 1 (more on costs later)

13-03-2023
---
### Quiz: DFS vs. BFS
When will either outperform the other?

### Iterative Deepening
Idea: get DFS's space advantage with BFS's time/shallow solution advantages
- Run a DFS with depth limit 1. If no solution...
- Run a DFS with depth limit 2. If no solution...
- Run a DFS with depth limit 3. ...

Isn't that wastefully redundant?
- Generally most work happens in the lowest level searched, so not so bad.

### Cost-Sensitive Search
BFS finds shortest path in terms of number of actions, not the least-cost path.

### Uniform Cost Search
Strategy: expand cheapest node first
Implementation: Fringe is a priority queue (priority: cumulative cost)

Properties:
- What nodes does UCS expand?
	- Processes all nodes with cost less than cheapest solution
	- If that solution costs $C^*$ and arcs cost at least $\varepsilon$ ($\varepsilon > 0$), then the "effective depth" is roughly $\frac{C^*}{\varepsilon}$
	- Takes time $O(b^\frac{C^*}{\varepsilon})$ (exponential in effective depth)
- How much space dees the fringe take?
	- Has roughly the last tier, so $O(b^\frac{C^*}{\varepsilon})$
- Is it complete?
	- Assuming best solution has a finite cost and minimum arc cost is positive, yes
- Is it optimal?
	- Yes

#### Uniform Cost Issues
Remember: UCS explores increasing cost contours

The good: UCS is complete and optimal

The bad:
- Explores options in every direction
- No information about goal location

## The One Queue
All these search algorithms are the same except for fringe strategies
- Conceptually, all fringes are priority queues
- Practically, for DFS and BFS, you can avoid the $\log(n)$ overhead from priority queues using stacks and queues
- Can even code one implementation that takes a variable queuing objects

## Search and Models
Search operates over models of the world
- The agent doesn't actually try all the plans out in the real world
- Planning is all "in simulation"
- Your search is only as good as your models...

