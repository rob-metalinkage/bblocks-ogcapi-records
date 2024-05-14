---
title: Schema for landingPage (Schema)

toc_footers:
  - Version 0.1
  - <a href='#'>Schema for landingPage</a>
  - <a href='https://blocks.ogc.org/register.html'>Building Blocks register</a>

search: true

code_clipboard: true

meta:
  - name: Schema for landingPage (Schema)
---


# Schema for landingPage `ogc.api.records.v1.schemas.landingPage`

This building block corresponds to the schema for an OGC API Records landingPage

<p class="status">
    <span data-rainbow-uri="http://www.opengis.net/def/status">Status</span>:
    <a href="http://www.opengis.net/def/status/under-development" target="_blank" data-rainbow-uri>Under development</a>
</p>

<aside class="success">
This building block is <strong>valid</strong>
</aside>


# JSON Schema

```yaml--schema
$comment: Adapted from https://github.com/opengeospatial/ogcapi-records/raw/master/core/openapi/schemas/landingPage.yaml
allOf:
- $ref: https://rob-metalinkage.github.io/bblocks-ogcapi-features/build/annotated/api/features/v1/schemas/landingPage/schema.yaml
- type: object
  properties:
    linkTemplates:
      type: array
      items:
        $ref: https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/landingPage/schema.yaml

```

> <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=yaml&amp;dataUrl=https%3A%2F%2Frob-metalinkage.github.io%2Fbblocks-ogcapi-records%2Fbuild%2Fannotated%2Fapi%2Frecords%2Fv1%2Fschemas%2FlandingPage%2Fschema.yaml&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on YAML Viewer</a>

Links to the schema:

* YAML version: <a href="https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/landingPage/schema.yaml" target="_blank">https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/landingPage/schema.yaml</a>
* JSON version: <a href="https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/landingPage/schema.json" target="_blank">https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/landingPage/schema.json</a>


# JSON-LD Context

```json--ldContext
{
  "@context": {
    "href": {
      "@type": "@id",
      "@id": "oa:hasTarget"
    },
    "rel": {
      "@context": {
        "@base": "http://www.iana.org/assignments/relation/"
      },
      "@id": "http://www.iana.org/assignments/relation",
      "@type": "@id"
    },
    "type": "dct:type",
    "hreflang": "dct:language",
    "title": "rdfs:label",
    "length": "dct:extent",
    "oa": "http://www.w3.org/ns/oa#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "dct": "http://purl.org/dc/terms/",
    "@version": 1.1
  }
}
```

> <a target="_blank" href="https://json-ld.org/playground/#json-ld=https%3A%2F%2Frob-metalinkage.github.io%2Fbblocks-ogcapi-records%2Fbuild%2Fannotated%2Fapi%2Frecords%2Fv1%2Fschemas%2FlandingPage%2Fcontext.jsonld">View on JSON-LD Playground</a>

You can find the full JSON-LD context here:
<a href="https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/landingPage/context.jsonld" target="_blank">https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/landingPage/context.jsonld</a>

# References

* [OGC API Records - Draft](https://docs.ogc.org/DRAFTS/20-004.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: <a href="https://github.com/rob-metalinkage/bblocks-ogcapi-records" target="_blank">https://github.com/rob-metalinkage/bblocks-ogcapi-records</a>
* Path:
<code><a href="https://github.com/rob-metalinkage/bblocks-ogcapi-records/blob/HEAD/_sources/v1/schemas/landingPage" target="_blank">_sources/v1/schemas/landingPage</a></code>

