# Duolingo – magyar nyelvű magyarázó tanulási rendszer

Ez a privát repó két Duolingo-kurzushoz tartalmaz magyar nyelvű magyarázó tananyagot, tanulási térképet és ChatGPT-projektekhez készített tanulási csomagot.

**A Duolingo az elsődleges tanulófelület.** A ChatGPT nem helyettesíti a szókincs-, hallásértés- és mondatgyakorlást. A feladata, hogy megmagyarázza a nyelvtani és nyelvhasználati logikát, különösen a magyar és a tanult nyelv közötti eltéréseket, majd ellenőrizze a megértést.

## Ajánlott kezdés Free ChatGPT-ben

A [Free ChatGPT projektcsomag](free-chatgpt/README.md) az ajánlott út. Hozz létre két külön projektet (spanyol és angol), és mindegyikbe a közös rövid protokollt, a megfelelő kurzus-routert és egy üres v5 állapotkártya-sablont tölts fel. A projektutasításokat külön, a Project Instructions mezőbe másold.

A rendszer mindkét kurzusnál ugyanazt a tanítási, tudáskövetési és folytonossági módszert használja. Alapértelmezésben a projekt korábbi beszélgetéseiből folytat; a v5 JSON-állapotkártya opcionális tartalék, nem napi adminisztráció.

## Haladó / közvetlen GitHub-hozzáférésű használat

Ha olyan ChatGPT-felületet használsz, amely ténylegesen hozzáfér a privát repóhoz, a régi, részletes indító promptok továbbra is elérhetők. A Free projektmódban az aktuális modult csak a router pontos sorai alapján másold be, ha a chat nem tudja a GitHub-fájlt elérni.

## Kezdés új ChatGPT-projektben

1. Nyisd meg a [START-HERE.md](START-HERE.md) útmutatót.
2. Válaszd ki a megfelelő kurzust.
3. Hozd létre a projektet, töltsd fel a három szükséges fájlt, és illeszd be a projektutasításokat.
4. A tanuló egyszerűen a „Kezdjük!” vagy „Folytassuk!” üzenettel indulhat. A ChatGPT a projektben elérhető előzmények alapján próbálja visszaállítani a tanulási pontot; csak hiányzó adat esetén kérdez.

## Támogatott kurzusok

| Kulcs | Kurzus | Duolingo-azonosító | Magyarázat |
|---|---|---|---|
| `es-hu` | Spanyol magyarból | `DUOLINGO_ES_HU` | Magyar |
| `en-hu` | Angol magyarból | `DUOLINGO_EN_HU` | Magyar |

### Spanyol magyarból
- [Indító prompt](prompts/DUOLINGO-HU-ES-CHATGPT-PROMPT.md)
- [Moduljegyzék](learning-modules/es-hu/index.json)
- [Állapotkártya-sablon](progress/es-hu-state-card.json)
- [Spanyol kurzusadatok](courses/es-hu/course.json)
- [Teljes A1–B2 tanulási térkép](curricula/espanol-a1-b2-tanulasi-terkep.md) – referencia, nem alapértelmezett beolvasás

### Angol magyarból
- [Indító prompt](prompts/DUOLINGO-EN-HU-CHATGPT-PROMPT.md)
- [Moduljegyzék](learning-modules/en-hu/index.json)
- [Állapotkártya-sablon](progress/en-hu-state-card.json)
- [Angol kurzusadatok](courses/en-hu/course.json)
- [Teljes A1–B2 tanulási térkép](curricula/angol-a1-b2-tanulasi-terkep.md) – referencia, nem alapértelmezett beolvasás

## Kontextustakarékos tanulási rendszer

- [Tanítási, modulhatár- és állapotkártya-protokoll](LEARNING-PROTOCOL.md)
- [Modulbankok és pontos beolvasási szabályok](learning-modules/README.md)
- [Kurzusnyilvántartás](courses/registry.json)
- [Állapotkártya JSON-sémája](schemas/state-card.schema.json)
- [Free projekt-router séma](schemas/free-course-router.schema.json)
- [Tantervi bizonyítékok indexsémája](schemas/curriculum-index.schema.json)

Az új beszélgetés csak a kiválasztott kurzus routerét, állapotkártya-sablonját és az aktuális modul pontos sorait használja. A teljes A1–B2 térkép, a másik kurzus és a kutatási háttér nem része az alapértelmezett kontextusnak. A megértés-ellenőrzés feleletválasztós; a tanulónak elég az A/B/C/D opciót kiválasztania.

## Tanulási módszer

1. **Duolingo-first:** a tanuló a Duolingóban gyakorolja a szókincset, mondatokat, hallásértést és ismétlést.
2. **Magyarázat, nem duplikáció:** a ChatGPT a nyelvtan és a nyelvhasználat logikáját fejti ki.
3. **Aktuális egységhez igazodás:** a magyarázat a felhasználó tényleges moduljához, egységéhez és témájához kapcsolódik.
4. **Megértés-ellenőrzés:** minden fontos új nyelvtani témát rövid, interaktív ellenőrzés követ.
5. **Fokozatos haladás:** ha a tanuló nem érti a szabályt, a ChatGPT más példával és más magyarázattal segít.
6. **Projektalapú folytonosság:** a tanuló alapértelmezésben ugyanazt a projektbeszélgetést folytatja; új chat esetén a projektmemória és a korábbi beszélgetések segíthetik a folytatást.
7. **Opcionális állapotkártya:** a teljes v5 JSON csak kérésre, külön mentéshez vagy bizonytalan chatváltásnál szükséges.
8. **Külön haladási tengelyek:** a Duolingo-egységben való előrehaladás nem emeli automatikusan a nyelvtani tudás státuszát; szükség esetén csak a hiányzó előfeltétel kerül rövid ismétlésre.

## Forráskritika

A Duolingo Data közösségi kurzustérképei az útvonal és az egységtémák azonosítására használhatók, de nem hivatalos Duolingo-exportok. A CEFR, az English Grammar Profile, a British Council és az Instituto Cervantes referenciái a nyelvtani mélységet segítik; nem bizonyítják, hogy egy adott szabály biztosan egy adott Duolingo-egységben jelenik meg.

A repó saját magyar nyelvű magyarázó tanterveket, tanulási útvonalakat, előfeltételeket és pedagógiai következtetéseket tárol. Nem a Duolingo teljes leckeszövegének vagy feladatsorainak másolása a cél.

**Utolsó frissítés:** 2026-11-05.
