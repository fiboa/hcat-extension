# Hierarchical Crop and Agriculture Taxonomy Extension Specification

- **Title:** Hierarchical Crop and Agriculture Taxonomy Extension
- **Identifier:** <https://fiboa.github.io/hcat-extension/v0.1.0/schema.yaml>
- **Property Name Prefix:** ec
- **Extension Maturity Classification:** Proposal
- **Owner**: @cholmes

This document explains the Hierarchical Crop and Agriculture Taxonomy (HCAT) Extension to the
[Field Boundaries for Agriculture (fiboa) Specification](https://github.com/fiboa/specification).

The Hierarchical Crop and Agriculture Taxonomy (HCAT) was defined by the
[Eurocrops](https://github.com/maja601/EuroCrops) project,
which harmonized a number of European crop datasets.
It provides a consistent schema for crop classification, covering
almost 400 different crop types, and is currently on it's third iteration.
The HCAT core list of names and codes is defined in the file
[HCAT3.csv](https://github.com/maja601/EuroCrops/blob/main/hcat_core/HCAT3.csv).
Its goal is to harmonise all declared crops across the European Union, but it is likely a useful
as crop classification taxonomy beyond Europe.

Note that this extension does not attempt to use the exact same field names as Eurocrops, as they
were designed for use with Shapefiles, a restriction Fiboa does not share. This attempts to be
more descriptive, and fit with the 'Fiboa style', reusing the 'EC_' prefix of the original fields,
but adapting it to be `ec:`. But feedback is welcome, we could have it stay more true, or also
adapt it more (like use `hcat:` as the prefix).

- Examples:
  - [GeoJSON](examples/geojson/)
  - [GeoParquet](examples/geoparquet/)
- [Schema](schema/schema.yaml)
- [Changelog](./CHANGELOG.md)

## Properties

The properties in the table below can be used in these parts of fiboa documents:

- [ ] Collection
- [x] Feature Properties

| Property Name      | Type   | Description |
| ------------------ | ------ | ----------- |
| ec:hcat_name       | string | **REQUIRED**. The machine-readable HCAT name of the crop |
| ec:hcat_code       | uint32 | **REQUIRED**. The 10-digit HCAT code indicating the hierarchy of the crop |
| ec:translated_name | string | The original crop name translated into English |

## Contributing

See the [contributing guideline](CONTRIBUTING.md) for more details.
