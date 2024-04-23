---
title: Schema for recordGeoJSON (Schema)

toc_footers:
  - Version 0.1
  - <a href='#'>Schema for recordGeoJSON</a>
  - <a href='https://blocks.ogc.org/register.html'>Building Blocks register</a>

search: true

code_clipboard: true

meta:
  - name: Schema for recordGeoJSON (Schema)
---


# Schema for recordGeoJSON `ogc.api.records.schemas.recordGeoJSON`

This building block corresponds to the schema for an OGC API Records recordGeoJSON

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
- id
- type
- geometry
- properties
- links
properties:
  id:
    type: string
    description: A unique identifier of the catalog record.
    format: uri
  conformsTo:
    type: array
    items:
      type: string
  type:
    type: string
    enum:
    - Feature
  time:
    oneOf:
    - enum:
      - null
    - $ref: https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/time/schema.yaml
  geometry:
    oneOf:
    - enum:
      - null
    - $ref: https://schemas.opengis.net/ogcapi/features/part1/1.0/openapi/schemas/geometryGeoJSON.yaml
  properties:
    type: object
    required:
    - type
    - title
    properties:
      created:
        type: string
        description: Date of creation of this record.
        format: date-time
      updated:
        type: string
        description: The most recent date on which the record was changed.
        format: date-time
      type:
        type: string
        description: The nature or genre of the resource. The value should be a code,
          convenient for filtering records. Where available, a link to the canonical
          URI of the record type resource will be added to the 'links' property.
        maxLength: 64
      title:
        type: string
        description: A human-readable name given to the resource.
      description:
        type: string
        description: A free-text account of the resource.
      keywords:
        type: array
        description: The topic or topics of the resource. Typically represented using
          free-form keywords, tags, key phrases, or classification codes.
        items:
          type: string
      language:
        description: The language used for textual values in this record representation.
        $ref: https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/language/schema.yaml
      languages:
        type: array
        description: This list of languages in which this record is available.
        items:
          $ref: https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/language/schema.yaml
      resourceLanguages:
        type: array
        description: The list of languages in which the resource described by this
          record is available.
        items:
          $ref: https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/language/schema.yaml
      externalIds:
        type: array
        description: An identifier for the resource assigned by an external (to the
          catalog) entity.
        items:
          type: object
          properties:
            scheme:
              type: string
              description: A reference to an authority or identifier for a knowledge
                organization system from which the external identifier was obtained.
                It is recommended that the identifier be a resolvable URI.
            value:
              type: string
              description: The value of the identifier.
          required:
          - value
      themes:
        type: array
        description: A knowledge organization system used to classify the resource.
        minItems: 1
        items:
          $ref: https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/theme/schema.yaml
      formats:
        type: array
        description: A list of available distributions of the resource.
        items:
          type: string
      contacts:
        type: array
        description: A list of contacts qualified by their role(s) in association
          to the record or the resource described by the record.
        items:
          $ref: https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/contact/schema.yaml
      license:
        $ref: https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/license/schema.yaml
      rights:
        type: string
        description: A statement that concerns all rights not addressed by the license
          such as a copyright statement.
  links:
    type: array
    items:
      $ref: https://schemas.opengis.net/ogcapi/features/part1/1.0/openapi/schemas/link.yaml
  linkTemplates:
    type: array
    items:
      $ref: https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/linkTemplate/schema.yaml

```

> <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=yaml&amp;dataUrl=https%3A%2F%2Fogcincubator.github.io%2Fbblocks-ogcapi-records%2Fbuild%2Fannotated%2Fapi%2Frecords%2Fschemas%2FrecordGeoJSON%2Fschema.yaml&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on YAML Viewer</a>

Links to the schema:

* YAML version: <a href="https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/recordGeoJSON/schema.yaml" target="_blank">https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/recordGeoJSON/schema.yaml</a>
* JSON version: <a href="https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/recordGeoJSON/schema.json" target="_blank">https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/recordGeoJSON/schema.json</a>

# References

* [OGC API Records - Draft](https://docs.ogc.org/DRAFTS/20-004.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: <a href="https://github.com/ogcincubator/bblocks-ogcapi-records" target="_blank">https://github.com/ogcincubator/bblocks-ogcapi-records</a>
* Path:
<code><a href="https://github.com/ogcincubator/bblocks-ogcapi-records/blob/HEAD/_sources/schemas/recordGeoJSON" target="_blank">_sources/schemas/recordGeoJSON</a></code>

