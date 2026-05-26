
# Land Parcel (Schema)

`ogc.ladm.land-parcels.parcel` *v0.1*

A parcel of land, corresponds to LA_SpatialUnit from LADM (ISO 19162)

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## Land Parcel

LADM ....
## Examples

### Primary parcel
#### json
```json
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
}
```

#### jsonld
```jsonld
{
  "@context": "https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/parcel/context.jsonld",
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
}
```

#### ttl
```ttl
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix parcel: <https://w3id.org/ogc/ladm/parcels/> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix topo: <https://purl.org/geojson/topo#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<file:///github/workspace/8446454> a geojson:Feature ;
    geojson:topology [ a geojson:Polygon ;
            topo:relatedFeatures ( ( <file:///github/workspace/l535242> <file:///github/workspace/l535759> <file:///github/workspace/l985190> <file:///github/workspace/l952702> <file:///github/workspace/l965727> <file:///github/workspace/l589282> ) ) ] ;
    parcel:appellation [ ] ;
    parcel:interest [ parcel:interestLink <file:///github/workspace/1040074> ;
            parcel:interestType <nz-interest-type:fh> ] ;
    parcel:purpose <nz-parcel-purpose:fst> ;
    parcel:state <nz-parcel-state:created> ;
    parcel:surfaceArea 484 ;
    parcel:type <nz-parcel-type:fee-simple-title> .


```


### Secondary parcel
#### json
```json
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

```

#### jsonld
```jsonld
{
  "@context": "https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/parcel/context.jsonld",
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
```

#### ttl
```ttl
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix parcel: <https://w3id.org/ogc/ladm/parcels/> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix topo: <https://purl.org/geojson/topo#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<file:///github/workspace/8446456> a geojson:Feature,
        parcel:SecondaryParcel ;
    geojson:topology [ a geojson:Polygon ;
            topo:relatedFeatures ( ( <file:///github/workspace/l999724> <file:///github/workspace/l591175> <file:///github/workspace/l369793> <file:///github/workspace/l435861> <file:///github/workspace/l345344> <file:///github/workspace/l685716> <file:///github/workspace/l832940> <file:///github/workspace/l715872> <file:///github/workspace/l641327> <file:///github/workspace/l852048> <file:///github/workspace/l949729> <file:///github/workspace/l951515> <file:///github/workspace/l761760> <file:///github/workspace/l580762> ) ) ] ;
    parcel:appellation [ ] ;
    parcel:interest [ parcel:interestLink <file:///github/workspace/1040075> ;
            parcel:interestType <nz-interest-type:fh> ] ;
    parcel:purpose <nz-parcel-purpose:c-l> ;
    parcel:state <nz-parcel-state:created> ;
    parcel:surfaceArea 1196 ;
    parcel:type <nz-parcel-type:covenant-land> .


```


### ContainingParcelRef
Has a relationship from a parcel to a "ParentParcel" - with an explicit semantic relationship and a topolgy constraint relationship.

Note, the topology constraint "within" for a 3D Parcel, referencing a Parent Parcel defined in 2 or 2.5D implies within a virtual extruded volume defined by the footprint of the Parent Parcel.

#### json
```json
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
    ],
    "relationships": [
      {
        "rel": "topology",
        "href": "myParcels:1234",
        "targetFeatureType": "parcel:PrimaryParcel",
        "role": [
          "topo:within",
          "parcel:containingParentParcel"
        ]
      }
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
}
```

#### jsonld
```jsonld
{
  "@context": "https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/parcel/context.jsonld",
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
    ],
    "relationships": [
      {
        "rel": "topology",
        "href": "myParcels:1234",
        "targetFeatureType": "parcel:PrimaryParcel",
        "role": [
          "topo:within",
          "parcel:containingParentParcel"
        ]
      }
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
}
```

