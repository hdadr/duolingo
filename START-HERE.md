# Indítás új ChatGPT-beszélgetésben

Ez a privát repó egy Duolingo-kiegészítő tanulási rendszer magyar nyelvű tudásanyaga. A Duolingo az elsődleges tanulófelület; a ChatGPT a nyelvtani és nyelvhasználati logikát magyarázza, majd rövid interakcióval ellenőrzi a megértést.

## 1. Válaszd ki a tanulási irányt

**Spanyol angolból**
- Kurzusazonosító: `DUOLINGO_ES_EN`
- Magyarázat: magyar
- Prompt: [DUOLINGO-HU-CHATGPT-PROMPT.md](prompts/DUOLINGO-HU-CHATGPT-PROMPT.md)
- Tanterv: [spanyol A1–B2 tanulási térkép](curricula/espanol-a1-b2-tanulasi-terkep.md)

**Angol magyarból**
- Kurzusazonosító: `DUOLINGO_EN_HU`
- Magyarázat: magyar
- Prompt: [DUOLINGO-EN-HU-CHATGPT-PROMPT.md](prompts/DUOLINGO-EN-HU-CHATGPT-PROMPT.md)
- Tanterv: [angol A1–B2 tanulási térkép](curricula/angol-a1-b2-tanulasi-terkep.md)

A két kurzus teljesen külön kezelendő. Mindig a megfelelő promptot és kurzusadatokat használd.

## 2. Indítás új chatben

1. Nyiss új ChatGPT-beszélgetést.
2. Győződj meg arról, hogy a beszélgetés hozzáfér a privát `hdadr/duolingo` GitHub-repóhoz a csatlakoztatott GitHub-integráción keresztül.
3. Másold be a kiválasztott kurzushoz tartozó prompt teljes tartalmát.
4. A ChatGPT olvassa be a promptban felsorolt fájlokat, majd kérdezze meg a tényleges aktuális Duolingo-modult és egységet.

**Ha az új chat nem fér hozzá a privát repóhoz:** ne küldj jelszót, access tokent vagy más belépési adatot. Töltsd fel a repó ZIP-archívumát, vagy csatlakoztasd a GitHubot. A privát repó URL-je önmagában nem garantál hozzáférést.

## 3. Tanulási módszer

- A szókincset, mondatgyakorlást, hallásértést és ismétlést elsősorban a Duolingóban végzed.
- A ChatGPT elmagyarázza, mit és miért tanulsz, hogyan működik a nyelvtan, és miben tér el a magyar nyelvtől.
- Minden fontos új szerkezet után rövid, interaktív megértés-ellenőrzés következik.
- Egy kérdés/forduló ritmusban dolgozunk; a ChatGPT értékeli a választ, és szükség esetén másképp magyaráz.
- Amikor a magyarázó részt stabilan elsajátítottad, a ChatGPT felajánlja a következő Duolingo-egységhez kapcsolódó magyarázatot. Nem lép tovább automatikusan.

## 4. Kötelező háttérfájlok

Közös:
- `README.md`
- `courses/registry.json`
- `LEARNING-PROTOCOL.md`
- `schemas/progress.schema.json`

Spanyol:
- `courses/es-en/course.json`
- `curricula/espanol-a1-b2-tanulasi-terkep.md`
- `curricula/espanol-a1-b2-tanulasi-terkep.json`
- `research/open-data-coverage-assessment-2026-11-05.md`
- `research/es-en-public-module-description-crosswalk.md`

Angol:
- `courses/en-hu/course.json`
- `curricula/angol-a1-b2-tanulasi-terkep.md`
- `curricula/angol-a1-b2-tanulasi-terkep.json`
- `research/en-hu-open-data-coverage-assessment-2026-11-05.md`
- `research/en-hu-course-path-and-grammar-crosswalk.md`

A haladási fájlok sablonok, nem előre feltöltött tanulói előzmények:
- `progress/es-en-template.json`
- `progress/en-hu-template.json`

A GitHub-módosítás sikerét a ChatGPT csak akkor állíthatja, ha a fájlt ténylegesen megírta és visszaellenőrizte.

