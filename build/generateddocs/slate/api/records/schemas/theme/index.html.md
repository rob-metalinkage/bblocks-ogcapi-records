---
title: Schema for theme (Schema)

toc_footers:
  - Version 0.1
  - <a href='#'>Schema for theme</a>
  - <a href='https://blocks.ogc.org/register.html'>Building Blocks register</a>

search: true

code_clipboard: true

meta:
  - name: Schema for theme (Schema)
---


# Schema for theme `ogc.api.records.schemas.theme`

This building block corresponds to the schema for an OGC API Records theme

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
required:
- concepts
- scheme
properties:
  concepts:
    type: array
    description: One or more entity/concept identifiers from this knowledge system.
      it is recommended that a resolvable URI be used for each entity/concept identifier.
    minItems: 1
    items:
      type: object
      required:
      - id
      properties:
        id:
          type: string
          description: An identifier for the concept.
        title:
          type: string
          description: A human readable title for the concept.
        description:
          type: string
          description: A human readable description for the concept.
        url:
          type: string
          format: uri
          description: A URI providing further description of the concept.
  scheme:
    type: string
    description: An identifier for the knowledge organization system used to classify
      the resource.  It is recommended that the identifier be a resolvable URI.  The
      list of schemes used in a searchable catalog can be determined by inspecting
      the server's OpenAPI document or, if the server implements CQL2, by exposing
      a queryable (e.g. named `scheme`) and enumerating the list of schemes in the
      queryable's schema definition.

```

> <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=yaml&amp;dataUrl=https%3A%2F%2Fogcincubator.github.io%2Fbblocks-ogcapi-records%2Fbuild%2Fannotated%2Fapi%2Frecords%2Fschemas%2Ftheme%2Fschema.yaml&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on YAML Viewer</a>

Links to the schema:

* YAML version: <a href="https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/theme/schema.yaml" target="_blank">https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/theme/schema.yaml</a>
* JSON version: <a href="https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/theme/schema.json" target="_blank">https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/theme/schema.json</a>

# References

* [OGC API Records - Draft](https://docs.ogc.org/DRAFTS/20-004.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: <a href="https://github.com/ogcincubator/bblocks-ogcapi-records" target="_blank">https://github.com/ogcincubator/bblocks-ogcapi-records</a>
* Path:
<code><a href="https://github.com/ogcincubator/bblocks-ogcapi-records/blob/HEAD/_sources/schemas/theme" target="_blank">_sources/schemas/theme</a></code>

