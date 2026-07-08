Mám systém, který vykazuje toto chování: Sekvenční povaha systému: -
vznik systému: iniciace CU - zánik systému: výstup z poslední aktivní
interakce (do CU, nebo KR) - Interakce: Jedna sekvenční výměna
(iniciace - výstup) CU - KR - CU (CU iniciuje, KR aktivní/pasivní,
výstup do CU) KR - AU - KR (KR iniciuje na základě CU interakce, AU
aktivní, výstup do KR) Vazby jsou CU-KR-AU Interakce KR-AU-KR je
iniciována KR na základě iniciace CU, ale současně iniciace CU to dělá
jako interakci, tedy jde do ni i vstup Jak bys to rozbil na co
nejelementárnější, axiomický popis systému. Čím méně a jednodušeji, tím
lépe.

Tady je rozklad na nejjednodušší možné elementy:

------------------------------------------------------------------------

**Entity:**

- CU

- KR

- AU

**Vazby:**

- CU → KR

- KR → AU

- AU → KR

- KR → CU

**Stav KR:**

- aktivní

- pasivní

------------------------------------------------------------------------

**Axiomy chování:**

1.  **Vznik systému** = CU iniciuje interakci

2.  **Interakce** = sekvence: vstup → zpracování → výstup

3.  **CU → KR**:

    - KR je pasivní → konec systému (výstup do CU)

    - KR je aktivní → pokračuje bodem 4

4.  **KR → AU → KR**:

    - AU vždy aktivní

    - výstup vždy do KR

5.  **Zánik systému** = výstup z poslední interakce do CU nebo do
    pasivní KR

------------------------------------------------------------------------

**Graficky:**

text

CU ──→ KR ──→ AU

↑ ↑ │

└───────┴──────┘

(při pasivní KR nebo dokončení AU cyklu)

To je vše. Tři entity, dvě možné větve, jeden cyklus.

Co takhle? Je tam vše? Změnil jsem CU=IB KR=CB AU=AB \" Definice Systém:
tvoří 3 bloky CB, IB, AB a je dynamicky definován těmi, mezi kterými
probíhá interakce. Interakce: Probíhají mezi IB-CB a CB-AB Základní
principy systému 1. Interakce je jedna sekvenční výměna mezi 2ma bloky,
začíná iniciací a končí výstupem ve stejném bloku. 2. IB iniciuje
interakci IB-CB. 3. IB přes svou interakci iniciuje interakci CB-AB 4.
Výstup do IB mění parametry IB a referenci dalšího výstupu. \"

V tom popisu mi chybí dvě zásadní věci:

1.  **Konec / zánik systému** -- původně byl jasně daný (výstup do CU
    nebo pasivní KR). Tady není vůbec řečeno, kdy systém končí.

2.  **Chování CB** -- původně mělo dva stavy (aktivní/pasivní), které
    určovaly, jestli se jde do AB nebo rovnou ven. Tady CB jen
    \"přeposílá\", ale není jasné, zda je to vždy, nebo za nějaké
    podmínky.

------------------------------------------------------------------------

Co bych doplnil:

- **Podmínka větvení v CB** -- buď aktivní CB spustí interakci CB-AB,
  nebo pasivní CB vrátí výstup do IB.

- **Ukončovací podmínka** -- systém končí, když výstup z interakce
  skončí v IB a *není iniciována další interakce* (nebo když CB je
  pasivní).

Pak by to sedělo a nic podstatného by nechybělo.

Malá změna: \" Definice Systém: tvoří 3 bloky CB, IB, AB a je dynamicky
definován bloky, mezi kterými probíhá interakce. Interakce: Probíhají
mezi IB-CB a CB-AB Základní principy systému 1. Interakce je jedna
sekvenční výměna mezi 2ma bloky, začíná iniciací a končí výstupem ve
stejném bloku. 2. IB iniciuje interakci IB-CB. 3. IB přes svou interakci
iniciuje interakci CB-AB 4. Výstup do IB mění parametry IB a referenci
dalšího výstupu. \" Pokud je systém definován interakcemi a ty mají
definován svůj začátek a konec, není to totéž?

Ano, máš pravdu. Když je interakce definovaná jako sekvence se začátkem
a koncem, tak:

- **Vznik systému** = iniciace interakce (bod 2)

