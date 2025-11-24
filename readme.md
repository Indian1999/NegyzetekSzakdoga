# Egy négyzet fedése egységnyi méretű négyzetek felhasználásával

## Bevezető
Jelen szakdolgozatomban a következő problémával foglalkozom: Adott *n* darab egységnyi oldalhosszúságú négyzet. Mekkora annak a lehető legnagyobb négyzetnek a mérete, melyet teljesen le tudunk fedni ezen kisebb négyzetek felhasználásával. Az egységnyi méretű négyzetek fedését és forgatását megengedjük. Egy 2025-ben publikált cikk már foglalkozott egy hasonló problémával (méretben egymást követő négyzetekkel kell lefedni a lehető legnagyobb négyzet alakú területet), viszont azonos méretű négyzetek használata újnak ígérkezik. 

## A kutatási téma bemutatása

### A probléma és célkitűzés
**Kérdés:** Le tudunk-e fedni egy K x K méretű négyzetet *n* darab 1 x 1 méretű kisebb négyzet felhasználásával?
**Másként:** Melyik az a legnagyobb K érték melyre teljesül, hogy *n* darab 1 x 1 méretű négyzetet stratégikusan elhelyezve le tudjuk fedni a K x K méretű négyzetet?

A kis négyzetek forgathatók és fedhetik egymást.

**Cél:** A kutatás fő célja egy olyan algoritmus kidolgozása, amely képes egy közel optimális elrendezést megtalálni adott n esetén.

**Részcélok:**
1. Hasonló problémával foglalkozó cikkek átfogó elemzése
2. Az esetleges korlátok megtalálása és definiálása *n* értékétől függően
3. A megközelítés kidolgozása a probléma megoldására
4. Vizuális segédprogram készítése, mellyel könnyen tesztelhetők különböző konstrukciók manuálisan



## Szakirodalmi áttekintés
### Kapcsolódó kutatások
Mivel jelen probléma még új, így konkrétan ezzel a problémával foglalkozó munkát nem tudtam azonosítani, de számos, hasonló témával foglalkozó releváns cikkre bukkantam:
1. [1] Covering a square with consecutive squares (Balogh János, Dósa György, Lars Magnus Hvattum, Olaj Tomas Attila, Szalkai István, Tuza Zsolt)
Ebben a kutatásban a kérdés megegyezik, viszont azonos méretű négyzetek helyett, különböző méretű (egymást követve) négyzeteket használunk a nagyobb négyzet kialakításához, a kis négyzetek forgatását mellőzve.

2. [2] Packing Unit Squares in Squares (Erich Friedman)
Kérdés mellyel a kutatás foglalkozik: Mekkora annak a legkisebb négyzetnek a mérete, melyben el tudunk helyezni *n* darab egységnyi oldalhosszúságú négyzetet. A négyzetek forgatása itt is megendedett, de a fedésük nem.

### Alkalmazott módszerek

A fent említett kutatásokban használt megközelítések:
1. **Matematikai programozás:** Binary Integer és Mixed Integer Programming
2. **Heurisztikus keresőalgoritmusok:** Genetikus algoritmus, lokális keresés
3. **Expanziós algoritmus:** Konstrukciós eljárás, már megtalált K értékre építkezve talál jobb megoldást
4. **Szimmetriai tulajdonságok kihasználása**
5. **Alsó-felső korlátok bizonyítása**
6. **Terület alapú becslés**

### Kutatási rés

A szakirodalom áttekintése után egyértelműen kirajzolódott, hogy míg hasonló jellegű problémákra már jelentős eredmények fel lettek tárva, jelen probléma még feltérképezetlen terület, jelentős kutatási rés mutatkozik, a jelenlegi cikkek nem foglalkoznak a jelenlegi kérdéssel. Jelen kutatás ezt a rést kívánja betölteni, azáltal, hogy `n <= 50` értékekre, közel optimális megoldásokat keresünk.

## A tervezett megoldás

### Kutatási módszertan
A kutatási munka főbb fázisai a következők:
1. Előkészítési fázis: szakirodalmi kutatás, a probléma definiálása, kutatási terv kidolgozása
2. Fejlesztési fázis: a megoldó algoritmusok kidolgozása, grafikus segédprogram elkészítése
3. Értékelési fázis: tesztelés, eredmények validálása és kiértékelése
4. Dokumentálási fázis: eredmények összegzése, szakdolgozat elkészítése

