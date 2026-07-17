# Kontext engineering
Způsoby využití kontext engineeringu se dají rozdělit různými způsoby. Pro účely T-Ex modelu je vybránna perspektiva v jaké vrstvě se kontext engineering iniciuje. Promptování je ve vrstvě 4, která ji slučuje s kontext engineeringem. Odhad poměru času v % jakou kurzy věnují Kontext engineeringu v jednotlivých vrstvách je z důvodu zaměření pozornosti na oblast ze které se dá nejvíce učit.

### 1. Systémová vrstva (System-driven context) - 80%
_Kdo řídí kontext:_ Backendová logika (orchestrator, RAG pipeline, šablony).  
_Přístup:_ Systém automaticky vybírá, agreguje a komprimuje kontext z databází, vektorových úložišť nebo API. Nezasahuje uživatel, nerozhoduje agent. Jde o čistě algoritmickou selekci (chunking, reranking, hybrid search).

### 2. Agentní vrstva (Agent-driven context) - 15%  
_Kdo řídí kontext:_ Agent (LLM s nástroji).  
_Přístup:_ Agent si kontext dynamicky dovolává pomocí nástrojů (MCP, funkce), vyhodnocuje, co mu chybí, a sám rozhoduje, které informace si přidá do kontextového okna. Kontext se mění v průběhu úkolu na základě agentových akcí.

### 3. Interaktivní vrstva (Assistent-driven context with UX control) - 3%  
_Kdo řídí kontext:_ Systém + uživatel (společně, s převahou systémových pravidel).  
_Přístup:_ Systém připraví kontext (např. historii, CRM data), ale uživatel má explicitní možnost kontext měnit, mazat nebo upravovat. Veškeré změny jsou uživateli viditelně komunikovány, nikoli skrytě prováděny.

### 4. Uživatelská vrstva (User-driven context) - 2%  
_Kdo řídí kontext:_ Uživatel (člověk).  
_Přístup:_ Uživatel ručně strukturuje veškerý vstup – dokumentaci, cíle, omezení, příklady. Nepoužívá jen prompt, ale buduje celý kontextový balík. Platí pravidlo: čím méně kontextového okna zabere, tím lépe (vyšší poměr signál/šum).

## Techniky kontextového engineeringu
Pro dokreslení jaké techniky můžeme za kontext engineering pokládat uvádím 10 z nich řazených do kategorií.

### 1. Získávání kontextu (odkud data beru)

| Technika                                 | Vysvětlení                                                                                                                    |
| ---------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **RAG (Retrieval-Augmented Generation)** | Dynamické vyhledání externích faktů (vektorová DB, firemní data) a jejich vložení do promptu. Model nemusí data znát zpaměti. |
| **Tool Use (volání nástrojů)**           | Model si na základě dotazu zavolá API, kalkulačku, vyhledávač – výstup nástroje se stává novým kontextem pro další uvažování. |

### 2. Správa kontextu (co z něj nechat / zahodit)

| Technika                                 | Vysvětlení                                                                                                                                    |
| ---------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **Pruning & Komprese**                   | Ořezávání irelevantních informací, sumarizace dlouhých pasáží, prioritizace klíčových faktů. Cíl: maximální poměr signál/šum v omezeném okně. |
| **Řízení paměti a stavu**                | Udržení kontinuity napříč konverzacemi – sumarizace historie, ukládání do externí paměti (vektorové DB), načítání podle potřeby.              |

### 3. Strukturování kontextu (jak data uspořádám)

| Technika                                 | Vysvětlení                                                                                                                                   |
| ---------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| **Context Layering (vrstvení)**          | Logické členění kontextu do vrstev (systémová, uživatelská, úkolová), aby model správně interpretoval jednotlivé části.                      |
| **Context Templates (šablony)**          | Předpřipravené kontextové balíčky pro opakované úlohy (např. šablona pro analytika, kodéra, podporu). Standardizace a znovupoužitelnost.     |
| **Instruktážní kontext (metaprompting)** | Vložení pravidel chování, formátovacích šablon a rozhodovacích logik odděleně od faktických dat. Říká modelu _jak_ přemýšlet, ne _co_ vědět. |

