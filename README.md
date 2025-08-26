# Hierarchical Crop and Agriculture Taxonomy Extension Specification

- **Title:** Hierarchical Crop and Agriculture Taxonomy Extension
- **Identifier:** <https://fiboa.github.io/hcat-extension/v0.3.0/schema.yaml>
- **Property Name Prefix:** hcat
- **Extension Maturity Classification:** Proposal
- **Owner**: @cholmes @ivorbosloper

This document explains the Hierarchical Crop and Agriculture Taxonomy (HCAT) Extension to the
[Field Boundaries for Agriculture (fiboa)](https://fiboa.org) and
[Vecorel](https://vecorel.org) specifications.

The Hierarchical Crop and Agriculture Taxonomy (HCAT) was defined by the
[Eurocrops](https://github.com/maja601/EuroCrops) project,
which harmonized a number of European crop datasets.
It provides a consistent schema for crop classification, covering
almost 400 different crop types, and is currently on it's third iteration.
The HCAT core list of names and codes is defined in the file
[HCAT3.csv](https://github.com/maja601/EuroCrops/blob/main/hcat_core/HCAT3.csv).
Its goal is to harmonise all declared crops across the European Union, but it is likely a useful
as crop classification taxonomy beyond Europe. In order to prepare for this wider use case, we
will use the `hcat` abbreviations instead of `ec`.

Note that this extension does not attempt to use the exact same field names as Eurocrops, as they
were designed for use with Shapefiles, a restriction Fiboa does not share. This attempts to be
more descriptive, and fit with the 'Fiboa style'.

- Examples:
  - [GeoJSON](examples/geojson/)
  - [GeoParquet](examples/geoparquet/)
- [Schema](schema/schema.yaml)
- [Changelog](./CHANGELOG.md)

## Properties

| Property Name | Type   | Description                                                 |
|---------------|--------|-------------------------------------------------------------|
| hcat:name     | string | The machine-readable HCAT name of the crop                  |
| hcat:code     | uint32 | The 10-digit HCAT code indicating the hierarchy of the crop |
| hcat:name_en  | string | The original crop name translated into English              |

## Contributing

See the [contributing guideline](CONTRIBUTING.md) for more details.
