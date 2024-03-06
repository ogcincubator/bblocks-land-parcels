
# Land Parcel (Schema)

`ogc.land-parcels.parcel` *v0.1*



[*Status*](http://www.opengis.net/def/status): Under development

## Description

## My Schema

Defines a set of properties that may be used in **any** JSON schema.

> Note these properties may be used in the "properties" sub-component of a GeoJSON object, as a simple object

The numeric properties "b" and "c" have an example SHACL rule that if c is present, then c > b
## Examples

### Primary parcel
#### json
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


### Secondary parcel
#### json
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

## Schema

```yaml
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
    $ref: https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/compound-name/schema.yaml
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

Links to the schema:

* YAML version: [schema.yaml](https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/parcel/schema.json)
* JSON version: [schema.json](https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/parcel/schema.yaml)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/ogcincubator/bblocks-land-parcels](https://github.com/ogcincubator/bblocks-land-parcels)
* Path: `_sources/parcel`

