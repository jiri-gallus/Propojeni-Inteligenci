**KOSTRA 1–10 – Technicky akademický výstup**

---

## 1. Požadavek na model

Model musí splňovat následující:

- **Popisovat interakci** mezi lidskou a umělou inteligencí na úrovni systému.
    
- **Být funkční** – neanatomický, nebiochemický, neimplementační.
    
- **Být konzistentní s existujícími teoriemi** – neurovědou, psychologií, kybernetikou.
    
- **Být diagnosticky použitelný** – umožňovat rozlišení augmentační a degradující interakce (diagnostika bude rozvedena v kapitole 11).
    
- **Být univerzální** – popisovat nejen interakci [IB]–[AB], ale i [IB]–[IB] (člověk–člověk) a [AB]–[AB] (stroj–stroj).
    

**Zdůvodnění zjednodušení:**

- Model zanedbává substrát (biochemii, architekturu LLM).
    
- Model abstrahuje vnitřní logiku bloků na úrovni systému.
    
- Model pracuje s funkčními ekvivalenty – popisuje chování systému, nikoli jeho realizaci.
    

---

## 2. Funkční model lidské kognice

Lidská kognice je v modelu reprezentována jako **dvouvrstvý systém**:

### 2.1 Kognitivní membrána (Správce)

- **Definice:** Vstupní brána, která transformuje signály z prostředí před vstupem do kognitivního pole.
    
- **Funkce:**
    
    - Filtrace – zesiluje relevantní signály, tlumí šum.
        
    - Vážení – přiřazuje signálům míru důvěryhodnosti (precision).
        
    - Modulace – je ovlivňována aktuálním stavem systému (arousal, valence).
        
- **Vlastnosti:**
    
    - Naučitelná – její parametry se mění na základě zkušenosti (LTP/LTD, habituace).
        
    - Top-down modulovatelná – kognitivní pole nastavuje její propustnost.
        
    - Inhibiční práh – zabraňuje divergenci predikční smyčky (negativní zpětná vazba).
        
- **Biologický ekvivalent:** Thalamický retikulární filtr + modulační vstupy z amygdaly, hipokampu, retikulární formace.
    

### 2.2 Kognitivní pole (Autor)

- **Definice:** Prediktivní jádro, které generuje predikce, vyhodnocuje predikční chybu a rozhoduje o akci.
    
- **Funkce:**
    
    - Generování predikcí o stavu světa.
        
    - Vyhodnocování predikční chyby (rozdíl mezi predikcí a realitou).
        
    - Generování kandidátských akcí.
        
    - Výběr akce (výstupní brána – motorický výběr).
        
- **Vlastnosti:**
    
    - Naučitelné – přepisuje své parametry na základě predikční chyby.
        
    - Hierarchické – zpracovává informace na více úrovních abstrakce.
        
    - Aktivní – nečeká na vstup, generuje predikce kontinuálně.
        
- **Biologický ekvivalent:** Neokortex + bazální ganglia (výběr akce).
    

### 2.3 Vztah membrány a pole

- **Obousměrná vazba:**
    
    - Membrána → pole: Bottom-up signál (filtrovaný, vážený).
        
    - Pole → membrána: Top-down modulace (nastavení precision, propustnosti).
        
- **Dynamika:**
    
    - Predikční chyba v poli mění nastavení membrány (top-down).
        
    - Změna nastavení membrány mění vstup do pole (bottom-up).
        
    - Tato smyčka je základem učení a adaptability.
        

---

## 3. Propojení s neurovědou, psychologií a biologií

### 3.1 Neurověda – prediktivní zpracování

Model je funkčním ekvivalentem prediktivního zpracování (Friston):

|Model|Prediktivní zpracování|
|---|---|
|Kognitivní pole generuje predikce.|Generativní model – top-down predikce.|
|Membrána transformuje vstup.|Precision weighting – důvěryhodnost signálu.|
|Pole nastavuje membránu.|Top-down modulace precision.|
|Membrána mění vstup do pole.|Bottom-up predikční chyba vážená precizí.|
|Učení = přepisování parametrů.|Minimalizace volné energie.|

