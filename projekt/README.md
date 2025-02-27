# Projekt

Cieľom projektu je osvojiť si základné koncepty a techniky analýzy dát, pochopiť, ako fungujú a získať intuíciu pre ich vhodnú aplikáciu za účelom objavovania znalostí v dátach. Mali by ste tiež získať predstavu, aké otázky vieme pomocou analýzy dát zodpovedať a byť schopní aplikovať a vyhodnotiť základné prístupy strojového učenia.

**Projekt sa vypracúva vo dvojiciach.** Pri riešení sa očakáva využitie jazyka `Python` a dostupných knižníc na analýzu dát (`pandas`, `matplotlib` a pod.). V každej fáze sa odovzdáva vykonateľný `Jupyter Notebook`, ktorý by mal zachytávať a vhodne dokumentovať všetky vykonané transformácie nad dátami. Odovzdaný notebook musí obsahovať nielen kód, ale aj jeho výsledky (vypočítané hodnoty, výpisy, vizualizácie a pod.) spolu s komentárom intrepretujúcim získané výsledky a z toho plynúce rozhodnutia pre ďalšie kroky dátovej analýzy. Schopnosť dobre odkomunikovať a vybrať relevantné výsledky analýzy bude predstavovať významnú zložku hodnotenia. *Pri každej fáze v odovzdanom notebooku tiež uveďte percentuálny podiel práce jednotlivých členov dvojice.*

## Dáta

Každá dvojica bude pracovať s im náhodne pridelenou dátovou sadou. Dáta predstavujú záznamy o pacientoch s chorobou štítnej žľazy. Vašou úlohou je vedieť predikovať hodnotu **Y** (môže sa líšiť v závislosti od pridelenej dátovej sady). Budete sa musieť pritom vysporiadať s viacerými problémami, ktoré sa v dátach nachádzajú (formáty dát, chýbajúce, nezmyselné alebo vychýlené hodnoty a pod.).

## Prieskumná analýza (max. 12b)
Prieskumná analýza je kľúčovou časťou analýzy dát. Bez nej nie sme schopní dáta spracúvať, pretože nevieme, čo sa v nich nachádza. Využíva sa  pritom predovšetkým deskriptívna štatistika a rôzne podporné vizualizácie. 

V tejto fáze sa od vás očakáva:

- **Základný opis dát spolu s ich charakteristikami (3b).** Pre dosiahnutie plného počtu bodov uveďte počet záznamov, počet atribútov, ich typy a pre zvolené významné atribúty ich distribúcie, základné deskriptívne štatistiky a pod.
- **Párová analýza dát (4b).** Preskúmajte vzťahy medzi zvolenými dvojicami atribútov. Zamerajte sa pritom na identifikáciu závislostí medzi dvojicami atribútov (napr. korelácie) a na závislosti medzi predikovanou premennou a ostatnými premennými (potenciálnymi prediktormi).
- **Formulácia a štatistické overenie hypotéz o dátach (2b).** Mali by ste sformulovať aspoň dve hypotézy o dátach, ktoré budú relevantné v kontexte zadanej predikčnej úlohy. Príkladom hypotézy (v závislosti od pridelenej dátovej sady) môže byť, že *pacienti s chorobou štítnej žľazy majú v priemere inú (vyššiu/nižšiu) hodnotu nejakej látky alebo hormónu ako pacienti bez danej choroby*. Vami sformulované hypotézy overte vhodne zvoleným štatistickým testom.
- **Identifikácia problémov v dátach spolu s predpokladaným scenárom riešenia v ďalšej fáze (3b).** Mali by ste identifikovať, čo budete musieť v rámci predspracovania vyriešiť (aj s naznačením možností, ako tieto problémy plánujete v ďalšej fáze riešiť). Medzi problémy, na ktoré môžete v rámci analýzy naraziť, patria napr.: 
   - nevhodná štruktúra dát (dáta nie sú v tabuľkovej podobe alebo jedna entita je opísaná viacerými riadkami tabuľky)
   - duplicitné záznamy, resp. nejednoznačné mapovanie medzi záznamami
   - nejednotné formáty dát
   - chýbajúce hodnoty
   - vychýlené (odľahlé) hodnoty
   - a ďalšie, t. j. v dátach sa môžu nachádzať aj iné, tu nevymenované problémy, ktoré tiež treba identifikovať a vo vašej analýze adresovať.