A kutatás során különös hangsúlyt fektetek a heurisztikus kereső-algoritmusok alkalmazására, mivel ez lehetővé teszi nagy *n* értékek esetén egy közelítő megoldás megtalálását. A gyorsabb futási idő érdekében a kiindulási állapotot egy konstruktív algoritmus segítségével tervezem meghatározni, amely egy biztosan konstruálható konstrukció egy `K >= floor(sqrt(n))` értékre.

### Eszközök és technológiák
A kutatás során a következő szoftvereket, eszközöket és technológiákat tervezem használni:
- **Programozási nyelvek:** Python (optimum kereséshez), JavaScript (grafikus programhoz)
- **Keretrendszerek, könyvtárak:** NumPy, MatplotLib, Flask
- **Fejlesztői eszközök:** Git, Visual Studio Code, Putty, WinSCP


## Féléves munkaterv és előrehaladás

### A félév során kitűzött célok

| Feladat | Cél | Státusz | Befejezettség |
|----------|----------|----------|----------|
| Szakirodalmi kutatás | Legalább 2 releváns forrás feldolgozása | Elkészült | 100% |
| Probléma specifikálása | Pontos kérdés megfogalmazása | Elkészült | 100% |
| Kutatási rés azonosítása | Újdonság meghatározása | Elkészült | 100% |
| Módszer kidolgozása | Fejlesztési és kutatási terv | Folyamatban | 50% |
| Eszközkörnyezet kialakítása | Szükséges eszközök telepítése | Elkészült | 100% |

### Elvégzett munka és elért eredmények

**Szakirodalmi kutatás:** A félév során összesen 2 tudományos publikációt dolgoztam fel. Ezek közül kiemelkedő jelentőséggel bír [1], amely nagyban befolyásolja a kutatás irányát.

**Kutatási probléma specifikálása:** A kezdeti problémamegfogalmazást az első konzultációnk alkalmával pontosítottuk. A jelenlegi megfogalmazás szerint a kérdés:
`
Melyik az a legnagyobb K érték melyre teljesül, hogy *n* darab 1 x 1 méretű négyzetet stratégikusan elhelyezve le tudjuk fedni a K x K méretű négyzetet?
`

**Módszer kidolgozása:** {Ide majd valamit}

**Fejlesztői környezet kialakítása:** Beállítottam a szükséges szoftver- és hardverkörnyezetet. Telepítettem a fejlesztéshez szükséges python csomagokat. A szerveremen beállítottam a program futtatásához szükséges környezetet, a program alapverzióját kiszolgálja jelenleg. A projekt fájlszerkezete kialakításra került.

### Időráfordítás

A féléves munka során összesen 13 hetet fordítottam a projektre, hetente átlagosan 15 órát foglalkozva vele. Az időráfordítás megoszlása az alábbi:
- Szakirodalmi kutatás: 2 hét
- Konzultációk: 4 alkalom
- Módszer kidolgozása: 1 hét
- Előzetes kísérletek és prototípus fejlesztés: 6 hét
- Dokumentáció készítése: 1 hét

## Első részeredmények

### Előzetes kutatási eredmények
A félév során végzett munka első konkrét eredményei a következők:

**Szakirodalmi tanúlságok:** A szakirodalom áttekintése során azonosítottam a kutatási terület fő megközelítéseit, ezek erősségeit és gyengeségeit, milyen módon alkalmazhatóak az én kutatásomban. Különösen jelentős felismerés a heurisztikus kereső-algoritmusok használata, a konstruktív megközelítés, illetve a már meglévő eredményekre való kiegészítő építkezés.

**Kutatási rés:** Jelen kérdés még érintetlen területnek bizonyul, pontosan ezzel a problémával foglalkozó publikációt nem találtam.

**Segédprogram prototípus:** Elkészítettem egy alap verzióját a segédprogramnak, mely segíti és lehetővé teszi különböző konstrukciók manuális tesztelését.

