16-08-2023
---
# Model-Driven Engineering
## Models
What is a model?

*Mapping feature*: A model is based on an original (a system)
*Reduction feature*: A model only reflects a (relevant) selection of the original's properties
*Pragmatic feature*: A model needs to be usable in place of an original with respect to some purpose

Purposes:
- descriptive: describing the reality of a system or context
- prescriptive: determining the scope and details in which to study a program
- defining how a system shall be implemented

The model always exists, the only option designers have is about its form: it may be *mental* or it may be *explicit*

## Motivation
Model as the *central artifact* of software dev. enables
- Static analysis
- Documentation
- Refactoring/transformation
- Automated testing
- Rapid prototyping
- Code generation

Motivations:
- Increasing *complexity* of software
	- Increasing basic requirements
	- Complex infrastructures
- Software for *specific devices*
	- Web browser, mobile phone, navigation system, etc.
- *Technological progress*
	- Integration of different technologies and legacy systems, migration to new technologies

- ... leads to *problems* with software development
	- Late finishes
	- Wrong functionality
	- Poorly documented software
	- Difficulty in further development

*Traditional* use of models in software development
- *Communication* with customers and users
- Support for software design
- etc.

How models can change SE:
- *Models as drafts*
- *Models as guidelines*
- *Models as programs*

## MDSE: Aim at large
MDSE considers models as first-class citizens in SE

The way in which models are defined and managed is based on the actual needs that they will address

MDSE defines sound engineering approaches to the definition of
- models
- transformations
- development process

## Concepts
**Abstraction** from specific realization technologies
- Requires modeling languages with no specific concepts of any technology
- Improved *portability*: model once, build everywhere
- *Interoperability* between different technologies can be automated (so called technology bridges)

**Automated code generation** from abstracted models
- Requires expressive and precise models
- Increased *productivity* and *efficiency* (models stay up-to-date)

**Separate development** of applications and infrastructures
- Separation of application-code and infrastructure-code (e.g. Application Framework) increases *reusability*

**Models + Transformations = Software**

