## Description

A property is a single measured or observed characteristic or response of a system. Exactly one of `scalars`, `vectors`, or `matrices` should be set. Any applied conditions should be stored under the `conditions` field. Two-dimensional data can be stored by setting, for example, _N_ (> 1) values in the `scalars` field along with a condition that contained _N_ values in its `scalars` field.

## Fields

Field name | Value type | Description
-----------|------------|------------
`name` | String | Name of the property.
`scalars` | Array of [`Scalar`](!schema_definition/common/Scalar) objects | One or more scalar values that were obtained for the property.
`vectors` | Array of arrays of [`Scalar`](!schema_definition/common/Scalar) objects | One or more arrays of scalars, where each inner array represents a vector that was obtained for the property.
`matrices` | Array of arrays of arrays of [`Scalar`](!schema_definition/common/Scalar) objects | One or more arrays of arrays of scalars, where each represents a single matrix (with innermost arrays being rows of the matrix).
`units` | String | Units of the property value.
`conditions` | Array of [`Value`](!schema_definition/common/Value) objects | External conditions under which the property was measured or observed.
`methods` | Array of [`Method`](!schema_definition/common/Method) objects | Methods that were used in the measurement of the property.
`dataType` | "MACHINE_LEARNING", "COMPUTATIONAL", or "EXPERIMENTAL" | Whether the property was obtained from machine learning, computational methods, or experiment.
`references` | Array of [`Reference`](!schema_definition/common/Reference) objects | References where information about the property is published.
`contacts` | Array of [`Person`](!schema_definition/common/Person) objects | People that can be contacted for further information about the property.
`licenses` | Array of [`License`](!schema_definition/common/License) objects | Licenses that apply to the data about the property.
`tags` | Array of strings | Tags that apply to the property.

## Examples
