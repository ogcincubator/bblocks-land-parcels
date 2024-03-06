---
title: Land Parcel (Schema)


toc_footers:
  - Version 0.1
  - <a href='#'>Land Parcel</a>
  - <a href='https://blocks.ogc.org/register.html'>Building Blocks register</a>

search: true

code_clipboard: true

meta:
  - name: Land Parcel (Schema)
---


# Land Parcel `ogc.land-parcels.parcel`



<p class="status">
    <span data-rainbow-uri="http://www.opengis.net/def/status">Status</span>:
    <a href="http://www.opengis.net/def/status/under-development" target="_blank" data-rainbow-uri>Under development</a>
</p>

<aside class="success">
This building block is <strong><a href="https://github.com/ogcincubator/bblocks-land-parcels/blob/master/build/tests/land-parcels/parcel/" target="_blank">valid</a></strong>
</aside>

# Description

## My Schema

Defines a set of properties that may be used in **any** JSON schema.

> Note these properties may be used in the "properties" sub-component of a GeoJSON object, as a simple object

The numeric properties "b" and "c" have an example SHACL rule that if c is present, then c > b
# Examples

## Primary parcel



```json
{
  "id": "primaryparcels",
  "type": "FeatureCollection",
  "featureType": "PrimaryParcel",
  "properties": null,
  "features": [
    {
      "type": "Feature",
      "id": "8446454",
      "geometry": null,
      "topology": {
        "type": "Polygon",
        "references": [
          [
            "l535242",
            "l535759",
            "l985190",
            "l952702",
            "l965727",
            "l589282"
          ]
        ]
      },
      "properties": {
        "appellation": {
          "label": "Lot 1 DP 572532",
          "hasPart": [
            {
              "type": "PlanType",
              "label": "DP"
            },
            {
              "type": "PlanIdentifier",
              "label": "572532"
            },
            {
              "type": "ParcelType",
              "label": "Lot"
            },
            {
              "type": "ParcelIdentifier",
              "label": "1"
            }
          ]
        },
        "area": 484,
        "parcelType": "nz-parcel-type:fee-simple-title",
        "parcelPurpose": "nz-parcel-purpose:fst",
        "parcelState": "nz-parcel-state:created",
        "class": "nz-parcel-class:allotment",
        "interests": [
          {
            "interestLink": "1040074",
            "interestType": "nz-interest-type:fh"
          }
        ]
      }
    },
    {
      "type": "Feature",
      "id": "8446455",
      "geometry": null,
      "topology": {
        "type": "Polygon",
        "references": [
          [
            "l746686",
            "l999724",
            "l591175",
            "l435861",
            "l874826",
            "l952702",
            "l985190",
            "l535759",
            "l535242",
            "l329256"
          ]
        ]
      },
      "properties": {
        "appellation": {
          "label": "Lot 2 DP 572532",
          "hasPart": [
            {
              "type": "PlanType",
              "label": "DP"
            },
            {
              "type": "PlanIdentifier",
              "label": "572532"
            },
            {
              "type": "ParcelType",
              "label": "Lot"
            },
            {
              "type": "ParcelIdentifier",
              "label": "2"
            }
          ]
        },
        "area": 1196,
        "parcelType": "nz-parcel-type:fee-simple-title",
        "parcelPurpose": "nz-parcel-purpose:fst",
        "parcelState": "nz-parcel-state:created",
        "class": "nz-parcel-class:allotment",
        "interests": [
          {
            "interestLink": "1040075",
            "interestType": "nz-interest-type:fh"
          }
        ]
      }
    }
  ]
}
```

<blockquote class="lang-specific json">
  <p class="example-links">
    <a target="_blank" href="https://raw.githubusercontent.com/ogcincubator/bblocks-land-parcels/master/build/tests/land-parcels/parcel/example_1_1.json">Open in new window</a>
    <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=json&amp;dataUrl=https%3A%2F%2Fraw.githubusercontent.com%2Fogcincubator%2Fbblocks-land-parcels%2Fmaster%2Fbuild%2Ftests%2Fland-parcels%2Fparcel%2Fexample_1_1.json&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on JSON Viewer</a></p>
</blockquote>



## Secondary parcel



