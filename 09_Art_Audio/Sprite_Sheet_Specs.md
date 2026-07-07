# Sprite Sheet Specs

## Purpose

Acest document definește cerințele pentru sprite sheets 2D, utile pentru prototip, concept art și producție.

## Global unit sprite standard

### Recommended base sizes

- Worker: 128x128 px per frame
- Infantry: 160x160 px per frame
- Heavy infantry: 192x192 px per frame
- Hero: 256x256 px per frame
- Siege: 256x256 or 384x384 px per frame
- Boss: 512x512 px per frame

## Directions

Minimum RTS production set:

- 8 directions: N, NE, E, SE, S, SW, W, NW

Prototype set:

- 4 directions: N, E, S, W

## Animation states

### Worker
- idle;
- walk;
- gather;
- carry;
- build;
- repair;
- death.

### Infantry
- idle;
- walk;
- attack 1;
- attack 2;
- block/hit;
- ability;
- death.

### Ranged
- idle;
- walk;
- aim;
- fire;
- reload;
- hit;
- death.

### Caster
- idle;
- walk;
- cast small;
- cast channel;
- cast ultimate;
- hit;
- death.

### Hero
- idle;
- walk;
- attack;
- ability 1;
- ability 2;
- ability 3;
- ultimate;
- wounded;
- death;
- victory pose.

## Faction silhouette rules

### Ferrum
- square armor shapes;
- heavy boots;
- large shoulder plates;
- visible metal weight;
- orange forge glow for elite units.

### Aurelia
- vertical posture;
- clean capes;
- spear and sun symbols;
- gold-white readable silhouettes;
- crystal highlights.

### Thalassia
- curved armor;
- lighter stance;
- flowing cloth;
- tridents and nets;
- blue/coral highlights.

### Ashlands
- broken silhouettes;
- asymmetry;
- glowing cracks;
- rusted protrusions;
- unstable idle animation.

## Export naming convention

`faction_unit_animation_direction_frame.png`

Examples:

- `ferrum_iron_guard_walk_ne_001.png`
- `aurelia_light_weaver_cast_s_004.png`
- `thalassia_tide_galleon_attack_e_003.png`
- `ashlands_rust_beast_idle_sw_002.png`

## Atlas packing

Recommended:

- one atlas per faction per class;
- one atlas for each hero;
- boss atlases separate;
- VFX atlases separate.
