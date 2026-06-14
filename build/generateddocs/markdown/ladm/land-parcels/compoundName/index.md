
# Compound Name (Schema)

`ogc.ladm.land-parcels.compoundName` *v0.1*

A multiple part name, consisting of a set of strings with functional roles that can be combined into single string using a template.

[*Status*](http://www.opengis.net/def/status): Under development

## Examples

### Example CompoundName
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


### Referenced Parts
An example name where part of the name is a reference to a vocabulary source.  This can us used for validation and multi-linual applications
#### json
```json
{
    "id": "CompoundNameExample",
    "type": "CompoundName",
    "label": "IS II - DP 3333",
    "comment": "the label of the part is optional - but can be cross checked",
    "hasPart": [
        {
            "type": "wa-plan:planTypes",
            "ref": "wa-plan-register:dp333",
            "label": "DP 3333"
        },
        {
            "type": "Stamp",
            "label": "IS II"
        }
    ]
}
```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: Compound Name
anyOf:
- required:
  - label
- required:
  - hasPart
additionalProperties: true
properties:
  label:
    anyOf:
    - type: 'null'
    - type: string
  template:
    type: string
  hasPart:
    type: array
    items:
      type: object
      additionalProperties: false
      properties:
        label:
          type: string
        ref:
          $ref: https://opengeospatial.github.io/bblocks/annotated-schemas/ogc-utils/iri-or-curie/schema.yaml
        type:
          $ref: https://opengeospatial.github.io/bblocks/annotated-schemas/ogc-utils/iri-or-curie/schema.yaml
      anyOf:
      - required:
        - label
      - required:
        - ref

```

Links to the schema:

* YAML version: [schema.yaml](https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/compoundName/schema.json)
* JSON version: [schema.json](https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/ladm/land-parcels/compoundName/schema.yaml)


# JSON-LD Context

```jsonld
None
```

You can find the full JSON-LD context here:
[context.jsonld](/github/workspace/_sources/compoundName/context.jsonld)

## Sources

* [CSDM model](https://github.com/icsm-au/3d-csdm)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/ogcincubator/bblocks-land-parcels](https://github.com/ogcincubator/bblocks-land-parcels)
* Path: `_sources/compoundName`

