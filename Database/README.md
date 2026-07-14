# Canonical Game Database

Acest folder este sursa oficială pentru valorile de gameplay și viitorul import în Unity.

## Reguli

1. Fiecare entitate are un ID stabil și unic.
2. Valorile din `Database/` au prioritate față de prototipurile din `10_Data/`.
3. Documentele Markdown descriu intenția; fișierele CSV/JSON din `Database/` stabilesc valorile curente.
4. Resursele recoltate și meta-resursele sunt păstrate separat.
5. Facțiunea principală și afilierea unui personaj sunt câmpuri diferite.
6. Ashlands este o facțiune PvE/criză, nu facțiune jucabilă la lansare.

## Zone principale

- `Units`, `Buildings`, `Heroes`, `Abilities`
- `Tech`, `Upgrades`, `Resources`
- `Damage`, `ArmorTypes`, `DamageTypes`
- `AI`, `Formations`, `Veterancy`, `Projectiles`
