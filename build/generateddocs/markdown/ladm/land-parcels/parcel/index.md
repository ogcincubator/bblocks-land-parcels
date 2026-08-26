
# Land Parcel (Schema)

`ogc.ladm.land-parcels.parcel` *v0.1*

A parcel of land, corresponds to LA_SpatialUnit from LADM (ISO 19162)

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## Land Parcel

A Land Parcel is a specialisation of a LADM spatial unit with attributes to support key metadata provided during survey lodgement. Note that some of these attributes are modelled through references from other objects in the LADM model.

As such it should be considered an implementation of LADM SpatialUnit for the survey activity scope.

Future development of this building block may include rules for extracting LADM object types from this model, or annotating a Parcel with information from other data types.
## Examples

### Primary parcel
#### json
```json
{
  "type": "Feature",
  "id": "8446454",
"geometry":  null,
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
    "parcelType": "eg-parcel-type:l",
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
}
```

#### jsonld
```jsonld
{
  "@context": [
    {
      "eg-parcel-purpose": "https://w3id.org/ogc/ladm/vocabs/eg/parcel-purpose/",
      "eg-parcel-type": "https://w3id.org/ogc/ladm/vocabs/eg/parcel-type/",
      "eg-parcel-state": "https://w3id.org/ogc/ladm/vocabs/eg/parcel-state/"
    },
    "https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/parcel/context.jsonld"
  ],
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
    "parcelType": "eg-parcel-type:l",
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
}
```

#### ttl
```ttl
@prefix commonpatterns: <https://w3id.org/ogc/utils/label/> .
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix eg-parcel-purpose: <https://w3id.org/ogc/ladm/vocabs/eg/parcel-purpose/> .
@prefix eg-parcel-state: <https://w3id.org/ogc/ladm/vocabs/eg/parcel-state/> .
@prefix eg-parcel-type: <https://w3id.org/ogc/ladm/vocabs/eg/parcel-type/> .
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix parcel: <https://w3id.org/ogc/ladm/parcels/> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix topo: <https://purl.org/geojson/topo#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<http://www.example.com/features/8446454> a geojson:Feature ;
    geojson:topology [ a geojson:Polygon ;
            topo:relatedFeatures ( ( <http://www.example.com/features/l535242> <http://www.example.com/features/l535759> <http://www.example.com/features/l985190> <http://www.example.com/features/l952702> <http://www.example.com/features/l965727> <http://www.example.com/features/l589282> ) ) ] ;
    parcel:appellation [ rdfs:label "Lot 1 DP 572532" ;
            dcterms:hasPart [ rdfs:label "1" ;
                    commonpatterns:namePartType <http://www.example.com/features/ParcelIdentifier> ],
                [ rdfs:label "DP" ;
                    commonpatterns:namePartType <http://www.example.com/features/PlanType> ],
                [ rdfs:label "Lot" ;
                    commonpatterns:namePartType <http://www.example.com/features/ParcelType> ],
                [ rdfs:label "572532" ;
                    commonpatterns:namePartType <http://www.example.com/features/PlanIdentifier> ] ] ;
    parcel:interest [ parcel:interestLink <http://www.example.com/features/1040074> ;
            parcel:interestType <eg-interest-type:fh> ] ;
    parcel:purpose eg-parcel-purpose:fst ;
    parcel:state eg-parcel-state:created ;
    parcel:surfaceArea 484 ;
    parcel:type eg-parcel-type:l .


```


### Secondary parcel
#### json
```json
{
  "type": "Feature",
  "id": "8446456",
  "featureType": "SecondaryParcel",
"geometry": {
                "type": "Polygon",
                "coordinates": [
                    [
                        [
                            174.75076068885278,
                            -36.93102914553119
                        ],
                        [
                            174.75072255725163,
                            -36.931021544248715
                        ],
                        [
                            174.75054006892805,
                            -36.93106104934007
                        ],
                        [
                            174.75079103780536,
                            -36.93124895649441
                        ],
                        [
                            174.75099188136608,
                            -36.93120233371059
                        ],
                        [
                            174.75096726702185,
                            -36.931183910797834
                        ],
                        [
                            174.75076068885278,
                            -36.93102914553119
                        ]
                    ]
                ]
            },
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
    "parcelType": "eg-parcel-type:au",
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

```

