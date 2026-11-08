# Modulbankok – takarékos kontextusbetöltés

## Szerkezet

- `es-hu/`: spanyol magyarból; 32 teljes nyelvtani modul.
- `en-hu/`: angol magyarból; 35 teljes nyelvtani modul.
- Kurzusonként négy szintfájl van (A1, A2, B1, B2); a pontos modulhatárokat az adott kurzus `index.json` fájlja tartalmazza.

## Beolvasási szabály

1. Először csak a kiválasztott kurzus `index.json` fájlját olvasd be.
2. Azonosítsd az aktuális Duolingo-egységhez legjobban illeszkedő modult, és olvasd el a `duolingo_grammar_evidence`, `evidence_basis`, `evidence_note` mezőket.
3. A GitHub-integrációval kizárólag az indexben megadott `path`, `start_line` és `end_line` tartományt olvasd be. A sorhatárok zártak.
4. Előfeltételt csak akkor tölts be, ha a tanuló válasza vagy az állapotkártya bizonytalanságot jelez; akkor is csak a szükséges modul pontos sorait olvasd be.
5. Ne olvasd be alapértelmezésként a teljes tantervi térképet, a teljes szintfájlt, a másik kurzust vagy a teljes kutatási hátteret.

### A kurzusillesztés bizonyossága

Az index `duolingo_grammar_evidence` mezőjének értékei:
- `explicit`: a nyilvános kurzusadat megnevezi a nyelvtani elemet;
- `observed`: a nyelvtani minta egy tényleges egységpéldában megfigyelhető, de nincs hivatalos célként megnevezve;
- `inferred`: a téma/referencia alapján valószínű kapcsolat, nem bizonyított tantervi tény;
- `reference_only`: CEFR- vagy egyéb nyelvtani referencia, közvetlen egységszintű bizonyíték nélkül;
- `unknown`: nincs elegendő adat.

Az `evidence_basis` őrzi az eredeti adatforrás címkéjét, az `evidence_note` pedig röviden megmagyarázza a korlátait. Ez a címke a Duolingo-egység és a nyelvtani modul kapcsolatát jelzi, **nem a tanuló tudását**.

## Pedagógiai határ

Egy `A1-01` típusú modul teljes, önálló tanulási egység. Nem szabad tokenkeret vagy fájlméret miatt kettévágni. Ha több egymásra épülő altémát tartalmaz, azok csak saját, teljes fogalmi határuknál dolgozhatók fel külön munkamenetben. Magyarázatot, példasort, összehasonlítást vagy megértés-ellenőrzést soha ne szakíts félbe csak a chatváltás miatt.

A modulbankok az eredeti tanulási térképek modulblokkjait őrzik meg; a tartalom sorrendje és a nyelvtani összefüggések nem lettek önkényesen átalakítva.

## Külön kezelt tanulási előrehaladás

A Duolingo-pozíciót csak a tanuló aktuális közlése vagy képernyőképe frissítheti. A nyelvtani `mastery` csak a ChatGPT-ben megfigyelt tanulói teljesítmény alapján változhat. Ha a tanuló az alkalmazásban továbbhaladt, de egy szükséges előfeltétel nem stabil, az asszisztens rövid, célzott ismétlést végez, majd visszatér az aktuális egységhez. Nem kezdi újra a teljes korábbi modult vagy a kurzust.

## Megértés-ellenőrzés

A fontos új nyelvtani szabályok ellenőrzése négylépcsős: felismerés, a logika megindoklása, irányított alkalmazás, majd új helyzetű transzfer. A negyedik lépésben az asszisztens mindig más alanyt és más igét használ, mint a korábbi példákban; egyszerre csak egy kérdést tesz fel, és a tanuló válasza alapján adaptálja a következőt. A kártya megőrzi, hogy a tanuló a négylépcsős ellenőrzés mely részénél tart, valamint a függőben lévő feleletválasztós kérdés pontos opcióit. A tanuló egy betűvel válaszolhat; a helyes opciót a kártya nem tárolja.

## Hibadiagnosztikai katalógus

A `error-pattern-catalog.md` nem kötelező indítófájl. Csak akkor olvasd be, ha egy nyelvtani hiba visszatér, az oka bizonytalan, vagy célzott javító stratégiára van szükség. Az első hiba csak jelölt; visszatérő mintához két független mondat/feladathelyzet kell.
