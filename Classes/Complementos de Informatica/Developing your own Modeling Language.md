06-09-2023
---
# Developing your own Modeling Language

Main components of a modeling language:
- Semantics: *Meaning* of the language concepts
- Abstract syntax: Language concepts and how these concepts can be combined
	- *Neither defines meaning* nor *notation*
- Concrete syntax: *Notation* to illustrate the language concepts intuitively
	- *Graphical*, *textual* or a mixture of both

Additional components
- *Extension* of the language by new concepts
- *Mapping* to other languages, domains

## Abstract syntax

### Metamodel-centric language design
All language aspects base on the abstract syntax of the language defined by its metamodel

Advantages in language design:
- Precise
- Accessible
- Evolvable

*Generalization* on a higher level of abstraction by means of the *meta-metamodel*

MOF, with Ecore as its implementation, is considered as a universally accepted meta-metamodel

### MOF: Meta Object Family
OMG standard for the definition of metamodels

*Object-oriented* modeling language:
- *Objects* are described by *classes*
- *Intrinsic properties* of objects are defined as *attributes*
- *Extrinsic properties* (links) between objects are defined as *associations*
- *Packages* group classes

MOF itself is defined by MOF (reflexive) and divided into
- eMOF (essential MOF)
	- Target audience: *metamodelers*
- cMOF (complete MOF)
	- extends eMOF
	- Target audience: *tool manufacturers*

MOF is only a *subset of UML*, similar to a class diagram but more limited

