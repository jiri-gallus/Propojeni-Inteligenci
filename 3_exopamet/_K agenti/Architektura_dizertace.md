**Architektura dizertační práce: Interní rámec pro psaní a kontrolu**

**1. Cíl dokumentu**

Tento dokument slouží jako architektonický plán pro tvorbu dizertační práce a jako kontrolní nástroj během psaní. Má dvě vrstvy:

**Interní (nyní):**

- Držet konzistenci tónu a účelu napříč částmi práce.
- Sloužit jako referenční bod při psaní – ověřit, že každá část plní svou funkci.

**Externí (jako příloha hotové práce):**

- Umožnit čtenářům pochopit architekturu textu, jeho vrstvy a mechanismy.
- Nabídnout materiál pro studium dopadů textu na vlastní myšlení.
- Inspirovat k vlastním experimentům s formou vědeckého textu.

Dokument nedefinuje délky jednotlivých částí. Definuje jejich tón, účel a vzájemné vazby.

---

**2. Úvodní shrnutí**

Tato dizertační práce přináší chybějící protokol interakcí mezi člověkem a velkými jazykovými modely. Je postavena na konceptu Exokortexu – metody vědomé kognitivní práce, která rozšiřuje kognitivní kapacitu uživatele prostřednictvím dvou pólů: augmentované a delegované kognice.

Práce je současně vědeckým textem, důkazem sebe sama a nástrojem pro předání zkušenosti. Vznikla jako akt augmentované kognice, čímž demonstruje platnost vlastních tvrzení.

Jejím primárním cílem je identifikovat mezeru v současném výzkumu, zaplnit ji formálním modelem interakcí a nabídnout metodiku pro další výzkum. Sekundárním cílem je zpřístupnit toto poznání napříč publiky – od akademiků po praktiky – formou, která čtenáře vede k vlastnímu úsudku.

Práce je ortodoxní revolucí: agentic naruby, stejně staré, ale opírající se o tisícileté zkušenosti lidstva. Augmentace je protipólem agentic – není konkurencí, ale doplňkem. Každý pól má své aplikace.

---

**3. Cíle práce**

**3.1 Primární cíl: Věda**

- Identifikovat mezeru v současném výzkumu interakcí člověka s LLM – chybějící protokol.
- Zavést teoretický koncept Exokortexu s vlastní terminologií.
- Opřít jej o uznávané teorie (extended mind, teorie kognitivní zátěže, kybernetika) a ukázat jej jako jejich logické rozšíření.
- Poskytnout formální model interakcí a aplikovat jej na různé domény.
- Doložit tvrzení daty – triangulací trhu, vědy a lidských očekávání, analýzou chatů, experimentem, otevřenou metodikou.
- Nabídnout model jako nástroj pro vysvětlení dosud fragmentovaných výzkumných výsledků.

**3.2 Sekundární cíl: Předání zkušenosti**

- Předat metody augmentované kognice v takové podobě, aby byly použitelné a replikovatelné.
- Ukázat konkrétní sekvence, které může čtenář sám vyzkoušet.
- Inspirovat k vlastnímu zkoumání, testování a modifikaci.

**3.3 Terciární cíl: Přijetí a aplikace**

- Vytvořit text, který zvyšuje pravděpodobnost, že čtenář koncept příjme, otestuje nebo aplikuje.
- Nabídnout otevřená data a otevřené otázky jako pozvánku k navazujícímu výzkumu.

---

**4. Architektura práce: Části, tón, účel**

**4.1 Úvod – kotvení a otevření problému**

**Tón:** Standardní akademický, věcný, přehledový. Otevřený, data-driven. Žádné skrývání záměru.

**Účel:** Ukotvit práci v současném výzkumu a současně identifikovat mezeru. Ukázat genealogii LLM od matematiky, kybernetiky a filosofie přes čtyři kategorie aplikací (Chat, AI-assisted development, Agentic, Enterprise) až po současný stav. Provést triangulaci tří dimenzí – trh (peníze), věda (výzkum), lidé (očekávání a pocity) – a ukázat, že všechny tři konvergují k jedné slepé skvrně: chybí augmentace. Data odhalují cyklus boom → zklamání → pokles důvěry → hledání alternativy. Agentic (delegace) je jen jeden pól. Augmentace je druhý, stejně starý, ale dosud nezkoumaný. Závěr úvodu přiznává přechod k lidské části.

