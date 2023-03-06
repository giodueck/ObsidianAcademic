03-03-2023
---
# Chapter 2 - Agents and Environments

## Agents
Agents include humans, robots, softbots, thermostats, etc.

The agent function maps from percept histories to actions
$f:p^* \rightarrow A$

The agent program runs on the physical architecture to produce $f$

### Vacuum-cleaner world

```
   v- Vacuum-cleaner
+-----+-----+
| [o] |     +
| Drt | Drt +  <- dirt
+-----+-----+
```

Percept: location and contents, e.g. $[A, Dirty]$
Actions: $Left, Right, Suck, NoOp$

Percept sequence | Action
---------------- | ------
$[A, Clean]$ | $Right$
$[A, Dirty]$ | $Suck$
$[B, Clean]$ | $Left$
$[B, Dirty]$ | $Suck$
$[A, Clean], [A, Clean]$ | $Right$
$[A, Clean], [A, Dirty]$ | $Suck$
... | ...

This behavior can be translated into a function:
```
function REFLEX-VACUUM-AGENT([location, status]) returns an action
	if status = Dirty then return Suck
	else if location = A then return Right
	else if location = B then return Left
```

What is the *right* function?
Can it be implemented in a small agent program?

## Rationality
Fixed performance measure evaluates the environment sequence
- 1 point per square cleaned in time T?
- 1 point per clean square per time step, minus 1 per move?
- penalize for $> k$ dirty squares?

A rational agent chooses whichever action maximizes the expected value of the performance measure given the percept sequence to date

Rational $\ne$ omniscient
- percepts may not supply all relevant information

Rational $\ne$ clairvoyant
- action outcomes may not be as expected

Hence, rational $\ne$ successful

Rational $\Rightarrow$ exploration, learning, autonomy

## PEAS

To design a rational agent, we must specify the task environment

Consider for example the design of an automated taxi

**Performace measure?** safety, destination, profits, legality, comfort...

**Environment?** US streets/freeways, traffic, pedestrians, weather...

**Actuators?** steering, accelerator, brake, horn, speaker/display

**Sensors?** video, accelerometers, gauges, engine sensores, keyboard, GPS

Excercises for design can be done by considering these four elements

## Environment types

/ | Solitaire | Backgammon | Internet Shopping | Taxi
--- | --- | --- | --- | ---
**Observable?** | Yes | Yes | No | No
**Deterministic?** | Yes | No | Partly | No
**Episodic?** | No | No | No | No
**Static?** | Yes | Semi | Semi | No
**Discrete?** | Yes | Yes | Yes | No
**Single-agent?** | Yes | No | Yes (except auctions) | No

*The environment type largely determines the agent design*

The real world is (of course) partially observable, stochastic, sequential, dynamic, continuous, milti-agent

## Agent types
Four basic types in increasing order of generality
- Simple reflex agents:
	- capts some information from sensors and acts through its actuators according to some condition-action rules
- Reflex agents with state:
	- same as above, but keeps some information about the environment, which evolves with new information from sensors. The sensor input and internal state both influence the taken actions
- Goal-based agents:
	- keeps an internal state like the above agent, but now a goal determines the next action, and not a set of rules. Acts according to sensor input, internal state, how the world changes and what the goal is
- Utility-based agents:
	- Same as above, but instead of goals the leading metric is utility. Acts based on state and inputs and which action will maximize some utility function

All these can be turned into learning agents.
This is done using some performance element, judged by a critic whose feedback changes the behavior of the agent based on the learning goals.