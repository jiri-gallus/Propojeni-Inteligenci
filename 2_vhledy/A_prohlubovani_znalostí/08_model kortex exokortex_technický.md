**Bod 1: Požadavek na model – zavedení pojmů a vztahů**

---

### 1.1 Východisko

Model kognicí člověka je aplikací systému interakcí [IB]–[CB]–[AB] na interakci uživatele s LLM. Systém interakcí definuje [IB] jako iniciátora, [CB] jako prostor interakce a [AB] jako generátor výstupu. Pro účely popisu kognitivních procesů v interakci tento model zpřesňuje, co se uvnitř [IB] a v jeho vztahu k [CB] odehrává.

Nejedná se o anatomický model mozku. Nejde o biochemii, cytoarchitekturu ani přesné nervové dráhy. Model si z neurovědy, biologie a psychologie půjčuje pouze to, co je pro popis interakce podstatné – a záměrně zanedbává detaily, které nemají vliv na chování systému na úrovni interakce. Toto zjednodušení je metodologické: modelujeme interakci, nikoli mozek.

---

### 1.2 Důsledek interakce na [IB]

Systém interakcí stanovuje (princip 4), že výstup do [IB] mění parametry [IB]. V kontextu interakce s LLM to znamená, že každá interakce uživatele s modelem má přímý dopad na vnitřní nastavení jeho kognice – přepisuje jeho parametry, mění jeho váhy a predispozice. Interakce tedy není pouze výměnou signálů, ale trénovacím vzorkem, který kontinuálně formuje kognici uživatele.

---

### 1.3 Zavedení pojmů

Pro účely modelování kognice v interakci zavádíme tři funkční pojmy:

**Kortex** – funkční celek, který integruje zpracování vstupů, generování výstupů a řízení interakcí. Je nositelem kognitivních procesů.

**Kognitivní membrána** – vstupní rozhraní kortexu. Transformuje signály z prostředí (včetně výstupů z LLM) před vstupem do pole kognicí. Filtruje, zesiluje, tlumí a váží vstupní signály.

**Pole kognicí** – aktivní prediktivní jádro kortexu. Generuje predikce o stavu světa, vyhodnocuje predikční chybu a produkuje kognitivní výstupy (rozhodnutí, akce, odpovědi) na základě vstupů z membrány a vlastních predikcí.

---

### 1.4 Vztahy a vlastnosti

Mezi zavedenými pojmy platí následující vztahy a vlastnosti:

**Vzájemné ovlivňování** – membrána a pole jsou v obousměrné vazbě. Membrána ovlivňuje pole tím, že mu předává transformované vstupy. Pole ovlivňuje membránu tím, že nastavuje její propustnost a váhy.

**Přepis parametrů** – membrána i pole se přepisují na základě vstupů, které do nich vcházejí. Každý vstup je potenciálním trénovacím vzorkem, který generuje změnu vnitřního nastavení systému.

**Kognitivní výstup** – je generován polem kognicí a je definován jako výběr nejvhodnější položky (rozhodnutí, záměru, akce) z naučeného modelu na základě aktuálního vstupu a aktuálního nastavení parametrů. Tento výstup spouští akce v těle a iniciuje interakce.

---

### 1.5 Shrnutí požadavků

Model kognicí člověka v našem kontextu musí:

- Být **funkční** – popisovat chování systému na úrovni interakce, nikoli jeho substrát.
    
- Obsahovat **tři pojmy** – kortex, kognitivní membrána, pole kognicí.
    
- Definovat **vztahy mezi nimi** – vzájemné ovlivňování, přepis parametrů.
    
- Definovat **kognitivní výstup** – jako predikční výběr generovaný polem.
    
- Být **aplikovatelný na interakci s LLM** – popisovat, jak výstup z LLM vstupuje do kognice uživatele a přepisuje její parametry.

**Bod 2: Funkční model kortexu – membrána a pole**

---

