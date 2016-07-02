## Description

A `ChemicalSystem` is a specialization of the more generic [`System`](!schema_definition/system/System) type. Chemical systems add information about chemical composition to a system.

## Fields

Field name | Value type | Description
-----------|------------|------------
`chemicalFormula` | String | Chemical formula of the system.
`composition` | Array of [`Composition`](!schema_definition/system/chemical/common/Composition) objects | The elements in the chemical system and their relative atomic and weight percentages.
`names` | Array of strings | Common names of the chemical system.
`ids` | Array of [`Id`](!schema_definition/common/Id) objects | IDs (named labels) of the chemical system.
`properties` | Array of [`Property`](!schema_definition/common/Property) objects | Measured or observed properties.
`preparation` | Array of [`ProcessStep`](!schema_definition/common/ProcessStep) objects | Process steps carried out in preparing the chemical system.
`subSystems` | Array of [`System`](!schema_definition/system/System) objects | Subsystems that the chemical system is composed of.
`references` | Array of [`Reference`](!schema_definition/common/Reference) objects | References where information about the chemical system is published.
`contacts` | Array of [`Person`](!schema_definition/common/Person) objects | People that can be contacted for further information about the chemical system.
`licenses` | Array of [`License`](!schema_definition/common/License) objects | Licenses that apply to the data about the chemical system.
`tags` | Array of strings | Tags that apply to the chemical system.

## Examples