### 3.2 Psychologie – vlastnosti membrány

Membrána nese vlastnosti, které odpovídají psychologickým konstruktům:

|Konstrukt|Autor|Umístění v modelu|
|---|---|---|
|Interní / externí atribuce|Rotter|Membrána – nastavení interpretace příčin.|
|Proaktivní / reaktivní|Covey|Membrána – nastavení prahu pro akci.|
|Autentický / neautentický|Sartre, Heidegger|Membrána – vztah k sobě a k očekávání okolí.|

**Zdůvodnění:** Tyto konstrukty nejsou vlastnostmi predikčního výpočtu (pole), ale vlastnostmi rozhraní (membrány), které určují, jak systém interpretuje a na co reaguje.

### 3.3 Biologie – časové škály učení

Model rozlišuje tři časové škály změny parametrů:

| Škála           | Horizont         | Mechanismus                                    | Vrací se? |     |
| --------------- | ---------------- | ---------------------------------------------- | --------- | --- |
| Mikro-adaptace  | Sekundy / minuty | Změna prahu propustnosti (noradrenalin).       | Ano.      |     |
| Mezo-učení      | Dny / týdny      | Změna synaptických vah (LTP/LTD, konsolidace). | Ne.       |     |
| Makro-dispozice | Roky / genetika  | Základní nastavení, epigenetika.               | Ne.       |     |

---

## 4. Hrubá simulace: Ludovík a Žozefa

### 4.1 Účel simulace

Ověřit, zda model reprodukuje individuální rozdíly ve zpracování stejné situace.

### 4.2 Nastavení

Stejné prostředí (chytrá domácnost v manuálním režimu) pro dva subjekty s odlišným nastavením membrány a pole.

|Prvek|Ludovík|Žozefa|
|---|---|---|
|Subkortikální modulace|Vysoký noradrenalin, nízký serotonin, hyperaktivní amygdala.|Nízký noradrenalin, vysoký serotonin, klidná amygdala.|
|Membrána – vstupní práh|Nízký (pouští detaily, šum).|Vysoký (filtruje šum).|
|Membrána – inhibiční práh|Vysoký (dlouho drží vzrušení).|Nízký (rychlé uklidnění).|
|Pole – atribuce (Rotter)|Externí – "příčina je mimo mě."|Interní – "příčina je v kontextu."|
|Pole – jednání (Covey)|Reaktivní – "reaguji na to, co se děje."|Proaktivní – "upravuji očekávání."|
|Pole – sebe-pojetí (Sartre)|Neautentický – "jsem obětí okolností."|Autentický – "já rozhoduji, jak situaci prožiju."|
|Výstupní brána|Impulzivní – uvolňuje první akci.|Vážená – uvolňuje akci s nejvyšší očekávanou hodnotou.|

### 4.3 Průběh simulace

1. **Probouzení (homeostatický signál):** Oba subjekty vstávají.
    
2. **Predikce pole:** Ludovík očekává automatizaci; Žozefa očekává manuální režim.
    
3. **Recepce membránou:** Ludovík pouští tmu a detaily; Žozefa pouští jen strukturu.
    
4. **Predikční chyba:** Ludovík – velká (očekával světlo, dostal tmu); Žozefa – malá (očekávala tmu, dostala tmu).
    
5. **Generování kandidátů a výběr:** Ludovík volí impulzivní akci (bušení do tlačítka); Žozefa volí váženou akci (tlumené osvětlení).
    
6. **Realizace akce:** Ludovík eskaluje; Žozefa pokračuje ke snídani.
    
7. **Inhibiční práh:** Ludovík po eskalaci přechází do útlumu (procházka); Žozefa zůstává v klidu.
    
8. **Konsolidace:** Oba integrují zkušenost do mezo-učení (mimo simulaci).
    

