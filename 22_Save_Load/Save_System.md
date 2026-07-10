# Save System

## Save types
- Campaign autosave
- Manual campaign save
- Skirmish save
- Replay file
- Profile progression

## Required data
- Current map and mission state
- Units and buildings
- Resources
- Hero levels, abilities, and relics
- Objectives and scripted events
- Diplomacy state
- Corruption state

## Rules
- Version save files.
- Keep at least three rotating autosaves.
- Validate content IDs on load.
- Provide recovery for missing optional data.
- Replays store commands and deterministic seeds rather than full snapshots where possible.
