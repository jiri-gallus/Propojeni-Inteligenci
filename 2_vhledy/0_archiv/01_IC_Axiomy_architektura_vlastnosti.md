# Definice

1. **Bloky systému:** Systém je tvořen bloky tří typů – Iniciační blok (IB), Centrální blok (CB) a Akční blok (AB). Bloky existují nezávisle na sobě. Systém vzniká, když mezi nimi probíhá interakce, a zaniká, když interakce skončí. Bloky přetrvávají.
2. **Interakce:** Probíhá výhradně mezi IB–CB a CB–AB. Každá jednotlivá interakce je právě jednou sekvenční výměnou mezi dvěma bloky. Interakce na opačných stranách CB mohou probíhat současně.

# Základní principy systému

1. Interakce začíná iniciací a končí výstupem ve stejném bloku, který interakci zahájil.
2. IB iniciuje interakci IB–CB. Tím může vyvolat, že CB následně iniciuje interakci CB–AB.
3. Výstup do IB mění parametry IB.
4. Interakce IB–CB a CB–AB mohou probíhat současně.

**Poznámka:** Vnitřní logika CB – kdy a jak zprostředkuje interakci směrem k AB – je záměrně abstrahována. Na této úrovni není předmětem modelu.

---

# Popis systému

Systém je dynamický útvar tvořený bloky tří typů: Iniciačním blokem (IB), Centrálním blokem (CB) a Akčním blokem (AB). Tyto bloky existují nezávisle na sobě. Systém vzniká teprve tehdy, když mezi nimi probíhá interakce – propojením bloků do činného celku. Jakmile interakce skončí, systém jako činný celek zaniká. Bloky samotné přetrvávají i mimo systém a uchovávají svůj stav pro příští interakce.

Centrální blok je komunikačním středem systému. Veškeré interakce vedou přes něj: mezi Iniciačním blokem a Centrálním blokem (IB–CB) a mezi Centrálním blokem a Akčním blokem (CB–AB). Iniciační blok a Akční blok spolu nekomunikují napřímo. CB je výhradním prostředníkem – přijímá vstupy od IB a zprostředkovává je AB, přijímá výstupy od AB a vrací je IB. Vnitřní logika CB je záměrně abstrahována.

Iniciační blok je nadřazeným prvkem systému. Pouze on zahajuje činnost – iniciuje interakci IB–CB. Tímto aktem může vyvolat, že CB následně iniciuje interakci CB–AB. Akční blok je vykonavatelem – interaguje s CB pouze tehdy, je-li k tomu CB vyzván.

Každá interakce je právě jedna sekvenční výměna mezi dvěma bloky. Začíná iniciací jednoho bloku a končí výstupem v tomtéž bloku. Interakce na opačných stranách Centrálního bloku mohou probíhat současně – zatímco IB–CB stále běží, CB–AB může již být v chodu. Výstup interakce CB–AB je přijat CB a tvoří základ pro výstup interakce IB–CB směrem k IB. Tím se datový tok uzavírá.

Výstup do Iniciačního bloku je jediným okamžikem, kdy dochází ke změně parametrů IB. Každá dokončená interakce IB–CB tak zanechává v IB stopu, která ovlivní jeho stav pro interakce následující. CB a AB jsou během interakce neměnné – výstup do nich jejich stav nemění.

Systém je definován třemi charakteristikami:

1. Centralitou CB – veškerá komunikace prochází skrze Centrální blok.
2. Hierarchií řízení – IB iniciuje, CB zprostředkovává, AB vykonává.
3. Sekvenčností a vnořitelností interakcí – každá interakce je ohraničená výměna; interakce na opačných stranách CB mohou běžet současně.

---

# Definice

- **Systém:** tvoří 3 bloky CB, IB, AB a je dynamicky definován těmi, mezi kterými probíhá interakce.
- **Interakce:** Probíhají mezi IB-CB a CB-AB

# Základní principy systému

1. Interakce je jedna sekvenční výměna mezi 2ma bloky, začíná iniciací a končí výstupem ve stejném bloku.
2. IB iniciuje interakci IB-CB a tím může iniciovat interakci CB-AB.
3. Výstup do IB mění parametry IB a referenci dalšího výstupu.

# Popis systému

