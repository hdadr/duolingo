# Duolingo – magyar nyelvű magyarázó tanulási rendszer

Ez a privát repó két Duolingo-kurzushoz tartalmaz magyar nyelvű magyarázó tananyagot, tanulási térképet és új ChatGPT-beszélgetésben használható indító promptot.

**A Duolingo az elsődleges tanulófelület.** A ChatGPT nem helyettesíti a szókincs-, hallásértés- és mondatgyakorlást. A feladata, hogy megmagyarázza a nyelvtani és nyelvhasználati logikát, különösen a magyar és a tanult nyelv közötti eltéréseket, majd ellenőrizze a megértést.

## Kezdés új ChatGPT-beszélgetésben

1. Nyisd meg a [START-HERE.md](START-HERE.md) útmutatót.
2. Válaszd ki a megfelelő kurzust.
3. Másold be a kurzushoz tartozó teljes indító promptot.
4. A ChatGPT olvassa be a szükséges tantervi fájlokat, és kérdezze meg az aktuális Duolingo-helyzetedet.

A privát GitHub-repóhoz az új chatnek hozzáférés kell a csatlakoztatott GitHub-integráción keresztül. Ha nem látja a fájlokat, töltsd fel a repó ZIP-archívumát. A privát URL önmagában nem biztosít hozzáférést.

## Támogatott kurzusok

| Kulcs | Kurzus | Duolingo-azonosító | Magyarázat |
|---|---|---|---|
| `es-en` | Spanyol angolból | `DUOLINGO_ES_EN` | Magyar |
| `en-hu` | Angol magyarból | `DUOLINGO_EN_HU` | Magyar |

### Spanyol angolból
- [Indító prompt](prompts/DUOLINGO-HU-CHATGPT-PROMPT.md)
- [Spanyol kurzusadatok](courses/es-en/course.json)
- [Spanyol A1–B2 tanulási térkép – Markdown](curricula/espanol-a1-b2-tanulasi-terkep.md)
- [Spanyol A1–B2 tanulási térkép – JSON](curricula/espanol-a1-b2-tanulasi-terkep.json)
- [Nyílt adatok értékelése](research/open-data-coverage-assessment-2026-11-05.md)
- [Spanyol modulok keresztmegfeleltetése](research/es-en-public-module-description-crosswalk.md)

### Angol magyarból
- [Indító prompt](prompts/DUOLINGO-EN-HU-CHATGPT-PROMPT.md)
- [Angol kurzusadatok – 1005 egységes útvonal](courses/en-hu/course.json)
- [Angol A1–B2 tanulási térkép – Markdown](curricula/angol-a1-b2-tanulasi-terkep.md)
- [Angol A1–B2 tanulási térkép – JSON](curricula/angol-a1-b2-tanulasi-terkep.json)
- [Nyílt adatok lefedettségi értékelése](research/en-hu-open-data-coverage-assessment-2026-11-05.md)
- [Duolingo útvonal és nyelvtani keresztmegfeleltetés](research/en-hu-course-path-and-grammar-crosswalk.md)

## Közös tanítási protokoll

- [Tanítási és megértés-ellenőrzési protokoll](LEARNING-PROTOCOL.md)
- [Kurzusnyilvántartás](courses/registry.json)
- [Haladási adatok JSON-sémája](schemas/progress.schema.json)

## Tanulási módszer

1. **Duolingo-first:** a tanuló a Duolingóban gyakorolja a szókincset, mondatokat, hallásértést és ismétlést.
2. **Magyarázat, nem duplikáció:** a ChatGPT a nyelvtan és a nyelvhasználat logikáját fejti ki.
3. **Aktuális egységhez igazodás:** a magyarázat a felhasználó tényleges moduljához, egységéhez és témájához kapcsolódik.
4. **Megértés-ellenőrzés:** minden fontos új nyelvtani témát rövid, interaktív ellenőrzés követ.
5. **Fokozatos haladás:** ha a tanuló nem érti a szabályt, a ChatGPT más példával és más magyarázattal segít.
6. **A tanuló dönt:** az elsajátítás után felajánlja a következő egység magyarázatát, de nem kezdi el automatikusan.

## Forráskritika

A Duolingo Data közösségi kurzustérképei az útvonal és az egységtémák azonosítására használhatók, de nem hivatalos Duolingo-exportok. A CEFR, az English Grammar Profile, a British Council és az Instituto Cervantes referenciái a nyelvtani mélységet segítik; nem bizonyítják, hogy egy adott szabály biztosan egy adott Duolingo-egységben jelenik meg.

A magyar–angol kontrasztív forrásokat azért használjuk, hogy az angol nyelv magyar anyanyelvűek számára különösen nehéz szerkezeteit érthetően magyarázzuk.

A repó saját magyar nyelvű magyarázó tanterveket, tanulási útvonalakat, előfeltételeket és pedagógiai következtetéseket tárol. Nem a Duolingo teljes leckeszövegének vagy feladatsorainak másolása a cél.

**Utolsó frissítés:** 2026-11-05.
