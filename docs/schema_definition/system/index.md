A system is a root level object in a PIF record. Systems contain three general categories of information:

* Identifiers - What is this?
* Preparation - How was this made?
* Properties - How does this perform?

Additionally, systems can contain publication information for the system, contact information for people that worked on or the system, and licensing information.

A [`System`](!schema_definition/system/System) object is the most generic root object in a PIF record and contains fields that could apply to any physical system. For more specialized use cases, the [`System`](!schema_definition/system/System) type is sub-classed and fields appropriate to that use case are added. For example, [`ChemicalSystem`](!schema_definition/system/chemical/ChemicalSystem) contains all of the fields in [`System`](!schema_definition/system/System), but also adds fields for composition and chemical formula.
