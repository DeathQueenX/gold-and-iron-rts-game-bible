# Repository Consistency Audit

Audit realizat pentru identificarea dublurilor, contradicțiilor și surselor de date ambigue.

## Probleme confirmate și corectate

1. **Două surse de date paralele**
   - `10_Data/` și `Database/` conțineau aceleași tipuri de entități cu valori diferite.
   - Rezolvare: `Database/` este sursa canonică; `10_Data/` este marcat ca legacy/prototip.

2. **Clădiri cu statistici diferite**
   - Exemple: Iron Hall, Solar Forum și Tide Hall aveau HP, armor și costuri diferite între fișiere.
   - Rezolvare: valorile din `Database/Buildings/Buildings_Master.csv` au prioritate.

3. **Unități duplicate**
   - Unitățile de bază apăreau atât în `10_Data/units.csv`, cât și în `Database/Units/Units_Master.csv`.
   - Rezolvare: master database este canonic; fișierul vechi rămâne doar pentru migrarea unităților încă neincluse.

4. **Aria Vance — facțiune contradictorie**
   - Apărea ca `Aurelia`, respectiv `Aurelia/Ferrum Alliance`.
   - Rezolvare: `PrimaryFaction = Aurelia`, `Affiliation = Ferrum Alliance`.

5. **Solar Edict clasificat greșit**
   - În documentul lui Solon era abilitate normală, iar în baza de date era Ultimate.
   - Rezolvare: Solar Edict este Active; `Siphon of the Twin Suns` este Ultimate.

6. **ArmorTypes contrazicea matricea de damage**
   - Light era marcat ca rezistent la Pierce, deși matricea aplica 120% Pierce damage.
   - `Structure` și `Fortified` erau folosite pentru aceeași categorie.
   - Rezolvare: matricea și tipurile au fost aliniate; termenul canonic este `Fortified`.

7. **Ashlands tratat simultan ca facțiune standard și PvE**
   - Rezolvare: Ashlands este `PlayableAtLaunch = No`, cu rol de facțiune de criză/PvE.

8. **Salt lipsea din master resource list**
   - Unitățile Thalassia aveau cost în Salt, dar resursa nu exista în `Resources_Master.csv`.
   - Rezolvare: Salt a fost adăugat.

9. **Resurse economice și meta-resurse amestecate**
   - Authority, Forge Heat, Tide Favor și Corruption apăreau în documentație fără o clasificare comună.
   - Rezolvare: au fost separate în `Database/Resources/Meta_Resources.csv`.

## Dubluri intenționate rămase

- Documentele Markdown descriu designul și intenția.
- CSV/JSON din `Database/` stabilesc valorile curente.
- Fișierele din `10_Data/` rămân temporar pentru migrarea conținutului care nu a ajuns încă în master database.

## Convenții canonice

- Ferrum, Aurelia și Thalassia sunt facțiunile jucabile principale.
- Ashlands este facțiune PvE/criză la lansare.
- Helios este centrul/capitala Aurelia, nu o facțiune separată.
- Solar Court este instituție/afiliere Aurelia.
- Sea Kingdom este denumire politică/afiliere Thalassia.
- Aethelgard este centru politic/port major Thalassia.
- Coin este moneda universală canonică.
- Fortified este tipul de armor pentru clădiri.

## Probleme încă deschise

1. Valorile master pentru clădiri sunt mult mai mari decât prototipurile vechi; necesită playtesting, nu reconciliere textuală.
2. `Food` și `Wood` sunt marcate provisional până la stabilirea economiei finale.
3. ID-urile scurte (`FER001`) și ID-urile semantice (`ferrum_iron_guard`) coexistă. Pentru Unity este recomandată alegerea unei singure convenții înainte de import.
4. Unele entități există doar în fișierele legacy și trebuie migrate gradual în `Database/`.
5. Tech tree-urile descriptive sunt mai complete decât `Tech_Master.csv`; master-ul trebuie extins fără a importa automat toate valorile neverificate.
