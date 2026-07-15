
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
        "parcelType": "eg-parcel-type:l",
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
  ],
    "points": [
    {
      "id": "BoundaryMarks",
      "type": "FeatureCollection",
      "featureType": "SurveyPoint",
      "features": [
        {
          "id": "1725787",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7501603083,
              -36.9307359096
            ]
          },
          "properties": {
            "name": {
              "label": "RM E DP 119552",
              "hasPart": [
                {
                  "type": "Source",
                  "label": "DP 119552"
                },
                {
                  "type": "Stamp",
                  "label": "RM E"
                }
              ]
            },
            "purpose": "nz-surveypoint-purpose:boundary",
            "fromSurvey": "DP_119552",
            "comment": "ALP in channel of drive",
            "occupation": {
              "comment": "No occupation"
            },
            "monumentedBy": {
              "form": "nz-monument-form:plaque",
              "condition": "nz-monument-condition:markfound",
              "state": "nz-monument-state:original"
            }
          }
        },
        {
          "id": "44396823",
          "type": "Feature",
          "featureType": "CadastralMark",
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7508196767,
              -36.9314093194
            ]
          },
          "time": null,
          "properties": {
            "name": {
              "label": "ALP I DP 481392",
              "hasPart": [
                {
                  "type": "Source",
                  "label": "DP 481392"
                },
                {
                  "type": "Stamp",
                  "label": "ALP I"
                }
              ]
            },
            "purpose": "nz-surveypoint-purpose:nonBoundary",
            "occupation": {
              "comment": "ALP in channel of drive"
            },
            "monumentedBy": {
              "form": "nz-monument-form:pin",
              "condition": "nz-monument-condition:markfound",
              "state": "nz-monument-state:original"
            }
          }
        },
        {
          "id": "11745160",
          "type": "Feature",
          "featureType": "CadastralMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7501603083,
              -36.9307359096
            ]
          },
          "properties": {
            "name": {
              "label": "RM E DP 119552",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119552"
                },
                {
                  "type": "MarkType",
                  "label": "RM"
                },
                {
                  "type": "Stamp",
                  "label": "E"
                }
              ]
            },
            "purpose": "nz-surveypoint-purpose:non-boundary",
            "fromSurvey": "DP_119552",
            "ptQualityMeasure": 6,
            "comment": null,
            "monumentedBy": {
              "form": "nz-monument-form:plaque",
              "condition": "nz-monument-condition:mark-found",
              "state": "nz-monument-state:original"
            }
          }
        },
        {
          "id": "44438418",
          "type": "Feature",
          "featureType": "CadastralMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7508196767,
              -36.9314093194
            ]
          },
          "properties": {
            "name": {
              "label": "ALP I DP 481392",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "481392"
                },
                {
                  "type": "MarkType",
                  "label": "ALP"
                },
                {
                  "type": "Stamp",
                  "label": "I"
                }
              ]
            },
            "purpose": "nz-surveypoint-purpose:non-boundary",
            "fromSurvey": "DP_481392",
            "ptQualityMeasure": 6,
            "comment": "ALP in channel of drive",
            "monumentedBy": {
              "form": "nz-monument-form:pin",
              "condition": "nz-monument-condition:mark-found",
              "state": "nz-monument-state:original"
            }
          }
        },
        {
          "id": "11745104",
          "type": "Feature",
          "featureType": "GeodeticReferenceMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.749997996,
              -36.930903937
            ]
          },
          "properties": {
            "name": {
              "label": "RM C DP 119552 (EQ9W)",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119552"
                },
                {
                  "type": "MarkType",
                  "label": "RM"
                },
                {
                  "type": "Stamp",
                  "label": "C"
                },
                {
                  "type": "geodeticStamp",
                  "label": "EQ9W"
                }
              ]
            },
            "geodeticid": "EQ9W",
            "purpose": "nz-surveypoint-purpose:prm",
            "fromSurvey": "DP_119552",
            "ptQualityMeasure": 5,
            "comment": "Brass circular plaque flush in channel",
            "monumentedBy": {
              "form": "nz-monument-form:plaque",
              "condition": "nz-monument-condition:reliably-placed",
              "state": "nz-monument-state:original"
            }
          }
        },
        {
          "id": "11745161",
          "type": "Feature",
          "featureType": "CadastralMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7503985651,
              -36.9303670583
            ]
          },
          "properties": {
            "name": {
              "label": "LP X DP 119552",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119552"
                },
                {
                  "type": "MarkType",
                  "label": "LP"
                },
                {
                  "type": "Stamp",
                  "label": "X"
                }
              ]
            },
            "purpose": "nz-surveypoint-purpose:non-boundary",
            "fromSurvey": "DP_119552",
            "ptQualityMeasure": 6,
            "comment": null,
            "monumentedBy": {
              "form": "nz-monument-form:plug",
              "condition": "nz-monument-condition:mark-found",
              "state": "nz-monument-state:original"
            }
          }
        },
        {
          "id": "49655185",
          "type": "Feature",
          "featureType": "CadastralMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.75043155,
              -36.9309699441
            ]
          },
          "properties": {
            "name": {
              "label": "AP 1 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "AP"
                },
                {
                  "type": "Stamp",
                  "label": "1"
                }
              ]
            },
            "purpose": "icsm:prm",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 6,
            "comment": "Flush in conc",
            "monumentedBy": {
              "form": "nz-monument-form:pin",
              "condition": "nz-monument-condition:reliably-placed",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "44438410",
          "type": "Feature",
          "featureType": "CadastralMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7505837059,
              -36.9311866966
            ]
          },
          "properties": {
            "name": {
              "label": "RM I DP 119553",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119553"
                },
                {
                  "type": "MarkType",
                  "label": "RM"
                },
                {
                  "type": "Stamp",
                  "label": "I"
                }
              ]
            },
            "purpose": "nz-surveypoint-purpose:prm",
            "fromSurvey": "DP_119553",
            "ptQualityMeasure": 6,
            "comment": "ORM in channel above catch pits",
            "monumentedBy": {
              "form": "nz-monument-form:plaque",
              "condition": "nz-monument-condition:mark-found",
              "state": "nz-monument-state:original"
            }
          }
        },
        {
          "id": "49655186",
          "type": "Feature",
          "featureType": "CadastralMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7502384493,
              -36.9309318616
            ]
          },
          "properties": {
            "name": {
              "label": "RM H DP 119553",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119553"
                },
                {
                  "type": "MarkType",
                  "label": "RM"
                },
                {
                  "type": "Stamp",
                  "label": "H"
                }
              ]
            },
            "purpose": "nz-surveypoint-purpose:non-boundary",
            "fromSurvey": "DP_119553",
            "ptQualityMeasure": 6,
            "comment": "ORM in channel above catch pits",
            "monumentedBy": {
              "form": "nz-monument-form:plaque",
              "condition": "nz-monument-condition:mark-found",
              "state": "nz-monument-state:original"
            }
          }
        },
        {
          "id": "29960715",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.750791041,
              -36.9312489607
            ]
          },
          "properties": {
            "name": {
              "label": "Peg 6 DP 119553",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119553"
                },
                {
                  "type": "MarkType",
                  "label": "Peg"
                },
                {
                  "type": "Stamp",
                  "label": "6"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_119553",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:peg",
              "condition": "nz-monument-condition:searched-for-not-found",
              "state": "nz-monument-state:Adopted"
            }
          }
        },
        {
          "id": "29959289",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7505110058,
              -36.9310392342
            ]
          },
          "properties": {
            "name": {
              "label": "Peg 3 DP 119553",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119553"
                },
                {
                  "type": "MarkType",
                  "label": "Peg"
                },
                {
                  "type": "Stamp",
                  "label": "3"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_119553",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:peg",
              "condition": "nz-monument-condition:not-found-replaced",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "29962820",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7512489947,
              -36.9308797133
            ]
          },
          "properties": {
            "name": {
              "label": "Peg 4 DP 119552",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119552"
                },
                {
                  "type": "MarkType",
                  "label": "Peg"
                },
                {
                  "type": "Stamp",
                  "label": "4"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_119552",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:peg",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:adopted"
            }
          }
        },
        {
          "id": "29963073",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7513031028,
              -36.9310543825
            ]
          },
          "properties": {
            "name": {
              "label": "Peg 8 DP 119553",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119553"
                },
                {
                  "type": "MarkType",
                  "label": "Peg"
                },
                {
                  "type": "Stamp",
                  "label": "8"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_119553",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:peg",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:adopted"
            }
          }
        },
        {
          "id": "29963182",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.751324788,
              -36.9311247115
            ]
          },
          "properties": {
            "name": {
              "label": "Peg 7 DP 119553",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119553"
                },
                {
                  "type": "MarkType",
                  "label": "Peg"
                },
                {
                  "type": "Stamp",
                  "label": "7"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_119553",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:peg",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:adopted"
            }
          }
        },
        {
          "id": "49655170",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7509918818,
              -36.9312023381
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 14 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "14"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:mark-impractible",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655172",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7507606923,
              -36.9310291431
            ]
          },
          "properties": {
            "name": {
              "label": "Peg 18 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "Peg"
                },
                {
                  "type": "Stamp",
                  "label": "18"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:Peg",
              "condition": "nz-monument-condition:reliably-placed",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655173",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7507225544,
              -36.9310215435
            ]
          },
          "properties": {
            "name": {
              "label": "Peg 19 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "Peg"
                },
                {
                  "type": "Stamp",
                  "label": "19"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:Peg",
              "condition": "nz-monument-condition:reliably-placed",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655187",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7509672626,
              -36.9311839118
            ]
          },
          "properties": {
            "name": {
              "label": "Peg 38 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "Peg"
                },
                {
                  "type": "Stamp",
                  "label": "38"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:Peg",
              "condition": "nz-monument-condition:reliably-placed",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655174",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7508909488,
              -36.9309571156
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 20 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "20"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655175",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7510988383,
              -36.9311774613
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 21 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "21"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655176",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7509396099,
              -36.9309904554
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 22 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "22"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 8,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655177",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7509925285,
              -36.9309870924
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 23 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "23"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 8,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655178",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.751010805,
              -36.9310015962
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 24 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "24"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 8,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655179",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7510101475,
              -36.9310253792
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 25 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "25"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 8,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655180",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.750980056,
              -36.9310510313
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 26 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "26"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 8,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655181",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7509573691,
              -36.9310656315
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 27 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "27"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 8,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655182",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7509509094,
              -36.9310856987
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 28 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "28"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 8,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655183",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7509568685,
              -36.9311076188
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 29 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "29"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 8,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655184",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7510438631,
              -36.9311710421
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 30 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "30"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 8,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655171",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.750540074,
              -36.9310610479
            ]
          },
          "properties": {
            "name": {
              "label": "DISK 15 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "Disk"
                },
                {
                  "type": "Stamp",
                  "label": "15"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:peg",
              "condition": "nz-monument-condition:reliably-placed",
              "state": "nz-monument-state:new"
            }
          }
        }
      ]
    }
  ],
  "edges": [
    {
      "id": "observedVectors",
      "type": "FeatureCollection",
      "featureType": "ObservedVector",
      "features": [
        {
          "type": "Feature",
          "id": "l566592",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "11745160",
              "44438418"
            ]
          },
          "properties": {
            "purpose": "radiation"
          }
        },
        {
          "type": "Feature",
          "id": "l973158",
          "geometry": {
            "type": "LineString",
            "coordinates": [
              [
                174.7501603083,
                -36.9307359096
              ],
              [
                174.749997996,
                -36.930903937
              ]
            ]
          },
          "topology": {
            "type": "LineString",
            "references": [
              "1725787",
              "11745104"
            ]
          },
          "properties": {
            "purpose": "traverse"
          }
        },
        {
          "type": "Feature",
          "id": "l910380",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "11745160",
              "11745161"
            ]
          },
          "properties": {
            "purpose": "traverse"
          }
        },
        {
          "type": "Feature",
          "id": "l472486",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "11745160",
              "49655185"
            ]
          },
          "properties": {
            "purpose": "traverse"
          }
        },
        {
          "type": "Feature",
          "id": "l922788",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655185",
              "49655186"
            ]
          },
          "properties": {
            "purpose": "radiation"
          }
        },
        {
          "type": "Feature",
          "id": "l773277",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655185",
              "44438410"
            ]
          },
          "properties": {
            "purpose": "traverse"
          }
        },
        {
          "type": "Feature",
          "id": "l388393",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655185",
              "49655172"
            ]
          },
          "properties": {
            "purpose": "radiation"
          }
        },
        {
          "type": "Feature",
          "id": "l941613",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655185",
              "49655187"
            ]
          },
          "properties": {
            "purpose": "radiation"
          }
        },
        {
          "type": "Feature",
          "id": "l818068",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655185",
              "49655170"
            ]
          },
          "properties": {
            "purpose": "calculation"
          }
        },
        {
          "type": "Feature",
          "id": "l599462",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655185",
              "49655171"
            ]
          },
          "properties": {
            "purpose": "radiation"
          }
        },
        {
          "type": "Feature",
          "id": "l746686",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "29959289",
              "49655174"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l999724",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655174",
              "29962820"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l591175",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "29962820",
              "29963073"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l874826",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655175",
              "49655170"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l369793",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "29963073",
              "29963182"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l435861",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "29963182",
              "49655175"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l965727",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655170",
              "29960715"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l535242",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655171",
              "49655173"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l535759",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655173",
              "49655172"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l985190",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655172",
              "49655187"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l952702",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655187",
              "49655170"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l580762",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655174",
              "49655176"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l761760",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655176",
              "49655177"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l951515",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655177",
              "49655178"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l949729",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655178",
              "49655179"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l852048",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655179",
              "49655180"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l641327",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655180",
              "49655181"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l715872",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655181",
              "49655182"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l832940",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655182",
              "49655183"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l685716",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655183",
              "49655184"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l345344",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655184",
              "49655175"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        }
      ]
    },
    {
      "id": "adoptedVectors",
      "type": "FeatureCollection",
      "featureType": "AdoptedVector",
      "features": [
        {
          "type": "Feature",
          "id": "l636624",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "11745104",
              "49655186"
            ]
          },
          "properties": {
            "purpose": "adoption"
          }
        },
        {
          "type": "Feature",
          "id": "l595769",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "44438410",
              "29960715"
            ]
          },
          "properties": {
            "purpose": "adoption"
          }
        },
        {
          "type": "Feature",
          "id": "l520719",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "44438410",
              "49655186"
            ]
          },
          "properties": {
            "purpose": "adoption"
          }
        },
        {
          "type": "Feature",
          "id": "l947230",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "11745104",
              "44438418"
            ]
          },
          "properties": {
            "purpose": "adoption"
          }
        },
        {
          "type": "Feature",
          "id": "l595769",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "44438418",
              "29960715"
            ]
          },
          "properties": {
            "purpose": "adoption"
          }
        },
        {
          "type": "Feature",
          "id": "l622186",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "44438418",
              "29959289"
            ]
          },
          "properties": {
            "purpose": "adoption"
          }
        },
        {
          "type": "Feature",
          "id": "l329256",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "29959289",
              "49655171"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l589282",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655171",
              "29960715"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        }
      ]
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
        "parcelType": "eg-parcel-type:l",
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
  ],
  "points": [
    {
      "id": "BoundaryMarks",
      "type": "FeatureCollection",
      "featureType": "SurveyPoint",
      "features": [
        {
          "id": "1725787",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7501603083,
              -36.9307359096
            ]
          },
          "properties": {
            "name": {
              "label": "RM E DP 119552",
              "hasPart": [
                {
                  "type": "Source",
                  "label": "DP 119552"
                },
                {
                  "type": "Stamp",
                  "label": "RM E"
                }
              ]
            },
            "purpose": "nz-surveypoint-purpose:boundary",
            "fromSurvey": "DP_119552",
            "comment": "ALP in channel of drive",
            "occupation": {
              "comment": "No occupation"
            },
            "monumentedBy": {
              "form": "nz-monument-form:plaque",
              "condition": "nz-monument-condition:markfound",
              "state": "nz-monument-state:original"
            }
          }
        },
        {
          "id": "44396823",
          "type": "Feature",
          "featureType": "CadastralMark",
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7508196767,
              -36.9314093194
            ]
          },
          "time": null,
          "properties": {
            "name": {
              "label": "ALP I DP 481392",
              "hasPart": [
                {
                  "type": "Source",
                  "label": "DP 481392"
                },
                {
                  "type": "Stamp",
                  "label": "ALP I"
                }
              ]
            },
            "purpose": "nz-surveypoint-purpose:nonBoundary",
            "occupation": {
              "comment": "ALP in channel of drive"
            },
            "monumentedBy": {
              "form": "nz-monument-form:pin",
              "condition": "nz-monument-condition:markfound",
              "state": "nz-monument-state:original"
            }
          }
        },
        {
          "id": "11745160",
          "type": "Feature",
          "featureType": "CadastralMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7501603083,
              -36.9307359096
            ]
          },
          "properties": {
            "name": {
              "label": "RM E DP 119552",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119552"
                },
                {
                  "type": "MarkType",
                  "label": "RM"
                },
                {
                  "type": "Stamp",
                  "label": "E"
                }
              ]
            },
            "purpose": "nz-surveypoint-purpose:non-boundary",
            "fromSurvey": "DP_119552",
            "ptQualityMeasure": 6,
            "comment": null,
            "monumentedBy": {
              "form": "nz-monument-form:plaque",
              "condition": "nz-monument-condition:mark-found",
              "state": "nz-monument-state:original"
            }
          }
        },
        {
          "id": "44438418",
          "type": "Feature",
          "featureType": "CadastralMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7508196767,
              -36.9314093194
            ]
          },
          "properties": {
            "name": {
              "label": "ALP I DP 481392",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "481392"
                },
                {
                  "type": "MarkType",
                  "label": "ALP"
                },
                {
                  "type": "Stamp",
                  "label": "I"
                }
              ]
            },
            "purpose": "nz-surveypoint-purpose:non-boundary",
            "fromSurvey": "DP_481392",
            "ptQualityMeasure": 6,
            "comment": "ALP in channel of drive",
            "monumentedBy": {
              "form": "nz-monument-form:pin",
              "condition": "nz-monument-condition:mark-found",
              "state": "nz-monument-state:original"
            }
          }
        },
        {
          "id": "11745104",
          "type": "Feature",
          "featureType": "GeodeticReferenceMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.749997996,
              -36.930903937
            ]
          },
          "properties": {
            "name": {
              "label": "RM C DP 119552 (EQ9W)",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119552"
                },
                {
                  "type": "MarkType",
                  "label": "RM"
                },
                {
                  "type": "Stamp",
                  "label": "C"
                },
                {
                  "type": "geodeticStamp",
                  "label": "EQ9W"
                }
              ]
            },
            "geodeticid": "EQ9W",
            "purpose": "nz-surveypoint-purpose:prm",
            "fromSurvey": "DP_119552",
            "ptQualityMeasure": 5,
            "comment": "Brass circular plaque flush in channel",
            "monumentedBy": {
              "form": "nz-monument-form:plaque",
              "condition": "nz-monument-condition:reliably-placed",
              "state": "nz-monument-state:original"
            }
          }
        },
        {
          "id": "11745161",
          "type": "Feature",
          "featureType": "CadastralMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7503985651,
              -36.9303670583
            ]
          },
          "properties": {
            "name": {
              "label": "LP X DP 119552",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119552"
                },
                {
                  "type": "MarkType",
                  "label": "LP"
                },
                {
                  "type": "Stamp",
                  "label": "X"
                }
              ]
            },
            "purpose": "nz-surveypoint-purpose:non-boundary",
            "fromSurvey": "DP_119552",
            "ptQualityMeasure": 6,
            "comment": null,
            "monumentedBy": {
              "form": "nz-monument-form:plug",
              "condition": "nz-monument-condition:mark-found",
              "state": "nz-monument-state:original"
            }
          }
        },
        {
          "id": "49655185",
          "type": "Feature",
          "featureType": "CadastralMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.75043155,
              -36.9309699441
            ]
          },
          "properties": {
            "name": {
              "label": "AP 1 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "AP"
                },
                {
                  "type": "Stamp",
                  "label": "1"
                }
              ]
            },
            "purpose": "icsm:prm",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 6,
            "comment": "Flush in conc",
            "monumentedBy": {
              "form": "nz-monument-form:pin",
              "condition": "nz-monument-condition:reliably-placed",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "44438410",
          "type": "Feature",
          "featureType": "CadastralMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7505837059,
              -36.9311866966
            ]
          },
          "properties": {
            "name": {
              "label": "RM I DP 119553",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119553"
                },
                {
                  "type": "MarkType",
                  "label": "RM"
                },
                {
                  "type": "Stamp",
                  "label": "I"
                }
              ]
            },
            "purpose": "nz-surveypoint-purpose:prm",
            "fromSurvey": "DP_119553",
            "ptQualityMeasure": 6,
            "comment": "ORM in channel above catch pits",
            "monumentedBy": {
              "form": "nz-monument-form:plaque",
              "condition": "nz-monument-condition:mark-found",
              "state": "nz-monument-state:original"
            }
          }
        },
        {
          "id": "49655186",
          "type": "Feature",
          "featureType": "CadastralMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7502384493,
              -36.9309318616
            ]
          },
          "properties": {
            "name": {
              "label": "RM H DP 119553",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119553"
                },
                {
                  "type": "MarkType",
                  "label": "RM"
                },
                {
                  "type": "Stamp",
                  "label": "H"
                }
              ]
            },
            "purpose": "nz-surveypoint-purpose:non-boundary",
            "fromSurvey": "DP_119553",
            "ptQualityMeasure": 6,
            "comment": "ORM in channel above catch pits",
            "monumentedBy": {
              "form": "nz-monument-form:plaque",
              "condition": "nz-monument-condition:mark-found",
              "state": "nz-monument-state:original"
            }
          }
        },
        {
          "id": "29960715",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.750791041,
              -36.9312489607
            ]
          },
          "properties": {
            "name": {
              "label": "Peg 6 DP 119553",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119553"
                },
                {
                  "type": "MarkType",
                  "label": "Peg"
                },
                {
                  "type": "Stamp",
                  "label": "6"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_119553",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:peg",
              "condition": "nz-monument-condition:searched-for-not-found",
              "state": "nz-monument-state:Adopted"
            }
          }
        },
        {
          "id": "29959289",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7505110058,
              -36.9310392342
            ]
          },
          "properties": {
            "name": {
              "label": "Peg 3 DP 119553",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119553"
                },
                {
                  "type": "MarkType",
                  "label": "Peg"
                },
                {
                  "type": "Stamp",
                  "label": "3"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_119553",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:peg",
              "condition": "nz-monument-condition:not-found-replaced",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "29962820",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7512489947,
              -36.9308797133
            ]
          },
          "properties": {
            "name": {
              "label": "Peg 4 DP 119552",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119552"
                },
                {
                  "type": "MarkType",
                  "label": "Peg"
                },
                {
                  "type": "Stamp",
                  "label": "4"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_119552",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:peg",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:adopted"
            }
          }
        },
        {
          "id": "29963073",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7513031028,
              -36.9310543825
            ]
          },
          "properties": {
            "name": {
              "label": "Peg 8 DP 119553",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119553"
                },
                {
                  "type": "MarkType",
                  "label": "Peg"
                },
                {
                  "type": "Stamp",
                  "label": "8"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_119553",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:peg",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:adopted"
            }
          }
        },
        {
          "id": "29963182",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.751324788,
              -36.9311247115
            ]
          },
          "properties": {
            "name": {
              "label": "Peg 7 DP 119553",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "119553"
                },
                {
                  "type": "MarkType",
                  "label": "Peg"
                },
                {
                  "type": "Stamp",
                  "label": "7"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_119553",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:peg",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:adopted"
            }
          }
        },
        {
          "id": "49655170",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7509918818,
              -36.9312023381
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 14 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "14"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:mark-impractible",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655172",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7507606923,
              -36.9310291431
            ]
          },
          "properties": {
            "name": {
              "label": "Peg 18 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "Peg"
                },
                {
                  "type": "Stamp",
                  "label": "18"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:Peg",
              "condition": "nz-monument-condition:reliably-placed",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655173",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7507225544,
              -36.9310215435
            ]
          },
          "properties": {
            "name": {
              "label": "Peg 19 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "Peg"
                },
                {
                  "type": "Stamp",
                  "label": "19"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:Peg",
              "condition": "nz-monument-condition:reliably-placed",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655187",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7509672626,
              -36.9311839118
            ]
          },
          "properties": {
            "name": {
              "label": "Peg 38 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "Peg"
                },
                {
                  "type": "Stamp",
                  "label": "38"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:Peg",
              "condition": "nz-monument-condition:reliably-placed",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655174",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7508909488,
              -36.9309571156
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 20 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "20"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655175",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7510988383,
              -36.9311774613
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 21 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "21"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655176",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7509396099,
              -36.9309904554
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 22 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "22"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 8,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655177",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7509925285,
              -36.9309870924
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 23 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "23"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 8,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655178",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.751010805,
              -36.9310015962
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 24 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "24"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 8,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655179",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7510101475,
              -36.9310253792
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 25 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "25"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 8,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655180",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.750980056,
              -36.9310510313
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 26 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "26"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 8,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655181",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7509573691,
              -36.9310656315
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 27 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "27"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 8,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655182",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7509509094,
              -36.9310856987
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 28 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "28"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 8,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655183",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7509568685,
              -36.9311076188
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 29 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "29"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 8,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655184",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.7510438631,
              -36.9311710421
            ]
          },
          "properties": {
            "name": {
              "label": "UNMK 30 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "UNMK"
                },
                {
                  "type": "Stamp",
                  "label": "30"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 8,
            "monumentedBy": {
              "form": "nz-monument-form:UNMK",
              "condition": "nz-monument-condition:not-specified",
              "state": "nz-monument-state:new"
            }
          }
        },
        {
          "id": "49655171",
          "type": "Feature",
          "featureType": "BoundaryMark",
          "time": null,
          "geometry": {
            "type": "Point",
            "coordinates": [
              174.750540074,
              -36.9310610479
            ]
          },
          "properties": {
            "name": {
              "label": "DISK 15 DP 572532",
              "hasPart": [
                {
                  "type": "PlanType",
                  "label": "DP"
                },
                {
                  "type": "Stamp",
                  "label": "572532"
                },
                {
                  "type": "MarkType",
                  "label": "Disk"
                },
                {
                  "type": "Stamp",
                  "label": "15"
                }
              ]
            },
            "purpose": "boundary",
            "fromSurvey": "DP_572532",
            "ptQualityMeasure": 7,
            "monumentedBy": {
              "form": "nz-monument-form:peg",
              "condition": "nz-monument-condition:reliably-placed",
              "state": "nz-monument-state:new"
            }
          }
        }
      ]
    }
  ],
  "edges": [
    {
      "id": "observedVectors",
      "type": "FeatureCollection",
      "featureType": "ObservedVector",
      "features": [
        {
          "type": "Feature",
          "id": "l566592",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "11745160",
              "44438418"
            ]
          },
          "properties": {
            "purpose": "radiation"
          }
        },
        {
          "type": "Feature",
          "id": "l973158",
          "geometry": {
            "type": "LineString",
            "coordinates": [
              [
                174.7501603083,
                -36.9307359096
              ],
              [
                174.749997996,
                -36.930903937
              ]
            ]
          },
          "topology": {
            "type": "LineString",
            "references": [
              "1725787",
              "11745104"
            ]
          },
          "properties": {
            "purpose": "traverse"
          }
        },
        {
          "type": "Feature",
          "id": "l910380",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "11745160",
              "11745161"
            ]
          },
          "properties": {
            "purpose": "traverse"
          }
        },
        {
          "type": "Feature",
          "id": "l472486",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "11745160",
              "49655185"
            ]
          },
          "properties": {
            "purpose": "traverse"
          }
        },
        {
          "type": "Feature",
          "id": "l922788",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655185",
              "49655186"
            ]
          },
          "properties": {
            "purpose": "radiation"
          }
        },
        {
          "type": "Feature",
          "id": "l773277",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655185",
              "44438410"
            ]
          },
          "properties": {
            "purpose": "traverse"
          }
        },
        {
          "type": "Feature",
          "id": "l388393",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655185",
              "49655172"
            ]
          },
          "properties": {
            "purpose": "radiation"
          }
        },
        {
          "type": "Feature",
          "id": "l941613",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655185",
              "49655187"
            ]
          },
          "properties": {
            "purpose": "radiation"
          }
        },
        {
          "type": "Feature",
          "id": "l818068",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655185",
              "49655170"
            ]
          },
          "properties": {
            "purpose": "calculation"
          }
        },
        {
          "type": "Feature",
          "id": "l599462",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655185",
              "49655171"
            ]
          },
          "properties": {
            "purpose": "radiation"
          }
        },
        {
          "type": "Feature",
          "id": "l746686",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "29959289",
              "49655174"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l999724",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655174",
              "29962820"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l591175",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "29962820",
              "29963073"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l874826",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655175",
              "49655170"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l369793",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "29963073",
              "29963182"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l435861",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "29963182",
              "49655175"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l965727",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655170",
              "29960715"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l535242",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655171",
              "49655173"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l535759",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655173",
              "49655172"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l985190",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655172",
              "49655187"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l952702",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655187",
              "49655170"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l580762",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655174",
              "49655176"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l761760",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655176",
              "49655177"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l951515",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655177",
              "49655178"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l949729",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655178",
              "49655179"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l852048",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655179",
              "49655180"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l641327",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655180",
              "49655181"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l715872",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655181",
              "49655182"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l832940",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655182",
              "49655183"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l685716",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655183",
              "49655184"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l345344",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655184",
              "49655175"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        }
      ]
    },
    {
      "id": "adoptedVectors",
      "type": "FeatureCollection",
      "featureType": "AdoptedVector",
      "features": [
        {
          "type": "Feature",
          "id": "l636624",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "11745104",
              "49655186"
            ]
          },
          "properties": {
            "purpose": "adoption"
          }
        },
        {
          "type": "Feature",
          "id": "l595769",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "44438410",
              "29960715"
            ]
          },
          "properties": {
            "purpose": "adoption"
          }
        },
        {
          "type": "Feature",
          "id": "l520719",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "44438410",
              "49655186"
            ]
          },
          "properties": {
            "purpose": "adoption"
          }
        },
        {
          "type": "Feature",
          "id": "l947230",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "11745104",
              "44438418"
            ]
          },
          "properties": {
            "purpose": "adoption"
          }
        },
        {
          "type": "Feature",
          "id": "l595769",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "44438418",
              "29960715"
            ]
          },
          "properties": {
            "purpose": "adoption"
          }
        },
        {
          "type": "Feature",
          "id": "l622186",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "44438418",
              "29959289"
            ]
          },
          "properties": {
            "purpose": "adoption"
          }
        },
        {
          "type": "Feature",
          "id": "l329256",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "29959289",
              "49655171"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        },
        {
          "type": "Feature",
          "id": "l589282",
          "geometry": null,
          "topology": {
            "type": "LineString",
            "references": [
              "49655171",
              "29960715"
            ]
          },
          "properties": {
            "purpose": "boundary"
          }
        }
      ]
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
    topo:edges ( <http://www.example.com/features/observedVectors> <http://www.example.com/features/adoptedVectors> ) ;
    topo:points ( <http://www.example.com/features/BoundaryMarks> ) ;
    geojson:features <http://www.example.com/features/8446454>,
        <http://www.example.com/features/8446455> .

<http://www.example.com/features/44396823> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "CadastralMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747508e+02 -3.693141e+01 ) ] .

<http://www.example.com/features/8446454> a geojson:Feature ;
    geojson:topology [ a geojson:Polygon ;
            topo:relatedFeatures ( ( <http://www.example.com/features/l535242> <http://www.example.com/features/l535759> <http://www.example.com/features/l985190> <http://www.example.com/features/l952702> <http://www.example.com/features/l965727> <http://www.example.com/features/l589282> ) ) ] ;
    parcel:appellation [ rdfs:label "Lot 1 DP 572532" ;
            dcterms:hasPart [ rdfs:label "DP" ;
                    commonpatterns:namePartType "PlanType" ],
                [ rdfs:label "572532" ;
                    commonpatterns:namePartType "PlanIdentifier" ],
                [ rdfs:label "Lot" ;
                    commonpatterns:namePartType "ParcelType" ],
                [ rdfs:label "1" ;
                    commonpatterns:namePartType "ParcelIdentifier" ] ] ;
    parcel:interest [ parcel:interestLink <http://www.example.com/features/1040074> ;
            parcel:interestType <eg-interest-type:fh> ] ;
    parcel:purpose <eg-parcel-purpose:fst> ;
    parcel:state <eg-parcel-state:created> ;
    parcel:surfaceArea 484 ;
    parcel:type <eg-parcel-type:l> .

<http://www.example.com/features/8446455> a geojson:Feature ;
    geojson:topology [ a geojson:Polygon ;
            topo:relatedFeatures ( ( <http://www.example.com/features/l746686> <http://www.example.com/features/l999724> <http://www.example.com/features/l591175> <http://www.example.com/features/l435861> <http://www.example.com/features/l874826> <http://www.example.com/features/l952702> <http://www.example.com/features/l985190> <http://www.example.com/features/l535759> <http://www.example.com/features/l535242> <http://www.example.com/features/l329256> ) ) ] ;
    parcel:appellation [ rdfs:label "Lot 2 DP 572532" ;
            dcterms:hasPart [ rdfs:label "DP" ;
                    commonpatterns:namePartType "PlanType" ],
                [ rdfs:label "572532" ;
                    commonpatterns:namePartType "PlanIdentifier" ],
                [ rdfs:label "Lot" ;
                    commonpatterns:namePartType "ParcelType" ],
                [ rdfs:label "2" ;
                    commonpatterns:namePartType "ParcelIdentifier" ] ] ;
    parcel:interest [ parcel:interestLink <http://www.example.com/features/1040075> ;
            parcel:interestType <eg-interest-type:fh> ] ;
    parcel:purpose <eg-parcel-purpose:fst> ;
    parcel:state <eg-parcel-state:created> ;
    parcel:surfaceArea 1196 ;
    parcel:type <eg-parcel-type:l> .

<http://www.example.com/features/BoundaryMarks> a geojson:FeatureCollection ;
    geojson:collectionFeatureType "SurveyPoint" ;
    geojson:features <http://www.example.com/features/11745104>,
        <http://www.example.com/features/11745160>,
        <http://www.example.com/features/11745161>,
        <http://www.example.com/features/1725787>,
        <http://www.example.com/features/29959289>,
        <http://www.example.com/features/29960715>,
        <http://www.example.com/features/29962820>,
        <http://www.example.com/features/29963073>,
        <http://www.example.com/features/29963182>,
        <http://www.example.com/features/44396823>,
        <http://www.example.com/features/44438410>,
        <http://www.example.com/features/44438418>,
        <http://www.example.com/features/49655170>,
        <http://www.example.com/features/49655171>,
        <http://www.example.com/features/49655172>,
        <http://www.example.com/features/49655173>,
        <http://www.example.com/features/49655174>,
        <http://www.example.com/features/49655175>,
        <http://www.example.com/features/49655176>,
        <http://www.example.com/features/49655177>,
        <http://www.example.com/features/49655178>,
        <http://www.example.com/features/49655179>,
        <http://www.example.com/features/49655180>,
        <http://www.example.com/features/49655181>,
        <http://www.example.com/features/49655182>,
        <http://www.example.com/features/49655183>,
        <http://www.example.com/features/49655184>,
        <http://www.example.com/features/49655185>,
        <http://www.example.com/features/49655186>,
        <http://www.example.com/features/49655187> .

<http://www.example.com/features/adoptedVectors> a geojson:FeatureCollection ;
    geojson:collectionFeatureType "AdoptedVector" ;
    geojson:features <http://www.example.com/features/l329256>,
        <http://www.example.com/features/l520719>,
        <http://www.example.com/features/l589282>,
        <http://www.example.com/features/l595769>,
        <http://www.example.com/features/l622186>,
        <http://www.example.com/features/l636624>,
        <http://www.example.com/features/l947230> .

<http://www.example.com/features/l345344> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655184> <http://www.example.com/features/49655175> ) ] .

<http://www.example.com/features/l369793> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/29963073> <http://www.example.com/features/29963182> ) ] .

<http://www.example.com/features/l388393> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655185> <http://www.example.com/features/49655172> ) ] .

<http://www.example.com/features/l472486> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/11745160> <http://www.example.com/features/49655185> ) ] .

<http://www.example.com/features/l520719> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/44438410> <http://www.example.com/features/49655186> ) ] .

<http://www.example.com/features/l566592> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/11745160> <http://www.example.com/features/44438418> ) ] .

<http://www.example.com/features/l580762> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655174> <http://www.example.com/features/49655176> ) ] .

<http://www.example.com/features/l595769> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/44438410> <http://www.example.com/features/29960715> ) ],
        [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/44438418> <http://www.example.com/features/29960715> ) ] .

<http://www.example.com/features/l599462> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655185> <http://www.example.com/features/49655171> ) ] .

<http://www.example.com/features/l622186> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/44438418> <http://www.example.com/features/29959289> ) ] .

<http://www.example.com/features/l636624> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/11745104> <http://www.example.com/features/49655186> ) ] .

<http://www.example.com/features/l641327> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655180> <http://www.example.com/features/49655181> ) ] .

<http://www.example.com/features/l685716> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655183> <http://www.example.com/features/49655184> ) ] .

<http://www.example.com/features/l715872> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655181> <http://www.example.com/features/49655182> ) ] .

<http://www.example.com/features/l761760> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655176> <http://www.example.com/features/49655177> ) ] .

<http://www.example.com/features/l773277> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655185> <http://www.example.com/features/44438410> ) ] .

<http://www.example.com/features/l818068> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655185> <http://www.example.com/features/49655170> ) ] .

<http://www.example.com/features/l832940> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655182> <http://www.example.com/features/49655183> ) ] .

<http://www.example.com/features/l852048> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655179> <http://www.example.com/features/49655180> ) ] .

<http://www.example.com/features/l910380> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/11745160> <http://www.example.com/features/11745161> ) ] .

<http://www.example.com/features/l922788> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655185> <http://www.example.com/features/49655186> ) ] .

<http://www.example.com/features/l941613> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655185> <http://www.example.com/features/49655187> ) ] .

<http://www.example.com/features/l947230> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/11745104> <http://www.example.com/features/44438418> ) ] .

<http://www.example.com/features/l949729> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655178> <http://www.example.com/features/49655179> ) ] .

<http://www.example.com/features/l951515> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655177> <http://www.example.com/features/49655178> ) ] .

<http://www.example.com/features/l973158> a geojson:Feature ;
    geojson:geometry [ a geojson:LineString ;
            geojson:coordinates ( ( 1.747502e+02 -3.693074e+01 ) ( 1.7475e+02 -3.69309e+01 ) ) ] ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/1725787> <http://www.example.com/features/11745104> ) ] .

<http://www.example.com/features/observedVectors> a geojson:FeatureCollection ;
    geojson:collectionFeatureType "ObservedVector" ;
    geojson:features <http://www.example.com/features/l345344>,
        <http://www.example.com/features/l369793>,
        <http://www.example.com/features/l388393>,
        <http://www.example.com/features/l435861>,
        <http://www.example.com/features/l472486>,
        <http://www.example.com/features/l535242>,
        <http://www.example.com/features/l535759>,
        <http://www.example.com/features/l566592>,
        <http://www.example.com/features/l580762>,
        <http://www.example.com/features/l591175>,
        <http://www.example.com/features/l599462>,
        <http://www.example.com/features/l641327>,
        <http://www.example.com/features/l685716>,
        <http://www.example.com/features/l715872>,
        <http://www.example.com/features/l746686>,
        <http://www.example.com/features/l761760>,
        <http://www.example.com/features/l773277>,
        <http://www.example.com/features/l818068>,
        <http://www.example.com/features/l832940>,
        <http://www.example.com/features/l852048>,
        <http://www.example.com/features/l874826>,
        <http://www.example.com/features/l910380>,
        <http://www.example.com/features/l922788>,
        <http://www.example.com/features/l941613>,
        <http://www.example.com/features/l949729>,
        <http://www.example.com/features/l951515>,
        <http://www.example.com/features/l952702>,
        <http://www.example.com/features/l965727>,
        <http://www.example.com/features/l973158>,
        <http://www.example.com/features/l985190>,
        <http://www.example.com/features/l999724> .

<http://www.example.com/features/11745161> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "CadastralMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747504e+02 -3.693037e+01 ) ] .

<http://www.example.com/features/1725787> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747502e+02 -3.693074e+01 ) ] .

<http://www.example.com/features/l329256> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/29959289> <http://www.example.com/features/49655171> ) ] .

<http://www.example.com/features/l435861> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/29963182> <http://www.example.com/features/49655175> ) ] .

<http://www.example.com/features/l589282> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655171> <http://www.example.com/features/29960715> ) ] .

<http://www.example.com/features/l591175> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/29962820> <http://www.example.com/features/29963073> ) ] .

<http://www.example.com/features/l746686> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/29959289> <http://www.example.com/features/49655174> ) ] .

<http://www.example.com/features/l874826> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655175> <http://www.example.com/features/49655170> ) ] .

<http://www.example.com/features/l965727> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655170> <http://www.example.com/features/29960715> ) ] .

<http://www.example.com/features/l999724> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655174> <http://www.example.com/features/29962820> ) ] .

<http://www.example.com/features/29962820> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747512e+02 -3.693088e+01 ) ] .

<http://www.example.com/features/29963073> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747513e+02 -3.693105e+01 ) ] .

<http://www.example.com/features/29963182> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747513e+02 -3.693112e+01 ) ] .

<http://www.example.com/features/49655173> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747507e+02 -3.693102e+01 ) ] .

<http://www.example.com/features/49655176> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747509e+02 -3.693099e+01 ) ] .

<http://www.example.com/features/49655177> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.74751e+02 -3.693099e+01 ) ] .

<http://www.example.com/features/49655178> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.74751e+02 -3.6931e+01 ) ] .

<http://www.example.com/features/49655179> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.74751e+02 -3.693103e+01 ) ] .

<http://www.example.com/features/49655180> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.74751e+02 -3.693105e+01 ) ] .

<http://www.example.com/features/49655181> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.74751e+02 -3.693107e+01 ) ] .

<http://www.example.com/features/49655182> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.74751e+02 -3.693109e+01 ) ] .

<http://www.example.com/features/49655183> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.74751e+02 -3.693111e+01 ) ] .

<http://www.example.com/features/49655184> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.74751e+02 -3.693117e+01 ) ] .

<http://www.example.com/features/l535242> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655171> <http://www.example.com/features/49655173> ) ] .

<http://www.example.com/features/l535759> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655173> <http://www.example.com/features/49655172> ) ] .

<http://www.example.com/features/l952702> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655187> <http://www.example.com/features/49655170> ) ] .

<http://www.example.com/features/l985190> a geojson:Feature ;
    geojson:topology [ a geojson:LineString ;
            topo:relatedFeatures ( <http://www.example.com/features/49655172> <http://www.example.com/features/49655187> ) ] .

<http://www.example.com/features/11745104> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "GeodeticReferenceMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.7475e+02 -3.69309e+01 ) ] .

<http://www.example.com/features/11745160> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "CadastralMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747502e+02 -3.693074e+01 ) ] .

<http://www.example.com/features/29959289> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747505e+02 -3.693104e+01 ) ] .

<http://www.example.com/features/44438410> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "CadastralMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747506e+02 -3.693119e+01 ) ] .

<http://www.example.com/features/49655172> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747508e+02 -3.693103e+01 ) ] .

<http://www.example.com/features/49655174> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747509e+02 -3.693096e+01 ) ] .

<http://www.example.com/features/49655175> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747511e+02 -3.693118e+01 ) ] .

<http://www.example.com/features/49655186> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "CadastralMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747502e+02 -3.693093e+01 ) ] .

<http://www.example.com/features/49655187> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.74751e+02 -3.693118e+01 ) ] .

<http://www.example.com/features/29960715> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747508e+02 -3.693125e+01 ) ] .

<http://www.example.com/features/44438418> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "CadastralMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747508e+02 -3.693141e+01 ) ] .

<http://www.example.com/features/49655170> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.74751e+02 -3.69312e+01 ) ] .

<http://www.example.com/features/49655171> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "BoundaryMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747505e+02 -3.693106e+01 ) ] .

<http://www.example.com/features/49655185> a geojson:Feature ;
    rdfs:label [ ] ;
    geojson:collectionFeatureType "CadastralMark" ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( 1.747504e+02 -3.693097e+01 ) ] .


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
            dcterms:hasPart [ rdfs:label "Z" ;
                    commonpatterns:namePartType "ParcelIdentifier" ],
                [ rdfs:label "Area" ;
                    commonpatterns:namePartType "ParcelType" ],
                [ rdfs:label "DP" ;
                    commonpatterns:namePartType "PlanType" ],
                [ rdfs:label "572532" ;
                    commonpatterns:namePartType "PlanIdentifier" ] ] ;
    parcel:interest [ parcel:interestLink <http://www.example.com/features/1040075> ;
            parcel:interestType <eg-interest-type:fh> ] ;
    parcel:purpose <eg-parcel-purpose:c-l> ;
    parcel:state <eg-parcel-state:created> ;
    parcel:surfaceArea 1196 ;
    parcel:type <eg-parcel-type:au> .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
type: object
allOf:
- anyOf:
  - $ref: https://ogcincubator.github.io/topo-feature/build/annotated/geo/topo/features/topo-feature-collection/schema.yaml
  - $ref: https://opengeospatial.github.io/bblocks/annotated-schemas/geo/json-fg/featureCollection-lenient/schema.yaml
- properties:
    features:
      items:
        $ref: https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/parcel/schema.yaml

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

