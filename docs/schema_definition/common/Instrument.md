## Description
An instrument is a piece of physical equipment that was used in a measurement or other application.

## Fields
Field name | Value type | Description
-----------|------------|------------
`name` | String | Name of the instrument.
`model` | String | Model of the instrument.
`producer` | String | Manufacturer of the instrument.
`url` | String | URL to the website with information about the instrument.
`tags` | Array of strings | Tags that apply to the instrument.

## Examples

Store information about a Bruker NANOSTAR X-ray diffraction instrument:
```javascript
{
    "producer": "Bruker",
    "model": "NANOSTAR",
    "url": "https://www.bruker.com/products/x-ray-diffraction-and-elemental-analysis/x-ray-diffraction/nanostar"
}
```
