## Description

A `System` object is the most generic representation of a physical system in the PIF schema. All other systems are sub-classed from this type.

## Fields

Field name | Value type | Description
-----------|------------|------------
`uid` | String | Permanent ID associated with the system.
`names` | Array of strings | Common names of the system.
`ids` | Array of [`Id`](!schema_definition/common/Id) objects | IDs (named labels) of the system.
`source` | [`Source`](!schema_definition/common/Source) object | Source/producer/manufacturer of the system.
`quantity` | [`Quantity`](!schema_definition/common/Quantity) object | Quantity of the system.
`properties` | Array of [`Property`](!schema_definition/common/Property) objects | Measured or observed properties.
`preparation` | Array of [`ProcessStep`](!schema_definition/common/ProcessStep) objects | Process steps carried out in preparing the system.
`subSystems` | Array of [`System`](!schema_definition/system/System) objects | Subsystems that the system is composed of.
`references` | Array of [`Reference`](!schema_definition/common/Reference) objects | References where information about the system is published.
`contacts` | Array of [`Person`](!schema_definition/common/Person) objects | People that can be contacted for further information about the system.
`licenses` | Array of [`License`](!schema_definition/common/License) objects | Licenses that apply to the data about the system.
`tags` | Array of strings | Tags that apply to the system.

## Examples
