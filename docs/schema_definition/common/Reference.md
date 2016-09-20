## Description

A published work.

## Fields

Field name | Value type | Description
-----------|------------|------------
`doi` | String | Digital Object Identifier (DOI) of the work.
`isbn` | String | International Standard Book Number (ISBN) of the work.
`issn` | String | International Standard Serial Number (ISSN) of the work.
`url` | String | URL of the website where the work can be accessed.
`title` | String | Title of the work.
`publisher` | String | Publisher of the work.
`journal` | String | Journal in which the work was published.
`volume` | String | Volume of the series in which the work was published.
`issue` | String | Issue of the series in which the work was published.
`year` | String | Year in which the work was published.
`figure` | [`DisplayItem`](!schema_definition/common/DisplayItem) object | A specific figure being referenced.
`table` | [`DisplayItem`](!schema_definition/common/DisplayItem) object | A specific table being referenced.
`pages` | [`Pages`](!schema_definition/common/Pages) object | Starting and ending pages of the work.
`authors` | Array of [`Name`](!schema_definition/common/Name) objects | Authors of the work.
`editors` | Array of [`Name`](!schema_definition/common/Name) objects | Editors of the work.
`affiliations` | Array of strings | One or more affiliations of the authors or editors of the work.
`acknowledgements` | Array of strings | One or more acknowledgements made in the work.
`references` | Array of [`Reference`](!schema_definition/common/Reference) objects | Publications cited by the work.
`tags` | Array of strings | Tags that apply to the reference.

## Examples
