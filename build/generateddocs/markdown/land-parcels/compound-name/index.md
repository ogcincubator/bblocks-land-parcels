
# Compound name (Schema)

`ogc.land-parcels.compound-name` *v0.1*

A multiple part name, consisting of a set of strings with functional roles that can be combined into single string using a template.

[*Status*](http://www.opengis.net/def/status): Under development

## Examples

### Example Compound Name
A name with a label, but also a set of parts with roles that can be validated against content rules.
#### json
```json
{
    "id": "CompoundNameExample",
    "type": "CompoundName",
    "label": "IS II - DP 3333",
    "comment": "note: label may be absent or subject to rules regarding presence of parts",
    "hasPart": [
        {
            "type": "Source",
            "label": "DP 3333"
        },
        {
            "type": "Stamp",
            "label": "IS II"
        }
    ]
}
```

#### jsonld
```jsonld
{
  "id": "CompoundNameExample",
  "type": "CompoundName",
  "label": "IS II - DP 3333",
  "comment": "note: label may be absent or subject to rules regarding presence of parts",
  "hasPart": [
    {
      "type": "Source",
      "label": "DP 3333"
    },
    {
      "type": "Stamp",
      "label": "IS II"
    }
  ],
  "@context": "https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/compound-name/context.jsonld"
}
```

#### ttl
```ttl
@prefix dct: <http://purl.org/dc/terms/> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

[] rdfs:label "IS II - DP 3333" ;
    dct:hasPart [ a <file:///github/workspace/Source> ;
            rdfs:label "DP 3333" ],
        [ a <file:///github/workspace/Stamp> ;
            rdfs:label "IS II" ] .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: Compound Name
properties:
  label:
    anyOf:
    - type: 'null'
    - type: string
    x-jsonld-id: http://www.w3.org/2000/01/rdf-schema#label
  template:
    type: string
  hasPart:
    type: array
    items:
      type: object
      properties:
        label:
          type: string
          x-jsonld-id: http://www.w3.org/2000/01/rdf-schema#label
        type:
          type: string
          x-jsonld-id: '@type'
      required:
      - label
    x-jsonld-id: http://purl.org/dc/terms/hasPart
x-jsonld-extra-terms:
  name: http://purl.org/dc/terms/title
x-jsonld-prefixes:
  dct: http://purl.org/dc/terms/
  rdfs: http://www.w3.org/2000/01/rdf-schema#

```

Links to the schema:

* YAML version: [schema.yaml](https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/compound-name/schema.json)
* JSON version: [schema.json](https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/compound-name/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "label": "rdfs:label",
    "hasPart": {
      "@context": {
        "type": "@type"
      },
      "@id": "dct:hasPart"
    },
    "name": "dct:title",
    "dct": "http://purl.org/dc/terms/",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/compound-name/context.jsonld)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/ogcincubator/bblocks-land-parcels](https://github.com/ogcincubator/bblocks-land-parcels)
* Path: `_sources/compound-name`

