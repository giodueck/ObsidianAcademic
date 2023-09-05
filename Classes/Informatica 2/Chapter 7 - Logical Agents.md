24-04-2023
---
# Chapter 7 - Logical Agents

## Knowledge bases
*Knowledge base*: set of sentences in a formal language. Domain-specific knowledge.
*Inference engine*: Domain-independent algorithms.

Declarative approach to building an agentL *tell* it what it needs to know.
Then it can *ask* itself what to do, answers should follow from KB.

Agents can be viewed at the knowledge level:
- *what they know*

Or at the implementation level:
- which data structures are used, which algorithms are used

26-04-2023
---
## Entailment
Entailment means that one thing *follows from* another:
$KB \models \alpha$

Knowledge base $KB$ entails a sentence $\alpha$
if and only if
$\alpha$ is true in all worlds where $KB$ is true.

E.g., $x + y = 4$ entails $4 = x + y$

Entailment is a relationship between sentences (i.e. syntax) that is based on semantics.

Node: brains process syntax (of some sort)

### Models
Logicians typically think of models, which are formally structured worlds with respect to which truth can be evalueated.

$m$ is a model of a sentence $\alpha$ if $\alpha$ is true in $m$

$M(\alpha)$ is the set of all models of $\alpha$

Then $KB \models \alpha$ if and only if $M(KB) \subseteq M(\alpha)$

E.g.,
$KB$ - Giants won and Reds won
$\alpha$ - Giants won

### Inference
$KB \vdash_i \alpha$ - sentence $\alpha$ can be derived from $KB$ by a procedure $i$

Consequences of $KB$ are a haystack, $\alpha$ is a needle.
Entailment - needle in haystack; inference - fincding it

Soundness: $i$ is sound if whenever $FB \vdash \alpha$, it is also true that $KB \vdash_i \alpha$

Completeness: $i$ is complete if whenever #incomplete 

## Propositional logic
#incomplete
