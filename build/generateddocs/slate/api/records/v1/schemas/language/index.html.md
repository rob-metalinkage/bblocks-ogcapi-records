---
title: Schema for language (Schema)

toc_footers:
  - Version 0.1
  - <a href='#'>Schema for language</a>
  - <a href='https://blocks.ogc.org/register.html'>Building Blocks register</a>

search: true

code_clipboard: true

meta:
  - name: Schema for language (Schema)
---


# Schema for language `ogc.api.records.v1.schemas.language`

This building block corresponds to the schema for an OGC API Records language

<p class="status">
    <span data-rainbow-uri="http://www.opengis.net/def/status">Status</span>:
    <a href="http://www.opengis.net/def/status/under-development" target="_blank" data-rainbow-uri>Under development</a>
</p>

<aside class="success">
This building block is <strong>valid</strong>
</aside>


# JSON Schema

```yaml--schema
type: object
description: The language used for textual values in this record.
required:
- code
properties:
  code:
    type: string
    description: The language tag as per RFC-5646.
    example: el
  name:
    type: string
    minLength: 1
    description: The untranslated name of of the language.
    example: "\u0395\u03BB\u03BB\u03B7\u03BD\u03B9\u03BA\u03AC"
  alternate:
    type: string
    description: The name of the language in another well-understood language, usually
      English.
    example: Greek
  dir:
    type: string
    description: The direction for text in this language. The default, `ltr` (left-to-right),
      represents the most common situation. However, care should be taken to set the
      value of `dir` appropriately if the language direction is not `ltr`. Other values
      supported are `rtl` (right-to-left), `ttb` (top-to-bottom), and `btt` (bottom-to-top).
    enum:
    - ltr
    - rtl
    - ttb
    - btt
    default:
    - ltr

```

> <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=yaml&amp;dataUrl=https%3A%2F%2Frob-metalinkage.github.io%2Fbblocks-ogcapi-records%2Fbuild%2Fannotated%2Fapi%2Frecords%2Fv1%2Fschemas%2Flanguage%2Fschema.yaml&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on YAML Viewer</a>

Links to the schema:

* YAML version: <a href="https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/language/schema.yaml" target="_blank">https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/language/schema.yaml</a>
* JSON version: <a href="https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/language/schema.json" target="_blank">https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/language/schema.json</a>

# References

* [OGC API Records - Draft](https://docs.ogc.org/DRAFTS/20-004.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: <a href="https://github.com/rob-metalinkage/bblocks-ogcapi-records" target="_blank">https://github.com/rob-metalinkage/bblocks-ogcapi-records</a>
* Path:
<code><a href="https://github.com/rob-metalinkage/bblocks-ogcapi-records/blob/HEAD/_sources/v1/schemas/language" target="_blank">_sources/v1/schemas/language</a></code>