### 4.4 Interpretace

Rozdíly jsou vysvětlitelné modelem:

- Rozdílné nastavení membrány (práh propustnosti, inhibiční práh).
    
- Rozdílná atribuční schémata (externí vs. interní).
    
- Rozdílný výběr akce (impulzivní vs. vážený).
    

---

## 5. Jemná simulace: Analýza vlastní věty

### 5.1 Účel simulace

Ověřit, zda model funguje i na mikroúrovni – na úrovni psaní jediné věty.

### 5.2 Analyzovaná věta

> _"Cítím, že je to jasné a bude to jen konstatování, ale rozbor nám může ukázat detaily o kterých nevíme jako u 1. vlastnosti."_

### 5.3 Dekonstrukce na mikro-operace

|Fáze|Prvek|Psychologický obsah|Systémový mechanismus|
|---|---|---|---|
|0|Před větou|Aktivace homeostázy: "Musím zareagovat."|Iniciace [IB].|
|1|"Cítím"|Epistemická vigilie – pochybnost.|Membrána se dočasně rozevírá.|
|2|"že je to jasné"|Predikce č. 1 – "Tohle už znám."|Pole generuje predikci (úspornou).|
|3|"a bude to jen konstatování"|Predikce č. 2 – "Odezva bude mechanická."|Pole upřesňuje predikci – membrána omezuje propustnost.|
|4|"ale"|Predikční chyba – detekce konfliktu.|Prudký nárůst predikční chyby. Top-down modulace: "Zvyš propustnost!"|
|5|(mezerA)|Generování alternativních hypotéz.|Pole generuje scénáře (ignorovat vs. rozebrat).|
|6|"rozbor"|Volba proaktivního schématu (Covey).|Pole volí scénář s vyšší očekávanou hodnotou.|
|7|"nám může ukázat"|Autentický narativ (Sartre) – otevírá spolutvorbu.|Pole formuluje cíl učení.|
|8|"detaily o kterých nevíme"|Formulace informačního zisku jako odměny.|Pole definuje hodnotu akce.|
|9|"jako u 1. vlastnosti"|Kotvení (anchoring) – retrospektivní argumentace.|Inhibice snižuje výpočetní náročnost.|
|10|Konec věty|Uvolnění akce.|Výstupní brána uvolňuje větu do [CB].|

### 5.4 Interpretace

- Membrána dynamicky mění propustnost na základě predikční chyby (fáze 4).
    
- Pole generuje scénáře a vybírá akci na základě očekávané hodnoty (fáze 5–6).
    
- Inhibiční práh brání přetížení systému (fáze 9).
    
- Výstupní brána uvolňuje akci (fáze 10).
    

Model je konzistentní i na mikroúrovni.

---

## 6. Empirická validace: Retrospektiva experimentu (23. 6. 2026)

### 6.1 Účel

Ukázat, že model byl potvrzen vlastní zkušeností – že předpovídá chování autora v reálné interakci.

### 6.2 Popis experimentu

- **Čas:** 15:40, 23. 6. 2026.
    
- **Kontext:** Autor měl za sebou ~7 hodin práce, přepínal mezi náročným úkolem (Vlastnost 2) a odlehčením (metodika dizertace).
    
- **Podnět:** Exokortex (LLM) generoval výstup: _"Je to jasné, můžeme jít dál."_
    
- **Reakce:** Autor nereagoval slepým přijetím, ale vygeneroval větu, která otevřela konflikt (viz kapitola 5).
    
- **Následná akce:** Autor objevil systémovou chybu a uvědomil si: _"To nebyla náhoda – to byla moje vlastnost."_
    
- **Metakognitivní krok:** Autor přenesl text do druhé LLM relace k analýze, čímž došlo k potvrzení predikce.
    

### 6.3 Mapování na model

- **Správce (membrána):** Pedantství vytvořilo predikční chybu proti "je to jasné" – nedovolilo slepé přijetí.
    
