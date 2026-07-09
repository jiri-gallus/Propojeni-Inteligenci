Jak se v kybernetice nazývá proměnná, která ve zpětnovazební smyčce
určuje na co se reguluje?

V kybernetice a teorii automatického řízení se tato proměnná
nazývá **regulovaná veličina** (někdy též **řízená
veličina** nebo **výstupní veličina**).

Pokud hledáte konkrétnější termín v závislosti na úhlu pohledu, může to
být také:

- **Žádaná hodnota** (neboli **referenční hodnota**, angl. *setpoint*)
  -- to je konkrétní číselná hodnota, **na kterou** chceme regulovat
  (např. požadovaná teplota 20 °C). Tato veličina vstupuje do regulátoru
  jako žádaný stav.

- **Skutečná hodnota** (angl. *actual value*) -- to je aktuálně naměřená
  hodnota regulované veličiny, která se porovnává s žádanou hodnotou.

Nejčastěji se ale v rámci celé smyčky jako **\"to, co
regulujeme\"** označuje právě **regulovaná veličina** (značí se
obvykle **y**). Rozdíl mezi žádanou hodnotou (**w**) a skutečnou
hodnotou (**y**) se pak nazývá **regulační odchylka** (chyba,
angl. *error*).

Určitě nejde o výstupní, řízenou veličinu. Protože ta a rozdíl hledaného
termínu je regulační odchylka

Máte naprostou pravdu, omlouvám se za nepřesnost. Špatně jsem pochopil
vaši otázku -- vy se neptáte na to, **jaká hodnota** se reguluje, ale
na **termín pro proměnnou, která tuto hodnotu definuje/nastavuje** (tedy
tu, která určuje **na co** se má regulovat).

Tento hledaný termín je **žádaná
hodnota** (angl. *setpoint* nebo *reference*), značí se
obvykle **w** (popř. **r**).

A abych to uvedl na pravou míru a potvrdil vaši výhradu:

- **Regulovaná veličina (y)** = skutečný stav (např. naměřená teplota 19
  °C).

- **Žádaná hodnota (w)** = proměnná, která určuje, **na co** se reguluje
  (např. požadovaná teplota 20 °C). **To je hledaný termín.**

- **Regulační odchylka (e)** = rozdíl mezi nimi: **e = w − y**.

Děkuji za opravu -- měl jsem vaši otázku v prvním dotazu pochopit
přesněji.

co je diskrétní a jaký je opak?

V závislosti na kontextu (protože se bavíme o kybernetice, ale ptáte se
obecně) má slovo **diskrétní** dva hlavní významy a podle toho se liší i
jeho opak:

**1. V kybernetice, automatizaci a zpracování signálu**

- **Diskrétní** = **časově nespojitý** (pracuje v diskrétních časových
  okamžicích, např. počítač měří teplotu jednou za sekundu). Signál je
  znám jen v konkrétních bodech, nikoli spojitě po celou dobu.

- **Opak** = **spojitý** (angl. *continuous*). Spojitý signál má hodnotu
  definovanou v každém okamžiku (např. klasický analogový teploměr).

------------------------------------------------------------------------

**2. V matematice, logice a obecné češtině**

