# Free ChatGPT – telepítési útmutató

Két külön ChatGPT Projektet hozz létre: egyet a spanyol, egyet az angol kurzusnak. A Free csomagban egy projekt legfeljebb **5 fájlt** tartalmazhat, ezért az induláshoz pontosan három állandó fájlt használunk. A projektutasításokat a Projekt beállításainál külön szövegként kell beilleszteni; ne töltsd fel őket fájlként.

## 1. Spanyol projekt

Projekt neve: **Duolingo – Spanyol angolból**

A projekt Instructions mezőjébe másold be a [spanyol projektutasításokat](es-en/PROJECT-INSTRUCTIONS.md).

A projektbe töltsd fel ezt a három fájlt:
1. [FREE-PROTOCOL.md](FREE-PROTOCOL.md) – rövid tanítási és kontextuskezelési szabályok.
2. [COURSE-ROUTER.json](es-en/COURSE-ROUTER.json) – spanyol egység-/modulválasztó térkép.
3. [STATE-CARD.json](es-en/STATE-CARD.json) – spanyol v5 tanulói állapotkártya.

## 2. Angol projekt

Projekt neve: **Duolingo – Angol magyarból**

A projekt Instructions mezőjébe másold be az [angol projektutasításokat](en-hu/PROJECT-INSTRUCTIONS.md).

A projektbe töltsd fel ezt a három fájlt:
1. [FREE-PROTOCOL.md](FREE-PROTOCOL.md).
2. [COURSE-ROUTER.json](en-hu/COURSE-ROUTER.json).
3. [STATE-CARD.json](en-hu/STATE-CARD.json).

A két kurzust külön projektben kezeld, ne töltsd fel a másik kurzus routerét vagy állapotkártyáját.

## 3. Minden tanulási alkalom

1. A projektben indíts új beszélgetést, vagy folytasd a meglévőt.
2. Add meg a jelenlegi Duolingo-pozíciódat (szekció/modul, egység, cím). A pozíciót ne találja ki az asszisztens.
3. Az asszisztens válassza ki a routerből az 1–3 releváns nyelvtani modult.
4. Csak az aktív modul pontos tartományát add át. Ha a GitHub-fájl nem olvasható a chatben, nyisd meg a routerben szereplő útvonalat, és másold be csak a megadott sorok közötti modult. Ne töltsd fel a teljes A1–B2 tananyagot.
5. A tanítás végén az asszisztens adjon friss, teljes v5 JSON-állapotkártyát. Új beszélgetés indításakor a legutóbbi kártyát másold be, vagy cseréld le a Projektben tárolt `STATE-CARD.json` fájlt.

## 4. Öt fájlos keret és feltöltési keret

Az induló három projektfájl szándékosan kevés. Így két szabad hely marad:
- **Aktuális modul:** ha fájlként szeretnéd átadni, ez lehet a negyedik fájl. Alternatívaként egyszerűen másold be a chatbe, így nem fogyaszt projektfájl-helyet.
- **Hibakatalógus:** csak akkor add hozzá ötödik fájlként, ha egy hiba visszatér vagy nehezen diagnosztizálható. Alapértelmezésként ne töltsd fel.

A Free csomagban a projektfájlok száma legfeljebb 5. A fájlfeltöltés napi kerete külön korlát lehet; a jelenlegi hivatalos súgó 3 feltöltést jelez naponta Free felhasználóknak. Ezért a három alapfájlt érdemes egyszerre feltölteni, az aktuális modult pedig inkább üzenetként bemásolni. A limitek változhatnak.

## 5. Mit ne tölts fel?

Ne töltsd fel induláskor:
- a teljes `courses/*.json` kurzusadatokat;
- a teljes `curricula/*.md` vagy `.json` tantervet;
- a teljes A1–B2 modulbankot;
- a két hosszú, régi kezdő promptot;
- a hibakatalógust, ha még nincs rá szükség.

Ezek a GitHub-repóban megmaradnak részletes háttéranyagként, de nem részei az alapértelmezett Free projektkontextusnak.

## 6. Folytonosság

A GitHub állapotkártyái és a Projektben feltöltött kártyák egymástól külön példányok. Ha a ChatGPT friss JSON-t ad vissza:
- másold be az új beszélgetésbe, vagy
- frissítsd vele a Projektben feltöltött `STATE-CARD.json` fájlt, illetve a GitHubon a megfelelő `progress/*-state-card.json` fájlt.

GitHubra csak külön kérésre írjon az asszisztens. A projekt emlékezete segíthet a korábbi beszélgetések összekapcsolásában, de a legutóbbi JSON-kártya maradjon a tanulási állapot egyértelmű forrása.

## Hivatalos ChatGPT-korlátok

- [Projects in ChatGPT](https://help.openai.com/en/articles/10169521-projects-in-chatgpt)
- [File uploads](https://help.openai.com/en/articles/8555545-uploading-files-and-audio-to-chatgpt)
- [ChatGPT Free Tier FAQ](https://help.openai.com/en/articles/9275245-chatgpt-free-tier-faq)

A beállítások és a használati limitek változhatnak; a ChatGPT felületén megjelenő aktuális korlát az irányadó.
