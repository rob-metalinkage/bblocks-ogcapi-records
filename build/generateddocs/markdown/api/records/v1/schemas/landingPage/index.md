
# Schema for landingPage (Schema)

`ogc.api.records.v1.schemas.landingPage` *v0.1*

This building block corresponds to the schema for an OGC API Records landingPage

[*Status*](http://www.opengis.net/def/status): Under development

## Schema

```yaml
allOf:
- $ref: https://schemas.opengis.net/ogcapi/features/part1/1.0/openapi/schemas/landingPage.yaml
- type: object
  properties:
    linkTemplates:
      type: array
      items:
        $ref: https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/linkTemplate/schema.yaml

```

Links to the schema:

* YAML version: [schema.yaml](https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/landingPage/schema.json)
* JSON version: [schema.json](https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/landingPage/schema.yaml)

## Sources

* [OGC API Records - Draft](https://docs.ogc.org/DRAFTS/20-004.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/ogcincubator/bblocks-ogcapi-records](https://github.com/ogcincubator/bblocks-ogcapi-records)
* Path: `_sources/v1/schemas/landingPage`

