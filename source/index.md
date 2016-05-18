---
title: Citrination API Reference

language_tabs:
  - python

toc_footers:
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Citrination API Documentation! The Citrination API can be used to query our extensive database of material properties in a couple of exciting ways.

We have language bindings in Shell, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

Data from the API is returned in the MIF file format. Read more about the [Mif file format](http://citrineinformatics.github.io/mif-documentation). Our documentation also references a  python reference implementation. Download the [python reference implementation](https://github.com/CitrineInformatics/python-citrination-client).

# Authentication

> To authenticate, you must obtain your API key from Citrine Informatics

```python
from citrination_client import CitrinationClient
client = CitrinationClient('your-unique-api-key', 'https://yoursite.citrination.com')
```

```
# Authentication tokens must be applied to the headers of any requests made to the Citrination API
curl "api_endpoint_here"
  -H "X-API-Key: your-unique-api-key"
```

Citrination uses API keys to allow access to the API. You can register a new Kittn API key by logging in to your instance of Citrination, clicking on your username and selecting 'Account'.

Citrination expects for the API key to be included in all API requests to the server in a header that looks like the following:

`X-API-Key: your-unique-api-key`

# Materials Data

## Search Data
```python
from citrination_client import CitrinationClient
client = CitrinationClient('your-unique-api-key', 'https://yoursite.citrination.com')
client.search(term='RbOs2O6', from_page=0, per_page=10)
```

```shell
curl --data "term=RbOs2O6&from=0&per_page=10"
 "https://your-site.citrination.com/api/mifs/search"
  -H "X-API-Key: your-api-key"
  -H "Content-Type: application/json"
```

> The above command returns JSON structured like this:

```json
{
    "sample": {
        "data_set_id": 213,
        "material": {
            "chemicalFormula": "RbOs2O6"
        },
        "measurement": [
            {
                "property": {
                    "units": "K",
                    "scalar": [
                        {
                            "value": "6.3"
                        }
                    ],
                    "name": "Superconducting critical temperature (Tc)"
                },
                "reference": [
                    {
                        "url": "http://arxiv.org/abs/1109.5422v1"
                    },
                    {
                        "doi": "10.1143/jpsj.80.104708"
                    }
                ]
            }
        ]
    }
}
```

This endpoint searches data based on text input to the term field. We index chemical formulas in a variety of ways, and the term field in this method is very flexible. For example, you could search "band gap of gallium nitride", or "ternary oxides" and get back a variety of interesting results, ranked according to our proprietary scoring algorithm.

### HTTP Request
`POST https://your-site.citrination.com/api/mifs/search`

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
term | true | The basic search query
formula | false | Limit the search results by the chemical formula entered here
contributor | false | Limit the search results by the name of the person that contributed the data
reference | false | Limit the search results by the original reference for the data
min_measurement | false | Minimum decimal value for property value
max_measurement | false | Maximum decimal value for property value
from | false | If using pagination, set the starting record. Defaults to 0
per_page | false | If using pagination, sets how many records to return. Defaults to 10


<aside class="success">
Don't forget your API key!
</aside>


## Search a specific data set  
```python
from citrination_client import CitrinationClient
client = CitrinationClient('your-unique-api-key', 'https://yoursite.citrination.com')
client.search(term='RbOs2O6', from_page=0, per_page=10, data_set_id=213)
```

```shell
curl --data "term=RbOs2O6&from=0&per_page=10"
 "https://your-site.citrination.com/api/data_sets/213/mifs/search"
  -H "X-API-Key: your-api-key"
  -H "Content-Type: application/json"
```

> The above command returns JSON structured like this:

```json
{
    "sample": {
        "data_set_id": 213,
        "material": {
            "chemicalFormula": "RbOs2O6"
        },
        "measurement": [
            {
                "property": {
                    "units": "K",
                    "scalar": [
                        {
                            "value": "6.3"
                        }
                    ],
                    "name": "Superconducting critical temperature (Tc)"
                },
                "reference": [
                    {
                        "url": "http://arxiv.org/abs/1109.5422v1"
                    },
                    {
                        "doi": "10.1143/jpsj.80.104708"
                    }
                ]
            }
        ]
    }
}
```
This API is identical to the main search API, but limited to a particular data_set. You will notice that the search results include a "mif_id" field. This ID is the value to supply to the data_sets endpoint when searching.

This endpoint searches data based on text input to the term field. We index chemical formulas in a variety of ways, and the term field in this method is very flexible. For example, you could search "band gap of gallium nitride", or "ternary oxides" and get back a variety of interesting results, ranked according to our proprietary scoring algorithm.

<aside class="warning">
You can use a ? in the 'term' parameter to retrieve all structured data for a given sample.
</aside>

### HTTP Request

`POST https://your-site.citrination.com/api/data_sets/<id>/mifs/search`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the sample to search

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
term | true | The basic search query
formula | false | Limit the search results by the chemical formula entered here
contributor | false | Limit the search results by the name of the person that contributed the data
reference | false | Limit the search results by the original reference for the data
min_measurement | false | Minimum decimal value for property value
max_measurement | false | Maximum decimal value for property value
from | false | If using pagination, set the starting record. Defaults to 0
per_page | false | If using pagination, sets how many records to return. Defaults to 10


<aside class="success">
Don't forget your API key!
</aside>


## Upload Data
```python
from citrination_client import CitrinationClient
client = CitrinationClient('your-unique-api-key', 'https://yoursite.citrination.com')
client.upload(name='My Published Paper', description='Band Gaps of My Favorite Compounds', filename='mypaper.pdf')
```

You can upload data using the python client, but not directly through HTTP at this time.
Uploading data will start it off in our data processing pipeline, and in a few minutes time
it will be available on the web via https://your-site.citrination.com/data_uploads