- **Diskrétní** = **oddělený, nespojitý, jednotlivý** (např. diskrétní
  hodnoty = 1, 2, 3, ale ne 1,5; diskrétní množina = prvky, mezi nimiž
  jsou \"mezery\").

- **Opak** = **spojitý** (např. spojitá čára, spojitá funkce, kde mezi
  libovolnými dvěma body existuje nekonečně mnoho dalších).

------------------------------------------------------------------------

**Shrnutí:** Ať už jde o čas, signál nebo množinu, opakem diskrétního je
vždy **spojitý** (v angličtině *continuous*).

V kybernetice se tyto dva přístupy liší například v regulaci:

- **Spojitá regulace** počítá neustále.

- **Diskrétní regulace** (číslicová) počítá ve skocích -- vzorkuje,
  vyhodnotí, zareaguje, pak zase čeká na další vzorek.

Teď všeobecně. Jak propojit do jednoho slova schopnost něco stvořit, ale
izničit, respektive začít a ukončit? Jde to?

Ano, jde to. Všeobecně (mimo kybernetiku) existuje několik slov, která v
sobě nesou **obojí** -- schopnost začít/zrodit i ukončit/zničit. Záleží
na tom, jaký významový odstín chcete zdůraznit:

------------------------------------------------------------------------

**Nejobecnější a nejsilnější:**

- **Tvořit a rušit** -- to jsou dva póly, ale pokud je chcete spojit v
  jedno slovo, nejblíže je **kreovat** (z lat. *creare* = tvořit) -- to
  ale neobsahuje ničení.

------------------------------------------------------------------------

**Slova, která to spojují v sobě:**

1.  **Autorství** (angl. *authorship*) -- autor dílo zahajuje (stvoří
    ho) i uzavírá (dokončí, \"zabije\" další úpravy). Ale není to úplně
    \"ničit\".

2.  **Disponovat** -- máte moc něco uvést v život i to zrušit, ale je to
    spíše \"mít k dispozici\".

3.  **Manipulovat** -- může znamenat měnit stav od vzniku po zánik.

------------------------------------------------------------------------

**Filozoficky nejsilnější termín:**

- **Bytí a nebytí** -- ale to je dvojsloví.

Pokud to má být **jedno slovo**, které v sobě obsahuje obojí jako
podstatnou vlastnost, nejlépe funguje:

- **Proměňovat** -- protože začátek i konec je jen změna stavu.

- **Určovat** -- určíte začátek i konec.

------------------------------------------------------------------------

**Nejpřesnější český výraz pro obojí v jednom:**

**Ohraničovat** -- stanovujete hranice, tím definujete začátek (stvoření
vymezením) i konec (ukončení vymezením).

------------------------------------------------------------------------

**Anglické termíny, které se někdy přejímají:**

- **Orchestrovat** -- řídit od začátku do konce včetně ukončení.

- **Iniciovat a terminovat** -- ale to jsou dvě slova.

------------------------------------------------------------------------

**Pokud chcete opravdu jedno slovo, které v sobě nese obojí přirozeně:**

- **Vládnout** -- vládce může stvořit i zrušit.

- **Rozhodovat** -- rozhodnutí může být \"budiž\" i \"nechť není\".

------------------------------------------------------------------------

**Nejlepší kandidát na jedno slovo:**

**Spravovat** -- správa zahrnuje zřízení, údržbu i zrušení.

Pokud jde o **akt samotný**, pak:

**Ustavit** -- ustavíte, ale ustavení může být i zrušeno dalším
ustavením (obnova).

------------------------------------------------------------------------

**Závěr:**\
Neexistuje jedno jediné běžné slovo, které by výhradně znamenalo \"umět
stvořit i zničit\". Ale **nejblíže** se k tomu svým významem dostává:

- **Proměňovat** (začátek i konec je jen forma proměny)

- **Ohraničovat** (definujete existenci i neexistenci hranicí)

- **Disponovat** (mít plnou moc nad existencí)

Pokud byste chtěli **odborný termín**, ve filozofii se používá **kreace
a anihilace** -- ale to jsou dvě slova. V jediném slově by to
byla **kreanihilace** (neologismus), ale to není běžný výraz.

Poud mám kybernetický systém, kde jeden blok má moc vytvořit a nechat
zaniknout jiný blok, je vhodné že blok A určuje životnost libovolného
počtu bloků B? Jak to udělat elegantní? Aby tato věta byla kyberneticky
jasná, ale co nejkratší?

Ano, je to nejen vhodné, ale v kybernetice a teorii systémů naprosto
běžné. Říká se tomu **řízení životního cyklu** (lifecycle management)
nebo **správa existence** (existence management).

Pro vaši větu \"blok A určuje životnost libovolného počtu bloků B\" bych
navrhoval tyto **elegantní a kyberneticky korektní zkratky** (seřazeno
od nejodbornějšího po nejsrozumitelnější):

------------------------------------------------------------------------

**1. Nejkratší a nejkybernetičtější (pouze 4 slova):**

**\"A řídí životnost B.\"**

- V kybernetice slovo **řídí** (reguluje) implicitně zahrnuje obojí --
  vznik (inicializaci), průběh i zánik (terminaci). Nemusíte to dál
  rozvádět.

------------------------------------------------------------------------

**2. Odborně a přesně (5 slov):**

**\"A je správcem životního cyklu B.\"**

- **Správce** (angl. *manager*) je v kybernetice ustálený termín pro
  blok, který vytváří, udržuje a ruší jiné bloky.

------------------------------------------------------------------------

**3. Nejpřesnější systémový termín (6 slov):**

**\"A autorizuje existenci libovolného počtu B.\"**

- **Autorizuje** = dává povolení k bytí, ale i k nebytí. Krásně
  vystihuje tu dvojí moc.

------------------------------------------------------------------------

**4. Pokud chcete zdůraznit \"libovolný počet\" (škálovatelnost):**

**\"A je nadřazeným regulátorem životnosti množiny B.\"**

------------------------------------------------------------------------

**5. Extrémně strohá (pro blokové diagramy):**

**\"A → lifecycle(B)\"**

- To je zápis, který použijete v blokovém schématu -- šipka od A k bloku
  s nápisem *lifecycle* u B.

------------------------------------------------------------------------

**6. Pokud chcete česky a srozumitelně pro lidské čtenáře:**

**\"A spravuje vznik a zánik B.\"**

------------------------------------------------------------------------

**Co bych doporučil jako nejlepší kompromis mezi odborností, krátkostí a
elegancí?**

**\"A je správcem životního cyklu libovolného počtu B.\"**

- **Správce** -- v kybernetice standardní role.

- **Životní cyklus** -- zahrnuje vznik, trvání i zánik.

- **Libovolný počet** -- vyjadřuje škálovatelnost, aniž byste museli
  řešit, kolik jich je.

------------------------------------------------------------------------

Pokud chcete **ještě o slovo kratší** a přesto naprosto jasné:

**\"A spravuje existenci B.\"**

Tím říkáte vše -- existence zahrnuje obojí a \"spravuje\" dává A plnou
moc.

Připrav cele kontextové pole k archivaci paměti. Potřebuji rozdělit
kontext na logické celky o tom, co jsme probírali, opatřit je názvem,
krátkým popisem a citací, kterou úsek začíná. Postup: - Rozděl kontext
podle tématu (nejdi do detailů, 2-20 paměťových částí) - Indexuj část
(01, 02, 03, \... 20) - Vymysli krátký název (max. 4 slova) - Vymysli
krátký popis aby bylo jasno co která část obsahuje (max. 4 věty) - Vypiš
přesnou citaci začátku textu (max. 10 slov) pro zpětnou dohledatelnost v
textovém editoru (ctrl+f). - Musíš obsáhnout celé kontextové pole. 01
část je od citace 01 po citaci 02.

Ano, připravím kompletní kontextové pole k archivaci paměti. Rozdělím
celý průběh našeho rozhovoru do logických celků.

------------------------------------------------------------------------

**KONTEXTOVÉ POLE -- ARCHIVACE PAMĚTI**

------------------------------------------------------------------------

**01 \| REGULOVANÁ VELIČINA V KYBERNETICE**

**Popis:** Vysvětlení základního kybernetického pojmu regulovaná
veličina, její značení (y) a vymezení vůči žádané hodnotě (w) a
regulační odchylce (e).\
**Citace začátku:** *\"V kybernetice a teorii automatického řízení se
tato proměnná nazývá regulovaná veličina\...\"*

------------------------------------------------------------------------

**02 \| ŽÁDANÁ HODNOTA JAKO URČUJÍCÍ PRVEK**

**Popis:** Upřesnění, že hledaným termínem pro proměnnou určující \"na
co se reguluje\" je žádaná hodnota (setpoint). Korekce předchozí
odpovědi a rozlišení mezi žádanou hodnotou, regulovanou veličinou a
regulační odchylkou.\
**Citace začátku:** *\"Máte naprostou pravdu, omlouvám se za
nepřesnost\...\"*

------------------------------------------------------------------------

**03 \| DISKRÉTNÍ A JEHO OPAK -- SPOJITÝ**

**Popis:** Vysvětlení pojmu diskrétní ve dvou kontextech -- v
kybernetice (časově nespojitý signál) a v matematice/obecné češtině
(oddělený, nespojitý). Opakem je vždy spojitý (continuous). Zmíněn
rozdíl mezi spojitou a diskrétní regulací.\
**Citace začátku:** *\"V závislosti na kontextu (protože se bavíme o
kybernetice, ale ptáte se obecně) má slovo diskrétní dva hlavní
významy\...\"*

------------------------------------------------------------------------

**04 \| JEDNOSLOVNÉ VYJÁDŘENÍ TVOŘENÍ A NIČENÍ**

**Popis:** Hledání jednoho slova, které v sobě nese schopnost stvořit i
zničit (začít i ukončit). Navrženy varianty jako proměňovat,
ohraničovat, disponovat, spravovat, vládnout. Nejlepším kandidátem je
proměňovat, případně spravovat.\
**Citace začátku:** *\"Ano, jde to. Všeobecně (mimo kybernetiku)
existuje několik slov, která v sobě nesou obojí\...\"*

------------------------------------------------------------------------

**05 \| SPRÁVCE ŽIVOTNÍHO CYKLU BLOKŮ**

**Popis:** Aplikace předchozí úvahy na kybernetický systém -- blok A má
moc vytvářet a rušit bloky B. Navrženy elegantní a krátké formulace pro
tuto skutečnost, od odborných (A řídí životnost B) po srozumitelné (A
spravuje vznik a zánik B). Doporučený termín správce životního cyklu.\
**Citace začátku:** *\"Ano, je to nejen vhodné, ale v kybernetice a
teorii systémů naprosto běžné\...\"*

------------------------------------------------------------------------

**06 \| POKYN K ARCHIVACI KONTEXTOVÉHO POLE**

**Popis:** Zadání uživatele na vytvoření strukturovaného archivačního
záznamu -- rozdělení kontextu na logické celky s názvem, popisem a
úvodní citací pro zpětnou dohledatelnost.\
**Citace začátku:** *\"Připrav cele kontextové pole k archivaci
paměti\...\"*

------------------------------------------------------------------------

**KONTROLA POKRYTÍ:** Celý rozhovor od první otázky po poslední zadání
je obsažen v částech 01--06
