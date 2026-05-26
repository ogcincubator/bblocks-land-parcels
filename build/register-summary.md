# Land parcels

This repository contains a JSON schema model for land parcels, semantically annotated and aligned with LADM conceptual model.

These schemas use a generalised 3D topology model to provide explicit definition of parcels required for survey record keeping. 

The topology model supports transformations to well known geometry formats which may be used to visualise and validated geometry representations of  Parcel objects in 2 or 3D.


## Building Blocks

### `ogc.ladm.land-parcels.compound-name` — Compound name

**Type:** schema

A multiple part name, consisting of a set of strings with functional roles that can be combined into single string using a template.

### `ogc.ladm.land-parcels.ontology` — Land Parcels Ontology

**Type:** model

Terms and definitions for the Land Parcels model.  This is aligned with LADM semantics and terminology and could be evolved or mapped to an authoritative LADM ontology component as required/

### `ogc.ladm.land-parcels.parcel` — Land Parcel

**Type:** schema

A parcel of land, corresponds to LA_SpatialUnit from LADM (ISO 19162)

### `ogc.ladm.land-parcels.parcelCollection` — Land Parcel Collection

**Type:** schema

corresponds to LA_SpatialUnitGroup from LADM (ISO 19162)

