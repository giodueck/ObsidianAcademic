03-03-2023
---
# Chapter 1 - Introduccion a la Inteligencia Artificial

## What is AI?
Some definitions:

Systems that...   | Systems that...
----------------- | ------
think like humans | think rationally
act like humans   | act rationally

## Acting humanly: Turing test
1950s
Can machines think? Can machines behave intelligently?

- Operational test: the *Immitation Game*
	A human asks questions, to which either a person or a machine answers. The person does not know which one
- Predicted that by 2000, a machine would have a 30% chance to fool a lay person for 5 minutes
- Anticipated major arguments against AI by 50 years
- Suggested major components of AI:
	- knowledge
	- reasoning
	- language understanding
	- learning
- *Problem*: Turing test is not reproducible, constructive, or amenable to mathematical analysis

## Thinking humanly: Cognitive test
1960s
"Cognitive revolution": information-processing psycology replaced behaviorism

Requires scientific theories of internal activities of the brain:
- What level of abstraction? Knowledge or circuits?
- How to validate? Requires either:
	1. Predicting or testing behavior of human subjects (top-down)
	2. Direct identification from neurological data (bottom-up)

Cognitive Science and Cognitive neuroscience are separate from AI

## Thinking rationally: Laws of thought
Normative or prescriptive rather than descriptive

Aristotle: what are correct arguments/thought processes?

Greek schools of logic: notation and rules of derivation for thoughts, may or may not have preceeded the idea of mechanization

Direct line through math and philosofy to modern AI

Problem:
1. Not all intelligent behavior is derived logically
2. What is the purpose of thinking? What thoughts *should* I have out of all the thoughts that I *could* have?

## Acting rationally
Rational behavior: doing the right thing

The right thing: that which is expected to maximiza the goal achievement, given the right information

Doesn't necessarily involve thinkin - e.g. blinking reflex - but thinking should be in the service of ratoional action

Aristotle (Nicomachean Ethics):
> Every art and every inquiry, and similarly every action and pursuit, is thought to aim at some good

## Rational agents
An *agent* is an entity that perceives and acts

This course is about designing rational agents

Abtractly: an agent is a function from percept histories to actions:
$f:p^* \rightarrow A$

For any given class of environment and tasks, we seek the agent (or class of agents) with the best possible performance

Caveat: *computational limitations make perfect rationality unachievable*
$\rightarrow$ desigh best program for given machine resources

## AI prehistory

*Philosophy*
- logic, methods of reasoning
- mind as physical system
- foundations of learning, language, rationality

*Mathematics*
- formal representation and proof
- algorithms, computation, (un)decidability, (in)tractability
- probability

*Psychology*
- adaptation
- phenomena of perception and motor control
- experimental techniques (psychophysics, etc.)

*Economics*
- formal theory of rational decisions

*Linguistics*
- knowledge representation
- grammar

*Neuroscience*
- plastic physical substrate for mental activity

*Control theory*
- homeostatic systems, stability
- simple optimal agent designs

## State of the Art
Which can be done at present?
- [x] Play a decent game of ping-pong
- [x] Drive safely along a curving mountain road
- [ ] Drive safely along Telegraph avenue
- [x] Buy a week's worth of groceries on the web
- [ ] Buy a week's worth of groceries at Berkeley Bowl
- [x] Play a decent game of bridge
- [ ] [-] Discover and prove a new mathematical theorem
- [ ] [-] Design and execute a research program in molecular biology
- [ ] Write an intentionally funny story
- [x] Give competent legal advice in a specialized area of law
- [x] Translate spoken English into Swedish in real time
- [x] Converse successfully with another person for an hour
- [ ] [-] Perform a complex surgical operation
- [ ] Unload any dishwasher and put everything away