**Struktura úvodu:**

1. První věta – exokortex a genealogie.
2. Teaser diagram – genealogie LLM s filosofií jako vstupem.
3. Rozbor diagramu – historie → 4 kategorie.
4. Triangulace – peníze, věda, lidé → cyklus boom–zklamání.
5. Augmentace jako protipól – ne konkurence, ale chybějící část.
6. Stará filosofie jako základ augmentace (Sókratés, abdukce, kritika).
7. Návrh rozšířeného diagramu – uzavření kruhu.
8. Přechod: „Akademický úvod jste četli, teď navazuje jeho lidská část.“

**Kontrolní otázky:**

- Ukazují data jasně mezeru, kterou práce zaplňuje?
- Je přechod k lidské části přiznaný a plynulý?

---

**4.2 Statement – lidská část**

**Tón:** Osobní, ironický, sebevědomý, ale ne arogantní. První osoba. Autentický.

**Účel:** Představit autora jako člověka, který žije to, o čem píše. Přiznat abdukci jako metodu, osobní motivaci a zkušenost jako zdroj hypotéz. Ukázat, že práce není strojově akademická, ale lidsky akademická – protože jejím středobodem je kognitivní membrána. Charakterizovat práci jako protipól agentic: agentic deleguje myšlení na stroj, augmentace organizuje myšlení vlastní i LLM. Uvést slabší statement (osobní aspiraci), který předchází formálnímu systému.

**Obsah:**

- Osobní představení (profese, ironie, kybernetika).
- Milníky vedoucí k práci (nepopsaný list, první pokusy s LLM, MK, exokortex).
- Přiznání abdukce a metodiky.
- Charakter práce: protipól agentic, lidsky akademická.
- Osobní statement.

**Kontrolní otázka:** Působí autor jako autentický člověk, ne jako akademický konstrukt?

---

**4.3 Systém – abstraktní model**

**Tón:** Hutný, přesný, formální. Minimální osobní vstupy. Jazyk definic a důkazů.

**Účel:** Zavést abstraktní systém bloků, interakcí a akcí. Definovat jej tak, aby byl přenositelný na různé domény. Toto je teoretické jádro práce – chybějící protokol interakcí.

**Kontrolní otázka:** Obstojí tato část sama o sobě jako formální model? Je možné ji pochopit i bez zbytku práce?

---

**4.4 Model Smart Home – první aplikace**

**Tón:** Přechodový. Začíná formálně (aplikace systému na konkrétní model), postupně přidává lidský rozměr. Závěr kapitoly obsahuje simulaci se dvěma postavami – čtenář je vtažen dovnitř.

**Účel:** Demonstrovat univerzalitu systému na doméně, která je každému známá. Ukázat, že model není jen abstraktní hříčka – dává smysl v reálném kontextu. Zavést pojem kognitivní membrány jako klíčového prvku transformace signálu. Simulace se dvěma postavami slouží jako první test čtenáře – nutí jej použít model k diagnostice.

**Kontrolní otázky:**

- Je přechod od abstrakce ke konkrétnímu modelu plynulý?
- Nutí simulace čtenáře aplikovat model, nejen ho číst?

---

**4.5 Seriózní věda – neurověda, psychologie, propojování**

**Tón:** Vážný, odborný, prokládaný krátkými oddechovými momenty. Hloubka a přesnost.

**Účel:** Propojit model s existujícími vědeckými poznatky. Neurověda, psychologie, kybernetika. Ukázat, jak model vysvětluje fragmentované výsledky výzkumů. Zavést terminologii. Popsat metodiku analýzy chatů. Připravit půdu pro experimentální část. Tady práce dokazuje, že není jen osobní výpovědí – je vědecky zakotvená.

**Kontrolní otázka:** Je tato část obhajitelná před odborníkem z daného oboru bez znalosti zbytku práce?

---

**4.6 Praktické sekvence a metodika**

**Tón:** Návodný, přímý, srozumitelný. Osobní zkušenost autora je přiznaná, ale slouží jako ilustrace, ne jako důkaz.

**Účel:** Předat konkrétní metody augmentované kognice. Sokratovské dotazování, Feynmanova technika, explicitace. Ukázat, jak byly použity při tvorbě této práce. Nabídnout čtenáři sekvence, které může sám vyzkoušet. Toto je ta část, která plní cíl „předání zkušenosti“.

