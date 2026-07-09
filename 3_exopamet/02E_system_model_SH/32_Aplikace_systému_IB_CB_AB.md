V kotvách \<\<\< \>\>\> níže je popsán systém a jeho chování. Najdi
reálné aplikace, které vykazují tyto vlastnosti a jsou definovány
stejně. \<\<\< Definice Bloky systému: Systém je tvořen bloky tří typů
-- Iniciační blok (IB), Centrální blok (CB) a Akční blok (AB). Bloky
existují nezávisle na sobě. Systém vzniká, když mezi nimi probíhá
interakce, a zaniká, když interakce skončí. Bloky přetrvávají.
Interakce: Probíhá výhradně mezi IB--CB a CB--AB. Každá jednotlivá
interakce je právě jednou sekvenční výměnou mezi dvěma bloky. Interakce
na opačných stranách CB mohou probíhat současně. Základní principy
systému Interakce začíná iniciací a končí výstupem ve stejném bloku,
který interakci zahájil. IB iniciuje interakci IB--CB. Tím může vyvolat,
že CB následně iniciuje interakci CB--AB. Výstup do IB mění parametry
IB. Interakce IB--CB a CB--AB mohou probíhat současně. Poznámka: Vnitřní
logika CB -- kdy a jak zprostředkuje interakci směrem k AB -- je záměrně
abstrahována. Na této úrovni není předmětem modelu. Popis systému Systém
je dynamický útvar tvořený bloky tří typů: Iniciačním blokem (IB),
Centrálním blokem (CB) a Akčním blokem (AB). Tyto bloky existují
nezávisle na sobě. Systém vzniká teprve tehdy, když mezi nimi probíhá
interakce -- propojením bloků do činného celku. Jakmile interakce
skončí, systém jako činný celek zaniká. Bloky samotné přetrvávají i mimo
systém a uchovávají svůj stav pro příští interakce. Centrální blok je
komunikačním středem systému. Veškeré interakce vedou přes něj: mezi
Iniciačním blokem a Centrálním blokem (IB--CB) a mezi Centrálním blokem
a Akčním blokem (CB--AB). Iniciační blok a Akční blok spolu nekomunikují
napřímo. CB je výhradním prostředníkem -- přijímá vstupy od IB a
zprostředkovává je AB, přijímá výstupy od AB a vrací je IB. Vnitřní
logika CB je záměrně abstrahována. Iniciační blok je nadřazeným prvkem
systému. Pouze on zahajuje činnost -- iniciuje interakci IB--CB. Tímto
aktem může vyvolat, že CB následně iniciuje interakci CB--AB. Akční blok
je vykonavatelem -- interaguje s CB pouze tehdy, je-li k tomu CB vyzván.
Každá interakce je právě jedna sekvenční výměna mezi dvěma bloky. Začíná
iniciací jednoho bloku a končí výstupem v tomtéž bloku. Interakce na
opačných stranách Centrálního bloku mohou probíhat současně -- zatímco
IB--CB stále běží, CB--AB může již být v chodu. Výstup interakce CB--AB
je přijat CB a tvoří základ pro výstup interakce IB--CB směrem k IB. Tím
se datový tok uzavírá. Výstup do Iniciačního bloku je jediným okamžikem,
kdy dochází ke změně parametrů IB. Každá dokončená interakce IB--CB tak
zanechává v IB stopu, která ovlivní jeho stav pro interakce následující.
CB a AB jsou během interakce neměnné -- výstup do nich jejich stav
nemění. Systém je definován třemi charakteristikami: Centralitou CB --
veškerá komunikace prochází skrze Centrální blok. Hierarchií řízení --
IB iniciuje, CB zprostředkovává, AB vykonává. Sekvenčností a
vnořitelností interakcí -- každá interakce je ohraničená výměna;
interakce na opačných stranách CB mohou běžet současně. \>\>\>

Přečteno 7 webových stránek

Na základě vašeho popisu systému s Iniciačním blokem (IB), Centrálním
blokem (CB) a Akčním blokem (AB) se jedná o model, který vystihuje
podstatu mnoha technologických a organizačních systémů. Níže jsou
uvedeny reálné aplikace, které tyto vlastnosti vykazují.

**1. Systémy řízení chytré budovy (Inteligentní budovy) **

