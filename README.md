---
pretty_name: Garry's Mod Wiki Documentation
language:
- en
tags:
- garrys-mod
- gmod
- lua
- glua
- game-development
- programming
- documentation
- rag
task_categories:
- text-generation
configs:
- config_name: default
  data_files:
  - split: train
    path: data/*.json
license: mit
---
# Garry's Mod Wiki Documentation Dataset

## Overview

A structured collection of Garry's Mod API documentation intended for local language models, coding agents, retrieval-augmented generation (RAG), and programming assistance.

The dataset organizes documentation into structured JSON records, retaining API names, descriptions, realms, function signatures, enum fields, and source URLs where available.

## Data Fields

Records may contain the following fields, depending on their documentation type:

| Field               | Description                                                          |
| ------------------- | -------------------------------------------------------------------- |
| `name`              | Original documentation name                                          |
| `canonicalName`     | Normalized identifier derived from the documentation URL             |
| `description`       | Description of the API element                                       |
| `realms`            | Applicable execution realms, such as `client`, `server`, or `shared` |
| `documentationURLs` | Source documentation URLs                                            |
| `retrievalDate`     | Date the record was retrieved                                        |
| `functions`         | Nested function documentation, where applicable                      |
| `fields`            | Enum members or other structured fields, where applicable            |
| `arguments`         | Function arguments, where documented                                 |
| `returnValues`      | Function return values, where documented                             |

Not every record contains every field.

## Intended Uses

* API documentation retrieval for local coding agents
* Retrieval-augmented generation (RAG)
* Lua code-generation assistance
* API lookup and realm filtering
* Documentation search and cross-referencing

## Source

Documentation source: [Garry's Mod Wiki](https://wiki.facepunch.com/gmod/)

## Data Limitations

The dataset is programmatically collected and may contain missing fields, outdated descriptions, invalid URLs, or inconsistencies in canonical names. Verify generated code against the official documentation before use.

## License

The dataset's licensing and redistribution terms have not been specified here. Review the source website's terms and determine an appropriate dataset license before publishing.