#### ttl
```ttl
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix ns1: <http://www.iana.org/assignments/> .
@prefix oa: <http://www.w3.org/ns/oa#> .
@prefix parcel: <https://w3id.org/ogc/ladm/parcels/> .
@prefix prof: <http://www.w3.org/ns/dx/prof/> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix topo: <https://purl.org/geojson/topo#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<file:///github/workspace/8446454> a geojson:Feature ;
    geojson:topology [ a geojson:Polygon ;
            topo:relatedFeatures ( [ ns1:relation <http://www.iana.org/assignments/relation/topology> ;
                        prof:hasRole topo:within,
                            parcel:containingParentParcel ;
                        oa:hasTarget <myParcels:1234> ] ),
                ( ( <file:///github/workspace/l535242> <file:///github/workspace/l535759> <file:///github/workspace/l985190> <file:///github/workspace/l952702> <file:///github/workspace/l965727> <file:///github/workspace/l589282> ) ) ] ;
    parcel:appellation [ ] ;
    parcel:interest [ parcel:interestLink <file:///github/workspace/1040074> ;
            parcel:interestType <nz-interest-type:fh> ] ;
    parcel:purpose <nz-parcel-purpose:fst> ;
    parcel:state <nz-parcel-state:created> ;
    parcel:surfaceArea 484 ;
    parcel:type <nz-parcel-type:fee-simple-title> .


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
  parcelProperties:
    $anchor: parcelProperties
    appellation:
      $ref: https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/compound-name/schema.yaml
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
allOf:
- anyOf:
  - $ref: https://surroundaustralia.github.io/topo-feature/build/annotated/geo/topo/features/topo-feature/schema.yaml
  - $ref: https://opengeospatial.github.io/bblocks/annotated-schemas/geo/json-fg/feature-lenient/schema.yaml
- properties:
    properties:
      $ref: '#parcelProperties'
      x-jsonld-id: '@nest'
x-jsonld-extra-terms:
  featureType: '@type'
  name: rdfs:label
  address: https://schema.org/address
  bearingRotation: container:bearingRotation
  points: container:points
  parcels: https://w3id.org/ogc/ladm/parcels/parcels
  PrimaryParcel:
    x-jsonld-id: https://w3id.org/ogc/ladm/parcels/PrimaryParcel
    x-jsonld-type: '@id'
  SecondaryParcel:
    x-jsonld-id: https://w3id.org/ogc/ladm/parcels/SecondaryParcel
    x-jsonld-type: '@id'
  appellation: https://w3id.org/ogc/ladm/parcels/appellation
  parcelType:
    x-jsonld-id: https://w3id.org/ogc/ladm/parcels/type
    x-jsonld-type: '@id'
  parcelPurpose:
    x-jsonld-id: https://w3id.org/ogc/ladm/parcels/purpose
    x-jsonld-type: '@id'
  parcelQualityClass:
    x-jsonld-id: https://w3id.org/ogc/ladm/parcels/qualityClass
    x-jsonld-type: '@id'
  area: https://w3id.org/ogc/ladm/parcels/surfaceArea
  floor: https://w3id.org/ogc/ladm/parcels/floor
  zmin: https://w3id.org/ogc/ladm/parcels/zmin
  zmax: https://w3id.org/ogc/ladm/parcels/zmax
  terrainIntersectionCurve: https://w3id.org/ogc/ladm/parcels/terrainIntersectionCurve
  interests:
    x-jsonld-id: https://w3id.org/ogc/ladm/parcels/interest
    x-jsonld-container: '@set'
    x-jsonld-context:
      interestLink:
        '@type': '@id'
        '@id': https://w3id.org/ogc/ladm/parcels/interestLink
      interestName: https://w3id.org/ogc/ladm/parcels/interestName
      interestType:
        '@type': '@id'
        '@id': https://w3id.org/ogc/ladm/parcels/interestType
      dateInForce: https://w3id.org/ogc/ladm/parcels/interestDateInForce
      dateExpires: https://w3id.org/ogc/ladm/parcels/interestDateExpires
      statuteLink:
        '@type': '@id'
        '@id': https://w3id.org/ogc/ladm/parcels/statuteLink
      statuteName: https://w3id.org/ogc/ladm/parcels/statuteName
      benefitedPartyLink:
        '@type': '@id'
        '@id': https://w3id.org/ogc/ladm/parcels/benefitedPartyLink
      benefitedPartyName: https://w3id.org/ogc/ladm/parcels/benefitedPartyName
      referencedParcel:
        '@type': '@id'
        '@id': https://w3id.org/ogc/ladm/parcels/referencedParcel
      originalSurveyLink:
        '@type': '@id'
        '@id': https://w3id.org/ogc/ladm/parcels/originalSurveyLink
      burdenedParcels:
        '@id': https://w3id.org/ogc/ladm/parcels/burdened
        '@container': '@set'
      benefitedParcels:
        '@id': https://w3id.org/ogc/ladm/parcels/benefited
        '@container': '@set'
      entitlementPortion: https://w3id.org/ogc/ladm/parcels/entitlementPortion
      liabilityPortion: https://w3id.org/ogc/ladm/parcels/liabilityPortion
      description: https://w3id.org/ogc/ladm/parcels/interestDescription
  parcelState:
    x-jsonld-id: https://w3id.org/ogc/ladm/parcels/state
    x-jsonld-type: '@id'
x-jsonld-prefixes:
  sdo: https://schema.org/
  parcel: https://w3id.org/ogc/ladm/parcels/

```

