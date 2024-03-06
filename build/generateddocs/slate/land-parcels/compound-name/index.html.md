---
title: Compound name (Schema)


toc_footers:
  - Version 0.1
  - <a href='#'>Compound name</a>
  - <a href='https://blocks.ogc.org/register.html'>Building Blocks register</a>

search: true

code_clipboard: true

meta:
  - name: Compound name (Schema)
---


# Compound name `ogc.land-parcels.compound-name`

A multiple part name, consisting of a set of strings with functional roles that can be combined into single string using a template.

<p class="status">
    <span data-rainbow-uri="http://www.opengis.net/def/status">Status</span>:
    <a href="http://www.opengis.net/def/status/under-development" target="_blank" data-rainbow-uri>Under development</a>
</p>

<aside class="success">
This building block is <strong><a href="https://github.com/ogcincubator/bblocks-land-parcels/blob/master/build/tests/land-parcels/compound-name/" target="_blank">valid</a></strong>
</aside>

# Examples

## Example Compound Name



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

<blockquote class="lang-specific json">
  <p class="example-links">
    <a target="_blank" href="https://raw.githubusercontent.com/ogcincubator/bblocks-land-parcels/master/build/tests/land-parcels/compound-name/example_1_1.json">Open in new window</a>
    <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=json&amp;dataUrl=https%3A%2F%2Fraw.githubusercontent.com%2Fogcincubator%2Fbblocks-land-parcels%2Fmaster%2Fbuild%2Ftests%2Fland-parcels%2Fcompound-name%2Fexample_1_1.json&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on JSON Viewer</a></p>
</blockquote>


A name with a label, but also a set of parts with roles that can be validated against content rules.


# JSON Schema

```yaml--schema
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

> <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=yaml&amp;dataUrl=https%3A%2F%2Fraw.githubusercontent.com%2Fogcincubator%2Fbblocks-land-parcels%2Fmaster%2Fbuild%2Fannotated%2Fland-parcels%2Fcompound-name%2Fschema.yaml&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on YAML Viewer</a>

Links to the schema:

* YAML version: <a href="https://raw.githubusercontent.com/ogcincubator/bblocks-land-parcels/master/build/annotated/land-parcels/compound-name/schema.yaml" target="_blank">https://raw.githubusercontent.com/ogcincubator/bblocks-land-parcels/master/build/annotated/land-parcels/compound-name/schema.yaml</a>
* JSON version: <a href="https://raw.githubusercontent.com/ogcincubator/bblocks-land-parcels/master/build/annotated/land-parcels/compound-name/schema.json" target="_blank">https://raw.githubusercontent.com/ogcincubator/bblocks-land-parcels/master/build/annotated/land-parcels/compound-name/schema.json</a>

# For developers

The source code for this Building Block can be found in the following repository:

* URL: <a href="https://github.com/ogcincubator/bblocks-land-parcels" target="_blank">https://github.com/ogcincubator/bblocks-land-parcels</a>
* Path:
<code><a href="https://github.com/ogcincubator/bblocks-land-parcels/blob/HEAD/_sources/compound-name" target="_blank">_sources/compound-name</a></code>

