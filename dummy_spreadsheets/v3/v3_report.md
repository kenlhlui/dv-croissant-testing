# CROISSANT VALIDATION REPORT
================================================================================
## VALIDATION RESULTS
--------------------------------------------------------------------------------
Starting validation for file: v3.json
### JSON Format Validation
✓
The file is valid JSON.
### Croissant Schema Validation
✓
The dataset passes Croissant validation.
### Records Generation Test
?
Record set '_:N593ac8729f414b05938c6811ed561037' failed due to generation error:

```text
An error occured during the streaming generation of the dataset, more specifically during the operation Read(v2_csv.csv)

Traceback (most recent call last):
  File "/usr/local/lib/python3.10/site-packages/mlcroissant/_src/operation_graph/execute.py", line 97, in execute_operations_in_streaming
    yield from operation.call(result)
  File "/usr/local/lib/python3.10/site-packages/mlcroissant/_src/operation_graph/operations/field.py", line 254, in call
    yield from df[i : i + chunk_size].apply(_get_result, axis=1)
  File "/usr/local/lib/python3.10/site-packages/pandas/core/frame.py", line 10374, in apply
    return op.apply().__finalize__(self, method="apply")
  File "/usr/local/lib/python3.10/site-packages/pandas/core/apply.py", line 916, in apply
    return self.apply_standard()
  File "/usr/local/lib/python3.10/site-packages/pandas/core/apply.py", line 1063, in apply_standard
    results, res_index = self.apply_series_generator()
  File "/usr/local/lib/python3.10/site-packages/pandas/core/apply.py", line 1081, in apply_series_generator
    results[i] = self.func(v, *self.args, **self.kwargs)
  File "/usr/local/lib/python3.10/site-packages/mlcroissant/_src/operation_graph/operations/field.py", line 219, in _get_result
    assert column in df, (
AssertionError: Column "v2_csv.csv" does not exist. Inspect the ancestors of the field Field(uuid="_:Nc2e734a7645f4ca799171249d26cdc44") to understand why. Possible fields: Index([     'column_one_csv',      'column_two_csv', FileProperty.filepath,
       FileProperty.filename, FileProperty.fullpath],
      dtype='object')

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/usr/local/lib/python3.10/site-packages/mlcroissant/_src/operation_graph/execute.py", line 115, in execute_operations_in_streaming
    yield from read_all_files()
  File "/usr/local/lib/python3.10/site-packages/mlcroissant/_src/operation_graph/execute.py", line 108, in read_all_files
    yield from execute_operations_in_streaming(
  File "/usr/local/lib/python3.10/site-packages/mlcroissant/_src/operation_graph/execute.py", line 121, in execute_operations_in_streaming
    raise GenerationError(
mlcroissant._src.core.issues.GenerationError: An error occured during the streaming generation of the dataset, more specifically during the operation ReadFields(_:N593ac8729f414b05938c6811ed561037)

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
mlcroissant._src.core.issues.GenerationError: An error occured during the streaming generation of the dataset, more specifically during the operation Read(v2_csv.csv)
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
  "version": "3.0",
  "citeAs": "@data{FK2/KRWRTA_2025,author = {Lui, Ken},publisher = {Borealis},title = {Test croissant},year = {2025},url = {https://doi.org/10.80240/FK2/KRWRTA}}",
  "distribution": [
    {
      "@type": "cr:FileObject",
      "@id": "v2_csv.csv",
      "name": "v2_csv.csv",
      "encodingFormat": "text/csv",
      "md5": "c44e365e4093df3a2fd52cfb92211db9",
      "contentSize": "2331",
      "description": "",
      "contentUrl": "https://demo.borealisdata.ca/api/access/datafile/51757?format=original"
    },
    {
      "@type": "cr:FileObject",
      "@id": "v2_xlsx.xlsx",
      "name": "v2_xlsx.xlsx",
      "encodingFormat": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet",
      "md5": "c263b3e6a38ec6f1a143907782f02ab4",
      "contentSize": "12892",
      "description": "",
      "contentUrl": "https://demo.borealisdata.ca/api/access/datafile/51756?format=original"
    }
  ],
  "recordSet": [
    {
      "@type": "cr:RecordSet",
      "field": [
        {
          "@type": "cr:Field",
          "name": "column_one_csv",
          "description": "column_one_csv",
          "dataType": "sc:Float",
          "source": {
            "@id": "178190",
            "fileObject": {
              "@id": "v2_csv.csv"
            }
          }
        },
        {
          "@type": "cr:Field",
          "name": "column_two_csv",
          "description": "column_two_csv",
          "dataType": "sc:Float",
          "source": {
            "@id": "178191",
            "fileObject": {
              "@id": "v2_csv.csv"
            }
          }
        }
      ]
    },
    {
      "@type": "cr:RecordSet",
      "field": [
        {
          "@type": "cr:Field",
          "name": "coulumnonexlsx",
          "description": "coulumnonexlsx",
          "dataType": "sc:Float",
          "source": {
            "@id": "178192",
            "fileObject": {
              "@id": "v2_xlsx.xlsx"
            }
          }
        },
        {
          "@type": "cr:Field",
          "name": "columntwoxlsx",
          "description": "columntwoxlsx",
          "dataType": "sc:Float",
          "source": {
            "@id": "178194",
            "fileObject": {
              "@id": "v2_xlsx.xlsx"
            }
          }
        },
        {
          "@type": "cr:Field",
          "name": "columntreexlsx",
          "description": "columntreexlsx",
          "dataType": "sc:Float",
          "source": {
            "@id": "178193",
            "fileObject": {
              "@id": "v2_xlsx.xlsx"
            }
          }
        }
      ]
    }
  ]
}
```