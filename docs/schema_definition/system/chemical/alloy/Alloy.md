## Description

An `Alloy` is a specialization of the more generic [`ChemicalSystem`](!schema_definition/system/chemical/ChemicalSystem) type. Alloys simply alias the `subSystems` field of `ChemicalSystem` as `phases` in implementations of the schema in code. The serialized version of the `Alloy` objects and [`ChemicalSystem`](!schema_definition/system/chemical/ChemicalSystem) objects are the same.

## Fields

Field name | Value type | Description
-----------|------------|------------
`uid` | String | Permanent ID associated with the alloy.
`chemicalFormula` | String | Chemical formula of the alloy.
`composition` | Array of [`Composition`](!schema_definition/system/chemical/common/Composition) objects | The elements in the alloy and their relative atomic and weight percentages.
`names` | Array of strings | Common names of the alloy.
`ids` | Array of [`Id`](!schema_definition/common/Id) objects | IDs (named labels) of the alloy.
`source` | [`Source`](!schema_definition/common/Source) object | Source/producer/manufacturer of the alloy.
`quantity` | [`Quantity`](!schema_definition/common/Quantity) object | Quantity of the alloy.
`properties` | Array of [`Property`](!schema_definition/common/Property) objects | Measured or observed properties.
`preparation` | Array of [`ProcessStep`](!schema_definition/common/ProcessStep) objects | Process steps carried out in preparing the alloy.
`subSystems` | Array of [`System`](!schema_definition/system/System) objects | Subsystems that the alloy is composed of.
`references` | Array of [`Reference`](!schema_definition/common/Reference) objects | References where information about the alloy is published.
`contacts` | Array of [`Person`](!schema_definition/common/Person) objects | People that can be contacted for further information about the alloy.
`licenses` | Array of [`License`](!schema_definition/common/License) objects | Licenses that apply to the data about the alloy.
`tags` | Array of strings | Tags that apply to the alloy.

## Examples
