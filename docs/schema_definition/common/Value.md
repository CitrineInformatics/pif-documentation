A single scalar, vector, or matrix, or an array of one of those. Exactly one of `scalars`, `vectors`, or `matrices` should be set.

Field name | Value type | Description
-----------|------------|------------
`name` | String | Name of the value.
`scalars` | Array of [`Scalar`](!schema_definition/common/Scalar) objects | One or more scalar values.
`vectors` | Array of arrays of [`Scalar`](!schema_definition/common/Scalar) objects | One or more arrays of scalars, where each inner array represents a vector.
`matrices` | Array of arrays of arrays of [`Scalar`](!schema_definition/common/Scalar) objects | One or more arrays of arrays of scalars, where each represents a single matrix (with innermost arrays being rows of the matrix).
`units` | String | Units of the value.
`tags` | Array of strings | Tags that apply to the value.