- **Zánik systému** = výstup z poslední interakce, která už neiniciuje
  další

Je to v tom implicitně obsažené. Není to sice explicitně vyřčeno jako
samostatný axiom, ale logicky to z definice interakce plyne.

Takže chybí jen to **větvení v CB** -- jestli CB interakci CB-AB spustí
vždy, nebo jen někdy. Bez toho nelze poznat, kdy se řetězec interakcí
zastaví a systém zanikne.

Stačí doplnit jeden princip:

**5. CB buď předá výstup do AB (aktivní), nebo vrátí výstup do IB
(pasivní).**

Pak je to kompletní.

Co s touto změnou? \" Definice Systém: tvoří 3 bloky CB, IB, AB a je
dynamicky definován těmi, mezi kterými probíhá interakce. Interakce:
Probíhají mezi IB-CB a CB-AB Základní principy systému 1. Interakce je
jedna sekvenční výměna mezi 2ma bloky, začíná iniciací a končí výstupem
ve stejném bloku. 2. IB iniciuje interakci IB-CB. 3. IB může přes svou
interakci iniciuje interakci CB-AB 4. Výstup do IB mění parametry IB a
referenci dalšího výstupu. \"

Teď je to horší. Slovo **\"může\"** v bodě 3 zavádí nejednoznačnost:

- Není jasné, **kdy** IB tu interakci CB-AB iniciuje a kdy ne.

- Není jasné, **co se stane**, když ji neiniciuje -- systém rovnou
  končí? Nebo se děje něco jiného?

------------------------------------------------------------------------

Pro srovnání -- původní model měl tu logiku jasně danou přes **stav
CB** (aktivní/pasivní), který o větvení rozhodoval. Teď jsi odpovědnost
za větvení přesunul na IB, ale bez pravidla, podle kterého se rozhoduje.

------------------------------------------------------------------------

**Aby to dávalo smysl**, chtělo by to buď:

- a\) Dát IB explicitní stav (např. IB má parametr, který určuje, zda
  iniciuje CB-AB), nebo

- b\) Nechat větvení na CB jako dřív -- tedy vrátit aktivní/pasivní CB.

Jinak je v systému díra.