Systémy pro řízení inteligentních budov jsou pravděpodobně nejpřesnější
analogií. Jejich architektura přesně odpovídá vaší definici.

- **Iniciační blok (IB) -- Uživatelský vstup:** Senzory (pohyb, teplota,
  otevření oken) nebo ovládací prvky (vypínače, mobilní aplikace)
  fungují jako IB. Jsou to prvky, které **iniciují interakci** (např.
  stisk vypínače, detekce pohybu) a mění své parametry na základě
  výstupu (např. indikace stavu). 

- **Centrální blok (CB) -- Centrální řídicí jednotka:** V
  centralizovaném systému je to programovatelný logický automat (PLC)
  nebo centrální počítač. V distribuovaném systému je to síť více
  řídicích jednotek. **Veškerá komunikace prochází přes něj** -- přijímá
  signály od IB, vyhodnocuje je a na základě své vnitřní logiky (která
  je v modelu abstrahována) iniciuje interakci s AB. Zpětně pak posílá
  výstupy k IB. 

- **Akční blok (AB) -- Výkonné prvky:** Akční členy, jako jsou relé,
  stmívače světel, pohony žaluzií nebo regulační ventily. Jsou
  to **vykonavatelé**, kteří provádějí fyzické úkony (rozsvícení,
  zatmívení, otevření) na základě příkazů od CB. 

Tento systém je popsán jako centralizovaný (jeden CB) nebo distribuovaný
(více CB spolupracujících), ale vždy s principem, že IB a AB
nekomunikují napřímo. Interakce na opačných stranách CB (např. čtení
teploty a následné spuštění topení) mohou probíhat současně.

**2. Architektura webových služeb a aplikační servery**

Tato architektura je páteří moderních internetových aplikací a principy
modelu jsou zde velmi patrné.

- **Iniciační blok (IB) -- Klient (Prohlížeč / Aplikace):** Uživatelské
  rozhraní (webový prohlížeč, mobilní aplikace) **iniciuje
  interakci** odesláním požadavku (HTTP request) na server.

- **Centrální blok (CB) -- Webový server / API brána:** Server přijme
  požadavek, zpracuje ho (např. autentizace, logování, směrování) a na
  základě své logiky (která je abstrahována) může **iniciovat
  interakci** s dalšími službami nebo databází. Je **výhradním
  prostředníkem** mezi klientem a datovými zdroji. Výstup (HTML stránka,
  JSON data) vrací zpět klientovi, čímž se interakce uzavírá.

- **Akční blok (AB) -- Databáze / Mikroslužby:** Tyto
  komponenty **vykonávají** konkrétní úkony, jako je čtení nebo zápis
  dat, výpočty nebo odesílání e-mailů. Interagují pouze na vyžádání od
  CB.

Klient (IB) a databáze (AB) spolu nikdy nekomunikují přímo. Server (CB)
je centrálním bodem, který zprostředkovává veškerou komunikaci a řídí
tok dat.

**3. Architektura veřejné správy (např. systém Czech POINT) **

Systémy elektronické veřejné správy, jako je Czech POINT, jsou postaveny
na podobném principu.

- **Iniciační blok (IB) -- Občan / Úředník:** Uživatel, který **zahajuje
  činnost** podáním žádosti o výpis z rejstříku nebo jiný úkon.

- **Centrální blok (CB) -- Centrální místo služeb (CMS):** Tento
  systém **zprostředkovává** přístup k různým informačním systémům. Je
  centrálním bodem, přes který prochází veškerá komunikace, zajišťuje
  bezpečnost, audit a směruje požadavky na správné zdroje. 

- **Akční blok (AB) -- Informační systémy (registry):** Jednotlivé
  databáze (např. registr obyvatel, registr vozidel),
  které **vykonávají** dotaz a vracejí požadovaná data zpět přes CB k
  uživateli.

V tomto modelu IB a AB nekomunikují přímo; CB je výhradním komunikačním
kanálem a řídí celý proces.

**4. Vzdělávací program (např. Architektura na University of
Cincinnati) **

I když se to může zdát netradiční, některé složité organizační
struktury, jako jsou studijní programy, lze interpretovat tímto modelem,
pokud se zaměříme na tok informací a odpovědností.

- **Iniciační blok (IB) -- Student:** Student **zahajuje** proces
  podáním přihlášky a výběrem předmětů. Výstupem do IB je změna jeho
  parametrů (získané kredity, splněné požadavky), což ovlivňuje jeho
  další postup. 