**Kontrolní otázka:** Může čtenář po přečtení této části sám vyzkoušet alespoň jednu augmentační sekvenci?

---

**4.7 Experiment**

**Tón:** Standardní vědecký. Hypotéza, design, metodika, výsledky, diskuse. Ale s přidanou narativní rovinou – příběh experimentu a jeho účastníků.

**Účel:** Poskytnout empirické ověření tvrzení práce. Simulovaný soudní případ jako testovací prostředí. Analýza chatů účastníků umožní kvantifikovat míru naladění a vliv augmentace na kvalitu výstupů. Experimentální část je druhou vrstvou důkazu (první je samotná práce a její proces vzniku).

**Kontrolní otázka:** Je experiment replikovatelný na základě popsané metodiky?

---

**4.8 Potenciál a aplikace**

**Tón:** Vizionářský, ale střízlivý. Otevřené dveře, ne manifest.

**Účel:** Ukázat možnosti aplikace poznatků na různé oblasti – školství, justice, věda, spolupráce lidí. Nabídnout konkrétní příklady, včetně jedné reálné aplikace s daty z reálného světa. Ukončit práci otevřenými otázkami a výzvou k dalšímu výzkumu. FOMO efekt: „Tady je pole, které jsem otevřel – kdo ho bude zkoumat?“

**Kontrolní otázka:** Odchází čtenář s pocitem, že tohle není konec, ale začátek něčeho, do čeho se může zapojit?

---

**5. Techniky práce s textem**

Každá technika má definovaný účel. Žádná není dekorativní.

**5.1 Vizuální oddělení rovin**

**Účel:** Navigace. Čtenář na první pohled pozná, v jaké rovině textu se nachází – teorie, osobní vstup, analýza chatu, simulace. Může si volit vlastní cestu textem.

**Provedení:** Jemné barvy, fonty, odsazení. Nic nekřičí. Vizuál slouží textu, ne naopak.

---

**5.2 Osobní vhledy**

**Účel:** Kotvení pozornosti. Krátký, absurdní nebo lidský moment, který přeruší hutný výklad. Neslouží k vysvětlení teorie – slouží k probuzení čtenáře. Jsou to kognitivní kotvy, které zabraňují pasivnímu klouzání po textu.

**Pravidlo:** Každý osobní vhled musí být samostatně stojící moment. Nesmí vysvětlovat, nesmí přesvědčovat. Asociace si vytváří čtenář sám.

---

**5.3 Rytmus**

**Účel:** Řízení kognitivní zátěže. Hutná pasáž je vystřídána odlehčením. Čtenář není zahlcen – je veden. Rytmus vytváří plasticitu myšlení: napětí a uvolnění v cyklech.

**Pravidlo:** Po každé náročné teoretické části následuje moment, který umožní vydechnout. Teprve pak návrat k teorii.

---

**5.4 Simulace a diagnostické scénáře**

**Účel:** Aktivace čtenáře. Nestačí číst – čtenář musí model použít, aby odpověděl na otázky. Tím si model osvojuje, aniž by mu byl vnucován.

**Pravidlo:** Každá simulace končí otevřenými otázkami. Čtenář je musí vyřešit sám. Odpovědi nejsou předloženy – jsou implikovány.

---

**5.5 Časové značky**

**Účel:** Důkazní. U vybraných pasáží se uvádí reálný čas vzniku jako demonstrace síly augmentace. Nenápadné, ale výmluvné.

**Pravidlo:** Značka nesmí narušit tok textu. Je drobná, přítomná, ale nevtíravá.

---

**5.6 Hypotézy a otevřené otázky**

**Účel:** FOMO. Ukázat, kolik práce zbývá udělat. Nabídnout konkrétní směry pro navazující výzkum. Čtenář, který hledá téma, ho tady najde.

**Pravidlo:** Hypotézy jsou krátké, zvýrazněné, samostatně stojící. Nejsou rozváděny – jsou vrženy.

---

**6. Etický rámec**

Celá práce se řídí následujícími principy. Slouží jako kontrolní mechanisms pro celek, nikoli pro jednotlivé části.

