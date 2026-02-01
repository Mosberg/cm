# Minecraft Fabric Mod Assets & Data Packs

This document provides a comprehensive overview of the contents and structure of the `assets/` and `data/` folders for this Fabric-based Minecraft mod project. It is intended for mod developers, contributors, and advanced users who wish to understand, extend, or maintain the mod's resource and data pack system.

---

## Table of Contents

- [Minecraft Fabric Mod Assets \& Data Packs](#minecraft-fabric-mod-assets--data-packs)
  - [Table of Contents](#table-of-contents)
  - [Overview](#overview)
  - [Folder Structure](#folder-structure)
    - [assets/](#assets)
      - [Example: assets/backpacked/](#example-assetsbackpacked)
    - [data/](#data)
      - [Example: data/biomesoplenty/](#example-databiomesoplenty)
  - [Modular Design](#modular-design)
  - [Resource Pack Conventions](#resource-pack-conventions)
  - [Data Pack Conventions](#data-pack-conventions)
  - [Localization](#localization)
  - [Adding New Mods or Packs](#adding-new-mods-or-packs)
  - [References](#references)

---

## Overview

This project supports multiple mods and resource/data packs, each organized under their own namespace within the `assets/` and `data/` directories. This modular approach allows for easy addition, removal, or modification of individual mods or packs without affecting others.

- **assets/**: Contains client-side resources (textures, models, sounds, blockstates, etc.) for each mod or resource pack.
- **data/**: Contains server/data-driven content (recipes, loot tables, advancements, tags, worldgen, etc.) for each mod or data pack.

---

## Folder Structure

### assets/

Located at `src/main/resources/assets/`, this folder contains the following subfolders (one per mod or resource pack):

- **backpacked/**
  - `sounds.json`, item/block models, blockstates, textures, font icons, and multiple language files (e.g., `en_us.json`, `fr_fr.json`).
  - Subfolders: `blockstates/`, `font/`, `items/`, `lang/`, `models/`, `sounds/`, `textures/`.
- **biomesoplenty/**, **classicpipes/**, **cookingforblockheads/**, **emi/**, **farmersdelight/**, **farmingforblockheads/**, **fluidtank/**, **minecraft/**, **simple_copper_pipes/**, **thecopperierage/**, **cm/**
  - Each follows a similar structure, with subfolders for blockstates, items, models, sounds, textures, and language files as appropriate for the mod.
- **resourcepacks/**
  - Custom resource packs can be placed here, each with its own `pack.mcmeta`.

#### Example: assets/backpacked/

- `blockstates/`: Blockstate JSONs for custom blocks (e.g., backpack shelves, docks).
- `items/`: Item model JSONs for backpacks and related items.
- `lang/`: Localization files for multiple languages.
- `models/`, `sounds/`, `textures/`: Standard Minecraft resource folders.
- `font/icons.json`: Custom font icons for UI.

### data/

Located at `src/main/resources/data/`, this folder contains the following subfolders (one per mod or data pack):

- **backpacked/**
  - Contains item JSONs for each backpack variant.
- **biomesoplenty/**, **classicpipes/**, **cookingforblockheads/**, **farmersdelight/**, **farmingforblockheads/**, **fluidtank/**, **minecraft/**, **simple_copper_pipes/**, **thecopperierage/**, etc.
  - Each contains subfolders for advancements, recipes, loot tables, tags, worldgen, and other data-driven content.
- **c/**, **cm/**, **create/**, **createaddition/**, **forge/**, **frozenlib/**, **inspirations/**, **neoforge/**, **origins/**, **sereneseasons/**, **tconstruct/**, **toughasnails/**, **wilderwild/**
  - These may provide compatibility, integration, or additional data for other mods.

#### Example: data/biomesoplenty/

- `advancement/`, `recipe/`, `tags/`, `worldgen/`, etc.: Standard Minecraft data pack folders.
- Custom folders for mod-specific features (e.g., `chicken_variant/`, `cow_variant/`, `jukebox_song/`).

---

## Modular Design

- Each mod or resource/data pack is isolated under its own namespace (folder) in both `assets/` and `data/`.
- This allows for independent development and maintenance of each mod or pack.
- New mods or packs can be added by creating new folders under `assets/` and `data/` and following the established structure.

---

## Resource Pack Conventions

- **Textures**: PNG files in `textures/` subfolders.
- **Models**: JSON files in `models/` and `items/`.
- **Blockstates**: JSON files in `blockstates/`.
- **Sounds**: Defined in `sounds.json` and stored in `sounds/`.
- **Fonts**: Custom font icons in `font/`.
- **Localization**: Language files in `lang/` (e.g., `en_us.json`).

---

## Data Pack Conventions

- **Recipes**: JSON files in `recipe/`.
- **Loot Tables**: JSON files in `loot_table/` or `loot_tables/`.
- **Advancements**: JSON files in `advancement/` or `advancements/`.
- **Tags**: JSON files in `tags/`.
- **Worldgen**: JSON files in `worldgen/`.
- **Custom Data**: Mod-specific folders for unique features (e.g., `chicken_variant/`, `damage_type/`).

---

## Localization

- Each mod/resource pack can provide its own set of language files under `assets/{modid}/lang/`.
- Supported languages include (but are not limited to): English (US/GB/UD), German, French, Spanish (ES/MX/AR), Czech, Kazakh, Portuguese (BR), Russian, Ukrainian, Vietnamese, Chinese (CN/TW).
- Language files are standard Minecraft JSON format.

---

## Adding New Mods or Packs

1. **Create Folders**: Add a new folder under both `assets/` and `data/` using your modid or pack name.
2. **Populate Resources**: Add textures, models, blockstates, sounds, and language files as needed in `assets/{modid}/`.
3. **Populate Data**: Add recipes, loot tables, advancements, tags, and other data in `data/{modid}/`.
4. **Register in Mod Metadata**: Update `fabric.mod.json` and `gradle.properties` as needed to register your mod.
5. **Test**: Build and test your mod to ensure all resources and data are loaded correctly.

---

## References

- [Minecraft Wiki: Resource Pack](https://minecraft.fandom.com/wiki/Resource_Pack)
- [Minecraft Wiki: Data Pack](https://minecraft.fandom.com/wiki/Data_Pack)
- [Fabric Modding Documentation](https://fabricmc.net/wiki/tutorial:setup)
- [Project Homepage](https://mosberg.github.io/customMods)
- [Project Source](https://github.com/mosberg/customMods)

---

_This README was generated to provide a detailed map of the assets and data structure for this modular Fabric mod project. For further details, refer to the individual files and folders within each namespace._