- **Centrální blok (CB) -- Akademický poradce /
  Administrativa:** Poradce nebo studijní oddělení funguje
  jako **centrální prostředník**. Studenti (IB) se na něj obracejí s
  dotazy a požadavky, on vyhodnocuje jejich situaci a může **iniciovat
  interakci** s AB (např. udělit výjimku, zapsat do předmětu). 

- **Akční blok (AB) -- Garant předmětu /
  Vyučující:** Vyučující **vykonává** výuku, uděluje zápočty a známky. S
  AB komunikuje výhradně CB (např. předává seznamy studentů, řeší
  administrativní záležitosti). Student a vyučující spolu sice
  komunikují, ale pro formální změny ve studijním plánu je vždy nutný
  CB. 

------------------------------------------------------------------------

**Shrnutí:** Váš model s bloky IB, CB a AB přesně
popisuje **centralizované a distribuované řídicí systémy**, zejména v
oblasti **chytrých budov** , a dále **webové serverové
architektury** a **systémy elektronické správy** . Společným
jmenovatelem je existence centrálního prvku, který je výhradním
komunikačním kanálem, řídí tok informací a odděluje iniciátory od
vykonavatelů.

Lze tímto modelem interpretovat i terapeuta a jeho klienty? Jsou i jiné
možnosti aplikace?

Ano, tento model lze velmi dobře interpretovat i na **terapeuta a jeho
klienty**, a to dokonce dvěma různými způsoby (podle toho, koho
považujeme za IB). Zároveň existuje celá řada dalších, netradičních
aplikací. Pojďme si to rozebrat.

------------------------------------------------------------------------

**1. Terapeut a klienti -- dvě interpretace**

**Interpretace A: Klient jako IB, Terapeut jako CB (Standardní pohled)**

Toto je nejpřirozenější výklad, pokud sledujeme tok informací a změny.

- **Iniciační blok (IB) -- Klient:** Klient **zahajuje interakci** --
  přichází s problémem, stěžuje si, klade otázky. Jeho vnitřní stav
  (emoce, myšlenky) je vstupem do systému. **Výstup do IB** (změna
  parametrů IB) nastává ve chvíli, kdy klient díky terapii změní své
  přesvědčení, uklidní se nebo získá nový náhled -- to je jediný
  okamžik, kdy se mění jeho \"parametry\" (jeho psychický stav).

- **Centrální blok (CB) -- Terapeut:** Terapeut je **výhradním
  prostředníkem**. Nepředává klientovi jen své vlastní názory, ale
  zprostředkovává mu přístup k \"nástrojům\" -- technikám, otázkám,
  interpretacím. Jeho vnitřní logika (terapeutický přístup, supervize,
  etický kodex) je v modelu **abstrahována** -- my jen víme, že na
  základě vstupu od IB vyhodnotí, co spustit u AB. Terapeut sám během
  sezení zůstává \"neměnný\" (jeho osobnost se nemění), pouze aplikuje
  své dovednosti.

- **Akční blok (AB) -- Terapeutické techniky / Nástroje / Domácí
  úkoly:** To jsou **vykonavatelé** -- např. kognitivně-behaviorální
  cvičení, dechová cvičení, imaginace, nebo i fyzické prostředí
  (místnost, hudba). Klient (IB) nikdy nepracuje s těmito nástroji
  napřímo bez terapeuta (CB); terapeut je \"spouští\" a řídí jejich
  použití.