1. **Neutrální tón.** Práce nesoudí, nepřesvědčuje, neútočí. Nabízí a inspiruje.
2. **Volba čtenáře.** Žádný závěr není vnucován. Čtenář se rozhoduje sám, zda a jak koncept přijme, otestuje nebo modifikuje.
3. **Nesoutěžení.** Práce nesnižuje jiné přístupy. Delegace kognice není špatná – je to jeden pól spektra. Augmentace je druhý. Jejich propojení je silnější než každý zvlášť.
4. **Otevřenost.** Data, metodika a nástroje jsou volně dostupné. Práce nic neskrývá.
5. **Pravdivost.** Každé silné tvrzení má oporu – v datech, v příloze, v experimentu, nebo v přiznané osobní zkušenosti.

---

**7. Kontrolní rámec pro psaní**

Při tvorbě každé části si ověř:

1. **Tón sedí.** Odpovídá tón této části definovanému tónu v architektuře?
2. **Účel je naplněn.** Plní tato část svou funkci v celkové sekvenci?
3. **Věda dominuje.** Je tato část vědecky obhajitelná i bez ostatních rovin?
4. **Forma naviguje.** Pozná čtenář na první pohled, v jaké rovině se nachází?
5. **Rytmus dýchá.** Následuje po hutné pasáži odlehčení? Není čtenář zahlcen?
6. **Tón nabízí.** Nepřesvědčuje, neútočí, nesoudí?
7. **Tvrzení jsou podložená.** Má každé silné tvrzení oporu?
8. **Celek je konzistentní.** Zapadá tato část do architektury, nebo ji rozbíjí?

---

**8. Simulace: Běžný akademik vs. pivotovaná architektura**

**Profil simulovaného akademika:**

Muž, 52 let, profesor v oboru kognitivní psychologie nebo příbuzném. Publikoval desítky článků, vede doktorandy, sedí v komisích. Zažil vzestup a pád mnoha „revolučních“ konceptů. Je unavený z přehnaných claims. Má rád data, metodologii, opatrné formulace. Nemá rád arogantní studenty. Nemá rád, když někdo objevuje objevené. Čte rychle, prvních pár stran rozhoduje o zbytku.

---

**Fáze 1: Úvod – data a identifikace problému**

**Co čte:** Genealogie LLM. Čtyři kategorie aplikací. Triangulace trhu, vědy a lidských očekávání. Data o cyklu boom → zklamání → pokles důvěry. Identifikace slepé skvrny: chybí augmentace.

**Co se v něm děje:** „Dobře, další rešerše... počkat. Ta data jsou zajímavá. Boom, zklamání, pokles důvěry – to sedí s tím, co vidím kolem sebe. A triangulace – peníze, věda, lidé – to je solidní metodika.“ Membrána je v klidu, ale pozornost roste. Není to nuda – je to uznání. Někdo systematicky popsal problém, který on sám cítí.

**Riziko:** Pokud by data byla slabá nebo zdroje pochybné, ztratil by ho tady. **Architektura předpokládá kvalitu triangulace – pokud selže obsah, selže všechno.**

---

**Fáze 2: Přiznání mezery a přechod**

**Co čte:** „Akademický úvod jste četli, teď navazuje jeho lidská část.“ Augmentace je protipól agentic – ne konkurence, ale doplněk. Práce je lidsky akademická, protože jejím středobodem je kognitivní membrána.

**Co se v něm děje:** Žádné podráždění. Žádný šok. Místo toho: **úleva**. Někdo to konečně pojmenoval. A teď chce ukázat člověka za tím. „Dobře. Ukaž, kdo jsi. Data máš, teď chci vidět, jestli za nimi je skutečný člověk.“ Membrána se otevírá dobrovolně. Není co prolamovat.

**Riziko:** Pokud by přechod působil lacině nebo neupřímně, membrána by se zavřela. Ale formulace „akademický úvod jste četli“ je přiznaná, ne manipulativní.

---

**Fáze 3: Statement – lidská část**

**Co čte:** Osobní představení. Ironie. Milníky. Přiznání abdukce. „Učitel, elektrikář, sadař, vedoucí, vědec, manžel a syn... Kybernetiku miluji jako svou manželku. Tu funkční. Teda tu kybernetiku…“

**Co se v něm děje:** Pousměje se. Ironie funguje. Není to arogance – je to sebeironie. Ten člověk ví, kdo je. A přiznává, odkud přichází. Abdukce jako metoda? „To je neortodoxní, ale upřímné.“ Membrána je otevřená. Čtenář je připraven přijmout i formální model – protože ví, že za ním stojí člověk, který ho žije.