#### jsonld
```jsonld
{
  "@context": [
    {
      "eg-parcel-purpose": "https://w3id.org/ogc/ladm/vocabs/eg/parcel-purpose/",
      "eg-parcel-type": "https://w3id.org/ogc/ladm/vocabs/eg/parcel-type/",
      "eg-parcel-state": "https://w3id.org/ogc/ladm/vocabs/eg/parcel-state/"
    },
    "https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/parcel/context.jsonld"
  ],
  "type": "Feature",
  "id": "8446456",
  "featureType": "SecondaryParcel",
  "geometry": {
    "type": "Polygon",
    "coordinates": [
      [
        [
          174.75076068885278,
          -36.93102914553119
        ],
        [
          174.75072255725163,
          -36.931021544248715
        ],
        [
          174.75054006892805,
          -36.93106104934007
        ],
        [
          174.75079103780536,
          -36.93124895649441
        ],
        [
          174.75099188136608,
          -36.93120233371059
        ],
        [
          174.75096726702185,
          -36.931183910797834
        ],
        [
          174.75076068885278,
          -36.93102914553119
        ]
      ]
    ]
  },
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
    "parcelType": "eg-parcel-type:au",
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
```

#### ttl
```ttl
@prefix commonpatterns: <https://w3id.org/ogc/utils/label/> .
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix eg-parcel-purpose: <https://w3id.org/ogc/ladm/vocabs/eg/parcel-purpose/> .
@prefix eg-parcel-state: <https://w3id.org/ogc/ladm/vocabs/eg/parcel-state/> .
@prefix eg-parcel-type: <https://w3id.org/ogc/ladm/vocabs/eg/parcel-type/> .
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix parcel: <https://w3id.org/ogc/ladm/parcels/> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix topo: <https://purl.org/geojson/topo#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<http://www.example.com/features/8446456> a geojson:Feature,
        parcel:SecondaryParcel ;
    geojson:geometry [ a geojson:Polygon ;
            geojson:coordinates ( ( ( 1.747508e+02 -3.693103e+01 ) ( 1.747507e+02 -3.693102e+01 ) ( 1.747505e+02 -3.693106e+01 ) ( 1.747508e+02 -3.693125e+01 ) ( 1.74751e+02 -3.69312e+01 ) ( 1.74751e+02 -3.693118e+01 ) ( 1.747508e+02 -3.693103e+01 ) ) ) ] ;
    geojson:topology [ a geojson:Polygon ;
            topo:relatedFeatures ( ( <http://www.example.com/features/l999724> <http://www.example.com/features/l591175> <http://www.example.com/features/l369793> <http://www.example.com/features/l435861> <http://www.example.com/features/l345344> <http://www.example.com/features/l685716> <http://www.example.com/features/l832940> <http://www.example.com/features/l715872> <http://www.example.com/features/l641327> <http://www.example.com/features/l852048> <http://www.example.com/features/l949729> <http://www.example.com/features/l951515> <http://www.example.com/features/l761760> <http://www.example.com/features/l580762> ) ) ] ;
    parcel:appellation [ rdfs:label "Area Z DP 572532" ;
            dcterms:hasPart [ rdfs:label "DP" ;
                    commonpatterns:namePartType <http://www.example.com/features/PlanType> ],
                [ rdfs:label "Z" ;
                    commonpatterns:namePartType <http://www.example.com/features/ParcelIdentifier> ],
                [ rdfs:label "Area" ;
                    commonpatterns:namePartType <http://www.example.com/features/ParcelType> ],
                [ rdfs:label "572532" ;
                    commonpatterns:namePartType <http://www.example.com/features/PlanIdentifier> ] ] ;
    parcel:interest [ parcel:interestLink <http://www.example.com/features/1040075> ;
            parcel:interestType <eg-interest-type:fh> ] ;
    parcel:purpose eg-parcel-purpose:c-l ;
    parcel:state eg-parcel-state:created ;
    parcel:surfaceArea 1196 ;
    parcel:type eg-parcel-type:au .


```


### ContainingParcelRef
Has a relationship from a parcel to a "ParentParcel" - with an explicit semantic relationship and a topolgy constraint relationship.

Note, the topology constraint "within" for a 3D Parcel, referencing a Parent Parcel defined in 2 or 2.5D implies within a virtual extruded volume defined by the footprint of the Parent Parcel.

#### json
```json
{
  "type": "Feature",
  "id": "8446454",
"geometry": {
                "type": "Polygon",
                "coordinates": [
                    [
                        [
                            174.75076068885278,
                            -36.93102914553119
                        ],
                        [
                            174.75072255725163,
                            -36.931021544248715
                        ],
                        [
                            174.75054006892805,
                            -36.93106104934007
                        ],
                        [
                            174.75079103780536,
                            -36.93124895649441
                        ],
                        [
                            174.75099188136608,
                            -36.93120233371059
                        ],
                        [
                            174.75096726702185,
                            -36.931183910797834
                        ],
                        [
                            174.75076068885278,
                            -36.93102914553119
                        ]
                    ]
                ]
            },
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
    "parcelType": "eg-parcel-type:l",
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
}
```

