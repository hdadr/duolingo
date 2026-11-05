# Modulbankok – takarékos kontextusbetöltés

## Szerkezet

- `es-en/`: spanyol angolból; 32 teljes nyelvtani modul.
- `en-hu/`: angol magyarból; 35 teljes nyelvtani modul.
- Kurzusonként négy szintfájl van (A1, A2, B1, B2); a pontos modulhatárokat az adott kurzus `index.json` fájlja tartalmazza.

## Beolvasási szabály

1. Először csak a kiválasztott kurzus `index.json` fájlját olvasd be.
2. Azonosítsd az aktuális Duolingo-egységhez legjobban illeszkedő modult.
3. A GitHub-integrációval kizárólag az indexben megadott `path`, `start_line` és `end_line` tartományt olvasd be. A sorhatárok zártak.
4. Előfeltételt csak akkor tölts be, ha a tanuló válasza vagy az állapotkártya bizonytalanságot jelez; akkor is csak a szükséges modul pontos sorait olvasd be.
5. Ne olvasd be alapértelmezésként a teljes tantervi térképet, a teljes szintfájlt, a másik kurzust vagy a teljes kutatási hátteret.

## Pedagógiai határ

Egy `A1-01` típusú modul teljes, önálló tanulási egység. Nem szabad tokenkeret vagy fájlméret miatt kettévágni. Ha több egymásra épülő altémát tartalmaz, azok csak saját, teljes fogalmi határuknál dolgozhatók fel külön munkamenetben. Magyarázatot, példasort, összehasonlítást vagy megértés-ellenőrzést soha ne szakíts félbe csak a chatváltás miatt.

A modulbankok az eredeti tanulási térképek modulblokkjait őrzik meg; a tartalom sorrendje és a nyelvtani összefüggések nem lettek önkényesen átalakítva.
