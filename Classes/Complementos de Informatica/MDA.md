23-08-2023
---
# Model Driven Architecture

The Object Management Group (OMG) has defined its own comprehensive proposal applying MDE in systems programming: MDA.

## Four principles of MDA
1. Models must be expressed in a well-defined notation
2. Systems specifications must be organized around a set of models and associated transformations
3. Models must be compliant with metamodels
4. Increase acceptance, broad adoption and tool competition for MDE

## Modeling levels
- Computation independent (CIM): Business view of solution
- Platform independent (PIM): Description of the system
- Platform-specific (PSM): Description of the system including platform-specific technologies

## MDA Standards
- UML - Unified Modeling Language
- CWM - Common Warehouse Metamodel
- MOF - Meta Object Facility
- XMI - XML Metadata Interchange
- QVT - Queries/Views/Transformations
- ...

MDA's core is UML.
Two options for specifying your languages:
- (Domain-specific) UML Extensions can be defined through UML Profiles
- Full-fledged Domain-specific languages (DSMLs) can be defined by MOF

Many UML tools are expanded to MDA tools

## Advantages
- Standardization of the Meta Level
- Separation of platform independent and platform specific models (reuse)

## Disadvantages
- Modeling languages practically limited to UML with profiles