### 2.1 Struktura kortexu

Kortex modelujeme jako dvouvrstvý funkční celek:

- **Kognitivní membrána** (dále jen membrána) – vstupní rozhraní.
    
- **Pole kognicí** (dále jen pole) – prediktivní jádro.
    

Oba bloky jsou v obousměrné vazbě. Jejich propojení je dynamické – membrána transformuje vstupy do pole, pole moduluje nastavení membrány.

Pro účely dalšího textu zavádíme terminologickou konvenci:

|Funkční pojem|Ekvivalent pro aplikaci|
|---|---|
|Kognitivní membrána|Správce|
|Pole kognicí|Autor|

Tato konvence odpovídá dělení z modelu Smart Home, kde správce je nositel vlastností a autor je nositel kognitivních funkcí.

---

### 2.2 Kognitivní membrána (Správce)

#### 2.2.1 Funkce

Membrána je vstupní rozhraní kortexu. Jejím úkolem je transformovat signály z prostředí (včetně výstupů z LLM) před vstupem do pole.

Transformace zahrnuje:

- **Filtraci** – zesiluje relevantní signály, potlačuje šum.
    
- **Vážení** – přiřazuje signálům míru důležitosti.
    
- **Modulaci** – přizpůsobuje propustnost aktuálnímu stavu systému.
    

Membrána tedy neurčuje obsah kognice, ale nastavuje podmínky, za kterých se obsah do kognice dostane.

#### 2.2.2 Vlastnosti

Membrána je nositelkou vlastností, které určují způsob transformace signálů. Mezi tyto vlastnosti patří:

**Práh propustnosti** – určuje, jak silný signál musí být, aby vůbec prošel. Jde o binární filtraci: signál buď projde, nebo neprojde.

**Váhování** – určuje preferenci určitých typů signálů. Jde o relativní zesilování nebo tlumení – membrána může propustit všechny signály, ale některé zesílí, jiné potlačí.

**Transformační schéma** – určuje, jak je signál převeden z původní podoby do podoby vhodné pro pole. Dva různé vstupy mohou být transformovány na stejný výstup; stejný vstup může být transformován na různé výstupy v závislosti na nastavení membrány. Tím se vysvětluje, proč stejná situace vede u různých lidí k odlišnému prožitku.

**Inhibiční práh** – určuje, kdy se membrána uzavře před přetížením. Nejde o doplňkovou vlastnost, ale o zásadní mechanismus, který ovlivňuje všechny předchozí vlastnosti. Když je membrána přetížena (příliš mnoho signálů, příliš silná modulace z pole, nebo kombinace obojího), inhibiční práh:

- zvyšuje práh propustnosti (méně signálů prochází),
    
- mění váhování (preferuje jednodušší, známé signály),
    
- omezuje transformační schéma (redukuje komplexitu transformace).
    

Výsledkem je, že systém přestává vnímat detail, přestává rozlišovat a přechází do úsporného režimu – signály jsou buď ignorovány, nebo transformovány zjednodušeně. Tento mechanismus je zásadní pro pochopení individuálních rozdílů v interakci s LLM a bude hrát klíčovou roli v diagnostice.

---

#### 2.2.3 Kombinace vlastností

Vlastnosti nepůsobí izolovaně – kombinují se:

|Kombinace|Efekt|
|---|---|
|Práh + Váhování|Signál musí být dostatečně silný (práh) a navíc musí být preferovaného typu (váhování), aby prošel s plnou vahou.|
|Váhování + Transformace|Signál je nejen zesílen nebo potlačen, ale také převeden do jiné podoby – např. neutrální informace je transformována na ohrožující (cholerik) nebo na zvládnutelnou (flegmatik).|
|Práh + Transformace|Signál, který projde prahem, je transformován podle aktuálního schématu – stejný vstup tak může vést k zcela odlišnému vnitřnímu stavu.|
|Inhibiční práh + kterákoli vlastnost|Inhibice mění nastavení všech ostatních vlastností – systém přechází do úsporného režimu.|

