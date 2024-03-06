---
title: Compound name (Schema)

language_tabs:
  - json: JSON
  - jsonld: JSON-LD
  - turtle: RDF/Turtle

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
    <a target="_blank" href="https://ogcincubator.github.io/bblocks-land-parcels/build/tests/land-parcels/compound-name/example_1_1.json">Open in new window</a>
    <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=json&amp;dataUrl=https%3A%2F%2Fogcincubator.github.io%2Fbblocks-land-parcels%2Fbuild%2Ftests%2Fland-parcels%2Fcompound-name%2Fexample_1_1.json&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on JSON Viewer</a></p>
</blockquote>




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

<blockquote class="lang-specific jsonld">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/bblocks-land-parcels/build/tests/land-parcels/compound-name/example_1_1.jsonld">Open in new window</a>
    <a target="_blank" href="https://json-ld.org/playground/#json-ld=https%3A%2F%2Fogcincubator.github.io%2Fbblocks-land-parcels%2Fbuild%2Ftests%2Fland-parcels%2Fcompound-name%2Fexample_1_1.jsonld">View on JSON-LD Playground</a>
</blockquote>




```turtle
@prefix dct: <http://purl.org/dc/terms/> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

[] rdfs:label "IS II - DP 3333" ;
    dct:hasPart [ a <file:///github/workspace/Source> ;
            rdfs:label "DP 3333" ],
        [ a <file:///github/workspace/Stamp> ;
            rdfs:label "IS II" ] .


```

<blockquote class="lang-specific turtle">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/bblocks-land-parcels/build/tests/land-parcels/compound-name/example_1_1.ttl">Open in new window</a>
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

> <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=yaml&amp;dataUrl=https%3A%2F%2Fogcincubator.github.io%2Fbblocks-land-parcels%2Fbuild%2Fannotated%2Fland-parcels%2Fcompound-name%2Fschema.yaml&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on YAML Viewer</a>

Links to the schema:

* YAML version: <a href="https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/compound-name/schema.yaml" target="_blank">https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/compound-name/schema.yaml</a>
* JSON version: <a href="https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/compound-name/schema.json" target="_blank">https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/compound-name/schema.json</a>


# JSON-LD Context

```json--ldContext
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

> <a target="_blank" href="https://json-ld.org/playground/#json-ld=https%3A%2F%2Fogcincubator.github.io%2Fbblocks-land-parcels%2Fbuild%2Fannotated%2Fland-parcels%2Fcompound-name%2Fcontext.jsonld">View on JSON-LD Playground</a>

You can find the full JSON-LD context here:
<a href="https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/compound-name/context.jsonld" target="_blank">https://ogcincubator.github.io/bblocks-land-parcels/build/annotated/land-parcels/compound-name/context.jsonld</a>

# For developers

The source code for this Building Block can be found in the following repository:

* URL: <a href="https://github.com/ogcincubator/bblocks-land-parcels" target="_blank">https://github.com/ogcincubator/bblocks-land-parcels</a>
* Path:
<code><a href="https://github.com/ogcincubator/bblocks-land-parcels/blob/HEAD/_sources/compound-name" target="_blank">_sources/compound-name</a></code>