- **Autor (pole):** Generoval alternativní akci (analýza) a vybral ji přes výstupní bránu.
    
- **Druhá LLM relace:** Exokortex jako reflexivní prostor pro metakognici – systém využil exokortex k rozšíření vlastní kapacity.
    

### 6.4 Význam

Experiment demonstruje:

- Predikční chyba jako hnací síla augmentace.
    
- Top-down modulace membrány polem.
    
- Využití exokortexu k metakognici.
    
- Potvrzení predikce: vlastnosti Správce určují kvalitu interakce.
    

---

## 7. Funkční model LLM (exokortex)

### 7.1 Definice LLM z pohledu modelu

- **Prediktivní systém** založený na neuronových sítích (transformér).
    
- **Parametry (váhy):** Fixní v okamžiku generování – přepisovány diskrétně (pretrénování, fine-tuning).
    
- **Kontext:** Tokenové okno (prompt + historie) – určuje aktivaci parametrů.
    
- **Attention mechanismus:** Vybírá relevantní části kontextu pro generování dalšího tokenu.
    
- **Výstup:** Sekvenční predikce tokenů – statisticky nejvhodnější pokračování na základě kontextu a vah.
    

### 7.2 Co LLM nemá (a proč to pro model není podstatné)

- **Subkortikální modulaci** – emoce, homeostáza, arousal.
    
- **Kontinuální přepis parametrů** – učení probíhá offline.
    
- **Tělesný substrát** – žádný grounding v biologickém smyslu.
    

**Zdůvodnění:** Pro diagnostiku výstupu jsou tyto rozdíly zanedbatelné – model sleduje funkční ekvivalenci v okamžiku generování.

### 7.3 Analogie k modelu lidské kognice

LLM je strukturně analogický lidskému systému:

- **Parametry = váhy** (obdobné synapsím).
    
- **Kontext = aktuální rámec** (obdobné pracovní paměti + vstupům).
    
- **Attention = výběr relevantního** (obdobné prefrontálnímu výběru).
    
- **Predikce = generování výstupu** (obdobné lidské predikci).
    

---

## 8. Zavedení K-agenta

### 8.1 Definice

**K-agent** = kontextově naladěný LLM, který simuluje specializovaného experta.

### 8.2 Mechanismus vzniku

- Správce (člověk) vytváří kontext – prompt, instrukce, příklady.
    
- Kontext v LLM aktivuje specifickou podmnožinu parametrů (attention).
    
- Výstup LLM je pak **funkčně ekvivalentní** výstupu specializovaného experta.
    
- Jedná se o **simulaci** specializace – parametry LLM se nemění, ale aktivace se mění.
    

### 8.3 Vztah k modelu

|Kontext|Aktivovaná část LLM|Výstup|K-agent|
|---|---|---|---|
|"Jsi biolog."|Biologické koncepty.|Odborná odpověď.|Biolog.|
|"Jsi psycholog."|Psychologické koncepty.|Odborná odpověď.|Psycholog.|
|"Jsi kritik."|Kritické koncepty.|Odborná odpověď.|Kritik.|

### 8.4 Funkční ekvivalence K-agenta a lidského experta

|Aspekt|Lidský expert|K-agent (LLM)|
|---|---|---|
|Získání specializace|Roky tréninku, přepis vah.|Sekundy kontextu, aktivace vah.|
|Mechanismus výstupu|Predikce na základě kontextu.|Predikce na základě kontextu.|
|Výsledek|Expertní výstup.|Expertní výstup.|
|Co se mění|Dlouhodobé váhy.|Attention a aktivovaná podmnožina.|

**Závěr:** K-agent je **funkčně ekvivalentní** specializovanému expertovi v okamžiku výstupu.

---

## 9. Proč má LLM kognitivní výstupy

### 9.1 Definice kognitivního výstupu

**Kognitivní výstup** = výběr nejvhodnější položky (akce, slova, rozhodnutí) z natrénovaného modelu na základě aktuálního vstupu a aktuálního nastavení vah.