2\. Jedině IB iniciuje interakci s IB-CB (pinkají si něco mezi sebou,
systém je definován těmito bloky. 3. Jedině IB může ve své interakci
iniciovat interakci CB-AB (tedy jen on má moc, CB jen předá. Slovo může
znamená, že kdyby tam nebylo, tak to je nejednoznačné, jestli každá
iniciace IB-CB je taky iniciace CB-AB

Teď už to chápu -- díky za vysvětlení. To \"může\" tam není jako náhoda
nebo nedostatek, ale jako **záměrná otevřenost**: ne každá iniciace
IB-CB automaticky spouští CB-AB. A rozhoduje o tom výhradně IB, CB jen
poslouchá.

Pokud je to tak, pak to \"může\" je v pořádku a popis je **úplný**. Už
tam není žádná díra -- jen je to na první přečtení snadno
přehlédnutelné.

Shrnuto:

- **Vznik systému:** IB iniciuje IB-CB

- **Větvení:** IB **může** (ale nemusí) iniciovat CB-AB

- **Zánik systému:** výstup, který už nic dalšího neiniciuje (ať už
  proto, že IB CB-AB nevyvolalo, nebo že AB svůj výstup ukončilo)

Nic nechybí.

Dává tohle smysl jako celek? \" Definice Systém: tvoří 3 bloky CB, IB,
AB a je dynamicky definován těmi, mezi kterými probíhá interakce.
Interakce: Probíhají mezi IB-CB a CB-AB Základní principy systému 1.
Interakce je jedna sekvenční výměna mezi 2ma bloky, začíná iniciací a
končí výstupem ve stejném bloku. 2. IB iniciuje interakci IB-CB a tím
může iniciovat interakci CB-AB. 3. Výstup do IB mění parametry IB a
referenci dalšího výstupu. Popis systému Systém je dynamický útvar
tvořený třemi bloky -- Iniciačním blokem (IB), Centrálním blokem (CB) a
Akčním blokem (AB). Systém existuje pouze tehdy, když s Centrálním
blokem probíhá alespoň jedna interakce. Jakmile interakce ustane, systém
zaniká. Centrální blok je pasivním středem systému. Veškeré interakce
vedou přes něj -- buď mezi Iniciačním blokem a Centrálním blokem
(IB--CB), nebo mezi Centrálním blokem a Akčním blokem (CB--AB).
Iniciační blok a Akční blok spolu neinteragují napřímo. CB je výhradním
médiem jejich nepřímé komunikace. Iniciační blok je nadřazený. Pouze on
zahajuje interakce. Zápisem do CB iniciuje interakci IB--CB a tím může
nepřímo iniciovat i interakci CB--AB. Akční blok je podřízený --
interaguje s CB pouze tehdy, když je k tomu vyzván na základě předchozí
interakce IB. Každá interakce je právě jedna sekvenční výměna mezi dvěma
bloky. Začíná iniciací a končí výstupem ve stejném bloku, který
interakci zahájil. Výstup do IB je jediným okamžikem, kdy dochází ke
změně parametrů Iniciačního bloku a reference pro další výstup. Výstup
do CB žádnou takovou změnu nevyvolává -- CB je pasivní nosič, nikoli
aktivní účastník. Systém je tedy definován třemi charakteristikami: 1.
Centralitou CB -- vše prochází skrze něj. 2. Hierarchií řízení -- IB
iniciuje, CB je pasivní, AB je vykonavatel. 3. Sekvenčností interakcí --
každá interakce má jasný začátek a konec, výstupem končí. \"

Dává to smysl jako celek. Je to konzistentní, hierarchie je jasná, nic
si neprotiřečí.

Mám dvě drobné poznámky -- nejsou to chyby, spíš místa, kde by čtenář
mohl zaváhat:

------------------------------------------------------------------------

**1. \"Výstup ve stejném bloku\" v principu 1**

Píšeš: *\"začíná iniciací a končí výstupem ve stejném bloku\"* -- ale u
interakce CB-AB iniciuje CB, výstup jde do CB. U IB-CB iniciuje IB,
výstup jde do IB. To sedí.

Ale v popisu pak říkáš: *\"Výstup do CB žádnou změnu nevyvolává\"* --
tím naznačuješ, že výstup do CB existuje (což je správně, z CB-AB). Jen
princip 1 by mohl čtenář omylem vztáhnout i na CB (že CB iniciuje a
výstup jde do CB -- to je v pořádku, jen to chce chvilku zastavit se a
ověřit).

**Návrh:** Nic neměnit, jen jsem chtěl potvrdit, že to sedí.

------------------------------------------------------------------------

**2. \"Interakce CB-AB\" -- kdo ji fakticky iniciuje?**

V principech i popisu říkáš, že IB iniciuje CB-AB *skrze* svou interakci
s CB. To je důležité a správné. Ale místy to působí, jako by CB-AB
inicioval CB sám -- což by odporovalo hierarchii. Není to chyba, jen
jemná významová nuance: iniciátorem je IB, CB je prostředník.

------------------------------------------------------------------------

**Celkově:** Systém drží pohromadě, 3 charakteristiky v závěru ho hezky
uzavírají. Funguje to.

Tato nuance je tam protože kdyby se s tím dělalo složitěji, musela by se
interakce derinovat pro obě jinak.

Ano, přesně tak. Tím, že interakci definuješ jednotně (iniciace → výstup
ve stejném bloku), vyhneš se dvěma samostatným definicím pro IB-CB a
CB-AB. Je to elegantní.

A právě proto tam ta nuance být musí -- je to cena za jednoduchost
definice. Kdyby ji čtenář přehlédl, může si chybně myslet, že CB
iniciuje sám od sebe. Ale jakmile to jednou vidí, sedí to.

Je to čisté, nic bych neměnil.

Připrav cele kontextové pole k archivaci paměti. Potřebuji rozdělit
kontext na logické celky o tom, co jsme probírali, opatřit je názvem,
krátkým popisem a citací, kterou úsek začíná. Postup: - Rozděl kontext
podle tématu (nejdi do detailů, 2-20 paměťových částí) - Indexuj část
(01, 02, 03, \... 20) - Vymysli krátký název (max. 4 slova) - Vymysli
krátký popis aby bylo jasno co která část obsahuje (max. 4 věty) - Vypiš
přesnou citaci začátku textu (max. 10 slov) pro zpětnou dohledatelnost v
textovém editoru (ctrl+f). - Musíš obsáhnout celé kontextové pole. 01
část je od citace 01 po citaci 02.

**01 --- Definice systému CU-KR-AU**

**Popis:** Úvodní definice původního systému se třemi entitami CU, KR,
AU, jejich vazbami a stavy KR (aktivní/pasivní). Popisuje vznik systému
iniciací CU, průběh interakcí a zánik systému výstupem do CU nebo
pasivní KR.\
**Citace začátku:** Sekvenční povaha systému: - vznik systému: iniciace
CU

------------------------------------------------------------------------

**02 --- Rozklad na elementární axiomy**

**Popis:** Rozklad původního systému na nejjednodušší entity, vazby,
stavy a axiomy chování. Obsahuje grafické znázornění cyklu CU→KR→AU a
zpět.\
**Citace začátku:** Tady je rozklad na nejjednodušší možné elementy:
Entity: - CU

------------------------------------------------------------------------

**03 --- Přejmenování entit na IB, CB, AB**

**Popis:** Změna názvů entit z CU, KR, AU na IB, CB, AB. Uživatel se
ptá, zda je v novém popisu vše obsaženo. Nový popis obsahuje definici
systému, interakcí a čtyři základní principy.\
**Citace začátku:** Co takhle? Je tam vše? Změnil jsem CU=IB KR=CB AU=AB

------------------------------------------------------------------------

**04 --- Identifikace chybějících prvků (větvení a konec)**

**Popis:** Zpětná vazba na nový popis -- chybí explicitní podmínka
větvení v CB a ukončovací podmínka systému. Vysvětlení, proč je nutné
tyto prvky doplnit.\
**Citace začátku:** V tom popisu mi chybí dvě zásadní věci: 1. Konec

------------------------------------------------------------------------

**05 --- Implicitní vznik a zánik z definice interakce**

**Popis:** Uživatel argumentuje, že vznik a zánik systému je implicitně
obsažen v definici interakce jako sekvence se začátkem a koncem. Shoda,
že to tak platí, ale větvení v CB stále chybí.\
**Citace začátku:** Malá změna: Definice Systém: tvoří 3 bloky CB, IB

------------------------------------------------------------------------

**06 --- Zavedení slova \"může\" a jeho důsledky**

**Popis:** Uživatel mění princip 3 přidáním slova \"může\" (IB může
iniciovat CB-AB). Diskuze o tom, že tím vzniká nejednoznačnost -- chybí
pravidlo, kdy se tak děje.\
**Citace začátku:** Co s touto změnou? Definice Systém: tvoří 3 bloky CB

------------------------------------------------------------------------

**07 --- Objasnění záměru slova \"může\"**

**Popis:** Uživatel vysvětluje, že \"může\" je záměrná otevřenost -- ne
každá iniciace IB-CB automaticky spouští CB-AB. IB je jediný, kdo o tom
rozhoduje. Shoda, že popis je tím pádem úplný.\
**Citace začátku:** 2. Jedině IB iniciuje interakci s IB-CB (pinkají si

------------------------------------------------------------------------

**08 --- Kompletní definice systému ke kontrole**

**Popis:** Uživatel předkládá rozšířenou definici systému obsahující
definice, základní principy a popis systému se třemi charakteristikami.
Žádá o posouzení, zda dává smysl jako celek.\
**Citace začátku:** Dává tohle smysl jako celek? Definice Systém: tvoří
3

------------------------------------------------------------------------

**09 --- Dvě poznámky k finální verzi**

**Popis:** Potvrzení konzistence celku. Dvě drobné poznámky -- výstup ve
stejném bloku u obou typů interakcí a otázka, kdo fakticky iniciuje
CB-AB. Obě jsou vysvětleny jako správné.\
**Citace začátku:** Dává to smysl jako celek. Je to konzistentní,
hierarchie je

------------------------------------------------------------------------

**10 --- Nuance jako cena za jednotnou definici**

**Popis:** Uživatel potvrzuje, že nuance v iniciaci CB-AB je záměrná --
kdyby se řešila složitěji, musela by se interakce definovat pro oba typy
zvlášť. Shoda, že je to čisté a elegantní řešení.\
**Citace začátku:** Tato nuance je tam protože kdyby se s tím dělalo