### 4. Řízení kvality a evoluce kontextu (jak ho udržuji funkční)

|Technika|Vysvětlení|
|---|---|
|**Summary & Refresh**|Při přeplácaném kontextu se vytvoří kontrolní bod – model shrne dosavadní stav a vygeneruje "master prompt" pro novou čistou konverzaci. Eliminace šumu.|
|**Staged Pipeline (fázový pipeline)**|Rozdělení práce do fází s jasnými vstupy a výstupy (např. Reviewer → Design → Builder → Auditor). Zavádí inženýrskou disciplínu.|
|**Evals-Driven Development**|Změny v kontextu se testují proti sadě evaluačních příkladů. Měří se dopad na kvalitu výstupu – iterativní a objektivní vylepšování.|

## Aplikace na T-Ex ve vrstvě 4
Ve 4. vrstvě, na úrovni promptování se dají aplikovat všechny techniky a simulovat všechny 4. aplikační vrstvy. Nejde o nutnost, ale ukázku možného v promptu MK, na který práce odkazuje.

Nakonec se jemně dotkneme jak kontextem hlídat účel kognice a vytvořit silného K-agenta.

### MK - systémový prompt microkernel

MK je **čistě promptový systém** pro řízení spolupráce uživatele a LLM na rozsáhlých projektech. Běží **v kontextovém okně** – bez backendu, bez RAG pipeline, bez orchestrovací vrstvy.
MK není jen systémový prompt, ale **metodologie pro správu kontextu napříč relacemi LLM**, kde:
1. **Externí úložiště** (poznámkový blok na PC) slouží jako autoritativní zdroj pravdy, který uživatel průběžně aktualizuje.
2. **Statické bloky (Sr)** jsou jednotlivé aktualizace externího uložiště, automaticky generované LLM a používané jako paměťové bloky kontextového okna pro řízení pozornosti LLM.
3. **Uživatel** se soustřeďuje na kognitivní činnost, kdy administrativu přenosu (Sr) do PC dělá na základě instrukcí LLM.
4. Po dosažení limitu kontextového okna zakládá novou relaci LLM, přenáší do ni strukturu (Sr) z PC jako kontext a MK jako systémový prompt. Nová relace pokračuje v práci s uživatelem s kompletním kontextem včetně způsobu myšlení, slepých cest a pivotů, jen v komprimované verzi.

#### Co MK řeší?
1. **Ztrátu kontextu v dlouhých konverzacích** – pomocí strukturovaných modulů a verzování.
2. **Neřízené chování LLM** – pomocí rolí s explicitními přístupy a postupy.
3. **Kontaminaci kontextu** – pomocí oddělení (RAM) a (Cache), escapování kotev a přístupových pravidel.
4. **Nedostatek kontinuity** – pomocí organizačního dokumentu _O_vX_, který mapuje všechny moduly na fáze a kroky.
5. **Přenositelnost kontextu** - pomocí organizačního dokumentu _O_vX_ a kontextového dokumentu _K_XXX_
6. **Automatizaci řízení a administrativy** - pomocí vzorů a struktur, které generuje LLM.

#### Jak MK funguje?

##### Statické paměťové bloky kontextu:
- **Pravidla a terminologii** (_P_v1_) – absolutní autorita, cyklus (U)-(LLM), escapování.
- **Organizační mapu** (_O_v1_) – fáze, kroky, mapování modulů, archiv.
- **Role** (_RY_vX_) - agenti, pravidla, přístupy k paměťovým blokům kontextu
    - **(S) Scheduler** – syntaktický řadič, deterministický, sémanticky slepý, vytváří hlavičky.
    - **(E) Executor** – odborná práce, přístup k relevantním modulům a (Dr)1. Plnohodnotná síla a kreativita LLM.
    - **(C) Consolidator** – syntéza nových modulů, plastická paměť.