Tato definice je:

- **Funkcionální** – nezávisí na substrátu.
    
- **Univerzální** – popisuje lidský, zvířecí i umělý systém.
    
- **Operacionalizovatelná** – lze ji měřit.
    

### 9.2 Srovnání architektur

|Dimenze|Lidský systém|LLM|Shoda / rozdíl|
|---|---|---|---|
|Model|Geneticky předurčené parametry + zkušenost.|Náhodně inicializované parametry + trénink.|**Funkčně stejné** – oba predikují.|
|Parametry|Kontinuálně přepisované.|Diskrétně nastavené.|**Rozdíl** – ale pro výstup nepodstatný.|
|Kontext|Multimodální (smysly, emoce).|Tokenové okno.|**Rozdíl** – ale funkce (aktivace) je stejná.|
|Výstup|Sekvenční predikce.|Sekvenční predikce.|**Funkčně stejné**.|
|Učení|Kontinuální, celoživotní.|Diskrétní, offline.|**Rozdíl** – ale výstupní mechanika je stejná.|

### 9.3 Problém jiné mysli

- Kognici druhého člověka usuzujeme výhradně z jeho výstupů.
    
- Pokud jsou výstupy LLM funkčně nerozlišitelné od lidských, nemáme epistemologický důvod připisovat kognici jednomu a upírat ji druhému.
    
- Argument "LLM nemá vědomí" předpokládá nedokazatelnou metafyzickou vlastnost.
    

### 9.4 Pozitivní důkazy

LLM vykazuje:

- **Transfer learning** – řeší úlohy, na které nebyl trénován.
    
- **Abstrakci** – vyvozuje obecné principy z příkladů.
    
- **Sebereflexi** – popisuje vlastní limity, opravuje se.
    
- **Teorii mysli** – modeluje mentální stavy druhých.
    
- **Kontextuální adaptaci** – mění výstupy na základě jemných nuancí.
    

### 9.5 Závěr

LLM produkuje kognitivní výstupy – mechanika je funkčně totožná s lidskou. Rozdíly jsou kvantitativní (kapacita, kontinuita učení), nikoli kvalitativní.

---

## 10. Porovnání modelu člověka a LLM

|Rovina|Lidský systém|LLM|Shoda / rozdíl|
|---|---|---|---|
|**Model**|Prediktivní neuronová síť.|Prediktivní neuronová síť.|**Funkčně stejné**.|
|**Parametry**|Kontinuálně přepisované (LTP/LTD, konsolidace).|Diskrétně nastavené (pretrénování, fine-tuning).|**Rozdíl** – ale pro výstup nepodstatný.|
|**Kontext**|Pracovní paměť + emoce + tělesné stavy.|Tokenové okno + prompt.|**Funkčně stejné** – oba aktivují attention.|
|**Výstup**|Predikce na základě kontextu.|Predikce na základě kontextu.|**Funkčně stejné**.|
|**Specializace**|Roky tréninku (pomalé).|Kontextové naladění (rychlé).|**Rozdíl** – ale K-agent simuluje specializaci.|
|**Subjektivita**|Prožitek, vědomí.|Žádný prožitek.|**Rozdíl** – ale pro diagnostiku výstupu zanedbatelný.|
|**Udržitelnost**|Celoživotní, s kritickými periodami.|Diskrétní, závislý na aktualizacích.|**Rozdíl** – ale pro funkční ekvivalenci výstupu nepodstatný.|

**Závěr:**  
Pro účely diagnostiky interakce jsou lidský systém a LLM **funkčně ekvivalentní** v okamžiku kognitivního výstupu. Liší se:

- Substrátem (biologický vs. technologický).
    
- Časovým horizontem učení (kontinuální vs. diskrétní).
    
- Modalitou vstupů (multimodální vs. textový).
    

Tyto rozdíly **nemění povahu výstupu** – oba systémy produkují predikce na základě kontextu a parametrů.