Vlastnosti se mohou měnit – membrána je přepisovatelná na základě vstupů a modulace z pole. Inhibiční práh je přitom jedním z klíčových parametrů, který určuje, jak dlouho a za jakých podmínek je systém schopen zpracovávat komplexní vstupy, než přejde do úsporného režimu.

---

### 2.3 Pole kognicí (Autor)

#### 2.3.1 Funkce

Pole je prediktivní jádro kortexu. Jeho úkolem je generovat kognitivní výstupy na základě vstupů z membrány a vlastních predikcí.

Funkce zahrnují:

- **Predikci** – generuje očekávaný stav světa.
    
- **Vyhodnocení predikční chyby** – porovnává predikci se skutečností.
    
- **Generování kandidátů** – vytváří možné akce nebo odpovědi.
    
- **Výběr výstupu** – vybírá nejvhodnější kandidáta.
    

Pole tedy neurčuje, co vstoupí do kognice, ale co z kognice vystoupí jako rozhodnutí, záměr nebo akce.

#### 2.3.2 Vlastnosti

Pole je tvořeno členy, z nichž každý má své parametry. Tyto členy reprezentují jednotlivé kognitivní funkce – například predikční mechanismy, atribuční schémata, hodnotící kritéria.

Vlastnosti pole zahrnují:

- **Parametry členů** – nastavení jednotlivých kognitivních funkcí.
    
- **Váhy mezi členy** – míra vzájemného ovlivňování.
    
- **Aktivační prahy** – podmínky pro aktivaci jednotlivých členů.
    

Pole je přepisovatelné – jeho parametry se mění na základě predikční chyby a vstupů z membrány.

---

### 2.4 Vzájemné vazby a dynamika

Membrána a pole jsou v obousměrné vazbě:

**Bottom-up (membrána → pole):**

- Membrána transformuje vstupní signály.
    
- Transformovaný signál vstupuje do pole.
    
- Pole na jeho základě generuje predikce a vyhodnocuje chybu.
    

**Top-down (pole → membrána):**

- Pole na základě predikční chyby moduluje nastavení membrány.
    
- Mění její propustnost, váhy a inhibiční práh.
    
- Tím se mění podmínky pro následné vstupy.
    

Tato smyčka je základem dynamiky systému:

1. Vstup vstupuje do membrány.
    
2. Membrána jej transformuje a předá poli.
    
3. Pole generuje predikci a vyhodnocuje chybu.
    
4. Pole na základě chyby moduluje membránu.
    
5. Upravená membrána transformuje další vstupy odlišně.
    

Systém se tak neustále přizpůsobuje – membrána i pole se přepisují na základě průběhu interakce. Každý cyklus mění nastavení obou bloků, čímž se mění i způsob, jakým systém zpracovává následující vstupy.

**Bod 3: Propojení s neurovědou, psychologií a biologií**

---

### 3.1 Neurověda – prediktivní zpracování

Model je funkčním ekvivalentem prediktivního zpracování, jak jej formuloval Karl Friston v rámci free energy principle (FEP). FEP předpokládá, že mozek funguje jako hierarchický predikční stroj, který kontinuálně minimalizuje překvapení (surprise) minimalizací volné energie – tedy rozdílu mezi predikcemi a senzorickými vstupy.

|Model|Prediktivní zpracování|Neurobiologický korelát|
|---|---|---|
|Kognitivní pole generuje predikce.|Generativní model – top-down predikce.|Zpětné projekce z vyšších korových oblastí do nižších.|
|Membrána transformuje vstup (práh, váhování, transformační schéma).|**Precision weighting** – důvěryhodnost signálu.|Postsynaptický zisk neuronálních populací reportujících predikční chybu; neuromodulace (acetylcholin, noradrenalin).|
|Pole nastavuje membránu (top-down modulace).|**Top-down modulace precision**.|Zpětné projekce modulující gain predikčních chyb v nižších oblastech.|
|Membrána mění vstup do pole.|Bottom-up predikční chyba **vážená precizí**.|Forwardové projekce nesoucí precision-weighted predikční chyby (např. AMPA receptory).|
|Učení = přepisování parametrů.|Minimalizace volné energie – aktualizace generativního modelu.|Synaptická plasticita (LTP/LTD) měnící váhy spojení.|