Systém je dynamický útvar tvořený třemi bloky – Iniciačním blokem (IB), Centrálním blokem (CB) a Akčním blokem (AB). Systém existuje pouze tehdy, když s Centrálním blokem probíhá alespoň jedna interakce. Jakmile interakce ustane, systém zaniká.

Centrální blok je pasivním středem systému. Veškeré interakce vedou přes něj – buď mezi Iniciačním blokem a Centrálním blokem (IB–CB), nebo mezi Centrálním blokem a Akčním blokem (CB–AB). Iniciační blok a Akční blok spolu neinteragují napřímo. CB je výhradním médiem jejich nepřímé komunikace.

Iniciační blok je nadřazený. Pouze on zahajuje interakce. Zápisem do CB iniciuje interakci IB–CB a tím může nepřímo iniciovat i interakci CB–AB. Akční blok je podřízený – interaguje s CB pouze tehdy, když je k tomu vyzván na základě předchozí interakce IB.

Každá interakce je právě jedna sekvenční výměna mezi dvěma bloky. Začíná iniciací a končí výstupem ve stejném bloku, který interakci zahájil. Výstup do IB je jediným okamžikem, kdy dochází ke změně parametrů Iniciačního bloku a reference pro další výstup. Výstup do CB žádnou takovou změnu nevyvolává – CB je pasivní nosič, nikoli aktivní účastník.

Systém je tedy definován třemi charakteristikami:

1. Centralitou CB – vše prochází skrze něj.
2. Hierarchií řízení – IB iniciuje, CB je pasivní, AB je vykonavatel.
3. Sekvenčností interakcí – každá interakce má jasný začátek a konec, výstupem končí.

---

# fg

1. Centrální uzel řídí interakce a tím i životní cykly aktivních uzlů.
2. Účel interakce uzlů je výstup systému.
3. Interakce mění parametry centrálního uzlu a referenci výstupu.

# Definice pojmů

1. **Systém:** Je tvořen uzly a interakcemi mezi nimi.
2. **Interakce:** Právě jedna sekvenční výměna mezi uzly.
3. **Řízení:** Před zahájením interakce centrální uzel nejprve vynucuje výstup systému z interakce předchozí. Dále přistupuje a ruší.

# Vlastnost 1 - Existence systému

Centrální uzel řídí vznik systému. Systém zaniká výstupem systému.

## Definiční podmínky systému

1. Systém je tvořen uzly a interakcemi mezi nimi.
2. Interakce je právě jedna sekvenční výměna mezi uzly.
3. Centrální uzel interakce zahajuje.
4. Neexistuje jiný iniciátor interakce.
5. Účel interakce je výstup systému.
6. Interakce končí výstupem.

## Rozbor vlastnosti

**Část A: Centrální uzel řídí vznik systému.**

- **Krok 1:** Z definice 1 a 2 vyplývá, že systém existuje, když má interakci.
- **Krok 2:** Z principu 1 a definice 3 vyplývá, že centrální uzel interakce zahajuje, a protože v principech ani definicích není jiný aktor řízení, činí tak jako jediný.
- **Krok 3:** Podmínění existence systému interakcí mezi uzly, kterou zahajuje centrální uzel obhajuje část A 1. vlastnosti.

**Část B: Systém zaniká výstupem systému.**

- **Krok 4:** Z definice 2 a principu 2 vyplývá, že interakce je právě jedna diskrétní výměna, která zaniká výstupem systému.
- **Krok 5:** Podmínění existence systému interakcí mezi uzly, která zaniká výstupem systému obhajuje část B 1. vlastnosti.

# Vlastnost 2 – Sekvenční povaha systému

V daném okamžiku probíhá nejvýše jedna interakce.

## Definiční podmínky systému

1. Interakce má definovaný začátek a konec.
2. Interakce se nepřekrývají.
3. Centrální uzel nezahajuje novou interakci, dokud předchozí neskončila.
4. Aktivní uzel nemůže iniciovat interakci.
5. V systému je právě 1 interakce jako vazba.

## Rozbor vlastnosti

- **Krok 1:** Z rozboru vlastnosti 1 vyplývá, že centrální uzel zahajuje interakce jako jediný v systému.
- **Krok 2:** Z definice 3 vyplývá, že před zahájením interakce je předchozí interakce ukončena.
- **Krok 3:** Zahájením interakce z jediného zdroje v kombinaci s automatickým ukončením předchozí interakce obhajuje 2. vlastnost.

