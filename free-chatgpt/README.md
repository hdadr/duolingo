# Free ChatGPT – telepítési és használati útmutató

Két külön ChatGPT Projektet hozz létre: egyet a spanyol, egyet az angol kurzusnak. A két projekt ugyanazt a tanítási módszert használja, de a tananyaguk és tanulói előzményeik külön maradnak.

A Free csomagban egy projekt legfeljebb **5 fájlt** tartalmazhat, ezért az induláshoz pontosan három állandó fájlt használunk. A projektutasításokat a Projekt beállításainál külön szövegként kell beilleszteni; ne töltsd fel őket fájlként.

## 1. Spanyol projekt létrehozása

Projekt neve: **Duolingo – Spanyol angolból**

A projekt Instructions mezőjébe másold be a [spanyol projektutasításokat](es-en/PROJECT-INSTRUCTIONS.md).

A projektbe töltsd fel ezt a három fájlt:
1. [FREE-PROTOCOL.md](FREE-PROTOCOL.md) – a közös tanítási, folytonossági és chatváltási szabályok.
2. [COURSE-ROUTER.json](es-en/COURSE-ROUTER.json) – spanyol egység-/modulválasztó térkép.
3. [STATE-CARD.json](es-en/STATE-CARD.json) – üres v5 állapotkártya-sablon és tartalék.

(A router szerkezetét a [free-course-router.schema.json](../schemas/free-course-router.schema.json) ellenőrzi; ez nem projektfájl, nem kell feltölteni.)

## 2. Angol projekt létrehozása

Projekt neve: **Duolingo – Angol magyarból**

A projekt Instructions mezőjébe másold be az [angol projektutasításokat](en-hu/PROJECT-INSTRUCTIONS.md).

A projektbe töltsd fel ezt a három fájlt:
1. [FREE-PROTOCOL.md](FREE-PROTOCOL.md).
2. [COURSE-ROUTER.json](en-hu/COURSE-ROUTER.json) – az angol Duolingo-kurzus mind az 1005 egységének tömörített útvonaltérképe.
3. [STATE-CARD.json](en-hu/STATE-CARD.json) – üres v5 állapotkártya-sablon és tartalék.

A két kurzust külön projektben kezeld, ne töltsd fel a másik kurzus routerét vagy állapotkártyáját.

## 3. Memória beállítása – fontos a chatváltáshoz

A projekt korábbi beszélgetéseiből való folytatáshoz engedélyezni kell a ChatGPT memóriafunkcióit:
1. Nyisd meg a ChatGPT **Beállítások → Személyre szabás** részét.
2. Kapcsold be a **Mentett memóriák hivatkozása** és a **Csevegési előzmények hivatkozása** lehetőséget, ha megjelennek a fiókodban.
3. A projekt saját beállításainál válaszd a **Projektmemória / csak projektmemória** módot, ha elérhető. Így a spanyol projekt nem keveredik az angol vagy más beszélgetésekkel.
4. Megosztott projektek automatikusan csak projektmemóriát használnak. A projekt résztvevői hozzáférhetnek a projekt beszélgetéseihez és fájljaihoz.

A menüpontok és a lehetőségek fiókonként változhatnak. A memória segíti a korábbi beszélgetések felhasználását, de nem helyettesít garantált, strukturált adatbázist. Ezért marad meg az opcionális állapotkártya.

## 4. A tanuló napi használata

A tanulónak nem kell minden alkalommal indítópromptot vagy JSON-t másolnia. Lépjen be a megfelelő projektbe, és ugyanabban a beszélgetésben folytassa a tanulást, amíg az kényelmes.

Elég néhány egyszerű mondat:

