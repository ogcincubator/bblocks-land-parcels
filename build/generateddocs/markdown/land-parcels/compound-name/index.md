
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

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: Compound Name
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
      properties:
        label:
          type: string
        type:
          type: string
      required:
      - label

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/ogcincubator/bblocks-land-parcels/master/build/annotated/land-parcels/compound-name/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/ogcincubator/bblocks-land-parcels/master/build/annotated/land-parcels/compound-name/schema.yaml)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/ogcincubator/bblocks-land-parcels](https://github.com/ogcincubator/bblocks-land-parcels)
* Path: `_sources/compound-name`

