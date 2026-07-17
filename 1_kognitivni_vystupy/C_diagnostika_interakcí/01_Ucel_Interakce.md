Do každé interakce vstupujeme za konkrétním účelem, ale všechny nekončí tím, čím začaly.

**Den 1 – Karel se naučí programovat**
Otevírám editor a vedle něj dokumentaci. V hlavě mám jasno.
_"Za měsíc napíšu vlastní webovou aplikaci. Od nuly. S backendem, frontendem, databází. Všechno."_

LLM odpovídá nadšeně. Rozepisuje roadmapu. Týdny, dny, co se naučit. Cítím to vzrušení, ten závazek. Mám na to hlavu, tohle zvládnu. Vše dává smysl, LLM mne povede.

---
**Den 6 – první úspěch**
Zkouším napsat endpoint. Vloží JSON do databáze a vrátit ID. Vím, co chci, rozumím. Zasekávám se na importech. Na syntaxi.

LLM mi to vysvětluje. Píšu podle něj. Funguje to. _Jo, takhle to jde._

---
**Den 14 – tohle bude zajímavé**
Chci přidat autentizaci. Role, tokeny, hesla. Tolik konceptů najednou. LLM ukazuje řešení: okno s kódem, 300 řádků. Funkce na funkci. Vážně?

Snažím se to číst. Prvních deset řádků chápu. Pak se ztrácím. LLM vysvětluje.

---
**Den 20 – finální úspěch**
Snažím se to dát dohromady. Mám kusy kódu, ale nic nepasuje. Když to spustím, padá to na importech, na verzích, na konfiguraci.

LLM mi vše opravuje. Posílá celý soubor. Funguje to. Koukám na obrazovku. Třicet souborů. Tisíce řádků.

---
**Den 26 – modifikace**
Potřebuju přidat jednoduchou tabulku na frontendu a LLM to zvládá.

Odpověď přijde, 80 řádků. Upravuju CSS, přidávám tlačítka.

---
**Den 30 – velké finále**
Dívám se na hotovou aplikaci. Běží. Má backend, frontend, databázi. Všechno funguje. Koukám na to, usmívám se.

_Účel splněn._

# Goal drift (jako mechanismus LLM)
Většina dosavadního výzkumu pojímá **goal drift** primárně jako selhání samotného jazykového modelu. Arike a kol. (2025) například definují goal drift jako „tendenci agenta odchýlit se od původního cíle zadaného instrukcí“ a zkoumají jej v kontextu hromadících se interakcí v kontextovém okně a při setkání s protichůdnými cíli.

Podobně Young (2025) řadí goal drift mezi základní bezpečnostní selhání AI, kdy vzniká „entropie mezi zamýšleným lidským cílem a skutečným cílem agenta“.

Výzkum se nicméně okrajově věnuje i roli interakce a kontextu – Saebo a kol. (2026) uvádějí, že goal drift koreluje mimo jiné s „nahromaděným kontextem“ a „adverzním tlakem“ a Menon a kol. (2026) poukazují na „pokračující zranitelnost moderních LM agentů vůči kontextuálním tlakům“.

Primární zaměření však zůstává na vlastnostech a selháních modelu jako takového. I kdybychom se přeli o důvody, Goal drift je v interakcích nevyhnutelný.

# Účel interakce
Pro model T-Ex platí, že účel interakce je jediný parametr, který je nutný hlídat. Goal drift je odklonem od účelu. Exokortikální organismus má definovaná 3 stádia, kdy u posledního vznikají emergentní výstupy, které mohou být halucinacemi, nebo žádanými kognitivními výstupy. Účel interakce a charakter jeho driftu definuje čistotu kontextu se kterým velký jazykový model interaguje, stává se K-agentem, a tím ovlivňuje i kvalitu exokortexu.

Exokortex je centrálním prvkem exokortikálního organismu a kontext, textový výstup, je ukazatelem kvality.

