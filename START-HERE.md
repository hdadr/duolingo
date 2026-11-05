# Indítás új ChatGPT-beszélgetésben

Ez a privát repó két Duolingo-kurzushoz tartalmaz magyar nyelvű magyarázó tananyagot. A Duolingo az elsődleges gyakorlófelület; a ChatGPT a nyelvtani és nyelvhasználati logikát magyarázza.

## 1. Válaszd ki a tanulási irányt

**Spanyol angolból**
- Kurzusazonosító: `DUOLINGO_ES_EN`
- Kulcs: `es-en`
- Prompt: [DUOLINGO-HU-CHATGPT-PROMPT.md](prompts/DUOLINGO-HU-CHATGPT-PROMPT.md)
- Moduljegyzék: [learning-modules/es-en/index.json](learning-modules/es-en/index.json)
- Állapotkártya: [progress/es-en-state-card.json](progress/es-en-state-card.json)

**Angol magyarból**
- Kurzusazonosító: `DUOLINGO_EN_HU`
- Kulcs: `en-hu`
- Prompt: [DUOLINGO-EN-HU-CHATGPT-PROMPT.md](prompts/DUOLINGO-EN-HU-CHATGPT-PROMPT.md)
- Moduljegyzék: [learning-modules/en-hu/index.json](learning-modules/en-hu/index.json)
- Állapotkártya: [progress/en-hu-state-card.json](progress/en-hu-state-card.json)

A két kurzus teljesen külön kezelendő.

## 2. Indítás új chatben

1. Nyiss új ChatGPT-beszélgetést.
2. Legyen hozzáférés a privát `hdadr/duolingo` repóhoz. Ha nincs GitHub-hozzáférés, másold be a kiválasztott kurzus állapotkártyáját.
3. Másold be a kiválasztott kurzus indító promptját.
4. Az új chat erősítse meg az állapotkártyában szereplő utolsó Duolingo-pozíciót.

## 3. Kontextusbetöltés

Az indító prompt szerint csak ezek szükségesek:
- `LEARNING-PROTOCOL.md`;
- `courses/registry.json`;
- a kiválasztott kurzus `course.json` fájlja;
- a kiválasztott kurzus `learning-modules/{course}/index.json` fájlja;
- a kiválasztott kurzus `progress/{course}-state-card.json` állapotkártyája;
- az aktuális modul pontos sorintervalluma a modulbankból.

Ne töltsd be automatikusan a teljes `curricula/*.md` és `.json` térképeket, a másik kurzust vagy a teljes kutatási hátteret. Ezek csak konkrét bizonytalanság vagy forrásellenőrzés esetén szükségesek. A modulbankból kizárólag az indexben jelölt sorokat olvasd be, ne a teljes szintfájlt.

## 4. Pedagógiai feldarabolás

- Egy nyelvtani modul teljes, pedagógiailag összetartozó tanulási egység.
- Tokenkeret vagy chat-hossz miatt ne vágj ketté modult.
- A belső altémák között csak teljes fogalmi határnál lehet munkamenetet váltani.
- Magyarázatot, példasort, összehasonlítást vagy megértés-ellenőrzést soha ne szakíts félbe.
- Chatváltás előtt frissítsd az állapotkártyát, és rögzítsd a következő teljes altémát.

## 5. Állapotkártya

A kártya a folytatáshoz szükséges minimális tanulói előzményt tárolja, nem a teljes beszélgetést. A v5 kártya külön tárolja a Duolingo-pozíciót és a bizonyítékokon alapuló nyelvtani tudástérképet. Megőrzi a függőben lévő választós kérdés pontos szövegét és opcióit, a rövid előfeltétel-áttekintés visszatérési pontját, de nem tárolja a helyes választ. Minden lezárt modul vagy teljes altéma után készüljön friss, másolható JSON. GitHubra csak a tanuló kifejezett kérésére írható vissza; egyébként a JSON bemásolható az új chatbe.

## 6. Tanulási módszer

- A szókincset, mondatgyakorlást, hallásértést és ismétlést elsősorban a Duolingóban végzed.
- A ChatGPT a nyelvtan és a nyelvhasználat logikáját magyarázza.
- Minden fontos új szerkezetnél négylépcsős, feleletválasztós megértés-ellenőrzés következik. Egyszerre egy kérdés jelenik meg; a válaszhoz elég az A/B/C/D opciót kiválasztani. A zárópróba más alannyal és más igével teszteli az önálló alkalmazást.
- A következő egységre csak akkor tér át, amikor a tanuló ténylegesen elért oda, vagy ezt kéri.
- A Duolingo-egység teljesítése nem jelenti automatikusan a kapcsolódó nyelvtani fogalom elsajátítását.
- Ha egy új egységhez szükséges régi alap bizonytalan, csak azt a részt ismétli át röviden, majd visszatér az aktuális egységhez.

## 7. Háttérforrások

A teljes tantervi térképek és kutatási fájlok továbbra is elérhetők a `curricula/` és `research/` mappákban. Ezek referenciaanyagok, nem kötelező indítófájlok.

A GitHub-módosítás sikerét csak tényleges írás és visszaellenőrzés után állítsd.
