# Kognitivní model interakcí

## 1. Základní orientace v modelu

### 1.1 Deklarace pojmů a rozsahu modelu

Kognitivní model interakcí člověka je formalizací vnitřní struktury mozku pro účely modelování interakce s vnějším prostředím a ovlivnění kognicí pomocí těchto interakcí.

Nejedná se o anatomický model mozku. Nejde o biochemii, cytoarchitekturu ani přesné nervové dráhy. Model si z neurovědy, biologie a psychologie půjčuje pouze to, co je pro popis interakce podstatné – a záměrně zanedbává detaily, které nemají vliv na chování systému na úrovni interakce.

Toto zjednodušení je metodologické: modelujeme interakci kognicí s vnějším prostředím, nikoli jejich substrát.

### 1.2 Interakce kognicí s vnějším prostředím a její důsledek

Kognice člověka nejsou uzavřeným systémem. Jsou v neustálé interakci s vnějším prostředím. Přijímají z něj signály a kognitivními výstupy do prostředí zasahují.

Tato interakce má zpětnovazební důsledek. Výstup z prostředí do vstupu kognicí mění jejich vnitřní nastavení. Interakce tedy není pouze výměnou signálů, ale zdrojem změny parametrů kognitivního systému.

Pro účely tohoto modelu definujeme vnější prostředí vším, co s kognicemi interaguje. To zahrnuje fyzikální podněty, výstupy jiných systémů, včetně umělých, ale i vnitřních, jako je homeostáze.

### 1.3 Zavedení pojmů

Pro účely modelování kognicí v interakci s vnějším prostředím zavádíme tři funkční pojmy:

**Kortex** – funkční celek, který integruje zpracování vstupů, generování výstupů a řízení interakcí s vnějším prostředím. Je nositelem kognitivních procesů.

**Kognitivní membrána** – vstupní rozhraní kortexu. Transformuje signály z vnějšího prostředí před jejich vstupem do pole kognicí. Filtruje, zesiluje, tlumí a váží vstupní signály.

**Pole kognicí** – aktivní prediktivní jádro kortexu. Generuje predikce o stavu vnějšího prostředí, vyhodnocuje rozdíl mezi predikcí a skutečností a produkuje kognitivní výstupy na základě vstupů z membrány a vlastních predikcí.

### 1.4 Vztahy a vlastnosti

Mezi zavedenými pojmy platí následující vztahy:

**Vzájemné ovlivňování** – membrána a pole jsou v obousměrné vazbě. Membrána ovlivňuje pole tím, že mu předává transformované signály z vnějšího prostředí. Pole ovlivňuje membránu tím, že nastavuje její propustnost a váhy.

**Přepis parametrů** – membrána i pole podléhají změně svých parametrů na základě signálů, které do nich vstupují z vnějšího prostředí, a na základě modulace z pole. Každý signál z vnějšího prostředí je potenciálním podnětem ke změně vnitřního nastavení systému.

**Kognitivní výstup** – je generován polem kognicí jako výběr nejvhodnější položky z naučeného modelu na základě aktuálního vstupu a aktuálního nastavení parametrů. Tento výstup spouští akce směrem do vnějšího prostředí a iniciuje interakce.

## 2. Architektura minima – membrána a pole

### 2.1 Struktura kortexu

Kortex modelujeme jako dvouvrstvý funkční celek:

- **Kognitivní membrána** (dále jen membrána) – vstupní rozhraní.
    
- **Pole kognicí** (dále jen pole) – prediktivní jádro.
    

Oba bloky jsou v obousměrné vazbě. Jejich propojení je dynamické – membrána transformuje signály z vnějšího prostředí do pole, pole moduluje nastavení membrány.

### 2.2 Kognitivní membrána

Membrána je vstupní rozhraní kortexu. Jejím úkolem je transformovat signály z vnějšího prostředí před jejich vstupem do pole.

Membrána neurčuje obsah kognice, ale nastavuje za jakých podmínek, a jak transformovaný signál se z vnějšího prostředí do kognice dostane. Má vlastnosti, které určují způsob transformace vnějších signálů:

**Práh propustnosti**  
určuje, jak silný signál musí být, aby prošel. Jde o binární filtraci: signál buď projde, nebo neprojde.

