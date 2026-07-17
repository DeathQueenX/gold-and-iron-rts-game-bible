# Graphics Production Pipeline

Acest document descrie fluxul standard pentru fiecare asset grafic din Gold and Iron RTS.

## 1. Definire

Pentru fiecare asset se stabilește:

- rolul în joc;
- facțiunea sau zona de apartenență;
- dimensiunea în raport cu unitățile;
- importanța vizuală;
- starea finală necesară în Unity.

## 2. Concept

Se creează referințe și una sau mai multe variante vizuale. Se aprobă o singură direcție înainte de modelare.

## 3. Modelare

Asset-ul este modelat în Blender la scară reală, cu pivotul și orientarea corectă.

## 4. UV și texturi

Se creează UV-urile și texturile necesare. Pentru primul vertical slice se preferă materiale simple și reutilizabile.

## 5. Rig și animație

Se aplică numai asset-urilor care trebuie animate. Props-urile statice sar peste această etapă.

## 6. Export

Format recomandat: FBX pentru modele și PNG/TGA pentru texturi.

## 7. Import în Unity

Se verifică:

- scara;
- orientarea;
- materialele;
- collider-ul;
- pivotul;
- umbrele;
- performanța.

## 8. Prefab

Asset-ul final devine prefab și primește nume conform convenției proiectului.

## 9. QA

Asset-ul este verificat din camera RTS, nu doar de aproape.

## 10. Stări de producție

- Planned
- Reference
- Concept
- Modeling
- Texturing
- Rigging
- Animation
- Unity Integration
- Review
- Finished

## Regulă principală

Nu se începe producția unui volum mare de asset-uri până când primul vertical slice nu confirmă stilul, scara și pipeline-ul.