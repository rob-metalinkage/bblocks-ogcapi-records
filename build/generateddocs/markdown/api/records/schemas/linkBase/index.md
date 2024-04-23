
# Schema for linkBase (Schema)

`ogc.api.records.schemas.linkBase` *v0.1*

This building block corresponds to the schema for an OGC API Records linkBase

[*Status*](http://www.opengis.net/def/status): Under development

## Schema

```yaml
type: object
properties:
  rel:
    type: string
    description: The type or semantics of the relation.
    example: alternate
  type:
    type: string
    description: A hint indicating what the media type of the result of dereferencing
      the link should be.
    example: application/geo+json
  hreflang:
    type: string
    description: A hint indicating what the language of the result of dereferencing
      the link should be.
    example: en
  title:
    type: string
    description: Used to label the destination of a link such that it can be used
      as a human-readable identifier.
    example: Trierer Strasse 70, 53115 Bonn
  length:
    type: integer
  created:
    type: string
    description: Date of creation of the resource pointed to by the link.
    format: date-time
  updated:
    type: string
    description: Most recent date on which the resource pointed to by the link was
      changed.
    format: date-time

```

Links to the schema:

* YAML version: [schema.yaml](https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/linkBase/schema.json)
* JSON version: [schema.json](https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/linkBase/schema.yaml)

## Sources

* [OGC API Records - Draft](https://docs.ogc.org/DRAFTS/20-004.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/ogcincubator/bblocks-ogcapi-records](https://github.com/ogcincubator/bblocks-ogcapi-records)
* Path: `_sources/schemas/linkBase`