**Precision (přesnost, důvěryhodnost)** je v prediktivním zpracování klíčovým pojmem – určuje, jak silně bude predikční chyba aktualizovat parametry systému. Nízká precision znamená, že systému chybí důvěra ve vlastní predikce, a proto dává větší váhu senzorickým vstupům. Tento mechanismus je v našem modelu implementován jako **váhování membrány** – membrána určuje, jaké váze (precision) budou vstupy vstupovat do pole.

**Hierarchické zpracování** je dalším pilířem Fristonova modelu – mozek je uspořádán hierarchicky, přičemž vyšší úrovně generují predikce a nižší úrovně reportují predikční chyby prostřednictvím reciprokých forwardových a backwardových projekcí. Náš model tuto hierarchii abstrahuje do dvou funkčních vrstev (membrána a pole) s obousměrnou vazbou, která odpovídá reciprokému propojení mezi korovými oblastmi.

**Shrnutí:** Náš model je funkčním ekvivalentem prediktivního zpracování – nepopisuje anatomické dráhy, ale zachovává klíčové mechanismy: predikci, predikční chybu, precision weighting a hierarchickou obousměrnou komunikaci. Tato shoda umožňuje neurovědcům přijmout model jako konzistentní s existující teorií, aniž by vyžadoval detailní neuroanatomickou specifikaci.

---

### 3.2 Psychologie – vlastnosti membrány

Membrána nese vlastnosti, které odpovídají psychologickým konstruktům. Tyto konstrukty nejsou vlastnostmi predikčního výpočtu (pole), ale vlastnostmi rozhraní (membrány), které určují, jak systém interpretuje příčiny, reaguje na podněty a vztahuje se k sobě samému.

|Konstrukt|Autor|Umístění v modelu|Definice|
|---|---|---|---|
|Interní / externí atribuce|**Rotter**|Membrána – **transformační schéma** (jak je signál interpretován).|Rotter (1954) definoval **locus of control** jako generalizované očekávání, zda je posílení (reinforcement) kontrolováno vnitřně (schopnosti, úsilí) nebo externě (náhoda, osud, mocní druzí). Interní atribuce = membrána transformuje signály tak, že příčina je přičítána sobě; externí atribuce = příčina je přičítána vnějším okolnostem.|
|Proaktivní / reaktivní|**Covey**|Membrána – **práh propustnosti + váhování** (kdy a jaké signály spouštějí akci).|Covey (1989) rozlišuje proaktivní a reaktivní lidi. **Proaktivní** lidé jsou řízeni hodnotami, jednají na základě vlastního rozhodnutí a zaměřují se na to, co mohou ovlivnit. **Reaktivní** lidé jsou řízeni pocity, okolnostmi a prostředím – jejich jednání je odpovědí na vnější podněty. V modelu: proaktivní membrána má nižší práh pro akci a váhuje signály směřující k možnosti jednání; reaktivní membrána čeká na silný vnější podnět.|
|Autentický / neautentický|**Sartre, Heidegger**|Membrána – **transformační schéma** (vztah k sobě a k očekávání okolí).|Heidegger zavedl pojem **autentického a neautentického bytí** (Dasein). Autentický člověk žije v souladu se svou vlastní existencí a možnostmi; neautentický člověk podléhá očekáváním druhých a „ono se“ (das Man). Sartre tento koncept rozvinul v pojem **autentické volby** – jednání, které je výrazem svobodného sebeurčení, nikoli podřízením se sociálním očekáváním. V modelu: autentická membrána transformuje signály tak, aby odpovídaly vlastním hodnotám; neautentická membrána transformuje signály podle očekávání okolí.|