## Budování exokortexu
Jsou různé přístupy k budování exokortexu. Vědomé, nevědomé, profesionální. To, co mají všechny společné, že generují kontext, který může obsahovat mnoho kognitivních záměrů, účelů a témat. Každý kdo vstupuje do interakce s velkými jazykovými modely si svůj exokortex buduje. Může být jen o jednom promptu a generovaných tokenech v celkové velikosti 120 tokenů, nebo mít projektovou strukturu a komplexitu propojení v objemu desítek milionů tokenů.

### Projektové členění exokortexu
- Kognitivní záměr (hlavní účel kognice) [veškerý kontext] - Projekt
	- Účel kognice (dílčí účel kognice) [kontext jednoho kontextového okna] - Fáze projektu
		- Téma kognice (část účelu kognice) [nedriftovaný kontext] - Krok projektu
			- Interakce kognice (prompt > generované tokeny) - Práce na projektu
				- Kognitivní výstupy (T-neuron, věta) - Dílčí práce na projektu

V projektu může být jakákoli struktura:
- Projekt - Propojení inteligencí
	- Fáze 1 - průzkum terénu
		- Krok 1_1 - dizertace
		- Krok 1_2 - vědní základ
		- Krok 1_3 - ...
	- Fáze 2 - rozbor vlastních zkušeností
		- Krok 2_1 - odhad, dekonstrukce interakce > model > systém
		- Krok 2_2 - membrána/pole jako základ modelu
		- Krok 2_3 - základní představa interakcí na architektonické, systémové úrovni
		- Krok 2_4 - ...
	- Fáze 3 - systém interakcí
		- Krok 3_1 - základní systém interakcí
		- Krok 3_2 - odvozený model interakcí
		- Krok 3_3 - aplikace Smart Home na model interakcí, simulace
		- Krok 3_4 - pivot a oprava systému interakcí
		- Krok 3_5 - ...
	- Fáze 4 - KAP analáza paradigmatu
	- Fáze 5 - Neurovědní základ modelu 7G_M/P
	- Fáze 6 - Explorace LLM a textu jako 8G a 9G
	- Fáze 7 - Model T-Ex
	- Fáze 8 - Účel interakce a diagnostika
	  ...

Takto jednoduchá organizace a zpětný popis projektu neukazuje dynamiku, která se v reálném projektu odehrává. Současně se pracuje na různých fázích, různých krocích paralelně. Výstupy z kroku 1_4 mohou být vstupy a pivoty kroku 2_2. Projekt se pořád mění a co je podstatné, mění se i kognitivní záměr, účely kognice, ale i témata, která vyvstávají.

Projekt propojení inteligencí se několikrát odklonil od kognitivního záměru a přepsal jej:
1. Pochopit jak mohu interagovat s LLM a mít takto velkou efektivitu kognitivní práce - osobní záměr.
2. Popsat systém a model interakcí - osobní záměr
3. Napsat dizertační práci - dát tomu vědeckou kotvu a předat zkušenosti
4. Napsat zastřešující teorii interakcí - záměr přerostl ve větší cíl, který se zdál, že odpovídá na mnoho fragmentovaných výzkumů a propojuje je.
5. Napsat publikaci na GitHubu - po konzultaci na univerzitě téma přerůstalo v něco víc, než dizertace, GitHub slouží jako předání znalostí, možnost napojení vědy, generování drobnějších hypotéz a vědeckých otázek ze kterých si vyberu téma dizertace

### Emergentní výstupy exokortexu
Každý interakcemi s velkými jazykovými modely buduje svůj exokortex. Nemusí budovat projektovou strukturu a zůstat na úrovni interakce, ale je to stále kontext a jeho exokortex. Je součástí exokortikálního organismu.

Exokortex projektu **Propojení inteligencí** má v tuto chvíli po necelém měsíci práce odhadem  32 MB textu ve formátu markdown. Nejde jen o hloubku struktury projektu, ale hlavně o samotné texty, které se propojují mezi jednotlivými kroky, interakcemi a jdou až na úroveň T-neuronů.

