# Pathfinding and Terrain

## Design intent

Pathfinding-ul este critic într-un RTS cu munți, delte, poduri, canale și unități navale. Terenul trebuie să creeze decizii tactice fără să frustreze jucătorul.

## Movement layers

### Ground
Used by infantry, cavalry, workers, siege and most heroes.

### Heavy Ground
Used by heavy siege, mechanical walkers and large monsters. Cannot cross narrow paths unless marked as heavy-compatible.

### Naval
Used by ships and waterborne units. Requires water depth metadata.

### Amphibious
Rare layer for special units, monsters or campaign abilities.

### Air
Optional future expansion. Not required for base game.

## Terrain modifiers

### Mountain Road
- +movement for Ferrum heavy units;
- normal speed for infantry;
- cavalry penalty.

### Imperial Road
- +movement for Aurelia formations;
- improves reinforcement timing;
- can connect Authority economy.

### Marsh / Delta Mud
- slows heavy units;
- benefits Thalassia light units;
- can hide ambush points.

### Shallow Water
- passable by infantry with slow;
- Water Weavers gain bonus;
- siege takes major penalty.

### Deep Water
- naval only;
- transports required.

### Corrupted Ground
- applies corruption exposure;
- Ashlands units gain regen;
- purification can temporarily neutralize.

## Chokepoint rules

- Every major chokepoint should have at least one alternate route.
- Gates can block movement but must be interactable.
- Siege should be able to break static chokepoints with support.
- Heroes should not get permanently stuck in narrow paths.

## Formation pathing

Aurelia depends on formation discipline. Formation movement should use soft grouping, not rigid blocks that fail in narrow terrain.

Ferrum heavy formations can compress more tightly but move slower.

Thalassia units should spread naturally and benefit from open/fluid paths.

## Naval pathing

Ships need:

- collision radius by size;
- turning rate;
- shallow/deep water restrictions;
- docking behavior;
- port entrance priority;
- convoy mode.

## Terrain destruction

Optional but recommended:

- bridges can be damaged;
- barricades can be destroyed;
- ice sheets can crack;
- corrupted growths can block routes;
- gates can be captured or broken.

## Debug requirements

Developers need visualization overlays for:

- movement layer;
- unit radius;
- blocked cells;
- naval depth;
- corruption zones;
- road speed modifiers;
- objective capture radius.
