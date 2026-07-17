# Unity and Blender Standards

## Unități și scară

- Blender: Metric, Unit Scale 1.0.
- Unity: 1 unitate = 1 metru.
- Un personaj uman standard: aproximativ 1.8 m.
- Se aplică transformările înainte de export: Rotation și Scale.

## Axe și orientare

- Modelul trebuie să privească înainte în direcția stabilită pentru pipeline.
- La import se verifică orientarea în Unity înainte de crearea prefab-ului.
- Obiectele trebuie exportate fără rotații reziduale neintenționate.

## Pivot

- Unități și props: pivot la baza obiectului, centrat pe suprafața de contact.
- Clădiri: pivot la baza clădirii, într-un punct util pentru plasare pe grid.
- Uși, porți și obiecte articulate: pivotul pe axa reală de rotație.

## Nume

Format general:

`Categorie_Factiune_Nume_Varianta`

Exemple:

- `PRP_Neutral_Barrel_A`
- `UNT_Aurelia_Swordsman_A`
- `BLD_Ferrum_Barracks_T1`
- `VFX_Thalassia_TidalImpact_A`

## Mesh

- Se elimină geometria invizibilă inutilă.
- Se evită duplicatele și fețele interne.
- Normalele trebuie verificate înainte de export.
- Se folosesc margini și volume clare, potrivite camerei RTS.

## Texturi

Set minim recomandat:

- Base Color;
- Normal Map, când aduce valoare;
- Mask Map sau Metallic/Smoothness, după shader;
- Emission pentru magie și elemente speciale.

Dimensiuni orientative:

- props mici: 256–512 px;
- props importante: 512–1024 px;
- unități: 1024–2048 px, în funcție de reutilizare;
- eroi și clădiri principale: până la 2048 px în vertical slice.

## Materiale

- Se reutilizează materialele când este posibil.
- Se evită un material separat pentru fiecare piesă mică.
- Culorile de facțiune trebuie implementate prin zone clare sau măști reutilizabile.

## FBX

La export:

- doar obiectele necesare;
- transformările aplicate;
- fără camere și lumini, dacă nu sunt intenționate;
- animațiile incluse numai când sunt necesare;
- nume curate și stabile.

## Unity Import

Se verifică:

- Scale Factor;
- normals și tangents;
- materialele;
- rig type;
- animation clips;
- mesh compression;
- read/write doar când este necesar.

## Prefab

Fiecare asset final trebuie să aibă:

- mesh;
- materiale;
- collider potrivit;
- setări de umbre;
- layer și tag, dacă sunt necesare;
- variantă prefab clar denumită.

## LOD

LOD-urile se introduc după validarea vertical slice-ului. Prioritatea inițială este stabilirea stilului și a pipeline-ului.

## Control final

Asset-ul se testează într-o scenă Unity cu lumină, teren și cameră apropiate de condițiile reale de joc.