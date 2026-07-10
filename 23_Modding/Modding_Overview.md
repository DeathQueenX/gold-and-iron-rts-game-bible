# Modding Overview

## Goals
- Allow custom units, maps, missions, and balance packs.
- Keep official content separate from user content.
- Use readable data formats where practical.

## Supported mod types
- Data-only balance mods
- Custom maps
- Custom campaigns
- New units and buildings
- UI and localization packs

## Recommended structure
- manifest.json
- units/
- buildings/
- maps/
- scripts/
- localization/
- assets/

## Safety and compatibility
- Mods declare game version.
- Multiplayer requires matching mod manifests.
- Official ranked play disables gameplay-altering mods.
- Missing assets should fail gracefully with placeholders.
