
# Land Parcel Collection (Schema)

`ogc.land-parcels.parcelCollection` *v0.1*

A set of parcels and supporting features defining extent via topology

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## Land Parcel Collection

A schema for validating a bundle of Land Parcels contained in a Feature Collection.

The Feature Collection may contain the referenced topological boundaries and survey marks that define the extents.  

Features may optionally contain geometric coordinates for visualisation, or as a record in the event of no survey data available to define boundaries.
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

#### jsonld
```jsonld
{
  "@context": "https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/parcelCollection/context.jsonld",
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

#### ttl
```ttl
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix parcel: <https://w3id.org/ogc/ladm/parcels/> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<file:///github/workspace/primaryparcels> a geojson:FeatureCollection,
        parcel:PrimaryParcel ;
    geojson:features <file:///github/workspace/8446454>,
        <file:///github/workspace/8446455> .

<file:///github/workspace/8446454> a geojson:Feature ;
    geojson:topology [ a geojson:Polygon ;
            geojson:relatedFeatures ( ( <file:///github/workspace/l535242> <file:///github/workspace/l535759> <file:///github/workspace/l985190> <file:///github/workspace/l952702> <file:///github/workspace/l965727> <file:///github/workspace/l589282> ) ) ] ;
    parcel:appellation [ ] ;
    parcel:interest [ parcel:interestLink <file:///github/workspace/1040074> ;
            parcel:interestType <nz-interest-type:fh> ] ;
    parcel:purpose <nz-parcel-purpose:fst> ;
    parcel:state <nz-parcel-state:created> ;
    parcel:surfaceArea 484 ;
    parcel:type <nz-parcel-type:fee-simple-title> .

<file:///github/workspace/8446455> a geojson:Feature ;
    geojson:topology [ a geojson:Polygon ;
            geojson:relatedFeatures ( ( <file:///github/workspace/l746686> <file:///github/workspace/l999724> <file:///github/workspace/l591175> <file:///github/workspace/l435861> <file:///github/workspace/l874826> <file:///github/workspace/l952702> <file:///github/workspace/l985190> <file:///github/workspace/l535759> <file:///github/workspace/l535242> <file:///github/workspace/l329256> ) ) ] ;
    parcel:appellation [ ] ;
    parcel:interest [ parcel:interestLink <file:///github/workspace/1040075> ;
            parcel:interestType <nz-interest-type:fh> ] ;
    parcel:purpose <nz-parcel-purpose:fst> ;
    parcel:state <nz-parcel-state:created> ;
    parcel:surfaceArea 1196 ;
    parcel:type <nz-parcel-type:fee-simple-title> .


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

#### jsonld
```jsonld
{
  "@context": "https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/parcelCollection/context.jsonld",
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

#### ttl
```ttl
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix parcel: <https://w3id.org/ogc/ladm/parcels/> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<file:///github/workspace/covenants> a geojson:FeatureCollection,
        parcel:SecondaryParcel ;
    geojson:features <file:///github/workspace/8446456> .

<file:///github/workspace/8446456> a geojson:Feature,
        parcel:SecondaryParcel ;
    geojson:topology [ a geojson:Polygon ;
            geojson:relatedFeatures ( ( <file:///github/workspace/l999724> <file:///github/workspace/l591175> <file:///github/workspace/l369793> <file:///github/workspace/l435861> <file:///github/workspace/l345344> <file:///github/workspace/l685716> <file:///github/workspace/l832940> <file:///github/workspace/l715872> <file:///github/workspace/l641327> <file:///github/workspace/l852048> <file:///github/workspace/l949729> <file:///github/workspace/l951515> <file:///github/workspace/l761760> <file:///github/workspace/l580762> ) ) ] ;
    parcel:appellation [ ] ;
    parcel:interest [ parcel:interestLink <file:///github/workspace/1040075> ;
            parcel:interestType <nz-interest-type:fh> ] ;
    parcel:purpose <nz-parcel-purpose:c-l> ;
    parcel:state <nz-parcel-state:created> ;
    parcel:surfaceArea 1196 ;
    parcel:type <nz-parcel-type:covenant-land> .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
type: object
allOf:
- ref: bblocks://ogc.geo.json-fg.featureCollection-lenient
- anyOf:
  - $ref: https://surroundaustralia.github.io/topo-feature/build/annotated/geo/topo/features/topo-feature-collection/schema.yaml
  - $ref: https://opengeospatial.github.io/bblocks/annotated-schemas/geo/json-fg/featureCollection-lenient/schema.yaml
- properties:
    features:
      items:
        $ref: https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/parcel/schema.yaml

```

Links to the schema:

* YAML version: [schema.yaml](https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/parcelCollection/schema.json)
* JSON version: [schema.json](https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/parcelCollection/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "type": "@type",
    "features": {
      "@id": "geojson:features",
      "@container": "@set"
    },
    "bbox": {
      "@id": "geojson:bbox",
      "@container": "@list"
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
    "properties": "@nest",
    "featureType": "@type",
    "coordRefSys": "http://www.opengis.net/def/glossary/term/CoordinateReferenceSystemCRS",
    "Feature": "geojson:Feature",
    "FeatureCollection": "geojson:FeatureCollection",
    "GeometryCollection": "geojson:GeometryCollection",
    "LineString": "geojson:LineString",
    "MultiLineString": "geojson:MultiLineString",
    "MultiPoint": "geojson:MultiPoint",
    "MultiPolygon": "geojson:MultiPolygon",
    "Point": "geojson:Point",
    "Polygon": "geojson:Polygon",
    "id": "@id",
    "geometry": "geojson:geometry",
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
          "@context": {
            "ref": {
              "@type": "@id",
              "@id": "topo:ref"
            }
          },
          "@id": "geojson:relatedFeatures",
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
        "rings": {
          "@id": "topo:rings",
          "@container": "@list"
        },
        "shells": {
          "@id": "topo:shells",
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
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "geojson": "https://purl.org/geojson/vocab#",
    "oa": "http://www.w3.org/ns/oa#",
    "dct": "http://purl.org/dc/terms/",
    "owlTime": "http://www.w3.org/2006/time#",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "csdm": "https://linked.data.gov.au/def/csdm/",
    "topo": "https://purl.org/geojson/topo#",
    "sdo": "https://schema.org/",
    "parcel": "https://w3id.org/ogc/ladm/parcels/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/parcelCollection/context.jsonld)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/ogcincubator/bblocks-land-parcels](https://github.com/ogcincubator/bblocks-land-parcels)
* Path: `_sources/parcelCollection`