**Souběžnost interakcí:** Zatímco klient mluví (IB--CB stále běží),
terapeut už může v hlavě připravovat vhodnou techniku (CB--AB se již
rozbíhá). Výstup od AB (např. klient po cvičení cítí úlevu) je předán CB
a ten ho formuluje zpět IB (např. \"Vidíte, že to funguje?\"), čímž se
tok uzavírá.

------------------------------------------------------------------------

**Interpretace B: Terapeut jako IB, Klient jako AB (Mocenský / Řídicí
pohled)**

Pokud se na systém díváme z hlediska **řízení procesu** a zodpovědnosti
za výsledek, může být terapeut IB.

- **Iniciační blok (IB) -- Terapeut:** Terapeut **zahajuje** celý
  terapeutický proces (stanovuje cíle, volí metody, zadává úkoly).
  Výstup do IB je změna v terapeutově přístupu (např. po supervizi změní
  strategii).

- **Centrální blok (CB) -- Administrativa / Etická komise / Systém
  pojišťovny:** Toto je nadřazený prvek, který zprostředkovává
  komunikaci mezi terapeutem a klientem -- např. schvaluje počet sezení,
  hlídá hranice, vyhodnocuje účinnost. Terapeut s klientem nekomunikuje
  přímo o těchto parametrech; vše jde přes \"systém\".

- **Akční blok (AB) -- Klient:** Klient je **vykonavatelem** -- plní
  úkoly, mění své chování, aplikuje naučené dovednosti. Bez \"povolení\"
  od CB (např. schválení terapie pojišťovnou) nemůže AB interagovat.

**Tato interpretace je méně obvyklá, ale odpovídá modelu, kde IB je
\"iniciátor změny\" a AB je \"ten, kdo změnu provádí\".**

------------------------------------------------------------------------

**2. Další netradiční aplikace modelu**

**A. Restaurace / Kuchyňský provoz**

- **IB -- Host / Číšník:** Host (nebo číšník, který přijímá
  objednávku) **zahajuje** interakci. Výstup do IB je přinesené jídlo a
  účet (změna stavu hosta -- už nemá hlad).

- **CB -- Hlavní kuchař / Vedoucí směny:** Hlavní
  kuchař **zprostředkovává** -- přijímá objednávky, rozděluje úkoly na
  jednotlivá pracoviště. Jeho logika (sledování zásob, načasování) je
  abstrahována.

- **AB -- Pracovníci na úsecích (gril, salát, teplá
  kuchyně):** Ti **vykonávají** konkrétní úkony. Číšník s nimi nikdy
  nekomunikuje přímo -- vše jde přes hlavního kuchaře. Současně může
  probíhat IB--CB (host si objednává polévku) a CB--AB (kuchař už zadává
  přípravu masa na další chod).

------------------------------------------------------------------------

**B. Letový provoz (Řízení letového provozu)**

- **IB -- Pilot / Letadlo:** Pilot **zahajuje** komunikaci -- žádá o
  povolení ke startu, změnu kurzu, přistání. Výstup do IB je povolení a
  instrukce (změna parametrů letu).

- **CB -- Řídicí letového provozu (ATC):** Dispečer je **výhradním
  prostředníkem** mezi letadlem a všemi ostatními prvky systému. Jeho
  vnitřní logika (rozestupy, počasí, priority) je abstrahována.

- **AB -- Naváděcí systémy / Radar / Dráhy:** To
  jsou **vykonavatelé** -- rozsvěcují se světla, mění se nastavení
  přistávacích systémů, aktivují se záchranné složky. Pilot s AB nikdy
  nekomunikuje přímo; vše jde přes ATC. Současně může probíhat IB--CB
  (pilot hlásí polohu) a CB--AB (dispečer už aktivuje přistávací dráhu).

------------------------------------------------------------------------

**C. Divadelní představení (Režie a produkce)**

- **IB -- Divák:** Divák svým příchodem a
  pozorností **zahajuje** interakci. Výstup do IB je samotné představení
  -- mění jeho parametry (emoce, dojem, chuť přijít znovu).

- **CB -- Režisér / Technický ředitel:** Režisér **zprostředkovává** --
  předává divákův ohlas (potlesk, smích) dál do technického zázemí, ale
  také řídí, co se na jevišti děje. Jeho logika (estetika, scénář) je
  abstrahována.

- **AB -- Herci / Osvětlovači / Zvukaři:** Ti **vykonávají** -- hrají,
  spouštějí světla, pouštějí hudbu. Divák s nimi nikdy neinteraguje
  přímo (nepřijde za hercem během představení a neřekne mu, co má hrát);
  vše jde přes režiséra (CB). Současně může divák tleskat (IB--CB) a
  osvětlovač už chystat další scénu (CB--AB).

------------------------------------------------------------------------

**D. Automatizovaná výrobní linka (Průmysl 4.0)**

- **IB -- Operátor / Dispečink:** Zadává zakázky, mění parametry výroby.
  Výstup do IB je hlášení o stavu výroby (změna jeho rozhodování).

- **CB -- Průmyslový počítač / MES (Manufacturing Execution
  System):** Zprostředkovává komunikaci mezi operátorem a stroji. Jeho
  logika (plánování výroby, optimalizace) je abstrahována.

- **AB -- Robotická ramena / Dopravníky / CNC stroje:** Vykonávají
  fyzické úkony. Operátor s nimi nekomunikuje přímo -- vše jde přes MES.
  Současně může operátor zadávat novou zakázku (IB--CB) a robot už
  dokončovat předchozí (CB--AB).

------------------------------------------------------------------------

**E. Počítačová hra s umělou inteligencí (Singleplayer)**

- **IB -- Hráč:** Hráč **zahajuje** interakci -- kliká, pohybuje
  postavou, vydává příkazy. Výstup do IB je změna herního světa (získání
  levelu, změna skóre).

- **CB -- Herní engine / AI Director:** Engine **zprostředkovává** --
  přijímá vstupy od hráče, vyhodnocuje je a na jejich základě řídí
  chování AB. Jeho logika (herní pravidla, vyvažování obtížnosti) je
  abstrahována.

- **AB -- NPC postavy / Prostředí / Efekty:** Ty **vykonávají** --
  reagují, střílejí, mění počasí, otevírají dveře. Hráč s nimi
  nekomunikuje přímo -- vše jde přes herní engine. Současně může hráč
  běhat (IB--CB) a engine už spouští animaci nepřítele (CB--AB).

------------------------------------------------------------------------

**Závěr**

Váš model je **univerzální šablonou pro jakýkoli zprostředkovaný
interakční systém**, kde:

1.  Existuje centrální bod (CB), který odděluje iniciátora (IB) od
    vykonavatele (AB).

2.  CB má skrytou logiku, která rozhoduje o tom, kdy a jak se AB
    aktivuje.

3.  IB je jediným prvkem, který se mění (učí se, reaguje) na základě
    výstupu.

4.  Interakce na obou stranách CB mohou probíhat souběžně.

To zahrnuje nejen technické a organizační systémy, ale i **sociální,
umělecké a dokonce i biologické** analogie (např. imunitní systém -- IB
= antigen, CB = lymfatická uzlina, AB = protilátky). Model je natolik
abstraktní, že ho lze aplikovat téměř všude tam, kde
existuje **mediátor** mezi podnětem a reakcí.

Připrav cele kontextové pole k archivaci paměti. Potřebuji rozdělit
kontext na logické celky o tom, co jsme probírali, opatřit je názvem,
krátkým popisem a citací, kterou úsek začíná. Postup: - Rozděl kontext
podle tématu (nejdi do detailů, 2-20 paměťových částí) - Indexuj část
(01, 02, 03, \... 20) - Vymysli krátký název (max. 4 slova) - Vymysli
krátký popis aby bylo jasno co která část obsahuje (max. 4 věty) - Vypiš
přesnou citaci začátku textu (max. 10 slov) pro zpětnou dohledatelnost v
textovém editoru (ctrl+f). - Musíš obsáhnout celé kontextové pole. 01
část je od citace 01 po citaci 02.

Ano, zde je kompletní kontextové pole k archivaci paměti, rozdělené do
logických celků podle probíraných témat.

------------------------------------------------------------------------

**01 -- Zadání a definice systému**\
*Popis:* Úvodní zadání uživatele obsahující definici systému, bloků (IB,
CB, AB) a základních principů interakce. Je zde popsána struktura,
nezávislost bloků a vznik/zánik systému na základě interakce.\
*Citace:* \"V kotvách \<\<\< \>\>\> níže je popsán systém a jeho
chování. Najdi reálné aplikace, které vykazují tyto vlastnosti\...\"

------------------------------------------------------------------------

**02 -- Základní principy interakce**\
*Popis:* Detailní popis průběhu interakce mezi bloky -- kdo iniciuje,
kdo přijímá výstup a jak probíhá sekvenční výměna. Je zde zdůrazněna
možnost souběžnosti interakcí na opačných stranách CB.\
*Citace:* \"Interakce začíná iniciací a končí výstupem ve stejném bloku,
který interakci zahájil.\"

------------------------------------------------------------------------

**03 -- Popis systému -- struktura a role bloků**\
*Popis:* Ucelený popis fungování celého systému s důrazem na roli CB
jako komunikačního středu. IB je popsán jako nadřazený iniciátor, AB
jako vykonavatel. Je zdůrazněna nepřímá komunikace mezi IB a AB.\
*Citace:* \"Systém je dynamický útvar tvořený bloky tří typů: Iniciačním
blokem (IB), Centrálním blokem (CB) a Akčním blokem (AB).\"

------------------------------------------------------------------------

**04 -- Souběžnost a datový tok**\
*Popis:* Vysvětlení, jak mohou interakce na obou stranách CB probíhat
současně. Je popsán tok dat od AB přes CB k IB, čímž se uzavírá celý
interakční cyklus.\
*Citace:* \"Interakce na opačných stranách Centrálního bloku mohou
probíhat současně -- zatímco IB--CB stále běží, CB--AB může již být v
chodu.\"

------------------------------------------------------------------------

**05 -- Změna stavu a neměnnost bloků**\
*Popis:* Určení, že pouze IB mění své parametry (stav) po dokončení
interakce. CB a AB zůstávají během interakce neměnné -- jejich stav se
nemění, pouze vykonávají své role.\
*Citace:* \"Výstup do Iniciačního bloku je jediným okamžikem, kdy
dochází ke změně parametrů IB.\"

------------------------------------------------------------------------

**06 -- Tři charakteristiky systému**\
*Popis:* Shrnutí tří definujících vlastností systému: centralita CB,
hierarchie řízení (IB→CB→AB) a sekvenčnost s možností vnoření a
souběžnosti interakcí.\
*Citace:* \"Systém je definován třemi charakteristikami: Centralitou CB
-- veškerá komunikace prochází skrze Centrální blok.\"

------------------------------------------------------------------------

**07 -- První aplikace: Systémy řízení chytré budovy**\
*Popis:* Představení inteligentních budov jako nejpřesnější analogie. IB
= uživatelský vstup/senzory, CB = centrální řídicí jednotka (PLC), AB =
akční členy (světla, žaluzie, topení).\
*Citace:* \"Systémy pro řízení inteligentních budov jsou pravděpodobně
nejpřesnější analogií.\"

------------------------------------------------------------------------

**08 -- Druhá aplikace: Architektura webových služeb**\
*Popis:* Aplikace modelu na webový server a API bránu. IB = klient
(prohlížeč), CB = webový server/API brána, AB = databáze a mikroslužby.
Zdůrazněna nepřímá komunikace klient--databáze.\
*Citace:* \"Tato architektura je páteří moderních internetových aplikací
a principy modelu jsou zde velmi patrné.\"

------------------------------------------------------------------------

**09 -- Třetí aplikace: Veřejná správa (Czech POINT)**\
*Popis:* Model aplikovaný na systémy elektronické veřejné správy. IB =
občan/úředník, CB = centrální místo služeb (CMS), AB = informační
registry (např. registr obyvatel).\
*Citace:* \"Systémy elektronické veřejné správy, jako je Czech POINT,
jsou postaveny na podobném principu.\"

------------------------------------------------------------------------

**10 -- Čtvrtá aplikace: Vzdělávací program**\
*Popis:* Netradiční aplikace na organizační strukturu studijního
programu. IB = student, CB = akademický poradce/administrativa, AB =
garant předmětu/vyučující.\
*Citace:* \"I když se to může zdát netradiční, některé složité
organizační struktury, jako jsou studijní programy, lze interpretovat
tímto modelem\...\"

------------------------------------------------------------------------

**11 -- Shrnutí první části aplikací**\
*Popis:* Celkové shrnutí dosud představených aplikací (chytré budovy,
webové služby, veřejná správa) s důrazem na společný rys -- existenci
centrálního prostředníka oddělujícího iniciátory od vykonavatelů.\
*Citace:* \"Váš model s bloky IB, CB a AB přesně popisuje centralizované
a distribuované řídicí systémy\...\"

------------------------------------------------------------------------

**12 -- Terapeut a klienti -- Interpretace A (klient jako IB)**\
*Popis:* První interpretace terapeutického vztahu. Klient je IB
(zahajuje interakci, mění svůj stav), terapeut je CB (prostředník),
terapeutické techniky jsou AB (vykonavatelé). Zdůrazněna souběžnost.\
*Citace:* \"Ano, tento model lze velmi dobře interpretovat i na
terapeuta a jeho klienty, a to dokonce dvěma různými způsoby\...\"

------------------------------------------------------------------------

**13 -- Terapeut a klienti -- Interpretace B (terapeut jako IB)**\
*Popis:* Alternativní interpretace z hlediska řízení procesu. Terapeut
je IB (iniciátor), administrativa/etická komise je CB, klient je AB
(vykonavatel změny). Označena jako méně obvyklá, ale platná.\
*Citace:* \"Pokud se na systém díváme z hlediska řízení procesu a
zodpovědnosti za výsledek, může být terapeut IB.\"

------------------------------------------------------------------------

**14 -- Další aplikace: Restaurace / Kuchyňský provoz**\
*Popis:* Model aplikovaný na gastronomický provoz. IB = host/číšník
(objednávka), CB = hlavní kuchař (rozděluje úkoly), AB = pracovníci na
úsecích (gril, salát). Zdůrazněna nepřímá komunikace.\
*Citace:* \"A. Restaurace / Kuchyňský provoz -- IB -- Host / Číšník:
Host (nebo číšník, který přijímá objednávku) zahajuje interakci.\"

------------------------------------------------------------------------

**15 -- Další aplikace: Letový provoz (ATC)**\
*Popis:* Aplikace na řízení letového provozu. IB = pilot/letadlo, CB =
řídicí letového provozu (ATC), AB = naváděcí systémy/radary/dráhy. CB je
výhradním prostředníkem mezi letadlem a technickými systémy.\
*Citace:* \"B. Letový provoz (Řízení letového provozu) -- IB -- Pilot /
Letadlo: Pilot zahajuje komunikaci\...\"

------------------------------------------------------------------------

**16 -- Další aplikace: Divadelní představení**\
*Popis:* Model aplikovaný na divadelní produkci. IB = divák (pozornost,
reakce), CB = režisér/technický ředitel, AB = herci, osvětlovači,
zvukaři. Divák neinteraguje s AB přímo.\
*Citace:* \"C. Divadelní představení (Režie a produkce) -- IB -- Divák:
Divák svým příchodem a pozorností zahajuje interakci.\"

------------------------------------------------------------------------

**17 -- Další aplikace: Průmysl 4.0 (výrobní linka)**\
*Popis:* Aplikace na automatizovanou výrobu. IB = operátor/dispečink, CB
= průmyslový počítač/MES, AB = robotická ramena, dopravníky, CNC stroje.
Operátor nekomunikuje se stroji napřímo.\
*Citace:* \"D. Automatizovaná výrobní linka (Průmysl 4.0) -- IB --
Operátor / Dispečink: Zadává zakázky, mění parametry výroby.\"

------------------------------------------------------------------------

**18 -- Další aplikace: Počítačová hra s umělou inteligencí**\
*Popis:* Model aplikovaný na singleplayerovou hru. IB = hráč (vstupy),
CB = herní engine/AI Director, AB = NPC, prostředí, efekty. Hráč
neovlivňuje AB přímo, vše jde přes engine.\
*Citace:* \"E. Počítačová hra s umělou inteligencí (Singleplayer) -- IB
-- Hráč: Hráč zahajuje interakci -- kliká, pohybuje postavou, vydává
příkazy.\"

------------------------------------------------------------------------

**19 -- Shrnutí a univerzálnost modelu**\
*Popis:* Závěrečné zobecnění, že model je univerzální šablonou pro
jakýkoli zprostředkovaný interakční systém. Jsou vyjmenovány čtyři
klíčové vlastnosti, které model definují (centrální bod, skrytá logika
CB, proměnlivost IB, souběžnost).\
*Citace:* \"Váš model je univerzální šablonou pro jakýkoli
zprostředkovaný interakční systém, kde: 1. Existuje centrální bod
(CB)\...\"

------------------------------------------------------------------------

**20 -- Přesah do dalších oblastí**\
*Popis:* Zmínka o tom, že model lze aplikovat i na sociální, umělecké a
biologické analogie (např. imunitní systém). Uzavření kontextu
konstatováním, že model je natolik abstraktní, že pokrývá téměř všechny
systémy s mediátorem mezi podnětem a reakcí.\
*Citace:* \"To zahrnuje nejen technické a organizační systémy, ale i
sociální, umělecké a dokonce i biologické analogie (např. imunitní
systém -- IB = antigen, CB = lymfatická uzlina, AB = protilátky).\"