---

# Architektura systému

## Strukturální pohled

Systém je tvořen jedním interním blokem (IB) a množinou externích bloků (EB₁, EB₂, ..., EBₙ). Interní blok je centrálním uzlem systému – veškerá komunikace a stav se soustřeďují v něm. Externí bloky mezi sebou nekomunikují přímo a nejsou si vědomy své vzájemné existence. Každý externí blok interaguje výhradně s interním blokem.

Topologie je hvězdicová (hub-and-spoke):

EB₁ ──────────────┐
                  │
EB₂ ──────────────┼── IB (centrální stav: parametry + žádaná hodnota) ──→ Výstup
                  │
EBₙ ──────────────┘


Interní blok představuje jediné integrační místo a zároveň úzké hrdlo celého systému.

## Behaviorální pohled

Interní blok je správcem interakcí a životních cyklů externích bloků. Rozhoduje o jejich vzniku, aktivaci, činnosti a zániku, stejně jako o zahájení, průběhu a ukončení interakce. Externí bloky nejsou autonomní – jejich existence a činnost je vázána na řídicí rozhodnutí interního bloku.

Interakce mezi interním a externím blokem je diskrétní (nekontinuální) a obousměrná. Během jedné interakce:

- Oba bloky čtou parametry interního bloku.
    
- Oba bloky zapisují parametry interního bloku.
    
- Oba bloky čtou žádanou hodnotu výstupu.
    
- Oba bloky zapisují žádanou hodnotu výstupu.
    

Výsledný stav po interakci je tedy emergentním výsledkem společné činnosti obou bloků. Interní blok není pasivním úložištěm – je aktivním spoluautorem změn.

## Průběh cyklu

Systém pracuje v diskrétních cyklech:

text

[IB zahajuje interakci s EBₖ] → [EBₖ ⇄ IB: obousměrné čtení a zápis] → [Výstup] → [Přepis parametrů IB] → [Změna žádané hodnoty] → [IB ukončuje interakci] → [Případný další cyklus]

Každý cyklus má jasný začátek a konec. Výstup systému je jednorázový – je výsledkem dokončené interakce. Minimálně je potřeba jedna interakce, ale cyklů může být více, protože každá změna žádané hodnoty iniciuje nový cyklus.

## Stavový model interního bloku

Interní blok drží sdílený stav o dvou složkách, které jsou přístupné všem externím blokům bez jakékoli izolace kontextu:

|Složka stavu|Zápis|Čtení|
|---|---|---|
|Parametry IB|IB i EB (oba během interakce)|IB i EB (oba během interakce)|
|Žádaná hodnota|IB i EB (oba během interakce)|IB i EB (oba během interakce)|

Neexistuje transakční ohraničení, notifikace o změně ani izolace kontextu pro jednotlivé externí bloky. Jde o globální přepis s okamžitou viditelností pro všechny.

# Vlastnosti systému

1. **Dočasnost systému**  
    Systém jako činný celek vzniká, když interní blok zahájí interakci s externím blokem. Zaniká, když interní blok interakci ukončí. Existence systému je diskrétní a netrvalá – je vázána výhradně na rozhodnutí interního bloku. Bez aktivní interakce systém neexistuje.
    
2. **Hierarchické řízení životních cyklů**  
    Interní blok je nadřazenou entitou. Externí bloky jsou řízené zdroje – jejich existence a aktivita závisí na rozhodnutí interního bloku.
    
3. **Diskrétní, nikoli kontinuální výstup**  
    Výstup systému není spojitý. Je dosahován v jednotlivých dokončených interakcích. Minimální počet pro výstup je jedna interakce; další cykly následují při změně žádané hodnoty.
    
4. **Obousměrné vyjednávání, nikoli jednostranný přepis**  
    Interakce je dialogem, nikoli diktátem. Oba bloky čtou a zapisují do sdíleného stavu. Výsledný stav je emergentním produktem jejich společné činnosti. Interní blok je aktivním mediátorem a spoluautorem změn.
    