Links to the schema:

* YAML version: [schema.yaml](https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/parcel/schema.json)
* JSON version: [schema.json](https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/parcel/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "Feature": "geojson:Feature",
    "FeatureCollection": "geojson:FeatureCollection",
    "GeometryCollection": "geojson:GeometryCollection",
    "LineString": "geojson:LineString",
    "MultiLineString": "geojson:MultiLineString",
    "MultiPoint": "geojson:MultiPoint",
    "MultiPolygon": "geojson:MultiPolygon",
    "Point": "geojson:Point",
    "Polygon": "geojson:Polygon",
    "features": {
      "@container": "@set",
      "@id": "geojson:features"
    },
    "type": "@type",
    "id": "@id",
    "properties": "@nest",
    "geometry": "geojson:geometry",
    "bbox": {
      "@container": "@list",
      "@id": "geojson:bbox"
    },
    "links": {
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
        "length": "dct:extent"
      },
      "@id": "rdfs:seeAlso"
    },
    "featureType": "@type",
    "time": {
      "@context": {
        "date": {
          "@id": "owlTime:hasTime",
          "@type": "xsd:date"
        },
        "timestamp": {
          "@id": "owlTime:hasTime",
          "@type": "xsd:dateTime"
        },
        "interval": {
          "@id": "owlTime:hasTime",
          "@container": "@list"
        }
      },
      "@id": "dct:time"
    },
    "coordRefSys": "http://www.opengis.net/def/glossary/term/CoordinateReferenceSystemCRS",
    "place": "dct:spatial",
    "Polyhedron": "geojson:Polyhedron",
    "MultiPolyhedron": "geojson:MultiPolyhedron",
    "Prism": {
      "@id": "geojson:Prism",
      "@context": {
        "base": "geojson:prismBase",
        "lower": "geojson:prismLower",
        "upper": "geojson:prismUpper"
      }
    },
    "MultiPrism": {
      "@id": "geojson:MultiPrism",
      "@context": {
        "prisms": "geojson:prisms"
      }
    },
    "coordinates": {
      "@container": "@list",
      "@id": "geojson:coordinates"
    },
    "geometries": {
      "@id": "geojson:geometry",
      "@container": "@list"
    },
    "topology": {
      "@context": {
        "references": {
          "@id": "topo:relatedFeatures",
          "@type": "@id",
          "@container": "@list"
        },
        "directed_references": {
          "@context": {
            "ref": {
              "@type": "@id",
              "@id": "topo:ref"
            }
          },
          "@id": "topo:directedReferences",
          "@container": "@list"
        },
        "relationships": {
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
            "role": {
              "@id": "prof:hasRole",
              "@type": "@id"
            },
            "conformsTo": {
              "@id": "dct:conformsTo",
              "@type": "@id"
            }
          },
          "@id": "topo:relatedFeatures",
          "@type": "@id",
          "@container": "@list"
        }
      },
      "@type": "@id",
      "@id": "geojson:topology"
    },
    "name": "rdfs:label",
    "address": "sdo:address",
    "bearingRotation": "container:bearingRotation",
    "points": "container:points",
    "parcels": "parcel:parcels",
    "PrimaryParcel": {
      "@id": "parcel:PrimaryParcel",
      "@type": "@id"
    },
    "SecondaryParcel": {
      "@id": "parcel:SecondaryParcel",
      "@type": "@id"
    },
    "appellation": "parcel:appellation",
    "parcelType": {
      "@id": "parcel:type",
      "@type": "@id"
    },
    "parcelPurpose": {
      "@id": "parcel:purpose",
      "@type": "@id"
    },
    "parcelQualityClass": {
      "@id": "parcel:qualityClass",
      "@type": "@id"
    },
    "area": "parcel:surfaceArea",
    "floor": "parcel:floor",
    "zmin": "parcel:zmin",
    "zmax": "parcel:zmax",
    "terrainIntersectionCurve": "parcel:terrainIntersectionCurve",
    "interests": {
      "@id": "parcel:interest",
      "@container": "@set",
      "@context": {
        "interestLink": {
          "@type": "@id",
          "@id": "parcel:interestLink"
        },
        "interestName": "parcel:interestName",
        "interestType": {
          "@type": "@id",
          "@id": "parcel:interestType"
        },
        "dateInForce": "parcel:interestDateInForce",
        "dateExpires": "parcel:interestDateExpires",
        "statuteLink": {
          "@type": "@id",
          "@id": "parcel:statuteLink"
        },
        "statuteName": "parcel:statuteName",
        "benefitedPartyLink": {
          "@type": "@id",
          "@id": "parcel:benefitedPartyLink"
        },
        "benefitedPartyName": "parcel:benefitedPartyName",
        "referencedParcel": {
          "@type": "@id",
          "@id": "parcel:referencedParcel"
        },
        "originalSurveyLink": {
          "@type": "@id",
          "@id": "parcel:originalSurveyLink"
        },
        "burdenedParcels": {
          "@id": "parcel:burdened",
          "@container": "@set"
        },
        "benefitedParcels": {
          "@id": "parcel:benefited",
          "@container": "@set"
        },
        "entitlementPortion": "parcel:entitlementPortion",
        "liabilityPortion": "parcel:liabilityPortion",
        "description": "parcel:interestDescription"
      }
    },
    "parcelState": {
      "@id": "parcel:state",
      "@type": "@id"
    },
    "Arc": "geojson:Arc",
    "ArcWithCenter": "geojson:ArcWithCenter",
    "ArcByChord": "geojson:ArcByChord",
    "CircleByCenter": "geojson:CircleByCenter",
    "CubicSpline": "geojson:CubicSpline",
    "radius": "geojson:radius",
    "arcLength": "geojson:arcLength",
    "startTangentVector": "geojson:startTangentVector",
    "endTangentVector": "geojson:endTangentVector",
    "ref": "topo:ref",
    "orientation": "topo:orientation",
    "Edge": "topo:Edge",
    "Face": "topo:Face",
    "Ring": "topo:Ring",
    "Shell": "topo:Shell",
    "Solid": "topo:Solid",
    "rings": {
      "@id": "topo:rings",
      "@container": "@list"
    },
    "shells": {
      "@id": "topo:shells",
      "@container": "@list"
    },
    "faces": {
      "@id": "topo:faces",
      "@container": "@list"
    },
    "geojson": "https://purl.org/geojson/vocab#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "oa": "http://www.w3.org/ns/oa#",
    "dct": "http://purl.org/dc/terms/",
    "owlTime": "http://www.w3.org/2006/time#",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "topo": "https://purl.org/geojson/topo#",
    "prof": "http://www.w3.org/ns/dx/prof/",
    "sdo": "https://schema.org/",
    "parcel": "https://w3id.org/ogc/ladm/parcels/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/parcel/context.jsonld)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/ogcincubator/bblocks-land-parcels](https://github.com/ogcincubator/bblocks-land-parcels)
* Path: `_sources/parcel`

