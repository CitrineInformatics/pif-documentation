## Description

Information about an element in a chemical system including its type and relative amount.

## Fields

Field name | Value type | Description
-----------|------------|------------
`element` | String | Name or symbol of the element.
`actualWeightPercent` | [`Scalar`](!schema_definition/common/Scalar) object | Actual (measured) weight percent of the element.
`idealWeightPercent` | [`Scalar`](!schema_definition/common/Scalar) object | Ideal (theoretical/stoichiometric) weight percent of the element.
`actualAtomicPercent` | [`Scalar`](!schema_definition/common/Scalar) object | Actual (measured) atomic percent of the element.
`idealAtomicPercent` | [`Scalar`](!schema_definition/common/Scalar) object | Ideal (theoretical/stoichiometric) atomic percent of the element.
`tags` | Array of strings | Tags that apply to the composition.

## Examples