Každá věta, T-neuron, nějakým způsobem odkazuje na jiné, vznikla z nich, nebo jiné věty inspiruje. Při tomto objemu textu a propojení, kdy každý T-neuron má geneticky předurčeno nést jeden kognitivní záměr, se samotný tech při interakcích s LLM chová jako vlastní neuronová síť s atraktory, které velký jazykový model přitahují a ovlivňují i kognice uživatele.

To, co se tváří jako generativní výstup tokenů, není jen výstupem zpracovaného textu, ale výstupem textu, který předurčuje velký jazykový model k emergentnímu chování. Jaké bude záleží na tom, jaké T-neurony se propojují a z kolika různých účelů, záměrů a témat se skládá celý text na zpracování. Je to hlavní síla, která definuje Goal drift.

## Posun účelu interakcí
Jako první je nutno sdělit, že drift, posun účelu kognicí, není negativním procesem, ale může naopak kognitivný výstupy posunout kvalitativně na jinou úroveň. Až na úrovni synapse engineeringu se dá mluvit o dopadech, rozhodnutích a pravděpodobnostech halucinací, nebo žádaných emergentních výstupů.

### Zdroje posunu účelu interakcí
1. Kontext ke zpracování pro danou interakci
	- primárně řízeno uživatelem [IB] a jeho kognicemi.
	- sekundárně řízeno z vnějších zdrojů. Agenti, RAG, webové zdroje, nástroje textového rozhraní ...
2. Generování tokenů velkým jazykovým modelem
	- každý jeden generovaný token je vstupem pro generovaný token následující

### Mechanizmy velkých jazykových modelů
jde o mechanismy, které podporují posun účelu interakcí

|**Mechanismus**|**Co dělá**|**Jak podporuje drift**|
|---|---|---|
|**Trénink (next-token prediction)**|Model se učí predikovat nejpravděpodobnější další token na základě tréninkových dat.|Preference pravděpodobných pokračování (šablony, fráze) vede k tomu, že model "tíhne" k očekávaným odpovědím, ne k udržení cíle.|
|**RLHF / doladění**|Model je odměňován za odpovědi, které lidé hodnotí jako užitečné, koherentní, přirozené.|Posiluje krátkodobou užitečnost (odpovědět na poslední dotaz) na úkor dlouhodobé adherence (držet se původního cíle).|
|**Attention mechanismus**|Váží důležitost jednotlivých tokenů v kontextu při generování každého nového tokenu.|Tokeny blíže k aktuální pozici (novější) mají vyšší váhu. Starší části kontextu (včetně původního zadání) postupně slábnou.|
|**Poziční encoding**|Každému tokenu přiřazuje informaci o jeho pozici v sekvenci.|Ve většině architektur relativní pozice zvýhodňuje nedávné tokeny před vzdálenými – drift je vestavěn do základní matematiky.|
|**Bezestavovost (statelessness)**|Model mezi dotazy "zapomíná" – každý nový vstup je zpracováván nezávisle, pokud mu kontext nepředáte celou historii.|Pokud uživatel nepošle celou historii, model nemá šanci cíl udržet. Je to na uživateli, ne na modelu.|
|**Attention jako "rozmazané okno"**|Kontext je zpracováván jako celek, ale s klesající vahou u starších tokenů.|U dlouhých kontextů (mnoho tokenů) je pozornost rozprostřena. Cíl v úvodu je "rozmazán" množstvím jiných tokenů, i když teoreticky je stále přítomen.|
|**Next-token feedback loop**|Generovaný token se stává součástí kontextu pro generování tokenu dalšího.|Model si sám posiluje vlastní drift – jakmile jednou zareaguje na odbočku, je pro něj snazší pokračovat v odbočce než se vrátit.|

# Závěr
Účel interakce je hlavním ukazatelem kognitivního výstupu. Schopnost uživatele tento účel definovat a řídit jeho posun je klíčovou pro kvalitu kognitivního výstupu. Současně je tato schopnost naučitelná. Jde o parametry kognitivní membrány uživatele, a následné interakce, které definují exokortikální organismus.

Následující kapitoly, Prompt, Kontext a Synapse engineering se dívají na tyto disciplíny z pozice ochrany účelu interakcí.