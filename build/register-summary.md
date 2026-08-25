# Land parcels

This repository contains a JSON schema model for land parcels, semantically annotated and aligned with LADM conceptual model.

These schemas use a generalised 3D topology model to provide explicit definition of parcels required for survey record keeping. 

The topology model supports transformations to well known geometry formats which may be used to visualise and validated geometry representations of  Parcel objects in 2 or 3D.


## Building Blocks

### `ogc.ladm.land-parcels.codelists.examples.parcel-purpose` — Example Vocab: Parcel Purpose

**Type:** model

An example vocab - used in examples for parcel purpose codelist

### `ogc.ladm.land-parcels.codelists.examples.parcel-type` — Example Vocab: Parcel Types

**Type:** model

An example vocab - used in examples for parcel type codelist

### `ogc.ladm.land-parcels.ontology` — Land Parcels Ontology

**Type:** model

Terms and definitions for the Land Parcels model.  This is aligned with LADM semantics and terminology and could be evolved or mapped to an authoritative LADM ontology component as required/

### `ogc.ladm.land-parcels.spatialRepresentationDefinition` — Spatial Representation Definition

**Type:** schema

Generic, reusable properties that record how a 2D feature's geometry is being interpreted with respect to the vertical dimension: whether the representation is a plain 2D footprint, has contextual z-values, is bounded by a reference surface, carries a legally defined vertical boundary, or has a derived 3D solid — and how confidently that interpretation can be computed. Not specific to parcels; reusable by any 2D feature type gaining a 2.5D or 3D representation.

### `ogc.ladm.land-parcels.parcelSpatialRepresentationDefinition` — Parcel Spatial Representation Definition

**Type:** schema

The WA cadastral parcel-specific extension of the generic spatial representation definition pattern. Adds the jurisdictional source basis (rule type, source authority type, and verbatim source statement) needed to trace a parcel's vertical boundary back to a title, plan, statute, Crown Grant, strata statement, or other approved jurisdictional rule.

### `ogc.ladm.land-parcels.parcel` — Land Parcel

**Type:** schema

A parcel of land, corresponds to LA_SpatialUnit from LADM (ISO 19162)

### `ogc.ladm.land-parcels.parcelCollection` — Land Parcel Collection

**Type:** schema

corresponds to LA_SpatialUnitGroup from LADM (ISO 19162)

