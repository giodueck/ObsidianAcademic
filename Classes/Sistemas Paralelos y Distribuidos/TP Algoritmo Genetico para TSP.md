25-04-2023
---
# TP Algoritmo Genetico para TSP
## Algoritmos geneticos
> [!Note] Wikipedia
> In computer science and operations research, a genetic algorithm (GA) is a metaheuristic inspired by the process of natural selection that belongs to the larger class of evolutionary algorithms (EA). Genetic algorithms are commonly used to generate high-quality solutions to optimization and search problems by relying on biologically inspired operators such as mutation, crossover and selection.

Components:
- A genetic representation of solution domain
- A fitness function to evaluate the solution domain

### Initialization
Initial population is often randomly generated

### Selection
During each successive generation, a portion of the existing popultation is selected to to reproduce for a new generation (or survive). The selection is based on a fitness score basis, where fitter solutions are more likely to get selected.

This selection can apply to the whole population or only a few randomly selected individuals.

Elitist selection is a type of selection in which the fittest individuals are selected and remain unchanged across generations. This helps preserve good solutions.

### Genetic operators
From the selected population a new generation is created through some genetic operators:
- Crossover:
The parents genes are mixed to create a new individual with combined traits from its parents
- Mutation:
One or more genes of an individual are changed in some random, unpropable and atomic way, introducing genetic drift.

### Heuristics
Some heuristics may be used to make calculations faster or more robust. The *speciation* heuristic penalizes crossover between individuals with too similar chromosomes.

### Termination
This process repeats until some goal or condition is reached. Some common terminating conditions are:
- A solution is found which satisfies minimum criteria
- Fixed number of generations reached
- Allocated budget reached
- Fitness of the highest ranking solution has reached a plateau
- Manual inspection
- Combinations of the above

## TP: GA for TSP
### Chromosome
Sequence of cities visited (genes), length $n =$ number of cities, with no repeated cities.

### Mutations
Swap two or more random genes. Types of swaps:
- Adjacent swap
- Random swap

### Crossover
Given two parent solutions, copy half of the first parents solution and copy the remaining genes from the second parent in the order they appear in.

Types: defined by the half copied from the first parent
- First half
- Last half
- Middle half
- Head and tail quarters

### Selection process
1. Fitness test of entire population
2. Selection of top 50%
3. Some elitist selection for top solutions (next generation are unconditional clones)
4. Some random crossovers (next generation are crossovers)
5. The rest are clones
6. All new individuals (except elite) have a random chance of mutation