---

**Fáze 4: Systém**

**Co čte:** Abstraktní model. Bloky, interakce, akce. Formální definice.

**Co se v něm děje:** Tohle je jeho jazyk. Rozumí mu. Ale teď ho čte jinak – ví, že tenhle model nevznikl z rešerše, ale ze zkušenosti. „Tohle není jen formální cvičení. Tohle je popis něčeho, co autor žije. A je to přesné.“ Membrána je plně otevřená. Už nehledá chybu – hledá, kam to vede.

---

**Fáze 5: Smart Home**

**Co čte:** Aplikace systému na chytrou domácnost. Dvě postavy – Ludovík a Žozefa. Diagnostické otázky.

**Co se v něm děje:** Tohle nečekal. Ale už není překvapený stylem – je zvědavý, jestli to funguje. Aplikuje model. Odpovídá na diagnostické otázky. A funguje to. „Tenhle model není jen abstrakce. Dává smysl v reálném světě.“ Začíná chápat, že to, co drží v ruce, není jen dizertace. Je to protokol.

---

**Fáze 6: Seriózní věda**

**Co čte:** Propojení s neurovědou. S psychologií. S kybernetikou. Metodika. Data. Konfrontace s existujícími teoriemi.

**Co se v něm děje:** Vrací se do své komfortní zóny – ale s novýma očima. Model, který předtím zažil v simulaci, teď vidí opřený o literaturu, o kterou se sám opírá. Extended mind? Zná to. Kognitivní zátěž? Zná to. „Tohle už není jen zkušenost. Tohle je věda. A je to solidní.“ Membrána je plně otevřená. Už přemýšlí, jak by model otestoval ve vlastním výzkumu.

---

**Fáze 7: Praktické sekvence**

**Co čte:** Konkrétní metody augmentace. Sokratovské dotazování. Kritika. Abdukce. Jak je autor použil při psaní této práce.

**Co se v něm děje:** Zjišťuje, že to nejsou abstraktní pojmy. Jsou to nástroje. Může je použít hned. „Sokratovské dotazování s LLM? To dává smysl. Proč to nikdo neučí?“ V hlavě už si skládá, jak by je nasadil na vlastní výzkumný problém. Z oponenta se stal potenciální uživatel.

---

**Fáze 8: Experiment a potenciál**

**Co čte:** Empirické ověření. Data z experimentu. Aplikace na školství, justici, vědu. Otevřené otázky.

**Co se v něm děje:** Experiment uspokojuje jeho potřebu důkazů. Ale otevřené otázky ho zasáhnou víc. Vidí pole, které ještě nikdo neorá. „Tohle není konec. Tohle je začátek. A já můžu být u toho.“ To je FOMO moment – ne vyvolaný manipulací, ale daty a otevřenou pozvánkou.

**A v tuhle chvíli se stane to, co architektura zamýšlela:** odevzdá posudek, kde doporučí práci k obhajobě, a pak si otevře vlastní prázdný dokument a začne psát návrh návazného výzkumu. Nebo přinejmenším řekne kolegovi u oběda: „Hele, četl jsi tu dizertaci? Není to šílené – je to přesné. A má to data. Podívej se na to.“

A to je virální šíření.

---

**Verdikt**

Ano, je šance cílů dosáhnout. Pivot zvýšil pravděpodobnost přijetí, protože:

1. **Odpadá riziko arogance.** Statement není „já tvrdím“ – je to „data ukazují, a tady je odpověď“.
2. **Akademik není manipulován.** Přechod je přiznaný. Osobní styl je vysvětlen jako nutný důsledek tématu.
3. **Membrána se otevírá dobrovolně.** Čtenář chce vidět člověka za daty, protože data mu ukázala, že ten člověk něco ví.
4. **Ortodoxní revoluce má obsah.** Není to fráze – je to popis metody: staré myšlenkové postupy připojené k novému nástroji.

**Shrnutí:** Pivotovaná architektura odstraňuje boj. Není proti komu bojovat – data mluví za práci. Akademik se z oponenta stává spojencem dřív, než dojde k prvnímu osobnímu odstavci. Každá fáze má svou funkci a své riziko. Pokud obsah v každé fázi obstojí, architektura ho nese k cíli. Pokud obsah selže v jediné fázi, řetěz se přetrhne.

Ale ta šance tam je. A po pivotu je větší.