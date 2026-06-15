
# Land Parcel Collection (Schema)

`ogc.ladm.land-parcels.parcelCollection` *v0.1*

corresponds to LA_SpatialUnitGroup from LADM (ISO 19162)

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## Land Parcel Collection

A schema for validating a bundle of Land Parcels contained in a Feature Collection.

The Feature Collection may contain the referenced topological boundaries and survey marks that define the extents.  

Individual features may optionally contain geometric coordinates for visualisation, or as a record in the event of no survey data available to define boundaries using topological references to surveyed features.
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
        "parcelType": "eg-parcel-type:fee-simple-title",
        "parcelPurpose": "eg-parcel-purpose:fst",
        "parcelState": "eg-parcel-state:created",
        "class": "eg-parcel-class:allotment",
        "interests": [
          {
            "interestLink": "1040074",
            "interestType": "eg-interest-type:fh"
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
        "parcelType": "eg-parcel-type:fee-simple-title",
        "parcelPurpose": "eg-parcel-purpose:fst",
        "parcelState": "eg-parcel-state:created",
        "class": "eg-parcel-class:allotment",
        "interests": [
          {
            "interestLink": "1040075",
            "interestType": "eg-interest-type:fh"
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
  "@context": [
    {
      "eg-parcel-purpose": "https://w3id.org/ogc/ladm/vocabs/eg/parcel-purpose",
      "eg-parcel-type": "https://w3id.org/ogc/ladm/vocabs/eg/parcel-type",
      "eg-parcel-state": "https://w3id.org/ogc/ladm/vocabs/eg/parcel-state"
    },
    "https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/parcelCollection/context.jsonld"
  ],
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
        "parcelType": "eg-parcel-type:fee-simple-title",
        "parcelPurpose": "eg-parcel-purpose:fst",
        "parcelState": "eg-parcel-state:created",
        "class": "eg-parcel-class:allotment",
        "interests": [
          {
            "interestLink": "1040074",
            "interestType": "eg-interest-type:fh"
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
        "parcelType": "eg-parcel-type:fee-simple-title",
        "parcelPurpose": "eg-parcel-purpose:fst",
        "parcelState": "eg-parcel-state:created",
        "class": "eg-parcel-class:allotment",
        "interests": [
          {
            "interestLink": "1040075",
            "interestType": "eg-interest-type:fh"
          }
        ]
      }
    }
  ]
}
```

#### ttl
```ttl
@prefix commonpatterns: <https://w3id.org/ogc/utils/label/> .
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix parcel: <https://w3id.org/ogc/ladm/parcels/> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix topo: <https://purl.org/geojson/topo#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<http://www.example.com/features/primaryparcels> a geojson:FeatureCollection,
        parcel:PrimaryParcel ;
    geojson:features <http://www.example.com/features/8446454>,
        <http://www.example.com/features/8446455> .

<http://www.example.com/features/8446454> a geojson:Feature ;
    geojson:topology [ a geojson:Polygon ;
            topo:relatedFeatures ( ( <http://www.example.com/features/l535242> <http://www.example.com/features/l535759> <http://www.example.com/features/l985190> <http://www.example.com/features/l952702> <http://www.example.com/features/l965727> <http://www.example.com/features/l589282> ) ) ] ;
    parcel:appellation [ rdfs:label "Lot 1 DP 572532" ;
            dcterms:hasPart [ rdfs:label "1" ;
                    commonpatterns:namePartType "ParcelIdentifier" ],
                [ rdfs:label "Lot" ;
                    commonpatterns:namePartType "ParcelType" ],
                [ rdfs:label "572532" ;
                    commonpatterns:namePartType "PlanIdentifier" ],
                [ rdfs:label "DP" ;
                    commonpatterns:namePartType "PlanType" ] ] ;
    parcel:interest [ parcel:interestLink <http://www.example.com/features/1040074> ;
            parcel:interestType <eg-interest-type:fh> ] ;
    parcel:purpose <eg-parcel-purpose:fst> ;
    parcel:state <eg-parcel-state:created> ;
    parcel:surfaceArea 484 ;
    parcel:type <eg-parcel-type:fee-simple-title> .

<http://www.example.com/features/8446455> a geojson:Feature ;
    geojson:topology [ a geojson:Polygon ;
            topo:relatedFeatures ( ( <http://www.example.com/features/l746686> <http://www.example.com/features/l999724> <http://www.example.com/features/l591175> <http://www.example.com/features/l435861> <http://www.example.com/features/l874826> <http://www.example.com/features/l952702> <http://www.example.com/features/l985190> <http://www.example.com/features/l535759> <http://www.example.com/features/l535242> <http://www.example.com/features/l329256> ) ) ] ;
    parcel:appellation [ rdfs:label "Lot 2 DP 572532" ;
            dcterms:hasPart [ rdfs:label "Lot" ;
                    commonpatterns:namePartType "ParcelType" ],
                [ rdfs:label "DP" ;
                    commonpatterns:namePartType "PlanType" ],
                [ rdfs:label "572532" ;
                    commonpatterns:namePartType "PlanIdentifier" ],
                [ rdfs:label "2" ;
                    commonpatterns:namePartType "ParcelIdentifier" ] ] ;
    parcel:interest [ parcel:interestLink <http://www.example.com/features/1040075> ;
            parcel:interestType <eg-interest-type:fh> ] ;
    parcel:purpose <eg-parcel-purpose:fst> ;
    parcel:state <eg-parcel-state:created> ;
    parcel:surfaceArea 1196 ;
    parcel:type <eg-parcel-type:fee-simple-title> .


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
        "parcelType": "eg-parcel-type:covenant-land",
        "parcelPurpose": "eg-parcel-purpose:c-l",
        "parcelState": "eg-parcel-state:created",
        "interests": [
          {
            "interestLink": "1040075",
            "interestType": "eg-interest-type:fh"
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
  "@context": [
    {
      "eg-parcel-purpose": "https://w3id.org/ogc/ladm/vocabs/eg/parcel-purpose",
      "eg-parcel-type": "https://w3id.org/ogc/ladm/vocabs/eg/parcel-type",
      "eg-parcel-state": "https://w3id.org/ogc/ladm/vocabs/eg/parcel-state"
    },
    "https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/parcelCollection/context.jsonld"
  ],
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
        "parcelType": "eg-parcel-type:covenant-land",
        "parcelPurpose": "eg-parcel-purpose:c-l",
        "parcelState": "eg-parcel-state:created",
        "interests": [
          {
            "interestLink": "1040075",
            "interestType": "eg-interest-type:fh"
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
@prefix commonpatterns: <https://w3id.org/ogc/utils/label/> .
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix parcel: <https://w3id.org/ogc/ladm/parcels/> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix topo: <https://purl.org/geojson/topo#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<http://www.example.com/features/covenants> a geojson:FeatureCollection,
        parcel:SecondaryParcel ;
    geojson:features <http://www.example.com/features/8446456> .

<http://www.example.com/features/8446456> a geojson:Feature,
        parcel:SecondaryParcel ;
    geojson:topology [ a geojson:Polygon ;
            topo:relatedFeatures ( ( <http://www.example.com/features/l999724> <http://www.example.com/features/l591175> <http://www.example.com/features/l369793> <http://www.example.com/features/l435861> <http://www.example.com/features/l345344> <http://www.example.com/features/l685716> <http://www.example.com/features/l832940> <http://www.example.com/features/l715872> <http://www.example.com/features/l641327> <http://www.example.com/features/l852048> <http://www.example.com/features/l949729> <http://www.example.com/features/l951515> <http://www.example.com/features/l761760> <http://www.example.com/features/l580762> ) ) ] ;
    parcel:appellation [ rdfs:label "Area Z DP 572532" ;
            dcterms:hasPart [ rdfs:label "Area" ;
                    commonpatterns:namePartType "ParcelType" ],
                [ rdfs:label "Z" ;
                    commonpatterns:namePartType "ParcelIdentifier" ],
                [ rdfs:label "572532" ;
                    commonpatterns:namePartType "PlanIdentifier" ],
                [ rdfs:label "DP" ;
                    commonpatterns:namePartType "PlanType" ] ] ;
    parcel:interest [ parcel:interestLink <http://www.example.com/features/1040075> ;
            parcel:interestType <eg-interest-type:fh> ] ;
    parcel:purpose <eg-parcel-purpose:c-l> ;
    parcel:state <eg-parcel-state:created> ;
    parcel:surfaceArea 1196 ;
    parcel:type <eg-parcel-type:covenant-land> .


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
        anyOf:
        - $ref: https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/parcel/schema.yaml
        - $ref: https://surroundaustralia.github.io/topo-feature/build/annotated/geo/topo/features/topo-feature/schema.yaml

```

Links to the schema:

* YAML version: [schema.yaml](https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/parcelCollection/schema.json)
* JSON version: [schema.json](https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/parcelCollection/schema.yaml)


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
    "Face": "topo:Face",
    "Ring": "topo:Ring",
    "Shell": "topo:Shell",
    "Solid": "topo:Solid",
    "faces": {
      "@id": "topo:faces",
      "@container": "@list"
    },
    "rings": {
      "@id": "topo:rings",
      "@container": "@list"
    },
    "shells": {
      "@id": "topo:shells",
      "@container": "@list"
    },
    "solids": {
      "@id": "topo:shells",
      "@container": "@list"
    },
    "points": {
      "@context": {
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
        "featureType": "geojson:collectionFeatureType"
      },
      "@id": "topo:points",
      "@container": "@list"
    },
    "edges": {
      "@context": {
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
        "featureType": "geojson:collectionFeatureType"
      },
      "@id": "topo:edges",
      "@container": "@list"
    },
    "name": "rdfs:label",
    "bearingRotation": "parcel:bearingRotation",
    "parcels": "parcel:parcels",
    "PrimaryParcel": {
      "@id": "parcel:PrimaryParcel",
      "@type": "@id"
    },
    "SecondaryParcel": {
      "@id": "parcel:SecondaryParcel",
      "@type": "@id"
    },
    "parcelQualityClass": {
      "@id": "parcel:qualityClass",
      "@type": "@id"
    },
    "terrainIntersectionCurve": "parcel:terrainIntersectionCurve",
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
    "CompoundName": "commonpatterns:CompoundName",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "geojson": "https://purl.org/geojson/vocab#",
    "oa": "http://www.w3.org/ns/oa#",
    "dct": "http://purl.org/dc/terms/",
    "owlTime": "http://www.w3.org/2006/time#",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "topo": "https://purl.org/geojson/topo#",
    "prof": "http://www.w3.org/ns/dx/prof/",
    "sdo": "https://schema.org/",
    "parcel": "https://w3id.org/ogc/ladm/parcels/",
    "commonpatterns": "https://w3id.org/ogc/utils/label/",
    "appellation": {
      "@context": {
        "name": "commonpatterns:name",
        "label": "rdfs:label",
        "hasPart": {
          "@context": {
            "ref": "commonpatterns:namePartRef",
            "type": "commonpatterns:namePartType"
          },
          "@id": "dct:hasPart"
        }
      },
      "@id": "parcel:appellation"
    },
    "parcelType": {
      "@id": "parcel:type",
      "@type": "@id"
    },
    "parcelState": {
      "@id": "parcel:state",
      "@type": "@id"
    },
    "address": "sdo:address",
    "parcelPurpose": {
      "@id": "parcel:purpose",
      "@type": "@id"
    },
    "area": "parcel:surfaceArea",
    "floor": "parcel:floor",
    "zmin": "parcel:zmin",
    "zmax": "parcel:zmax",
    "interests": {
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
        "benefitedPartyName": "parcel:benefitedPartyName",
        "benefitedPartyLink": {
          "@type": "@id",
          "@id": "parcel:benefitedPartyLink"
        },
        "originalSurveyLink": {
          "@type": "@id",
          "@id": "parcel:originalSurveyLink"
        },
        "referencedParcel": {
          "@type": "@id",
          "@id": "parcel:referencedParcel"
        },
        "burdenedParcels": {
          "@id": "parcel:burdened",
          "@container": "@set"
        },
        "benefitedParcels": {
          "@id": "parcel:benefited",
          "@container": "@set"
        },
        "description": "parcel:interestDescription",
        "entitlementPortion": "parcel:entitlementPortion",
        "liabilityPortion": "parcel:liabilityPortion"
      },
      "@id": "parcel:interest",
      "@container": "@set"
    },
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/parcelCollection/context.jsonld)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/ogcincubator/bblocks-land-parcels](https://github.com/ogcincubator/bblocks-land-parcels)
* Path: `_sources/parcelCollection`

