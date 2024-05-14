---
title: Schema for linkTemplate (Schema)

toc_footers:
  - Version 0.1
  - <a href='#'>Schema for linkTemplate</a>
  - <a href='https://blocks.ogc.org/register.html'>Building Blocks register</a>

search: true

code_clipboard: true

meta:
  - name: Schema for linkTemplate (Schema)
---


# Schema for linkTemplate `ogc.api.records.v1.schemas.linkTemplate`

This building block corresponds to the schema for an OGC API Records linkTemplate

<p class="status">
    <span data-rainbow-uri="http://www.opengis.net/def/status">Status</span>:
    <a href="http://www.opengis.net/def/status/under-development" target="_blank" data-rainbow-uri>Under development</a>
</p>

<aside class="success">
This building block is <strong>valid</strong>
</aside>


# JSON Schema

```yaml--schema
allOf:
- $ref: https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/linkBase/schema.yaml
- type: object
  required:
  - uriTemplate
  properties:
    uriTemplate:
      type: string
      description: Supplies a resolvable URI to a remote resource (or resource fragment).
      example: http://data.example.com/buildings/(building-id}
    varBase:
      type: string
      description: The base URI to which the variable name can be appended to retrieve
        the definition of the variable as a JSON Schema fragment.
      format: url
    variables:
      type: object
      description: This object contains one key per substitution variable in the templated
        URL.  Each key defines the schema of one substitution variable using a JSON
        Schema fragment and can thus include things like the data type of the variable,
        enumerations, minimum values, maximum values, etc.

```

> <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=yaml&amp;dataUrl=https%3A%2F%2Frob-metalinkage.github.io%2Fbblocks-ogcapi-records%2Fbuild%2Fannotated%2Fapi%2Frecords%2Fv1%2Fschemas%2FlinkTemplate%2Fschema.yaml&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on YAML Viewer</a>

Links to the schema:

* YAML version: <a href="https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/linkTemplate/schema.yaml" target="_blank">https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/linkTemplate/schema.yaml</a>
* JSON version: <a href="https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/linkTemplate/schema.json" target="_blank">https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/linkTemplate/schema.json</a>

# References

* [OGC API Records - Draft](https://docs.ogc.org/DRAFTS/20-004.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: <a href="https://github.com/rob-metalinkage/bblocks-ogcapi-records" target="_blank">https://github.com/rob-metalinkage/bblocks-ogcapi-records</a>
* Path:
<code><a href="https://github.com/rob-metalinkage/bblocks-ogcapi-records/blob/HEAD/_sources/v1/schemas/linkTemplate" target="_blank">_sources/v1/schemas/linkTemplate</a></code>

