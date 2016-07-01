A process step is a single stage in a set of preparation steps.

Field name | Value type | Description
-----------|------------|------------
`name` | String | Name of the process step.
`details` | Array of [`Value`](!schema_definition/common/Value) objects | Details of the process step, such as temperature, applied pressure, or duration.
`instruments` | Array of [`Instrument`](!schema_definition/common/Instrument) objects | Instruments that were used during the process step.
`software` | Array of [`Software`](!schema_definition/common/Software) objects | Software packages that were used during the process step.
`tags` | Array of strings | Tags that apply to the process step.
