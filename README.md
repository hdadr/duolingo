# Duolingo – magyar nyelvű magyarázó tanulási rendszer

Ez a privát repó két Duolingo-kurzushoz tartalmaz magyar nyelvű magyarázó tananyagot, tanulási térképet és új ChatGPT-beszélgetésben használható indító promptot.

**A Duolingo az elsődleges tanulófelület.** A ChatGPT nem helyettesíti a szókincs-, hallásértés- és mondatgyakorlást. A feladata, hogy megmagyarázza a nyelvtani és nyelvhasználati logikát, különösen a magyar és a tanult nyelv közötti eltéréseket, majd ellenőrizze a megértést.

## Kezdés új ChatGPT-beszélgetésben

1. Nyisd meg a [START-HERE.md](START-HERE.md) útmutatót.
2. Válaszd ki a megfelelő kurzust.
3. Másold be a kurzushoz tartozó teljes indító promptot.
4. A ChatGPT olvassa be a szükséges kis kontextuscsomagot, és erősítse meg az állapotkártyában szereplő pozíciót.

A privát GitHub-repóhoz az új chatnek hozzáférés kell a csatlakoztatott GitHub-integráción keresztül. Ha a fájlok nem érhetők el, az állapotkártya és az aktuális modulblokk bemásolható.

## Támogatott kurzusok

| Kulcs | Kurzus | Duolingo-azonosító | Magyarázat |
|---|---|---|---|
| `es-en` | Spanyol angolból | `DUOLINGO_ES_EN` | Magyar |
| `en-hu` | Angol magyarból | `DUOLINGO_EN_HU` | Magyar |

### Spanyol angolból
- [Indító prompt](prompts/DUOLINGO-HU-CHATGPT-PROMPT.md)
- [Moduljegyzék](learning-modules/es-en/index.json)
- [Állapotkártya](progress/es-en-state-card.json)
- [Spanyol kurzusadatok](courses/es-en/course.json)
- [Teljes A1–B2 tanulási térkép](curricula/espanol-a1-b2-tanulasi-terkep.md) – referencia, nem alapértelmezett beolvasás

### Angol magyarból
- [Indító prompt](prompts/DUOLINGO-EN-HU-CHATGPT-PROMPT.md)
- [Moduljegyzék](learning-modules/en-hu/index.json)
- [Állapotkártya](progress/en-hu-state-card.json)
- [Angol kurzusadatok](courses/en-hu/course.json)
- [Teljes A1–B2 tanulási térkép](curricula/angol-a1-b2-tanulasi-terkep.md) – referencia, nem alapértelmezett beolvasás

## Kontextustakarékos tanulási rendszer

- [Tanítási, modulhatár- és állapotkártya-protokoll](LEARNING-PROTOCOL.md)
- [Modulbankok és pontos beolvasási szabályok](learning-modules/README.md)
- [Kurzusnyilvántartás](courses/registry.json)
- [Állapotkártya JSON-sémája](schemas/state-card.schema.json)

Az új beszélgetés csak a kiválasztott kurzus moduljegyzékét, állapotkártyáját és az aktuális modul pontos sorait olvassa be. A teljes A1–B2 térkép, a másik kurzus és a kutatási háttér nem része az alapértelmezett kontextusnak. A megértés-ellenőrzés alapértelmezésként egyenként feltett feleletválasztós kérdésekkel működik; a tanulónak elég az A/B/C/D opciót kiválasztania.

## Tanulási módszer

1. **Duolingo-first:** a tanuló a Duolingóban gyakorolja a szókincset, mondatokat, hallásértést és ismétlést.
2. **Magyarázat, nem duplikáció:** a ChatGPT a nyelvtan és a nyelvhasználat logikáját fejti ki.
3. **Aktuális egységhez igazodás:** a magyarázat a felhasználó tényleges moduljához, egységéhez és témájához kapcsolódik.
4. **Megértés-ellenőrzés:** minden fontos új nyelvtani témát rövid, interaktív ellenőrzés követ.
5. **Fokozatos haladás:** ha a tanuló nem érti a szabályt, a ChatGPT más példával és más magyarázattal segít.
6. **Tanulási folytonosság:** új chatben a rövid állapotkártya és az aktuális modul pontos blokkja biztosítja a folytatást.

## Forráskritika

A Duolingo Data közösségi kurzustérképei az útvonal és az egységtémák azonosítására használhatók, de nem hivatalos Duolingo-exportok. A CEFR, az English Grammar Profile, a British Council és az Instituto Cervantes referenciái a nyelvtani mélységet segítik; nem bizonyítják, hogy egy adott szabály biztosan egy adott Duolingo-egységben jelenik meg.

A repó saját magyar nyelvű magyarázó tanterveket, tanulási útvonalakat, előfeltételeket és pedagógiai következtetéseket tárol. Nem a Duolingo teljes leckeszövegének vagy feladatsorainak másolása a cél.

**Utolsó frissítés:** 2026-11-05.
