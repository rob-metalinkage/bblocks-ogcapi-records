---
title: Schema for contact (Schema)

toc_footers:
  - Version 0.1
  - <a href='#'>Schema for contact</a>
  - <a href='https://blocks.ogc.org/register.html'>Building Blocks register</a>

search: true

code_clipboard: true

meta:
  - name: Schema for contact (Schema)
---


# Schema for contact `ogc.api.records.schemas.contact`

This building block corresponds to the schema for an OGC API Records contact

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
description: 'Identification of, and means of communication with, person responsible

  for the resource.'
anyOf:
- required:
  - name
- required:
  - organization
properties:
  identifier:
    type: string
    description: A value uniquely identifying a contact.
  name:
    type: string
    description: The name of the responsible person.
  position:
    type: string
    description: The name of the role or position of the responsible person taken
      from the organization's formal organizational hierarchy or chart.
  organization:
    type: string
    description: Organization/affiliation of the contact.
  logo:
    description: Graphic identifying a contact. The link relation should be `icon`
      and the media type should be an image media type.
    allOf:
    - $ref: https://schemas.opengis.net/ogcapi/features/part1/1.0/openapi/schemas/link.yaml
    - type: object
      required:
      - rel
      - type
      properties:
        rel:
          enum:
          - icon
  phones:
    type: array
    description: Telephone numbers at which contact can be made.
    items:
      type: object
      required:
      - value
      properties:
        value:
          type: string
          description: The value is the phone number itself.
          pattern: ^\+[1-9]{1}[0-9]{3,14}$
          example: '+14165550142'
        roles:
          description: The type of phone number (e.g. home, work, fax, etc.).
          $ref: https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/roles/schema.yaml
  emails:
    type: array
    description: Email addresses at which contact can be made.
    items:
      type: object
      required:
      - value
      properties:
        value:
          type: string
          description: The value is the email number itself.
          format: email
        roles:
          description: The type of email (e.g. home, work, etc.).
          $ref: https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/roles/schema.yaml
  addresses:
    type: array
    description: Physical location at which contact can be made.
    items:
      type: object
      properties:
        deliveryPoint:
          type: array
          description: Address lines for the location.
          items:
            type: string
        city:
          type: string
          description: City for the location.
        administrativeArea:
          type: string
          description: State or province of the location.
        postalCode:
          type: string
          description: ZIP or other postal code.
        country:
          type: string
          description: Country of the physical address.  ISO 3166-1 is recommended.
        roles:
          description: The type of address (e.g. office, home, etc.).
          $ref: https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/roles/schema.yaml
  links:
    type: array
    description: On-line information about the contact.
    items:
      allOf:
      - $ref: https://schemas.opengis.net/ogcapi/features/part1/1.0/openapi/schemas/link.yaml
      - type: object
        required:
        - type
  hoursOfService:
    type: string
    description: Time period when the contact can be contacted.
    example: 'Hours: Mo-Fr 10am-7pm Sa 10am-22pm Su 10am-21pm'
  contactInstructions:
    type: string
    description: 'Supplemental instructions on how or when to contact the

      responsible party.'
  roles:
    description: The set of named duties, job functions and/or permissions associated
      with this contact. (e.g. developer, administrator, etc.).
    $ref: https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/roles/schema.yaml

```

> <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=yaml&amp;dataUrl=https%3A%2F%2Fogcincubator.github.io%2Fbblocks-ogcapi-records%2Fbuild%2Fannotated%2Fapi%2Frecords%2Fschemas%2Fcontact%2Fschema.yaml&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on YAML Viewer</a>

Links to the schema:

* YAML version: <a href="https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/contact/schema.yaml" target="_blank">https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/contact/schema.yaml</a>
* JSON version: <a href="https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/contact/schema.json" target="_blank">https://ogcincubator.github.io/bblocks-ogcapi-records/build/annotated/api/records/schemas/contact/schema.json</a>

# References

* [OGC API Records - Draft](https://docs.ogc.org/DRAFTS/20-004.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: <a href="https://github.com/ogcincubator/bblocks-ogcapi-records" target="_blank">https://github.com/ogcincubator/bblocks-ogcapi-records</a>
* Path:
<code><a href="https://github.com/ogcincubator/bblocks-ogcapi-records/blob/HEAD/_sources/schemas/contact" target="_blank">_sources/schemas/contact</a></code>

