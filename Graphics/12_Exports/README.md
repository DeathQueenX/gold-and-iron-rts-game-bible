# 12 — Exports

## Scop

Separarea clară a fișierelor finale pregătite pentru integrarea în Unity de fișierele sursă editabile și documentația de concept.

## Structură planificată

- `Models`
- `Textures`
- `Materials`
- `Animations`
- `Sprites`
- `UI`
- `VFX`
- `Prefabs_Reference`

## Reguli

- aici se păstrează numai fișiere aprobate sau candidate pentru integrare;
- fișierele Blender, PSD, Krita, Inkscape și alte surse editabile rămân în directoarele asset-urilor;
- fiecare export trebuie să respecte standardele din `10_Technical_Standards`;
- numele și versiunile trebuie să permită identificarea rapidă a asset-ului;
- exporturile înlocuite nu trebuie păstrate fără motiv în branch-ul principal;
- fișierele binare mari vor necesita evaluarea folosirii Git LFS.

## Notă

Acest repository este în principal Game Bible. Asset-urile finale foarte mari pot fi mutate ulterior într-un repository separat dedicat proiectului Unity, păstrând aici documentația, preview-urile și legăturile către variantele aprobate.