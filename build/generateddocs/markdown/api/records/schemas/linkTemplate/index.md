
# Schema for linkTemplate (Schema)

`ogc.api.records.schemas.linkTemplate` *v0.1*

This building block corresponds to the schema for an OGC API Records linkTemplate

[*Status*](http://www.opengis.net/def/status): Under development

## Schema

```yaml
allOf:
- $ref: https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/linkBase/schema.yaml
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

Links to the schema:

* YAML version: [schema.yaml](https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/linkTemplate/schema.json)
* JSON version: [schema.json](https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/linkTemplate/schema.yaml)

## Sources

* [OGC API Records - Draft](https://docs.ogc.org/DRAFTS/20-004.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/ogcincubator/bblocks-ogcapi-records](https://github.com/ogcincubator/bblocks-ogcapi-records)
* Path: `_sources/schemas/linkTemplate`

