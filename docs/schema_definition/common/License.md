## Description

A license describes the licensing agreement that is in place for the data in the object in which it is applied.

## Fields

Field name | Value type | Description
-----------|------------|------------
`name` | String | Name of the license.
`description` | String | Description of the license.
`url` | String | URL to the website with information about the license.
`tags` | Array of strings | Tags that apply to the license.

## Examples

Store the information about the Apache license version 2.0:
```javascript
{
    "name": "Apache License 2.0",
    "url": "https://www.apache.org/licenses/LICENSE-2.0"
}
```