V odovzdanej správe (`Jupyter Notebooku`) by ste tak mali vedieť zodpovedať na otázky:
- Majú dáta vhodný formát pre ďalšie spracovanie? Ak nie, aké problémy sa v nich vyskytujú?
- Sú niektoré atribúty medzi sebou závislé? Od ktorých (jednotlivých) atribútov závisí predikovaná premenná?
- Sú v dátach chýbajúce hodnoty? Ako sú reprezentované? Ako plánujete riešiť problém chýbajúcich hodnôt pre jednotlivé atribúty, resp. pozorovania? (Pre rôzne atribúty môže byť vhodné použiť rôzne stratégie.)
- Nadobúdajú niektoré atribúty nezmyselné (nekonzistentné) či inak výrazne odchýlené hodnoty? Ktoré?
- Ako plánujete v ďalšej fáze tieto identifikované problémy adresovať / riešiť?

Správa sa odovzdáva v 6. týždni semestra na cvičení (dvojica svojmu cvičiacemu odprezentuje vykonanú prieskumnú analýzu v `Jupyter Notebooku`). Následne správu elektronicky odovzdá jeden člen z  dvojice do systému AIS do **nedele 3.11.2019 do 23:59**.

## Predspracovanie (max. 18b)

Na základe identifikovaných problémov v dátach a návrhu ich riešenia v predchádzajúcej fáze treba zrealizovať predspracovanie. Výsledkom by mala byť upravená dátová sada (vo formáte `csv`) vo vhodnom tvare pre strojové učenie. To znamená, že jedno pozorovanie musí byť opísané jedným riadkom tabuľky; zároveň, keďže v tretej fáze budeme pracovať s algoritmom, ktorého implementácia podporuje len numerické dáta, bude potrebné všetky nenumerické atribúty transformovať na numerické. Napokon, keďže sa predspracovaním mohol zmeniť tvar a charakteristiky dát (počet atribútov, distribúcie hodnôt a pod.), treba znovu zrealizovať podstatné časti prieskumnej analýzy. Významnú časť hodnotenia bude predstavovať znovupoužiteľnosť (replikovateľnosť) predspracovania.

V tejto fáze sa od vás očakáva:
- **Integrácia dát a prípadná deduplikácia záznamov (4b).** Výsledkom by mala byť jednotná tabuľková reprezentácia dát, ktorá bude predstavovať vstup pre ďalšie spracovanie a (v 3. fáze) strojové učenie.
- **Realizácia krokov predspracovania dát a ich zdokumentovanie (5b).** 
  - Pri riešení chýbajúcich hodnôt vyskúšajte rôzne stratégie (očakáva sa vyskúšanie minimálne dvoch stratégií, pričom aspoň jedna z nich musí byť zvolená z posledných troch menovaných):
    - nahradenie chýbajúcej hodnoty mediánom
    - nahradenie chýbajúcej hodnoty priemerom
    - nahradenie chýbajúcej hodnoty pomerom ku korelovanému atribútu
    - nahradenie chýbajúcej hodnoty priemerom segmentu
    - nahradenie chýbajúcej hodnoty pomocou lineárnej regresie
    - nahradenie chýbajúcej hodnoty pomocou algoritmu k-najbližších susedov
  - Podobne postupujte aj pri riešení vychýlených (odľahlých) hodnôt, pričom vyskúšajte aspoň dve  zo stratégií uvedených nižšie:
    - odstránenie vychýlených (odľahlých) pozorovaní
    - nahradenie vychýlenej hodnoty hraničnými hodnotami rozdelenia (5 percentilom, resp. 95 percentilom)
    - transformácia atribútu s vychýlenými hodnotami pomocou zvolenej funkcie (logaritmus, odmocnina a pod.)
- **Znovupoužiteľnosť predspracovania (5b).** Upravte váš kód realizujúci predspracovanie trénovacej množiny tak, aby ho bolo možné bez ďalších úprav znovupoužiť na predspracovanie validačnej, resp. testovacej množiny (ich predspracovanie sa pritom v tej fáze nevyžaduje, odovzdaný kód v `Jupyter Notebooku` na to však musí byť pripravený). Očakáva sa preto, že bude predspracovanie realizované pomocou funkcií alebo využijete možnosti knižnice `sklearn.pipeline`. Častým problémom býva využitie informácií, ktoré nie sú dostupné v čase zbierania údajov (napr. štatistické informácie o celej testovacej sade pri spracovaní trénovacích údajov alebo aj pri spracovaní jednotlivých pozorovaní z testovacej sady), čím môžete do trénovania zaniesť znalosť z validačnej alebo testovacej množiny; vaše riešenie toto musí ošetrovať.
- **Opätovná realizácia podstatných častí prieskumnej analýzy (4b).** V rámci nej by ste mali vedieť zodpovedať na otázku, ako sa zmenili distribúcie hodnôt po realizácii krokov predspracovania (t. j. treba ju realizovať len tam, kde vaším predspracovaním došlo k nejakým zmenám).

