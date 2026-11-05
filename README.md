# Duolingo – magyar nyelvű magyarázó tanulási rendszer

Ez a privát repó egy olyan ChatGPT-kiegészítőt tartalmaz, amely a Duolingo tanulási folyamatát támogatja magyar nyelvű nyelvtani és nyelvhasználati magyarázatokkal.

**A Duolingo az elsődleges tanulófelület.** A ChatGPT nem helyettesíti a Duolingo szókincs- és mondatgyakorlását, hanem segít megérteni, hogy mit, miért és hogyan tanul a felhasználó.

## Kezdés új ChatGPT-chatben

1. Olvasd el a [START-HERE.md](START-HERE.md) útmutatót.
2. Új beszélgetésben használd a [teljes kezdő promptot](prompts/DUOLINGO-HU-CHATGPT-PROMPT.md).
3. Kövesd a [tanítási és megértés-ellenőrzési protokollt](LEARNING-PROTOCOL.md).

A privát GitHub-repóhoz az új chatnek hozzáférés kell a csatlakoztatott GitHub-integráción keresztül. Ha nem tudja olvasni, a repó ZIP-archívumát kell feltölteni. A privát URL önmagában nem biztosít hozzáférést.

## Támogatott kurzusok

| Kulcs | Kurzus | Duolingo-azonosító | Magyarázat nyelve |
|---|---|---|---|
| `es-en` | Spanyol angolból | `DUOLINGO_ES_EN` | Magyar |
| `en-hu` | Angol magyarból | `DUOLINGO_EN_HU` | Magyar |

A két kurzus külön kezelendő. Az elsődleges aktuális tanulási irány a spanyol angolból. Az angol magyarból kurzus tantervi adatai előkészítve vannak, de a spanyolhoz hasonló részletességű, teljes A1–B2 magyarázó térkép még nincs kidolgozva.

## Fontos fájlok

### Új chat indítása
- [START-HERE.md](START-HERE.md) – lépésről lépésre indítás.
- [Kezdő ChatGPT-prompt](prompts/DUOLINGO-HU-CHATGPT-PROMPT.md) – teljes, bemásolható szerep- és működési prompt.
- [LEARNING-PROTOCOL.md](LEARNING-PROTOCOL.md) – tanítási folyamat, megértés-ellenőrzés, hibajavítás és továbbhaladás.

### Kurzusok és tantervek
- [Kurzusnyilvántartás](courses/registry.json).
- [Spanyol angolból – kurzusadatok](courses/es-en/course.json).
- [Angol magyarból – kurzusadatok](courses/en-hu/course.json).
- [Spanyol A1–B2 tanulási térkép – Markdown](curricula/espanol-a1-b2-tanulasi-terkep.md).
- [Spanyol A1–B2 tanulási térkép – JSON](curricula/espanol-a1-b2-tanulasi-terkep.json).

### Kutatás és források
- [Nyílt adatok lefedettségi értékelése](research/open-data-coverage-assessment-2026-11-05.md).
- [Spanyol modul-leírások és tematikus megfeleltetés](research/es-en-public-module-description-crosswalk.md).
- [APK és API vizsgálat](sources/apk-extraction-findings.md).
- [Adatforrások és tananyag-feltárási módszer](sources/lesson-data-acquisition.md).
- [API-hozzáférés vizsgálata](sources/api-assessment-2026-11-05.md).

### Haladásnaplók
- [Spanyol haladási sablon](progress/es-en-template.json).
- [Angol haladási sablon](progress/en-hu-template.json).
- [Haladási adatok JSON-sémája](schemas/progress.schema.json).

A haladási sablonok üresek. A felhasználó tényleges pozícióját az új beszélgetésben kell megerősíteni; ne feltételezz régi vagy más kurzushoz tartozó képernyőkép alapján előrehaladást.

## Tanítási alapelvek

1. **Duolingo-first:** a tanuló a szókincset, mondatokat, hallásértést és ismétlést elsősorban a Duolingóban gyakorolja.
2. **Magyarázat, nem duplikáció:** a ChatGPT a nyelvtan és nyelvhasználat logikáját fejti ki, nem másolja a leckéket.
3. **Aktuális egységhez igazodás:** a magyarázat a felhasználó tényleges szekciójához, egységéhez és témájához kapcsolódik.
4. **Bizonyosság jelölése:** különbséget kell tenni a Guidebookkal/feladatpéldával igazolt, a CEFR-tanterv alapján releváns és a pusztán valószínű témák között.
5. **Megértés ellenőrzése:** minden fontos új nyelvtani téma után rövid, interaktív ellenőrzés következik. Ez nem szókincsteszt.
6. **Fokozatos haladás:** ha a tanuló még nem érti a szabályt, más magyarázattal és új példával kell segíteni.
7. **A tanuló dönt a továbbhaladásról:** amikor a magyarázó rész stabilan megy, a ChatGPT felajánlja a következő Duolingo-egységhez kapcsolódó magyarázatot, de nem kezd bele automatikusan.

## Forráskritika

A Duolingo Data közösségi kurzustérképe a szekciók és témák azonosítására használható, de nem hivatalos Duolingo-tanterv és nem bizonyítja az adott egység pontos nyelvtani célját. Az Instituto Cervantes Plan Curricular és AVE Global nyelvtani/tematikus referenciát ad; ezek sem a Duolingo hivatalos egységlistái.

A repó saját, magyar nyelvű tanulási térképet, magyarázatokat, előfeltételeket és pedagógiai következtetéseket tárol. Nem célja a Duolingo teljes leckeszövegének vagy feladatsorainak másolása.

**Utolsó dokumentációs frissítés:** 2026-11-05.