**Használni tervezett módszerek meghatározása:** A közel optimális megoldások keresésére kidolgoztam különféle módszereket, ezek implementálása a következő félévben fog megvalósulni. Tervezett megközelítések:
- **Heurisztikus kereső-algoritmusok**
    - Genetikus algoritmus
    - Részecske Raj Optimalizáció
    - Szimulált hűtés
- **Kunstruktív megközelítés:** A négyzeteket megfontoltan elhelyezve próbálunk egy lehető legjobb megoldást megtalálni.
- **Expanziós megközelítés:** kisebb *n* értékre megtalált megoldás továbbbővítése
- **Hibrid módszer:** A fenti módszerek ötvözése

### Tapasztalatok, megfigyelések

A félév során szerzett tapasztalatok közül a legfontosabbak:

- Annak ellenőrzése, hogy mekkora négyzetet fed le a négyzetek egy konstrukciója komoly kihívást jelent, mivel végtelen sok pontot nincs lehetőség megvizsgálni, ha csak bizonyos pontokat ellenőrzünk, akkor az eredmény pontatlan lehet, mindenképp szükséges lesz egy algoritmus ami a négyzetek elhelyezkedése és orientációja alapján számol egy pontos *K* értéket, illetve egy gyorsabb, csak becslést kínáló, de gyorsabban futó algoritmusra.

- A lehetséges legnagyobb *K* érték alsó határa:
`
K >= floor(sqrt(n))
`
- A lehetséges legnagyobb *K* érték felső határa
`
K <= ceil(sqrt(n))
`

## Következő lépések

A következő félévben tervezett főbb feladatok a következők:
- **Rövid távú célok (2 hónapon belül):**
    - Legalább 1 heurisztikus kereső-algoritmus implementálása
    - Egy konstruktív módszer implementálása, esetleges alkalmazása a kereső-algoritmusokban
    - A grafikus segédprogram finomítása

- **Középtávú célok (3-4 hónapon belül):**
    - A teljes rendszer elkészítése, grafikus vezérlőfelület
    - Több módszer közül lehessen választani futtatáskor
    - A megoldásokról a program készítsen grafikus megjelenítést
    - A felhasználó adhasson meg kezdőállapotot a kereső-algoritmusoknak
    - Az eredmények részletes dokumentálása

- **Hosszú távú célok (félév vége):**
    - A szakdolgozat teljes szöveges részének megírása
    - Záró prezentáció elkészítése
    - A teljes munka áttekintése, tesztelése, hibák javítása
    - A teljes projekt finomhangolása

A projekt sikeres befejezéséhez kritikus a heurisztikus algoritmusok mielőbbi megvalósítása, mivel erre épülnek a program és a kutatás további részei. A tervezett ütemezés reálisnak ígérkezik, de biztonsági időtartalékot is beépítettem a nem várt nehézségek kezelésére.

## Összegzés

A Tervezés I. tantárgy keretében gézett féléves munka során sikerült megalapozni a kutatást elméleti és módszertani szempontokból. Az átfogó szakirodalmi kutatás egyértelműen kijelölte a kutatási rést, melyre jelen projekt fókuszál.

A félév legfontosabb eredményei:
- Pontos kutatási kérdés megfogalmazása
- Részletes szakirodalmi áttekintés
- Módszertan kidolgozása
- Előzetes kísérletek elvégzése és korlátok meghatározása
- A teljes fejlesztői környezet kialakítása

A munka során felmerólt kihívások megoldása hozzájárult a munkaterv finomhangolásához. A témavezetői konzultációk visszajelzései biztosították, hogy a munka a helyes irányba haladjon.

Az elvégzett munka biztos alapot biztosyt a következő félév feladataihoz, az időbeosztás tarhatónak ígérkezik. Kellő előrehaladást sikerült elérni ahhoz, hogy a szakdolgozat határidőre sikeresen befejezhető legyen.

 
## Irodalomjegyzék

[1] Balogh, J., Dosa, G., Hvattum, L.M. et al. Covering a square with consecutive squares. Ann Oper Res 350, 911–926 (2025). https://doi.org/10.1007/s10479-025-06633-5

[2] Friedman, E. (2009). Packing unit squares in squares: A survey and new results. Electronic Journal of Combinatorics (DS#7). https://erich-friedman.github.io/papers/squares/squares.html