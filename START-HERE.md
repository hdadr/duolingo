# Indítás ChatGPT-ben

## Ajánlott módszer Free csomaghoz

Kövesd a [free-chatgpt/README.md](free-chatgpt/README.md) útmutatót. Hozz létre két külön ChatGPT Projektet: egyet a spanyol, egyet az angol kurzusnak. Mindkét projektbe három fájl kerüljön: az adott kurzus saját rövid protokollja, saját routere és üres v5 állapotkártya-sablonja. A projektutasításokat külön, a Projekt beállításainál illeszd be.

A két projekt ugyanazokat az alapvető tanulási elveket követi, de a protokolljuk, routerük és tanulói előzményeik különállók. A tanulónak nem kell minden alkalommal új indítópromptot vagy állapotkártyát másolnia.

## A projektmemória beállítása

A projekt korábbi beszélgetéseiből való folytatáshoz a ChatGPT memóriafunkcióinak engedélyezve kell lenniük. A **Beállítások → Személyre szabás** részen kapcsold be a mentett memóriák és a csevegési előzmények hivatkozását, ha ezek a kapcsolók megjelennek a fiókodban. A projekt beállításainál válaszd a csak projektmemória módot, ha elérhető; ez segít külön tartani a spanyol és az angol projektet. A megosztott projektek automatikusan csak projektmemóriát használnak.

A memória a korábbi projektbeszélgetésekből segíthet folytatni, de nem garantált, strukturált állapot-adatbázis. Ezért marad meg a másolható v5 állapotkártya tartalékmegoldásként.

## A tanuló napi használata

A tanuló ugyanabban a projektben dolgozzon. Alapesetben ugyanazt a beszélgetést folytassa. Elég ennyit írnia:
- „Kezdjük!”
- „Folytassuk!”
- „Ezt nem értem.”
- „Mára ennyi.”

A ChatGPT a projektben ténylegesen elérhető korábbi beszélgetésekből próbálja visszaállítani a tanulási pontot. Ha már ismert az aktuális pozíció, ne kérdezze meg újra.

## Mikor nyisson új chatet?

Nem kell minden modul után új beszélgetést nyitni. Csak akkor érdemes, ha a régi beszélgetés nagyon hosszúvá vagy nehezen követhetővé vált. Ilyenkor a tanuló ugyanabban a projektben nyisson új chatet, majd írja: „Folytassuk!” A ChatGPT először a projektelőzményekből próbáljon folytatni.

### Opcionális v5 állapotkártya

Ha az új chat nem tudja biztosan visszaállítani a legutóbbi állapotot, vagy a tanuló külön mentést szeretne, a régi chatben kérje: „Kérem az állapotkártyát.” A ChatGPT egy teljes v5 JSON-t ad. Ezt az új chat első üzenetébe lehet másolni ezzel: „Folytassuk ebből.” A projektbe feltöltött `STATE-CARD.json` fájlt nem kell rendszeresen lecserélni.

## Haladó / közvetlen GitHub-hozzáférésű módszer

Az alábbi részletes folyamat akkor hasznos, ha a ChatGPT-felület ténylegesen hozzáfér a privát GitHub-repóhoz. A Free projektmódban az aktuális modul pontos blokkja szükség esetén kézzel másolható be.

# Kurzusazonosítók

**Spanyol magyarból**
- Kurzusazonosító: `DUOLINGO_ES_HU`
- Kulcs: `es-hu`
- Projektutasítás: [free-chatgpt/es-hu/PROJECT-INSTRUCTIONS.md](free-chatgpt/es-hu/PROJECT-INSTRUCTIONS.md)
- Moduljegyzék: [learning-modules/es-hu/index.json](learning-modules/es-hu/index.json)
- Állapotkártya-sablon: [progress/es-hu-state-card.json](progress/es-hu-state-card.json)

**Angol magyarból**
- Kurzusazonosító: `DUOLINGO_EN_HU`
- Kulcs: `en-hu`
- Projektutasítás: [free-chatgpt/en-hu/PROJECT-INSTRUCTIONS.md](free-chatgpt/en-hu/PROJECT-INSTRUCTIONS.md)
- Moduljegyzék: [learning-modules/en-hu/index.json](learning-modules/en-hu/index.json)
- Állapotkártya-sablon: [progress/en-hu-state-card.json](progress/en-hu-state-card.json)

A két kurzus külön projektben, külön tanulói előzményekkel kezelendő.

## A tanítási módszer röviden

- A szókincset, mondatgyakorlást, hallásértést és ismétlést elsősorban a Duolingóban végzi a tanuló.
- A ChatGPT a nyelvtan és a nyelvhasználat logikáját magyarázza.
- Minden fontos új szerkezetnél négylépcsős, feleletválasztós megértés-ellenőrzés következik. Egyszerre egy kérdés jelenik meg; a válaszhoz elég az A/B/C/D opciót kiválasztani. A zárópróba más alannyal és más igével teszteli az önálló alkalmazást.
- A következő egységre csak akkor tér át, amikor a tanuló ténylegesen elért oda, vagy ezt kéri.
- A Duolingo-egység teljesítése nem jelenti automatikusan a kapcsolódó nyelvtani fogalom elsajátítását.
- Ha egy új egységhez szükséges régi alap bizonytalan, csak azt a részt ismétli át röviden, majd visszatér az aktuális egységhez.

## Háttérforrások

A teljes tantervi térképek és kutatási fájlok továbbra is elérhetők a `curricula/` és `research/` mappákban. Ezek referenciaanyagok, nem kötelező indítófájlok.