| Mit írjon? | Mit tesz a ChatGPT? |
|---|---|
| „Kezdjük az elejétől.” | Automatikusan az adott kurzus 1. egységétől (#1) indul. Nem kell nyelvtani témát választani. |
| „Kezdjük!” | Ha nincs korábbi haladás, az elejétől indít; ha van, a legutóbb megerősített Duolingo-pozícióból folytat. |
| „Folytassuk!” | A projekt legutóbbi megerősített tanulási pontját állítja vissza. |
| „Következő Duolingo-egység.” | A megerősített Duolingo-pozíciót a következő egységre lépteti, és kiválasztja az ahhoz tartozó nyelvtani témát. |
| „Már a 3. szekció 12. egységénél tartok.” (spanyol) / „A 3. modul 12. egységénél tartok.” (angol) | A megfelelő kurzusbeli helyre ugrik; egy képernyőkép is elég. |
| „Ezt nem értem.” | Egyszerűbb magyarázatot és új példát ad. |
| „Mára ennyi.” | Rövid, a projektbeszélgetésben maradó folytonossági jegyzetet készít. |
| „Kérem az állapotkártyát.” | Teljes, másolható v5 JSON-mentést ad. |

A tanulónak nem kell megneveznie a nyelvtani témát: a rendszer az aktuális Duolingo-egység alapján választ. A tanulónak nem kell nyelvtani témát választania: a rendszer a spanyol section/unit vagy az angol module/unit alapján automatikusan választ tananyagot. A legtöbb alkalom után egyszerűen kiléphet; nem kell a jegyzetet másolnia, fájlt cserélnie vagy a haladást kézzel frissítenie.

## 5. Mikor kell új beszélgetést nyitni?

Alapértelmezés szerint maradjon ugyanabban a chatben. Egy modul vagy altéma befejezése önmagában nem indokol új beszélgetést.

Új chatet csak akkor érdemes nyitni, ha a régi beszélgetés már nagyon hosszú, összekeveredtek benne a témák, vagy a ChatGPT ezt javasolja. Ilyenkor:
1. Nyisson új beszélgetést **ugyanabban a kurzusprojektben**.
2. Első üzenetként írja: „Folytassuk!”
3. A ChatGPT először próbálja a projekt korábbi beszélgetéseiből visszaállítani a haladást. Ha ez elég pontos, nincs további teendő.

### Opcionális biztosíték: állapotkártya másolása

Ha a ChatGPT nem tudja megbízhatóan visszaállítani a pontos tanulási állapotot, vagy a tanuló külön biztonsági mentést szeretne:
1. A régi beszélgetésben írja: „Kérem az állapotkártyát.”
2. A ChatGPT egyetlen kódblokkban megadja a teljes v5 JSON-t.
3. Az új beszélgetés első üzenetébe illessze be, ezzel: „Folytassuk ebből.”

Ez csak tartalékmegoldás. A projektbe feltöltött `STATE-CARD.json` fájlt nem kell minden alkalommal frissíteni; az induló sablonként szolgál.

## 6. Tananyag és további fájlok

A kiválasztott aktuális modul pontos szövegét csak akkor kell a chatbe bemásolni, amikor a ChatGPT kiválasztotta. A teljes modultárat ne töltsd fel.

A két szabad projektfájl-hely:
- **Aktuális modul:** ha fájlként szeretnéd átadni, ez lehet a negyedik fájl. Egyszerűbb a pontos modulblokkot a chatbe illeszteni, így nem fogyaszt projektfájl-helyet.
- **Hibakatalógus:** csak visszatérő vagy nehezen diagnosztizálható hiba esetén add hozzá ötödik fájlként.

Ne töltsd fel induláskor:
- a teljes `courses/*.json` kurzusadatokat;
- a teljes `curricula/*.md` vagy `.json` tantervet;
- a teljes A1–B2 modulbankot;
- a két hosszú, régi kezdő promptot;
- a hibakatalógust, ha még nincs rá szükség.

A Free csomagban a projektfájlok száma legfeljebb 5. A fájlfeltöltés napi kerete külön korlát lehet; ezért a három alapfájlt érdemes egyszerre feltölteni, az aktív modult pedig inkább üzenetként bemásolni.

## Hivatalos ChatGPT-tájékoztatók

- [Projects in ChatGPT](https://help.openai.com/en/articles/10169521-projects-in-chatgpt)
- [File uploads](https://help.openai.com/en/articles/8555545-uploading-files-and-audio-to-chatgpt)
- [ChatGPT Free Tier FAQ](https://help.openai.com/en/articles/9275245-chatgpt-free-tier-faq)

A beállítások és a használati limitek változhatnak; a ChatGPT felületén megjelenő aktuális korlát az irányadó.