**Váhování**  
určuje preferenci určitých typů signálů. Jde o relativní zesilování nebo tlumení. Membrána může propustit více signálů, ale některé zesílí, jiné potlačí.

**Transformační schéma**  
určuje, jak je signál převeden z původní podoby do podoby vhodné pro pole. Stejný vstup může být transformován na různé výstupy v závislosti na nastavení membrány.

**Inhibiční práh**  
určuje, kdy se membrána uzavře před přetížením. Když je membrána přetížena (příliš mnoho signálů, příliš silná modulace z pole, nebo kombinace obojího), inhibiční práh:  
- zvyšuje práh propustnosti,      
- mění váhování směrem k preferenci známých signálů,      
- omezuje transformační schéma.  
Výsledkem je přechod do úsporného režimu – signály jsou buď ignorovány, nebo transformovány zjednodušeně.

**Kombinace vlastností**

| Kombinace                            | Efekt                                                                                     |
| ------------------------------------ | ----------------------------------------------------------------------------------------- |
| Práh + Váhování                      | Signál musí být dostatečně silný a preferovaného typu, aby prošel s plnou vahou.          |
| Váhování + Transformace              | Signál je nejen zesílen nebo potlačen, ale také převeden do jiné podoby.                  |
| Práh + Transformace                  | Signál, který projde prahem, je transformován podle aktuálního schématu.                  |
| Inhibiční práh + kterákoli vlastnost | Inhibice mění nastavení všech ostatních vlastností – systém přechází do úsporného režimu. |

### 2.3 Pole kognicí

Pole je prediktivní jádro kortexu. Jeho úkolem je generovat kognitivní výstupy na základě vstupů z membrány. Má funkce, které definují kognitivní výstupy:

**Predikci**  
generuje očekávaný stav vnějšího prostředí.

**Vyhodnocení predikční chyby**  
porovnává predikci se signálem transformovaným membránou.

**Generování kandidátů**  
vytváří možné výstupy.

**Výběr výstupu**  
vybírá nejvhodnějšího kandidáta.

**Vlastnosti pole**  
je tvořeno členy, reprezentují jednotlivé kognitivní funkce, predikční mechanismy, hodnotící kritéria, rozhodovací pravidla, přístup k paměti a jiné, které jsou definovány hodnotou členu.

Celé pole je přepisovatelné a hodnoty jednotlivých členů se dynamicky mění na základě predikční chyby a vstupů z membrány.

### 2.4 Vzájemné vazby a dynamika pole-membrána

Membrána a pole je pro kognitivní model interakcí brán částečně jako jeden celek. Nejde jej rozdělit v jeho základu na 2 části. Je to architektonické rozhodnutí pro pochopení základního mechanismu transformace a dynamiky myšlení.

Z kybernetického, technického pohledu jde o rozdělení kognicí na vstupní, transformační blok a kognitivní blok.

Z psychologického, prožitkového pohledu jde o plasticitu myšlení a její spouštěče.

Membrána a pole jsou v obousměrné vazbě, ale jsou i sami sebou. Současně membrána obsahuje i jiné funkce kortexu. Oba pohledy mají zcela jiné vazby:

**Bottom-up (membrána → pole):**  
- Membrána transformuje signály z vnějšího prostředí.  
- Transformovaný signál vstupuje do pole.  
- Vstupní signál dynamicky mění hodnoty jednotlivých členů pole.

**Top-down (pole → membrána):**  
- Pole částečně definuje membránu pomocí hodnot členů pole a jejich vážení vůči sobě.
- Membrána mění svou propustnost, váhy a transformační schéma. 
- Tím se mění podmínky pro následné vstupy.

Tato smyčka je základem dynamiky systému:  
1. Signál vstupuje do membrány.  
2. Membrána jej transformuje, předává poli.  
3. Pole generuje predikci a vyhodnocuje chybu, generuje kognitivní výstup.  
4. Pole na základě změny svých členů moduluje membránu.  
5. Upravená membrána transformuje další signály odlišně.

Systém se tak neustále přizpůsobuje, membrána i pole se mění na základě průběhu interakce. Každý cyklus mění nastavení obou bloků, čímž se mění i způsob, jakým systém zpracovává následující signály z vnějšího prostředí.