**Shrnutí:** Tyto konstrukty jsou v modelu umístěny do membrány, nikoli do pole, protože určují **způsob transformace vstupů** – tedy jak je signál interpretován (atribuce), zda a kdy spouští akci (proaktivita) a v jakém vztahu k sobě samému je signál zpracováván (autenticita). Pole samotné (predikční výpočet) je na těchto nastaveních nezávislé – pracuje s tím, co mu membrána předá.

---

### 3.3 Biologie – časové škály učení a přepisu parametrů

Model rozlišuje tři časové škály změny parametrů membrány a pole. Toto rozlišení odpovídá biologickým mechanismům synaptické plasticity a konsolidace paměti.

|Škála|Horizont|Biologický mechanismus|Vrací se?|Reference|
|---|---|---|---|---|
|**Mikro-adaptace**|Sekundy / minuty|Změna prahu propustnosti, gainu a precision na základě aktuálního stavu (noradrenalin, acetylcholin, arousal).|**Ano** – vrací se po odeznění podnětu.|Precision je v prediktivním zpracování modulována neuromodulátory; pozornost je procesem precision inference.|
|**Mezo-učení**|Dny / týdny|Změna synaptických vah (LTP/LTD) vyžadující konsolidaci a proteinovou syntézu.|**Ne** – stabilizuje se.|LTP a LTD jsou považovány za neuronální korelát učení a paměti; konsolidace transformuje labilní krátkodobé změny v persistentní dlouhodobé.|
|**Makro-dispozice**|Roky / genetika|Základní nastavení dané genetickou výbavou a epigenetickými změnami – např. hustota receptorů, výchozí práh dráždivosti, temperament.|**Ne** – je trvalé.|Genetické predispozice ovlivňují synaptickou plasticitu a neuromodulační systémy; epigenetika umožňuje dlouhodobé změny v expresi genů.|

Plasticita probíhá na mnoha časových škálách – od milisekund (short-term plasticity) přes minuty (early-phase LTP) až po hodiny a dny (late-phase LTP a konsolidace). Konsolidace paměti vyžaduje přechod od labilních krátkodobých změn k persistentním dlouhodobým.

**Shrnutí:** Toto rozlišení je klíčové pro pochopení, proč interakce s LLM nemusí mít okamžitý dopad na dlouhodobé parametry kognice – a proč některé změny jsou dočasné (mikro-adaptace) a jiné trvalé (mezo-učení, makro-dispozice). Model tím získává biologickou konzistenci a vysvětluje, proč stejná interakce může u různých lidí vést k různým důsledkům v závislosti na jejich aktuálním stavu, historii učení a genetické dispozici.

---

### 3.4 Shrnutí propojení

|Vědecký obor|Klíčový koncept|Odpovídající prvek modelu|Reference|
|---|---|---|---|
|Neurověda|Prediktivní zpracování (Friston)|Pole kognicí – predikce, predikční chyba||
|Neurověda|Precision weighting|Membrána – váhování vstupů||
|Neurověda|Hierarchické zpracování|Obousměrná vazba membrána ↔ pole||
|Psychologie|Locus of control (Rotter)|Membrána – transformační schéma (atribuce)||
|Psychologie|Proaktivita / reaktivita (Covey)|Membrána – práh a váhování pro akci||
|Psychologie|Autenticita / neautenticita (Sartre, Heidegger)|Membrána – transformační schéma (vztah k sobě)||
|Biologie|Synaptická plasticita (LTP/LTD)|Přepis parametrů pole a membrány (mezo-učení)||
|Biologie|Neuromodulace (noradrenalin, acetylcholin)|Mikro-adaptace membrány (práh, váhování)||
|Biologie|Genetické predispozice|Makro-dispozice membrány a pole|—|