#### jsonld
```jsonld
{
  "@context": [
    {
      "eg-parcel-purpose": "https://w3id.org/ogc/ladm/vocabs/eg/parcel-purpose/",
      "eg-parcel-type": "https://w3id.org/ogc/ladm/vocabs/eg/parcel-type/",
      "eg-parcel-state": "https://w3id.org/ogc/ladm/vocabs/eg/parcel-state/"
    },
    "https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/parcel/context.jsonld"
  ],
  "type": "Feature",
  "id": "8446454",
  "geometry": {
    "type": "Polygon",
    "coordinates": [
      [
        [
          174.75076068885278,
          -36.93102914553119
        ],
        [
          174.75072255725163,
          -36.931021544248715
        ],
        [
          174.75054006892805,
          -36.93106104934007
        ],
        [
          174.75079103780536,
          -36.93124895649441
        ],
        [
          174.75099188136608,
          -36.93120233371059
        ],
        [
          174.75096726702185,
          -36.931183910797834
        ],
        [
          174.75076068885278,
          -36.93102914553119
        ]
      ]
    ]
  },
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
    "parcelType": "eg-parcel-type:l",
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
}
```

#### ttl
```ttl
@prefix commonpatterns: <https://w3id.org/ogc/utils/label/> .
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix eg-parcel-purpose: <https://w3id.org/ogc/ladm/vocabs/eg/parcel-purpose/> .
@prefix eg-parcel-state: <https://w3id.org/ogc/ladm/vocabs/eg/parcel-state/> .
@prefix eg-parcel-type: <https://w3id.org/ogc/ladm/vocabs/eg/parcel-type/> .
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix ns1: <http://www.iana.org/assignments/> .
@prefix oa: <http://www.w3.org/ns/oa#> .
@prefix parcel: <https://w3id.org/ogc/ladm/parcels/> .
@prefix prof: <http://www.w3.org/ns/dx/prof/> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix topo: <https://purl.org/geojson/topo#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<http://www.example.com/features/8446454> a geojson:Feature ;
    geojson:geometry [ a geojson:Polygon ;
            geojson:coordinates ( ( ( 1.747508e+02 -3.693103e+01 ) ( 1.747507e+02 -3.693102e+01 ) ( 1.747505e+02 -3.693106e+01 ) ( 1.747508e+02 -3.693125e+01 ) ( 1.74751e+02 -3.69312e+01 ) ( 1.74751e+02 -3.693118e+01 ) ( 1.747508e+02 -3.693103e+01 ) ) ) ] ;
    geojson:topology [ a geojson:Polygon ;
            topo:relatedFeatures ( [ ns1:relation <http://www.iana.org/assignments/relation/topology> ;
                        prof:hasRole topo:within,
                            parcel:containingParentParcel ;
                        oa:hasTarget <myParcels:1234> ] ),
                ( ( <http://www.example.com/features/l535242> <http://www.example.com/features/l535759> <http://www.example.com/features/l985190> <http://www.example.com/features/l952702> <http://www.example.com/features/l965727> <http://www.example.com/features/l589282> ) ) ] ;
    parcel:appellation [ rdfs:label "Lot 1 DP 572532" ;
            dcterms:hasPart [ rdfs:label "572532" ;
                    commonpatterns:namePartType <http://www.example.com/features/PlanIdentifier> ],
                [ rdfs:label "1" ;
                    commonpatterns:namePartType <http://www.example.com/features/ParcelIdentifier> ],
                [ rdfs:label "Lot" ;
                    commonpatterns:namePartType <http://www.example.com/features/ParcelType> ],
                [ rdfs:label "DP" ;
                    commonpatterns:namePartType <http://www.example.com/features/PlanType> ] ] ;
    parcel:interest [ parcel:interestLink <http://www.example.com/features/1040074> ;
            parcel:interestType <eg-interest-type:fh> ] ;
    parcel:purpose eg-parcel-purpose:fst ;
    parcel:state eg-parcel-state:created ;
    parcel:surfaceArea 484 ;
    parcel:type eg-parcel-type:l .


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
  interest:
    $anchor: interest
    properties:
      interestLink:
        $ref: '#/$defs/coderef'
        x-jsonld-type: '@id'
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/interestLink
      interestName:
        type: string
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/interestName
      interestType:
        $ref: '#/$defs/coderef'
        x-jsonld-type: '@id'
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/interestType
      dateInForce:
        $ref: '#/$defs/dateTime'
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/interestDateInForce
      dateExpires:
        $ref: '#/$defs/dateTime'
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/interestDateExpires
      statuteLink:
        $ref: '#/$defs/coderef'
        x-jsonld-type: '@id'
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/statuteLink
      statuteName:
        type: string
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/statuteName
      benefitedPartyName:
        type: string
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/benefitedPartyName
      benefitedPartyLink:
        $ref: '#/$defs/coderef'
        x-jsonld-type: '@id'
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/benefitedPartyLink
      originalSurveyLink:
        $ref: '#/$defs/coderef'
        x-jsonld-type: '@id'
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/originalSurveyLink
      referencedParcel:
        $ref: '#/$defs/coderef'
        x-jsonld-type: '@id'
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/referencedParcel
      burdenedParcels:
        $ref: '#/$defs/coderefList'
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/burdened
        x-jsonld-container: '@set'
      benefitedParcels:
        $ref: '#/$defs/coderefList'
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/benefited
        x-jsonld-container: '@set'
      description:
        type: string
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/interestDescription
      entitlementPortion:
        type: string
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/entitlementPortion
      liabilityPortion:
        type: string
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/liabilityPortion
    required:
    - interestLink
    - interestType
  parcelProperties:
    $anchor: parcelProperties
    properties:
      appellation:
        $ref: https://ogcincubator.github.io/bblocks-utility/build/annotated/bbr/utils/compoundName/schema.yaml
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/appellation
      parcelType:
        $ref: '#/$defs/coderef'
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/type
        x-jsonld-type: '@id'
      parcelState:
        $ref: '#/$defs/coderef'
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/state
        x-jsonld-type: '@id'
      address:
        type: object
        x-jsonld-id: https://schema.org/address
      parcelPurpose:
        $ref: '#/$defs/coderef'
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/purpose
        x-jsonld-type: '@id'
      area:
        type: number
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/surfaceArea
      floor:
        type: string
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/floor
      zmin:
        type: number
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/zmin
      zmax:
        type: number
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/zmax
      interests:
        type: array
        items:
          $ref: '#interest'
        x-jsonld-id: https://w3id.org/ogc/ladm/parcels/interest
        x-jsonld-container: '@set'
      spatialRepresentationDefinitions:
        $ref: https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/parcelSpatialRepresentationDefinition/schema.yaml
    required:
    - appellation
    - parcelType
    - parcelState
    - parcelPurpose
allOf:
- anyOf:
  - $ref: https://ogcincubator.github.io/topo-feature/build/annotated/geo/topo/features/topo-feature/schema.yaml
  - $ref: https://ogcincubator.github.io/topo-feature/build/annotated/geo/topo/features/topo-feature-multi-collection/schema.yaml
  - $ref: https://opengeospatial.github.io/bblocks/annotated-schemas/geo/json-fg/feature-lenient/schema.yaml
- properties:
    properties:
      $ref: '#parcelProperties'
x-jsonld-extra-terms:
  name: rdfs:label
  bearingRotation: https://w3id.org/ogc/ladm/parcels/bearingRotation
  parcels: https://w3id.org/ogc/ladm/parcels/parcels
  PrimaryParcel:
    x-jsonld-id: https://w3id.org/ogc/ladm/parcels/PrimaryParcel
    x-jsonld-type: '@id'
  SecondaryParcel:
    x-jsonld-id: https://w3id.org/ogc/ladm/parcels/SecondaryParcel
    x-jsonld-type: '@id'
  parcelQualityClass:
    x-jsonld-id: https://w3id.org/ogc/ladm/parcels/qualityClass
    x-jsonld-type: '@id'
  terrainIntersectionCurve: https://w3id.org/ogc/ladm/parcels/terrainIntersectionCurve
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
        },
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
        }
      },
      "@type": "@id",
      "@id": "geojson:topology"
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
    "solids": {
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
      "@id": "topo:solids",
      "@container": "@list"
    },
    "appellation": {
      "@context": {
        "name": "commonpatterns:name",
        "label": "rdfs:label",
        "hasPart": {
          "@context": {
            "ref": {
              "@type": "@id",
              "@id": "commonpatterns:namePartRef"
            },
            "type": {
              "@type": "@id",
              "@id": "commonpatterns:namePartType"
            }
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
    "Face": "topo:Face",
    "Ring": "topo:Ring",
    "Shell": "topo:Shell",
    "Solid": "topo:Solid",
    "directed_references": {
      "@id": "topo:directedReferences",
      "@container": "@list"
    },
    "CompoundName": "commonpatterns:CompoundName",
    "state": {
      "@id": "sr:boundaryState",
      "@type": "@vocab"
    },
    "definitionRef": {
      "@id": "sr:definitionRef",
      "@type": "@id"
    },
    "geometryRef": {
      "@id": "sr:geometryRef",
      "@type": "@id"
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
    "commonpatterns": "https://w3id.org/ogc/utils/label/",
    "sr": "https://linked.data.gov.au/def/csdm/spatial-representation/",
    "pvb": "https://linked.data.gov.au/def/csdm/parcel-vertical-boundary/",
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

