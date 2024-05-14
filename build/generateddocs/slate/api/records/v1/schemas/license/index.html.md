---
title: Schema for license (Schema)

toc_footers:
  - Version 0.1
  - <a href='#'>Schema for license</a>
  - <a href='https://blocks.ogc.org/register.html'>Building Blocks register</a>

search: true

code_clipboard: true

meta:
  - name: Schema for license (Schema)
---


# Schema for license `ogc.api.records.v1.schemas.license`

This building block corresponds to the schema for an OGC API Records license

<p class="status">
    <span data-rainbow-uri="http://www.opengis.net/def/status">Status</span>:
    <a href="http://www.opengis.net/def/status/under-development" target="_blank" data-rainbow-uri>Under development</a>
</p>

<aside class="success">
This building block is <strong>valid</strong>
</aside>


# JSON Schema

```yaml--schema
type: string
description: A legal document under which the resource is made available. If the resource
  is being made available under a common license then use an SPDX license id (https://spdx.org/licenses/).
  If the resource is being made available under multiple common licenses then use
  an SPDX license expression v2.3 string (https://spdx.github.io/spdx-spec/v2.3/SPDX-license-expressions/)
  If the resource is being made available under one or more licenses that haven't
  been assigned an SPDX identifier or one or more custom licenses then use a string
  value of 'other' and include one or more links (rel="license") in the `link` section
  of the record to the file(s) that contains the text of the license(s). There is
  also the case of a resource that is private or unpublished and is thus unlicensed;
  in this case do not register such a resource in the catalog in the first place since
  there is no point in making such a resource discoverable.

```

> <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=yaml&amp;dataUrl=https%3A%2F%2Frob-metalinkage.github.io%2Fbblocks-ogcapi-records%2Fbuild%2Fannotated%2Fapi%2Frecords%2Fv1%2Fschemas%2Flicense%2Fschema.yaml&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on YAML Viewer</a>

Links to the schema:

* YAML version: <a href="https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/license/schema.yaml" target="_blank">https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/license/schema.yaml</a>
* JSON version: <a href="https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/license/schema.json" target="_blank">https://rob-metalinkage.github.io/bblocks-ogcapi-records/build/annotated/api/records/v1/schemas/license/schema.json</a>

# References

* [OGC API Records - Draft](https://docs.ogc.org/DRAFTS/20-004.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: <a href="https://github.com/rob-metalinkage/bblocks-ogcapi-records" target="_blank">https://github.com/rob-metalinkage/bblocks-ogcapi-records</a>
* Path:
<code><a href="https://github.com/rob-metalinkage/bblocks-ogcapi-records/blob/HEAD/_sources/v1/schemas/license" target="_blank">_sources/v1/schemas/license</a></code>