5. **Adaptivní cíl**  
    Žádaná hodnota výstupu není pevná. Je výsledkem předchozí interakce – systém iterativně redefinuje svůj vlastní cíl na základě provozní zkušenosti.
    
6. **Vnořená zpětnovazební smyčka**  
    Systém obsahuje dvě úrovně zpětné vazby:
    
    - **Vnitřní smyčka:** obousměrné čtení a zápis uvnitř jediné interakce (IB ⇄ EB).
        
    - **Vnější smyčka:** modifikace parametrů a žádané hodnoty pro budoucí cykly.
        
7. **Sdílený stav bez izolace kontextu**  
    Všechny externí bloky sdílejí týž stav interního bloku. Jakákoli interakce kteréhokoli externího bloku přepisuje parametry a žádanou hodnotu globálně, bez ohledu na ostatní bloky.
    
8. **Nezamýšlené křížové ovlivnění výstupů**  
    Externí bloky se navzájem ovlivňují, aniž by o sobě věděly. Interakce EB₁ modifikuje stav IB, který následně čte a dále modifikuje EB₂ – a naopak. Stav se stává hybridní směsí otisků všech předchozích interakcí bez možnosti dohledat, který blok je za konkrétní hodnotu zodpovědný. Výstup každého bloku je tak ovlivněn aktivitou bloků, se kterými nesdílí žádný přímý vztah.
    
9. **Rozmazaná příčinnost**  
    Po sérii interakcí nelze jednoznačně určit, který blok způsobil konkrétní změnu parametru či žádané hodnoty. Příčinnost je emergentní a nedohledatelná – výsledný stav je produktem všech interakcí současně.
    
10. **Životní cykly jako nepřímý kanál přenosu informace**  
    Protože IB je správcem životních cyklů, může do interakce zapisovat i na základě znalosti o stavu ostatních EB (které jsou aktivní, které ukončeny). Tím se nepřímo přenáší informace mezi externími bloky, přestože o sobě nevědí – prostřednictvím IB jako aktivního mediátora.
    
11. **Zvýšené riziko nestability a chaosu**  
    Obousměrný zápis uvnitř interakce vytváří mikro-zpětnovazební smyčku, která může zesilovat nebo tlumit změny. Při více aktivních externích blocích se tyto efekty kumulují napříč cykly. Kombinace sdíleného stavu, obousměrného zápisu a absence izolace vytváří riziko oscilace žádané hodnoty nebo dokonce chaotického chování – cíl systému se může měnit dříve, než je předchozí cyklus dokončen.
    
12. **Vysoká adaptivita za cenu nízké předvídatelnosti**  
    Systém je extrémně adaptivní – učí se a přizpůsobuje parametry i cíle na základě každé interakce. Tato adaptivita je však vykoupena nízkou předvídatelností chování při více současně aktivních externích blocích, protože stavový prostor je sdílen, příčinnost je rozmazaná a neexistují ochranné mechanismy.
    

# Závěr

Model popisuje vysoce provázaný, adaptivní systém s emergentním chováním postavený na hvězdicové architektuře s jedním interním blokem a množinou vzájemně nevědomých externích bloků.

Klíčovým rysem je diskrétní, obousměrná interakce, během níž oba bloky současně čtou a zapisují do sdíleného stavu. Tím vzniká systém, který:

- **Je dočasný** – vzniká a zaniká rozhodnutím interního bloku.
    
- **Je adaptivní** – průběžně mění své parametry i cíle na základě zkušenosti.
    
- **Je křehký** – absence izolace kontextu znamená, že externí bloky se neúmyslně ovlivňují.
    
- **Má rozmazanou příčinnost** – výsledný stav je hybridem všech interakcí a nelze dohledat původce konkrétní změny.
    
- **Je obtížně předvídatelný** – kombinace sdíleného stavu, obousměrného zápisu a vnořených zpětnovazebních smyček vytváří potenciál pro nestabilitu až chaotické chování.
    

Systém je vhodný pro prostředí, kde je vyžadována extrémní adaptivita a kde důsledky křížového ovlivnění nejsou kritické – nebo kde je počet současně aktivních externích bloků omezen na jeden. Pro nasazení s více paralelními externími bloky by bylo vhodné doplnit mechanismy izolace kontextu, transakčního ohraničení interakcí nebo notifikace o změnách stavu.