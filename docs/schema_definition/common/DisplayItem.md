## Description

A display item (figure or table) that appears in a referenced work.

## Fields

Field name | Value type | Description
-----------|------------|------------
`number` | String | Number of the display item in the referenced work.
`title` | String | Title of the display item.
`caption` | String | Caption that appears with the display item.
`tags` | Array of strings | Tags that apply to the display item.

## Examples

Store the information about a plot 2a that appeared in a referenced work.
```javascript
{
    "number": "2a",
    "title": "Band gap vs. temperature",
    "description": "The band gap is presented in units of eV as a function of temperature in K."
}
```
