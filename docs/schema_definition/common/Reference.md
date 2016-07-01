A published work.

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
`pages` | [`Pages`](!schema_definition/common/Pages) object | Starting and ending pages of the work.
`authors` | Array of [`Name`] objects | Authors of the work.
`editors` | Array of [`Name`] objects | Editors of the work.
`references` | Array of [`Reference`] objects | Publications cited by the work.
`tags` | Array of strings | Tags that apply to the reference.