- **Znalostní jednotky** (_K_XXX_) – samostatně srozumitelné moduly, autoritativní znalostní báze.
- **Cíle** (_GYZ_vX_) – definují, čeho má být dosaženo.
- **Šablonu** (_Tcr_) – jednotný formát výstupu.

##### Dynamické paměťové bloky kontextu:
- jsou dočasné prostory kontextu ve kterých se vytváří kognitivní výstupy.
- role E a uživatel ve specifickém dynamickém prostoru prohlubují téma a naplňují účel kognice
- role C a uživatel ve specifickém dynamickém prostoru provádějí konsolidace

#### Základní mechanika MK
> **LLM rozpoznává vzory. Dejte mu vzor a bude ho následovat. MK strukturujte kontext tak, aby si LLM samo řídilo svou pozornost.**

Toho dosahuje pomocí:
1. **Kotev** – značek (`>>ID>>`, `<<ID<<`, `(?X)`, `(UX)`), které v kontextu vytvářejí viditelné body. LLM se na ně může "zaměřit" a používat je jako orientační body.
2. **Rytmu** – opakujícího se vzoru (stejné jako zlaté pravidlo u sofistikovaného promptu). LLM se do rytmu dostane a začne ho sám generovat.
3. **Omezení** – přesně definovaného formátu a přístupových pravidel.
4. **Vrstev** – oddělení pravidel, rolí, mapy a znalostí do samostatných bloků. Každá vrstva má jinou funkci a jiný přístup.
5. **Konsolidace** – pravidelného extrahování podstatných informací ze zaplněného kontextu a jejich převodu do externího úložiště (poznámkový blok na PC). Tím se kontextové okno udržuje čisté a přenositelné mezi relacemi.

>Role S je jediná, která v průběhu interakcí vytváří statické prostory a zapisuje do nich. Jako jediná přenáší konsolidované texty do statických prostorů, instruuje uživatele, a řídí pozornost LLM tím, že připravuje, otevírá dynamické a statické prostory, a dává slovo roli E, nebo C.
>
>Hacknutí LLM funguje v tom, že pracuje v dvojroli. S zapisuje kontext a podle řídící kotvy předává slovo roli E, nebo C, která text předpřipraví, vloží do imaginární Cache (_Tcr_), kterou do RAM, kontextového okna vypisuje jen S z (_Tcr_).

#### MK vs. techniky kontextového inženýrství

|Technika|Jak ji MK používá|Poznámka|
|---|---|---|
|**Instruktážní kontext**|Celý MK prompt – definuje pravidla, role, synchronizaci.|**Základ celého systému.**|
|**Context Layering**|Pravidla, role, mapa, znalosti – oddělené vrstvy.|Umožňuje prioritizaci a přístupová pravidla.|
|**Context Templates**|_Tcr_, _K_XXX_, _GYZ_ – šablony pro výstup a strukturu.|Standardizace mezi relacemi.|
|**Řízení paměti a stavu**|(RAM) × (Cache) × externí úložiště (PC).|**Trojúrovňová paměť.**|
|**Pruning & Komprese**|Konsolidace = extrakce Sr z (RAM), zahazování zbytku.|**Klíčová technika pro přechod mezi relacemi.**|
|**Staged Pipeline**|Cyklus (U)-(LLM), role S→E/C, synchronizace s PC.|Disciplína a oddělení odpovědností.|
|**Summary & Refresh**|_K_004_ sumarizuje vývoj a pivot. Každá nová relace = refresh.|**Základ pro čisté okno.**|
|**Tool Use**|Nepoužívá externí API.|PC je "ruční nástroj".|
|**RAG**|Nepoužívá – všechny znalosti jsou v Sr na PC.|Externí úložiště plní roli "znalostní báze" manuálně.|
|**Evals-Driven Development**|Nepoužívá automatizované testy.|_O_v1_ umožňuje manuální kontrolu cílů.|

