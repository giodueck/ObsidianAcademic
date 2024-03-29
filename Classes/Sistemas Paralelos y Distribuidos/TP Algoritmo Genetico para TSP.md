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

### Selection process
Truncation selection:
1. Fitness test of entire population
2. Selection of top 50%
3. Some elitist selection for top solutions (next generation are unconditional clones)
4. Some (or all) of the next generation
5. The rest are clones
6. All new individuals have a random chance of mutation

Tournament selection:
1. Select k individuals at random
2. Compare fitness of selected solutions
3. Select the top solution for breeding
4. Repeat for another candidate and cross solutions to form new offspring
5. Apply random mutation
6. Replace population with new offspring, except for elite

Tournaments are less costly as not all individuals need their fitness evaluated, and every individual has a chance of winning no matter where it would rank in fitness. Selection pressure can be increased by increasing k.
Supposedly works better in parallel implementations.

### Parallelization
Possible places to parallelize include:
- Fitness function if all are evaluated
- Parallel tournaments
- Several sequential runs in parallel with a merge of populations every N generations

#### Island model
The last parallelization option listed is also known as the *island model*, named after real-life populations that are isolated from each other on islands.

These populations can be evolved in parallel and crossed at one or several midpoints during evolution. Different populations will have different genetic history, and crossover may give new variety to both populations.

Another possibility is having different strategies for different islands, which may increase diversity even more with crossovers.

#### MPI
Islands are assigned to individual nodes, which evolve the population for a set amount of generations.

For crossover between islands either:
- Send whole population from slaves to master node, then crossover in master
- From master send requests for solutions, and send children back immediately
- Pair up islands randomly, perform crossover between them.

The first solution is simpler but will involve sending many solutions in bulk, crossing them in a single node, then sending the crossed populations back to the slaves.
The second is the same, but randomly accessed instead. The result will be the same, but possibly slower and more convoluted.
The third solution avoids the bottleneck of having a single master handling all crossover between islands, instead having it only coordinate how the slaves cross between each other.

### Implementation details
#### Parameters
- Population size: how many solutions are part of each generation
- Generation count: how many generations should be evolved
- Mutation rate: how likely it is for a new cell to present random mutations
- Crossover rate: what proportion of new individuals are generated by crossover as opposed to cloning
- Elite rate: what proportion of successful individuals survive without modification to the next generation
- Islands: how many semi-independent islands of individuals to evolve. Each will use one thread
- Selection strategy: truncation, tournament, or mixed (for more than 1 island)