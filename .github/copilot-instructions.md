# Copilot Instructions for AI Coding Agents

## Project Overview

- This is a Minecraft mod project using Fabric, written in Java (see `src/main/java/dk/mosberg/`).
- The project is modular, supporting multiple mods and resource/data packs under `src/main/resources/{assets,data,resourcepacks}`.
- Main mod entrypoints are defined in `gradle.properties` as `dk.mosberg.CM` (main) and `dk.mosberg.client.CMClient` (client).

## Build & Development

- **Build:** Use `./gradlew build` (Windows: `gradlew.bat build`) from the project root.
- **Java version:** 21 (see `gradle.properties`).
- **Dependencies:** Managed via Gradle. Versions are pinned in `gradle.properties`.
- **Resource/data packs:** Place assets in `src/main/resources/assets` and data in `src/main/resources/data`.
- **Debugging:** Standard Java/Fabric debugging applies. No custom debug scripts found.

## Project Structure & Conventions

- **Source code:**
  - Main: `src/main/java/dk/mosberg/`
  - Client: `src/client/java/dk/mosberg/`
- **Resources:**
  - Mod assets: `src/main/resources/assets/{modid}`
  - Data packs: `src/main/resources/data/{modid}`
  - Resource packs: `src/main/resources/resourcepacks/`
- **Mod metadata:** `src/main/resources/fabric.mod.json` and `gradle.properties`.
- **Naming:** Folders and files use lowercase, snake_case, or modid conventions (e.g., `cm`, `backpacked`).
- **No custom test or CI scripts** detected; standard Gradle tasks apply.

## Integration & Patterns

- **Entrypoints:** Set in `gradle.properties` and referenced in `fabric.mod.json`.
- **Multi-mod support:** Each mod or resource pack is isolated under its own subfolder in `assets`, `data`, or `resourcepacks`.
- **External links:**
  - Homepage: https://mosberg.github.io/customMods
  - Sources: https://github.com/mosberg/customMods
  - Issues: https://github.com/mosberg/customMods/issues

## Examples

- To add a new mod: Create a new folder under `assets/{modid}` and `data/{modid}`; update `fabric.mod.json` and `gradle.properties` as needed.
- To add a resource pack: Place it under `resourcepacks/{packname}` with a `pack.mcmeta` file.

---

**For AI agents:**

- Always check `gradle.properties` and `fabric.mod.json` for mod configuration.
- Follow the established folder structure for new mods, assets, and data packs.
- Use Java 21 and Gradle for all builds.
- Reference existing mod folders for examples of conventions and structure.
