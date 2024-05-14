---
title: Schema for time (Schema)

toc_footers:
  - Version 0.1
  - <a href='#'>Schema for time</a>
  - <a href='https://blocks.ogc.org/register.html'>Building Blocks register</a>

search: true

code_clipboard: true

meta:
  - name: Schema for time (Schema)
---


# Schema for time `ogc.api.records.v1.schemas.time`

This building block corresponds to the schema for an OGC API Records time

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
nullable: true
properties:
  date:
    type: string
    pattern: ^\d{4}-\d{2}-\d{2}$
  timestamp:
    type: string
    pattern: ^\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}(?:\.\d+)?Z$
  interval:
    type: array
    minItems: 2
    maxItems: 2
    items:
      oneOf:
      - type: string
        pattern: ^\d{4}-\d{2}-\d{2}$
      - type: string
        pattern: ^\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}(?:\.\d+)?Z$
      - type: string
        enum:
        - ..
  resolution:
    type: string
    description: Minimum time period resolvable in the dataset, as an ISO 8601 duration
    example:
    - P1D

```

> <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=yaml&amp;dataUrl=https%3A%2F%2Frob-metalinkage.github.io%2Fbblocks-ogcapi-records%2Fbuild%2Fannotated%2Fapi%2Frecords%2Fv1%2Fschemas%2Ftime%2Fschema.yaml&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on YAML Viewer</a>

Links to the schema:

* YAML version: <a href="https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/time/schema.yaml" target="_blank">https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/time/schema.yaml</a>
* JSON version: <a href="https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/time/schema.json" target="_blank">https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/time/schema.json</a>

# References

* [OGC API Records - Draft](https://docs.ogc.org/DRAFTS/20-004.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: <a href="https://github.com/rob-metalinkage/bblocks-ogcapi-records" target="_blank">https://github.com/rob-metalinkage/bblocks-ogcapi-records</a>
* Path:
<code><a href="https://github.com/rob-metalinkage/bblocks-ogcapi-records/blob/HEAD/_sources/v1/schemas/time" target="_blank">_sources/v1/schemas/time</a></code>