Správa sa odovzdáva v 9. týždni semestra na cvičení (dvojica svojmu cvičiacemu odprezentuje vykonané predspracovanie v `Jupyter Notebooku`). Následne správu elektronicky odovzdá jeden člen z  dvojice do systému AIS do **nedele 24.11.2019 do 23:59**.

## Strojové učenie (max. 15b)

Pri dátovej analýze nemusí byť naším cieľom získať len znalosti obsiahnuté v aktuálnych dátach, ale aj natrénovať model, ktorý bude schopný robiť rozumné predikcie pre nové pozorovania. Na to sa využívajú techniky strojového učenia. V tomto projekte sa zameriame na rozhodovacie stromy vzhľadom na ich jednoduchú interpretovateľnosť.

V tejto fáze dostanete nový dataset, na ktorom oddemonštrujete znovupoužiteľnosť vami realizovaného predspracovania. Vami natrénované klasifikátory budú porovnané medzi sebou; uvidíte tak, ako dobre ste sa umiestnili v rámci vášho cvičenia, resp. celého predmetu.

V poslednej fáze sa od vás očakáva:
- **Predspracovanie nového datasetu vami realizovaným postupom predspracovania a opis prípadných zmien (2b).** Spustite postup predspracovania realizovaný v predchádzajúcej fáze nad novým datasetom. Nový dataset bude mať rovnakú štruktúru ako váš pôvodný, nebudú sa v ňom však možno nachádzať niektoré problémy (nové vám nepribudnú). Ak si spustenie predspracovania vyžiada zmeny v kóde, opíšte ich.
- **Manuálne vytvorenie a vyhodnotenie rozhodovacích pravidiel pre klasifikáciu (3b).** Vyskúšajte jednoduché pravidlá zahŕňajúce jeden atribút, ale aj komplikovanejšie zahŕňajúce viacero atribútov (ich kombinácie). Pravidlá by v tomto kroku mali byť vytvorené manuálne na základe pozorovaných závislostí v dátach. Pravidlá (manuálne vytvorené klasifikátory) vyhodnoťte pomocou metrík správnosť (angl. *accuracy*), presnosť (angl. *precision*) a úplnosť (angl. *recall*). 
- **Natrénovanie a vyhodnotenie klasifikátora s využitím rozhodovacích stromov (4b).** Na trénovanie využite algoritmus dostupný v knižnici `scikit-learn` (`CART`). Vizualizujte natrénované pravidlá. Vyhodnoťte natrénovaný rozhodovací strom pomocou metrík správnosť (angl. *accuracy*), presnosť (angl. *precision*) a úplnosť (angl. *recall*). Porovnajte natrénovaný klasifikátor s vašimi manuálne vytvorenými pravidlami z druhého kroku. 
- **Optimalizácia hyperparametrov (4b).** Preskúmajte hyperparametre klasifikačného algoritmu `CART` a vyskúšajte ich rôzne nastavenie tak, aby ste minimalizovali preučenie. Vysvetlite, čo jednotlivé hyperparametre robia. Pri nastavovaní hyperparametrov algoritmu využite 10-násobnú krížovú validáciu na trénovacej množine.
- **Vyhodnotenie vplyvu zvolenej stratégie riešenia chýbajúcich hodnôt na správnosť klasifikácie (2b).** Zistite, či použitie zvolených stratégií riešenia chýbajúcich hodnôt vplýva na správnosť (angl. accuracy) klasifikácie. Ktorá stratégia sa ukázala ako vhodnejšia pre daný problém?

Správa sa odovzdáva v 12. týždni semestra na cvičení (dvojica svojmu cvičiacemu odprezentuje výsledky strojového učenia v `Jupyter Notebooku`). Následne správu elektronicky odovzdá jeden člen z  dvojice do systému AIS do **nedele 15.12.2019 do 23:59**.