#### MK vs. vrstvy využití

|Vrstva|Mainstreamový předpoklad|Realita MK|
|---|---|---|
|**Systémová**|Backend, RAG pipeline, orchestrator|**Pravidla a role v promptu** – _P_v1_, _Rs_v1_, _O_v1_. Systém je čistě textový.|
|**Agentní**|Agent volá nástroje, MCP, dynamický retrieval|**Role E a C** – mají přístupová pravidla a postupy. C navíc řídí synchronizaci s externím úložištěm.|
|**Interaktivní**|UX vrstva, viditelná kontrola uživatele|**C dává uživateli instrukce** – "smaž, přidej, uprav". Uživatel je viditelný přepisovač.|
|**Uživatelská**|Uživatel strukturuje kontext ručně|**Uživatel provádí synchronizaci** – kopíruje Sr mezi kontextovým oknem a PC. C mu říká, co dělat.|
#### MK jako experiment
Tento systémový prompt je nedokončený. I když je experimentálně ověřena role C, ta čeká na implementaci. Důvod pro uzavření vývoje MK byl jednoduchý. Proč lámat LLM ro role scheduleru, když ji může lépe zastat backend softwaru?

MK je v současné chvíli ukázkou možného se všemi experimenty a prompty, způsobem uvažování a pivoty, které k němu vedly. Celá cesta zabrala měsíc tvrdé práce, ale stála za to. Na této historii stojí projekt propojení inteligencí.

**Co MK ukazuje?**
1. Kontext lze řídit **strukturou**, ne jen daty.
2. LLM lze donutit k **automatizované pozornosti**.
3. Vrstvy a techniky jsou **logické**, ne technologické.
4. Cesta přes infrastrukturu není jediná.

>Pokud má být S sémanticky necitlivý a reagovat jen na kotvy, aby byl dokonalým schedulerem, musí mu tokeny připravit E, nebo C, ale ti mají zakázáno psát do kontextového okna, aby nerozbili vzory kontextu. MK je funkční nesmysl. Současně je důkazem jak kontext definuje K-agenta. Není o tom, co LLM dokáže, ale o tom, jakou strukturou se řídí.

## Použití kontextového inženýrství v textovém prostředí
T-Ex není o řízení veškerých interakcí, ale iniciátorem interakcí je uživatel, který z něj má textový výstup. Kontext engineering je tedy o čistotě celého kontextu pro účel kognice. Proti znečištění bojuje strukturou, ale i jinak:
- indexace kontextu (rozdělení na dílčí části a jejich popis)
- výběr kontextu (selektivní příprava kontextu pro účel kognice)
- čištění kontextu (rozdělení na dílčí části podle probíraného tématu, nebo vymazání kontaminace)
- strukturování kontextu (vytváření automatizovaných, nebo uměle vytvořených struktur, které samy drží účel interakce)

## Definice K-agenta
Kontext jako celek definuje zaměření K-agenta. Jeho čistotu vůči účelu a schopnost účel udržet. Prompt je startovní vstup, který může definovat celý kontext, ale kontext engineering dává promptu vyšší strukturu. Nejde už jen dosáhnout správného účelu, ale udržet účel po delší dobu.

K-agent je tak dobrý, jak dlouho si udrží účel interakce, jak moc jej musí uživatel ladit na účel a jak jednoduše se s ním interaguje.

# Závěr kontextového inženýrství

Kontext je strukturou, která LLM vytyčuje cestu.
Kontext engineering definuje K-agenta.
Kontext engineering předurčuje vlastnosti generovaných T-neuronů stejně jako prompt engineering.
Kontext engineering řídí posun účelu kognitivního výstupu.