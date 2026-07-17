# First Asset Test — Medieval Barrel

## De ce acest asset

Butoiul este suficient de simplu pentru un începător, dar permite testarea întregului pipeline: concept, modelare, UV, textură, export, import și prefab.

## Rezultat final

Un prefab Unity numit:

`PRP_Neutral_Barrel_A`

## Specificație vizuală

- butoi medieval simplu;
- corp din scânduri de lemn;
- trei cercuri metalice;
- siluetă ușor bombată;
- stil dark fantasy discret;
- uzură moderată, fără ornamente mici;
- lizibil din camera RTS.

## Dimensiuni

- înălțime: aproximativ 1 metru;
- diametru maxim: aproximativ 0.7 metri;
- pivot: centrul bazei.

## Buget inițial

- aproximativ 300–1000 triunghiuri;
- un singur material;
- o textură de 512×512 sau 1024×1024;
- collider simplu de tip Capsule sau Mesh simplificat.

## Pași Blender

1. Creează un Cylinder cu 12–16 laturi.
2. Scalează-l la dimensiunea aproximativă.
3. Adaugă bucle orizontale.
4. Lărgește zona centrală pentru forma bombată.
5. Modelează cercurile metalice ca piese simple sau parte din mesh.
6. Aplică transformările.
7. Verifică normalele.
8. Setează pivotul la baza obiectului.
9. Creează UV-urile.
10. Aplică materialul de test.

## Textură

Zone necesare:

- lemn principal;
- variații între scânduri;
- metal întunecat;
- muchii ușor uzate;
- pete discrete de murdărie.

## Export

Fișier:

`PRP_Neutral_Barrel_A.fbx`

Înainte de export:

- aplică Rotation și Scale;
- elimină obiectele inutile;
- verifică pivotul;
- exportă doar asset-ul.

## Import Unity

1. Importă FBX-ul în folderul de modele.
2. Importă texturile.
3. Creează materialul.
4. Aplică materialul pe model.
5. Adaugă collider.
6. Creează prefab-ul.
7. Pune prefab-ul într-o scenă de test.
8. Privește-l din camera RTS.

## Checklist final

- [ ] Scara este corectă.
- [ ] Butoiul stă pe teren.
- [ ] Pivotul este la bază.
- [ ] Materialele sunt corecte.
- [ ] Nu există fețe negre sau normale inversate.
- [ ] Collider-ul funcționează.
- [ ] Prefab-ul poate fi duplicat.
- [ ] Asset-ul este lizibil de la distanță.

## Criteriu de succes

Testul este reușit când butoiul poate fi tras în scenă ca prefab și arată corect fără alte ajustări manuale.