```json
{
  "id": "covenants",
  "type": "FeatureCollection",
  "featureType": "SecondaryParcel",
  "properties": null,
  "features": [
    {
      "type": "Feature",
      "id": "8446456",
      "featureType": "SecondaryParcel",
      "geometry": null,
      "topology": {
        "type": "Polygon",
        "references": [
          [
            "l999724",
            "l591175",
            "l369793",
            "l435861",
            "l345344",
            "l685716",
            "l832940",
            "l715872",
            "l641327",
            "l852048",
            "l949729",
            "l951515",
            "l761760",
            "l580762"
          ]
        ]
      },
      "properties": {
        "appellation": {
          "label": "Area Z DP 572532",
          "hasPart": [
            {
              "type": "PlanType",
              "label": "DP"
            },
            {
              "type": "PlanIdentifier",
              "label": "572532"
            },
            {
              "type": "ParcelType",
              "label": "Area"
            },
            {
              "type": "ParcelIdentifier",
              "label": "Z"
            }
          ]
        },
        "area": 1196,
        "parcelType": "nz-parcel-type:covenant-land",
        "parcelPurpose": "nz-parcel-purpose:c-l",
        "parcelState": "nz-parcel-state:created",
        "interests": [
          {
            "interestLink": "1040075",
            "interestType": "nz-interest-type:fh"
          }
        ],
        "burdened": {
          "x-comment": "References the parcel ID of the burdened primary parcel.",
          "references": [
            "8446455"
          ]
        }
      }
    }
  ]
}
```

<blockquote class="lang-specific json">
  <p class="example-links">
    <a target="_blank" href="https://raw.githubusercontent.com/ogcincubator/bblocks-land-parcels/master/build/tests/land-parcels/parcel/example_2_1.json">Open in new window</a>
    <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=json&amp;dataUrl=https%3A%2F%2Fraw.githubusercontent.com%2Fogcincubator%2Fbblocks-land-parcels%2Fmaster%2Fbuild%2Ftests%2Fland-parcels%2Fparcel%2Fexample_2_1.json&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on JSON Viewer</a></p>
</blockquote>



# JSON Schema

```yaml--schema
$schema: https://json-schema.org/draft/2020-12/schema
type: object
$defs:
  coderef:
    $ref: https://opengeospatial.github.io/bblocks/annotated-schemas/ogc-utils/iri-or-curie/schema.yaml
  coderefList:
    type: array
    items:
      $ref: '#/$defs/coderef'
  dateTime:
    type: string
    format: date-time
    pattern: ^\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}(?:\.\d+)?(?:Z|[+-]\d{2}:\d{2})?$
properties:
  appellation:
    $ref: https://raw.githubusercontent.com/ogcincubator/bblocks-land-parcels/master/build/annotated/land-parcels/compound-name/schema.yaml
  parcelType:
    $ref: '#/$defs/coderef'
  parcelState:
    $ref: '#/$defs/coderef'
  address:
    type: object
  parcelPurpose:
    $ref: '#/$defs/coderef'
  area:
    type: number
  floor:
    type: string
  zmin:
    type: number
  zmax:
    type: number
  interests:
    type: array
    additionalProperties: false
    items:
      properties:
        interestLink:
          $ref: '#/$defs/coderef'
        interestName:
          type: string
        interestType:
          $ref: '#/$defs/coderef'
        dateInForce:
          $ref: '#/$defs/dateTime'
        dateExpires:
          $ref: '#/$defs/dateTime'
        statuteLink:
          $ref: '#/$defs/coderef'
        statuteName:
          type: string
        benefitedPartyName:
          type: string
        benefitedPartyLink:
          $ref: '#/$defs/coderef'
        originalSurveyLink:
          $ref: '#/$defs/coderef'
        referencedParcel:
          $ref: '#/$defs/coderef'
        burdenedParcels:
          $ref: '#/$defs/coderefList'
        benefitedParcels:
          $ref: '#/$defs/coderefList'
        description:
          type: string
        entitlementPortion:
          type: string
        liabilityPortion:
          type: string
      required:
      - interestLink
      - interestType
    required:
    - appellation
    - parcelType
    - parcelState
    - parcelPurpose

```

> <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=yaml&amp;dataUrl=https%3A%2F%2Fraw.githubusercontent.com%2Fogcincubator%2Fbblocks-land-parcels%2Fmaster%2Fbuild%2Fannotated%2Fland-parcels%2Fparcel%2Fschema.yaml&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on YAML Viewer</a>

Links to the schema:

* YAML version: <a href="https://raw.githubusercontent.com/ogcincubator/bblocks-land-parcels/master/build/annotated/land-parcels/parcel/schema.yaml" target="_blank">https://raw.githubusercontent.com/ogcincubator/bblocks-land-parcels/master/build/annotated/land-parcels/parcel/schema.yaml</a>
* JSON version: <a href="https://raw.githubusercontent.com/ogcincubator/bblocks-land-parcels/master/build/annotated/land-parcels/parcel/schema.json" target="_blank">https://raw.githubusercontent.com/ogcincubator/bblocks-land-parcels/master/build/annotated/land-parcels/parcel/schema.json</a>

# For developers

The source code for this Building Block can be found in the following repository:

* URL: <a href="https://github.com/ogcincubator/bblocks-land-parcels" target="_blank">https://github.com/ogcincubator/bblocks-land-parcels</a>
* Path:
<code><a href="https://github.com/ogcincubator/bblocks-land-parcels/blob/HEAD/_sources/parcel" target="_blank">_sources/parcel</a></code>

