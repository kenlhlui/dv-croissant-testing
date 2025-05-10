# CROISSANT VALIDATION REPORT
================================================================================
## VALIDATION RESULTS
--------------------------------------------------------------------------------
Starting validation for file: v1_1.json
### JSON Format Validation
✓
The file is valid JSON.
### Croissant Schema Validation
✓
The dataset passes Croissant validation.
### Records Generation Test
?
Record set '_:Na1d3349ce07c4b129d3fd42966e49531' failed due to generation error:

```text
An error occured during the streaming generation of the dataset, more specifically during the operation Download(new_xlsx.xlsx)

Traceback (most recent call last):
  File "/usr/local/lib/python3.10/site-packages/mlcroissant/_src/operation_graph/execute.py", line 119, in execute_operations_in_streaming
    result = operation.call(result)
  File "/usr/local/lib/python3.10/site-packages/mlcroissant/_src/operation_graph/operations/download.py", line 232, in call
    self._download_from_http(filepath)
  File "/usr/local/lib/python3.10/site-packages/mlcroissant/_src/operation_graph/operations/download.py", line 191, in _download_from_http
    response.raise_for_status()
  File "/usr/local/lib/python3.10/site-packages/requests/models.py", line 1024, in raise_for_status
    raise HTTPError(http_error_msg, response=self)
requests.exceptions.HTTPError: 403 Client Error: Forbidden for url: https://demo.borealisdata.ca/api/access/datafile/51750?format=original

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/home/user/app/validation.py", line 61, in validate_records
    raise result  # re-raise actual error outside timeout
  File "/home/user/app/validation.py", line 37, in try_generate_record
    next(record_iterator)
  File "/usr/local/lib/python3.10/site-packages/mlcroissant/_src/datasets.py", line 166, in __iter__
    yield from execute_operations_in_streaming(
  File "/usr/local/lib/python3.10/site-packages/mlcroissant/_src/operation_graph/execute.py", line 121, in execute_operations_in_streaming
    raise GenerationError(
mlcroissant._src.core.issues.GenerationError: An error occured during the streaming generation of the dataset, more specifically during the operation Download(new_xlsx.xlsx)
```
## JSON-LD REFERENCE
================================================================================
```json
{
  "@context": {
    "@language": "en",
    "@vocab": "https://schema.org/",
    "citeAs": "cr:citeAs",
    "column": "cr:column",
    "conformsTo": "dct:conformsTo",
    "cr": "http://mlcommons.org/croissant/",
    "rai": "http://mlcommons.org/croissant/RAI/",
    "data": {
      "@id": "cr:data",
      "@type": "@json"
    },
    "dataType": {
      "@id": "cr:dataType",
      "@type": "@vocab"
    },
    "dct": "http://purl.org/dc/terms/",
    "examples": {
      "@id": "cr:examples",
      "@type": "@json"
    },
    "extract": "cr:extract",
    "field": "cr:field",
    "fileProperty": "cr:fileProperty",
    "fileObject": "cr:fileObject",
    "fileSet": "cr:fileSet",
    "format": "cr:format",
    "includes": "cr:includes",
    "isLiveDataset": "cr:isLiveDataset",
    "jsonPath": "cr:jsonPath",
    "key": "cr:key",
    "md5": "cr:md5",
    "parentField": "cr:parentField",
    "path": "cr:path",
    "recordSet": "cr:recordSet",
    "references": "cr:references",
    "regex": "cr:regex",
    "repeated": "cr:repeated",
    "replace": "cr:replace",
    "sc": "https://schema.org/",
    "separator": "cr:separator",
    "source": "cr:source",
    "subField": "cr:subField",
    "transform": "cr:transform",
    "wd": "https://www.wikidata.org/wiki/",
    "@base": "cr_base_iri/"
  },
  "@type": "sc:Dataset",
  "conformsTo": "http://mlcommons.org/croissant/1.0",
  "name": "Test croissant",
  "url": "https://doi.org/10.80240/FK2/KRWRTA",
  "creator": [
    {
      "@type": "Person",
      "givenName": "Ken",
      "familyName": "Lui",
      "affiliation": {
        "@type": "Organization",
        "name": "University of Toronto"
      },
      "name": "Lui, Ken"
    }
  ],
  "description": "Testing croissant metadata generation",
  "keywords": [
    "Computer and Information Science"
  ],
  "license": "http://creativecommons.org/publicdomain/zero/1.0",
  "datePublished": "2025-05-09",
  "dateModified": "2025-05-09",
  "includedInDataCatalog": {
    "@type": "DataCatalog",
    "name": "Borealis",
    "url": "https://demo.borealisdata.ca"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Borealis"
  },
  "version": "1.1",
  "citeAs": "@data{FK2/KRWRTA_2025,author = {Lui, Ken},publisher = {Borealis},title = {Test croissant},year = {2025},url = {https://doi.org/10.80240/FK2/KRWRTA}}",
  "distribution": [
    {
      "@type": "cr:FileObject",
      "@id": "new_csv.csv",
      "name": "new_csv.csv",
      "encodingFormat": "text/csv",
      "md5": "2c6c4f9b62753b51e184075eb7a7a421",
      "contentSize": "2331",
      "description": "file with same column header",
      "contentUrl": "https://demo.borealisdata.ca/api/access/datafile/51749"
    },
    {
      "@type": "cr:FileObject",
      "@id": "new_xlsx.xlsx",
      "name": "new_xlsx.xlsx",
      "encodingFormat": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet",
      "md5": "d07f189aec0ff5195c82843b88f84f11",
      "contentSize": "11584",
      "description": "",
      "contentUrl": "https://demo.borealisdata.ca/api/access/datafile/51750?format=original"
    }
  ],
  "recordSet": [
    {
      "@type": "cr:RecordSet",
      "field": [
        {
          "@type": "cr:Field",
          "name": "coulumnonexlsx",
          "description": "coulumnonexlsx",
          "dataType": "sc:Float",
          "source": {
            "@id": "178001",
            "fileObject": {
              "@id": "new_xlsx.xlsx"
            }
          }
        },
        {
          "@type": "cr:Field",
          "name": "columntwoxlsx",
          "description": "columntwoxlsx",
          "dataType": "sc:Float",
          "source": {
            "@id": "178002",
            "fileObject": {
              "@id": "new_xlsx.xlsx"
            }
          }
        }
      ]
    }
  ]
}
```