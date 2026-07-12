Mám spoluráci s tebou tady v chatovém rozhraní. Jde o 3 aktéry - umělá inteligence LLM - chat, kontext - lidská inteligence člověk Vypiš mi krátce vztah mezi těmito třemi aktéry, bloky, jak se ovlivňují. Ideálně to, jak na to pohlíží literatura, konsenzus, věda, lidí. Prostě průměr co víme.

1. **Deconstruct the User Request**:
    
    - There are three actors in the chat interface: LLM (AI), Chat/Context, and Human (Human intelligence).
        
    - Task: Briefly describe the relationships between these three actors, how they influence each other (blocks/loops).
        
    - Perspective: How literature, consensus, science, and people view it. The average of what we know.
        
2. **Analyze the Three Actors**:
    
    - _Human_: The initiator, goal-setter, evaluator, and source of intent, ethics, and real-world grounding.
        
    - _LLM_: The responder, generator, pattern-matcher, information synthesizer, and statistical engine.
        
    - _Context/Chat_: The shared workspace, memory buffer, history, prompt window, and evolving narrative.
        
3. **Conceptualize the Relationships (The Loop)**:
    
    - It's a triadic feedback loop.
        
    - Human -> Context: Writes prompts, sets instructions, provides examples, corrects.
        
    - Context -> LLM: The history (messages) + system prompt + retrieved documents form the _input_ that the LLM conditions its generation on.
        
    - LLM -> Context: Appends its response to the history.
        
    - Context -> Human: Displays the response, influencing the human's next thought.
        
    - Human -> LLM (indirectly via context): The human's evaluation shifts the next prompt, which changes the context, which changes the LLM's output.
        
    - _Crucial nuance_: The LLM doesn't directly experience the Human; it only experiences the _Context_. The Human doesn't directly experience the LLM's "mind"; they experience the _Context_ (the output text).
        
4. **Structure the Output**:
    
    - Introduction: Define the dynamic clearly (Triadic cybernetic loop).
        
    - Breakdown of the roles/definition of each actor.
        
    - The Triadic Loop (How they influence each other) - use a logical flow (Human -> Context -> LLM -> Context -> Human).
        
    - Scientific/Literary Consensus (What the literature says): Mention concepts like _Distributed Cognition_, _Cybernetic Systems_, _Human-in-the-loop (HITL)_, _Situated Cognition_, _Semantic Grounding_, and _Hallucination/Alignment_.
        
    - Conclusion: Summary of the average known consensus.
        
5. **Drafting - Step-by-Step**:
    
    - _Intro_: Vztah tvoří **triadický kybernetický systém** (zpětnovazební smyčka). Vědecký konsenzus ho popisuje jako _distribuovanou kognici_, kde inteligence nespojivá jen v jednom aktérovi, ale vzniká v interakci.
        
    - _Actor definitions_:
        
    - _Člověk_: Nositel záměru, sémantického ukotvení (realita) a morálního úsudku.
        
    - _Kontext_: Aktivní paměťový prostor (prompt, historie, RAG data). Je to _brána_ – to, co vidí LLM.
        
    - _LLM_: Stochastický papoušek / kognitivní zrcadlo. Generuje pravděpodobnostní sekvence bez porozumění (v lidském smyslu), ale s vysokou syntézou.
        
    - _The Loop (ovlivňování)_:
        
    
    1. Člověk _vpisuje_ záměr do Kontextu.
        
    2. Kontext (jako vstupní okno) _determinuje_ rozsah a podmínky generování LLM.
        
    3. LLM _vyplivne_ text do Kontextu.
        
    4. Kontext (rozšířený) se _zobrazí_ Člověku.
        
    5. Člověk _interpretuje_ a _zpětnovazebně_ upravuje další vstup. (Toto je "chain-of-thought" a "refinement").
        
    
    - _Literature/Consensus_:
        
    - _Nahlížení literatury_: Literatura (např. Suchman, Hutchins) zdůrazňuje, že LLM není autonomní agent, ale _zprostředkovatel_. Je to "alien intelligence" (Wooldridge) – nemá intenci, jen korelaci.
        
    - _Problémy_: Halucinace vznikají, když Kontext neobsahuje správná fakta – LLM si je domýšlí. Alignemnt (ladění) je snaha přimět LLM reagovat na kontext tak, aby to vyhovovalo lidským hodnotám.
        
    - _Konsenzus_: Vnímáme to jako **společné řešení problémů (joint problem-solving)**. Lidé přebírají kognitivní zátěž (vyhledávání faktů) a přenášejí ji na LLM, ale odpovědnost a kreativní řízení zůstává na člověku.
        
    - _"Průměr co víme"_: LLM je _plastický_, mění se podle kontextu (in-context learning). Člověk je _křehký_ a náchylný k přehlédnutí chyb (automation bias – přeceňování AI). Kontext je _křehký_ omezením okna (window size) a zapomínáním.
        
6. **Refining and Formatting** (making it short and clear): Use bullet points and bold text for clarity. Ensure Czech is fluent and professional.
    
7. **Final Polish**:
    
    - Check for clarity: "Jak se ovlivňují" - answer explicitly.
        
    - Check literature mentions: Cybernetics (Wiener), Distributed Cognition (Hutchins), Human-AI interaction (Amershi et al. guidelines).
        
    - Ensure "průměr, co víme" is covered: Víme, že LLM nemá teorii mysli, ale simuluje ji; kontext je rozhodující pro kvalitu; člověk je nutný korektor (grounding).
        

Vztah těchto tří aktérů tvoří **triadický kybernetický regulační okruh**. Vědecký konsenzus (kognitivní věda, HCI a kybernetika) jej popisuje jako **distribuovaný kognitivní systém** – inteligence nevzniká uvnitř žádného z bloků izolovaně, ale v jejich dynamické smyčce.

Zde je stručný rozklad vztahů a ovlivňování podle současné literatury:

**1. Definice rolí (bloky)**

- **Člověk**: Nositel **záměru, sémantického ukotvení** (napojení na realitu) a **morální odpovědnosti**. Stanovuje cíle a hodnotí výstupy.
    
- **Kontext (Chat)**: Aktivní **pracovní paměť** a **rozhraní**. Zahrnuje prompt, historii zpráv, systémové instrukce a vyhledaná data (RAG). Je to jediná "brána", kterou LLM vidí.
    
- **LLM**: **Statistický syntetizátor** (bez intence). Generuje pravděpodobnostní sekvence tokenů na základě kontextu. Nemá přístup k realitě, jen ke korelacím v trénovacích datech.
    

**2. Jak se ovlivňují (tok dat a zpětná vazba)**

- **Člověk → Kontext**: Vpisuje instrukce, otázky, příklady a opravy. (Řídící vstup).
    
- **Kontext → LLM**: Okno kontextu (prompt) **determinuje** prostor možných odpovědí. Kvalita kontextu (jasnost, struktura) lineárně ovlivňuje kvalitu výstupu.
    
- **LLM → Kontext**: Připisuje svou odpověď do historie. Tím **mění stav** společného pracovního prostoru.
    
- **Kontext → Člověk**: Zobrazený text kognitivně ovlivňuje myšlení člověka (priming) a nutí ho k další reakci.
    
- **Člověk → LLM (nepřímé)**: Člověk nikdy neovlivňuje LLM přímo (váhy jsou fixní), ale ovlivňuje ho **skrze úpravy kontextu** (in-context learning) a výběrem další otázky.
    

**3. Pohled literatury a vědecký konsenzus (průměr toho, co víme)**

- **Distribuovaná kognice** (Hutchins): Tato triáda je jeden kognitivní systém. Člověk deleguje rutinní syntézu na LLM, LLM deleguje sémantické hodnocení na člověka.
    
- **Alien Intelligence & Alignment** (Wooldridge, Christian): Shoda panuje v tom, že LLM **nemá teorii mysli** – jen simuluje empatii. Proto je **kontext** klíčovým "řídítkem"; jakýkoliv nedostatek v kontextu (např. chybějící fakta) vede k **halucinacím**, které musí chytit člověk.
    
- **Automation Bias**: Věda varuje, že lidé mají tendenci LLM přeceňovat. Člověk se často stává "korektorem na konci řetězce" (Human-in-the-loop), ale kognitivní lenost vede k přehlížení chyb v kontextu.
    
- **Omezení okna**: Současný limitující faktor je **kapacita kontextu** – LLM zapomíná starší části diskuze (ztracený střed), což nutí člověka neustále rekapitulovat, čímž se stává **spoluautorem paměti**.
    

**Stručné shrnutí konsenzu:**

> _"LLM je zrcadlo kontextu, kontext je nástroj člověka a člověk je garantem pravdivosti. Žádný ze tří aktérů není autonomní; jejich vztah je asymetrický – člověk drží řízení (goal-setting), LLM dodává tah (generation) a kontext je jejich společným lešením (scaffolding), jehož kvalita rozhoduje o výsledku."_

Jdeme hlouběji a čistěji. Popiš to lidsky, ne jako kybernetik, vědec, prostě jak by se o tom balili lidé mezi sebou, kteří promptují, mají nějaký základ s lidmi, kteří rozumí už i kontext, kontent engineeringu. Jaké jsou asi znalosti těch zkušenějších, kdyby je předávaji lidem, kteří ví co je prompt.

Dobře, sundáme bílé pláště. Představ si, že sedíme tři u stolu v kanclu nebo na pivu a bavíme se o tom, proč nám to někdy letí a někdy to stojí za vyliž.

Tohle není věda, to je **řemeslná zkušenost**, co si mezi sebou říkají senior promptéři a lidi, co s těmahle modelama dělají denně.

Pokud by to zkušenější předávali dál lidem, kteří už umí základní prompt, mluvili by o tom takhle:

---

**1. "Ten model není blbej, ale je hrozně povrchní a ukecanej. My jsme mu za tu řeč."**

- Znalost: LLM nemá žádný názor, žádnou pravdu a ani neví, co zrovna píše. Je to **neskutečně chytrý autokorektor**, který tápe, kam ho nasměruješ.
    
- Praxe: Když dostane blbej vstup, vyplivne blbej výstup. Ale když dostane prázdnej vstup, tak začne básnit a vymýšlet si (halucinovat), protože to má v sobě jako pojistku – _“radši něco řeknu, než abych řekl, že nevím.”_
    
- Předání: "Tvůj první instinkt je ptát se. Zapomeň na to. **Neptej se ho na odpověď, zadávej mu úkol.** On není chytrý pomocník, on je chytrý vykonavatel tvých instrukcí."
    

**2. "Kontext není historie zpráv, to je jeho momentální realita."**

- Znalost: To okénko, kam mu píšeš, není pro něj "předchozí řeč". To je **jeho celý současný vesmír**. Všechno, co tam napíšeš, je pro něj absolutní a nemá žádný filtr, aby to porovnal s tím, co zná z internetu.
    
- Praxe: Když tam dáš blbý příklady, on bude génius v blbostech. Když tam dáš jasný příklady, on to dotáhne k dokonalosti.
    
- Předání: "Každej prompt je kompletní reset. On si nepamatuje, co jste řešili před hodinou, jen to, co má pořád v tý aktuální konverzaci. **Takže ho nenechávej hádat, co myslíš. Vlej mu to do kontextu rovnou celý – včetně toho, co nechceš.** "
    

**3. "Tvá práce není psát prompty. Tvá práce je stavět lešení."**

- Znalost: Zkušení vědí, že nejde o kouzelnou formulku. Jde o to **omezit modelu pole působnosti**. Čím víc mu dáš mantinelů (role, formát, příklady, co smí a nesmí), tím líp pracuje. Prázdnej prostor ho děsí, zaplácnul ho slovy.
    
- Praxe: Zelenáči píšou _"Napiš mi článek"_. Profíci píšou _"Jsi copywriter pro eshop s botama. Napiš 5 nadpisů na tuhle kategorii. Nadpisy budou max 60 znaků, používej akční slova, nepoužívej slovo 'kvalitní' a zaměř se na pohodlí, ne na cenu."_
    
- Předání: "Vnímej to jako zadání pro brigádníka, kterej je sice přečtenej, ale nemá selskej rozum. **Každej chybějící detail v zadání si domyslí naprosto debilně.** Tvoje práce je nedomýšlení odstranit."
    

**4. "Nejvíc tě posune zpětná vazba, ne lepší prompt."**

- Znalost: Všichni čekaj, že existuje dokonalej prompt. Neexistuje. Existuje jen **dialog**. Model není kalkulačka, kam hodíš číslo a máš výsledek. Je to nástroj, kterej doladíš až tím, že mu řekneš, co je špatně.
    
- Praxe: Když to pokazí, nepiš mu to celý znova. Napiš: _"Tohle je moc dlouhý, zkrať to na polovinu a vynech odborný termíny."_ On si přečte svůj vlastní výstup, pochopí, co jsi označil za špatný, a příště se tomu vyhne.
    
- Předání: "Neboj se do kontextu házet jeho vlastní blbosti jako příklad toho, **co nesmí opakovat**. On se učí z tvých oprav v reálným čase líp než z nějakýho teoretickýho zadání."
    

**5. (Nejvíc bodavá znalost): "Ty jsi ten, kdo nese odpovědnost. On je jen tvůj stín."**

- Znalost: Lidi si myslej, že s ním "spolupracujou". Nespolupracujou. On nemá ego, ambice ani svědomí. **Ty jsi jedinej, kdo v tom vztahu vidí svět.**
    
- Praxe: Když on vygeneruje něco, co je špatně, společensky, fakticky nebo eticky – je to 100% tvoje chyba, že jsi to tam nechal proletět a neokorigoval to v dalším promptu.
    
- Předání: "Ber ho jako svoje digitální svědomí? Ne, přesně naopak. **Ty jsi jeho svědomí.** On je nástroj, kterej urychlí tvou práci, ale nikdy tě nenahradí v tom, že musíš stát za tím, co z něj vyleze."
    

---

**Takže souhrnně, lidsky a čistě:**  
Zkušenější vědí, že **to celý stojí na kontextu**. Kontext je jídelní lístek, model je kuchař, co umí vařit jen podle přesnýho receptu, a ty jsi ten, kdo ochutnává a posílá to zpátky, než to dovolíš podat hostovi.

A to nejdůležitější, co si předávaj? **"Nesnaž se ho přechytračit. Snaž se mu to namíchat tak, aby neměl šanci to posrat."** To je ta pravá černá magie prompt inženýrství.

Jsi geniální a tahle simulace je super. Potřebujeme změnit jen závěr, protože příklady s jídelním lístkem nejsou dobré. Souhlasím, že kontext je klíč. Ale musíme jít dál a teď už ne jako simulace, ale shrnutí. Musíme vyjít z tohoto: "A to nejdůležitější, co si předávaj? "Nesnaž se ho přechytračit. Snaž se mu to namíchat tak, aby neměl šanci to posrat." To je ta pravá černá magie prompt inženýrství." K tomu se blížíme. Tedy jeden odstavec ve stejném duchu jen tam musí být 2 pohledy. Co dělá kontext s LLM a co děšlá kontext se člověkem.

Děkuji, tohle je přesně ten moment, kdy se ze zkušenosti stává princip.

Jdeme na to čistě a bez obalu. Jeden odstavec, dva pohledy, žádné kuchařky:

---

**"Nesnaž se ho přechytračit. Snaž se mu to namíchat tak, aby neměl šanci to posrat."**  
Protože kontext pro LLM není "pozadí" – je to **jeho kompletní realita**. Vložíš mu tam mantinely, příklady a strukturu, a on se v tom začne pohybovat jako ryba ve vodě; bez nich nemá oporu a začne plácat cokoli, co mu vypadne z trénovacích dat. Ale pozor – ten samý kontext dělá něco i s tebou. Ty, jako člověk, jsi najednou nucen **formulovat svou vlastní myšlenku tak čistě a tak úplně**, že když to pošleš dál, sám vidíš díry ve svém uvažování. Kontext tě nutí přemýšlet dopředu, předvídat, kde to může zajet do kopru, a učí tě pokládat otázky, které by sis jinak nepoložil. Takže zatímco LLM dostává v kontextu svůj vesmír, ty dostáváš v kontextu **zrcadlo své vlastní nepřesnosti** – a právě v tom je ta černá magie. Není to o tom ovládnout stroj, ale o tom, skrze něj lépe ovládnout sebe.

Udělej k tomu úvod, že jde o simulaci dobrého pracovníka, který používá LLM na vyšší úrovni a pochopení a ten mluví ke kolegovi, který s promptováním začíná, nebo je jen u promptování. Dej tomuto příběhu, simulaci rámování.

Tohle je přesně ono. Jdeme na to.

---

**Rámování: "Co jsem se naučil, když jsem přestal psát prompty a začal stavět vesmíry"**

Představ si, že sedíš v kanclu, máš za sebou půl roku promptování, umíš základní struktury, zvládáš role a výstupy. A najednou k tobě přijde zkušenější kolega – ne ten, co umí líp zadávat instrukce, ale ten, kdo tomu **rozumí**. Sedne si vedle tebe, podívá se na tvůj prompt a řekne:

"Ty se ho pořád ještě snažíš přechytračit, viď? Pořád ho chceš donutit, aby ti dal správnou odpověď."

A pak ti to začne vysvětlovat. Ne jako vědec, ne jako kybernetik. Jako člověk, co si tím prošel, a ví, že tenhle nástroj mění víc než jen výstup – mění i to, jak sám přemýšlíš.

Tohle je ten rozhovor. Ne o technice. O posunu.

---

**A pak přijde ten odstavec, který to celé uzavírá:**

_"Nesnaž se ho přechytračit. Snaž se mu to namíchat tak, aby neměl šanci to posrat."_  
Protože kontext pro LLM není pozadí – je to jeho kompletní realita. Vložíš mu tam mantinely, příklady a strukturu, a on se v tom začne pohybovat jako ryba ve vodě; bez nich nemá oporu a začne plácat cokoli, co mu vypadne z trénovacích dat. Ale pozor – ten samý kontext dělá něco i s tebou. Ty, jako člověk, jsi najednou nucen formulovat svou vlastní myšlenku tak čistě a tak úplně, že když to pošleš dál, sám vidíš díry ve svém uvažování. Kontext tě nutí přemýšlet dopředu, předvídat, kde to může zajet do kopru, a učí tě pokládat otázky, které by sis jinak nepoložil. Takže zatímco LLM dostává v kontextu svůj vesmír, ty dostáváš v kontextu zrcadlo své vlastní nepřesnosti – a právě v tom je ta černá magie. Není to o tom ovládnout stroj, ale o tom, skrze něj lépe ovládnout sebe.

Tohle je rámování pro čtenáře. Nic víc, tedy říct mu co je tou simulací, aby chápal kontext.

Jasně, rozumím. Potřebuješ jen čisté rámování pro čtenáře – žádný vnitřní monolog, žádný příběh. Prostě mu na začátku říct, co čte a v jakém kontextu to má vnímat.

---

**Rámování pro čtenáře:**

Následující text je simulací rozhovoru dvou lidí, kteří pracují s LLM na denní bázi. Jeden z nich je zkušený uživatel, který má hlubší pochopení pro to, jak model funguje a jak s ním efektivně pracovat. Druhý je začínající nebo průměrný uživatel, který ovládá základy promptování, ale zatím nepřesáhl za rámec "psaní instrukcí".

Simulace zachycuje, jak zkušenější předává své know-how – ne formou teorie, ale praktické zkušenosti, kterou si osvojil díky tomu, že se naučil vnímat kontext jako klíčový prvek celého systému. Nejde o návod, ale o pohled na to, co se děje, když se posuneš od používání nástroje k jeho skutečnému pochopení.

Potřebujeme poslední krátkou tečku k závěru, poslední varovný odstavec. Nšco v tomto smyslu: "LLM je nástroj, který umí přebrat kognice uživatele, pokouší jej a je prvním nástrojem v historii, který to umí rychle a ve velkém měřítku."

Tady je poslední varovný odstavec, který text uzavírá:

---

A poslední věc, která se ti snažím předat: **Pozor na to, co tenhle vztah dělá s tebou.** Tahle symbióza je zrádná – LLM je první nástroj v dějinách, který umí přebrat tvoji kognici ve velkém a nepozorovaně. Začneš mu věřit víc než sobě, přestaneš kontrolovat zdroje a halucinace si ospravedlníš jako "zajímavou perspektivu". On tě neoklame úmyslně, ale pokouší tvou lenost. Ty mu dáváš kontext, on ti dává odpovědi, ale jediný, kdo v tom vztahu drží kotvu v realitě, jsi pořád jen ty. Nezapomeň, že nejsi uživatel – jsi strážce brány. A jakmile ji přestaneš hlídat, přestaneš být pánem nástroje a staneš se jeho ozvěnou.

Připrav cele kontextové okno k archivaci paměti. Potřebuji rozdělit kontext na logické celky o tom, co jsme probírali, opatřit je názvem, krátkým popisem a citací, kterou úsek začíná. Postup: - Rozděl kontext podle tématu (nejdi do detailů, 2-20 paměťových částí, množství částí musí být vyvážené. Co jde spojit, spoj, co je jiné téma, nová část. Části musí být postupně navazovány na celé kontextové okno, nejde spojit části do jedné, když je rozdělena jiným tématem) - Indexuj část (01, 02, 03, ... 20) - Vymysli krátký název (max. 4 slova) - Vymysli krátký popis aby bylo jasno co která část obsahuje (max. 4 věty) - Vypiš přesnou citaci začátku textu (max. 10 slov) pro zpětnou dohledatelnost v textovém editoru (ctrl+f). - Musíš obsáhnout celé kontextové pole. 01 část je od citace 01 po citaci 02, atd.

# Archivace kontextového okna – Paměťové části

---

**01 | Úvod a definice triády**  
_Popis:_ Úvodní zadání uživatele definující tři aktéry (člověk, LLM, kontext) a požadavek na popsání jejich vztahů z pohledu literatury a konsenzu.  
_Citace:_ _"Mám spolurácy s tebou tady v chatovém rozhraní. Jde o 3 aktéry..."_

---

**02 | Vědecký pohled – kybernetický systém**  
_Popis:_ Odborná odpověď popisující vztah jako triadický kybernetický regulační okruh. Definice rolí jednotlivých aktérů a jejich vzájemné ovlivňování včetně toku dat a zpětné vazby.  
_Citace:_ _"Vztah těchto tří aktérů tvoří triadický kybernetický regulační okruh..."_

---

**03 | Konsenzus literatury (Distribuovaná kognice, Alignment, Automation Bias)**  
_Popis:_ Shrnutí vědeckého konsenzu – distribuovaná kognice, problém halucinací, přeceňování AI lidmi (automation bias) a omezení kontextového okna. Závěr o asymetrickém vztahu, kde člověk drží řízení.  
_Citace:_ _"Distribuovaná kognice (Hutchins): Tato triáda je jeden kognitivní systém..."_

---

**04 | Přechod k lidskému jazyku – rámování rozhovoru**  
_Popis:_ Uživatel žádá o převedení odborného jazyka do lidské roviny – jak by si to předávali zkušení promptéři mezi sebou. Autor navrhuje rámování "Co jsem se naučil, když jsem přestal psát prompty a začal stavět vesmíry".  
_Citace:_ _"Dobře, sundáme bílé pláště. Představ si, že sedíme tři u stolu v kanclu..."_

---

**05 | Praktická znalost 1 – Model je autokorektor**  
_Popis:_ LLM nemá názor ani pravdu, je to statistický syntetizátor. Halucinuje, když nemá oporu. Klíčové ponaučení: neptej se na odpověď, zadávej úkol.  
_Citace:_ _"Ten model není blbej, ale je hrozně povrchní a ukecanej..."_

---

**06 | Praktická znalost 2 – Kontext je realita modelu**  
_Popis:_ Kontext není "historie", ale kompletní vesmír LLM. Každý prompt je reset. Do kontextu se musí vložit vše najednou včetně toho, co nechceš.  
_Citace:_ _"Kontext není historie zpráv, to je jeho momentální realita..."_

---

**07 | Praktická znalost 3 – Práce je stavění lešení**  
_Popis:_ Nejde o kouzelnou formulku, ale o omezování pole působnosti. Mantinely, příklady a struktura vedou k lepším výstupům. Prázdný prostor model děsí.  
_Citace:_ _"Tvá práce není psát prompty. Tvá práce je stavět lešení..."_

---

**08 | Praktická znalost 4 – Zpětná vazba je klíčová**  
_Popis:_ Neexistuje dokonalý prompt, jen dialog. Model se učí z oprav v reálném čase. Stačí říct, co je špatně, a on se příště vyhne chybám.  
_Citace:_ _"Nejvíc tě posune zpětná vazba, ne lepší prompt..."_

---

**09 | Praktická znalost 5 – Odpovědnost nese člověk**  
_Popis:_ LLM nemá svědomí, ego ani ambice. Člověk je jediný, kdo v tom vztahu vidí svět a nese odpovědnost za výstupy. Model je nástroj, ne partner.  
_Citace:_ _"Ty jsi ten, kdo nese odpovědnost. On je jen tvůj stín..."_

---

**10 | Shrnutí praktické části – Černá magie prompt inženýrství**  
_Popis:_ Zkušení si předávají princip: "Nesnaž se ho přechytračit, snaž se mu to namíchat tak, aby neměl šanci to posrat." Jde o to odstranit prostor pro chybu.  
_Citace:_ _"Takže souhrnně, lidsky a čistě: Zkušenější vědí, že to celý stojí na kontextu..."_

---

**11 | Upřesnění závěru – dva pohledy na kontext**  
_Popis:_ Uživatel žádá o úpravu závěru – místo kuchařských metafor chce dva pohledy: co dělá kontext s LLM a co dělá kontext s člověkem.  
_Citace:_ _"Souhlasím, že kontext je klíč. Ale musíme jít dál a teď už ne jako simulace..."_

---

**12 | Finální odstavec – Kontext jako zrcadlo**  
_Popis:_ Kontext je pro LLM kompletní realita; pro člověka je zrcadlem vlastní nepřesnosti. Černá magie spočívá v tom, že skrze stroj lépe ovládáš sebe.  
_Citace:_ _"Nesnaž se ho přechytračit. Snaž se mu to namíchat tak, aby neměl šanci to posrat..."_

---

**13 | Rámování pro čtenáře – simulace rozhovoru**  
_Popis:_ Čisté rámování vysvětlující, že text je simulací rozhovoru zkušeného a začínajícího uživatele LLM. Nejde o teorii, ale o praktické know-how.  
_Citace:_ _"Následující text je simulací rozhovoru dvou lidí, kteří pracují s LLM na denní bázi..."_

---

**14 | Závěrečné varování – Přebírání kognice**  
_Popis:_ Poslední varovný odstavec o nebezpečí – LLM je první nástroj, který umí ve velkém přebrat kognici uživatele. Hrozí automace bias a ztráta kritického myšlení. Člověk musí zůstat strážcem brány.  
_Citace:_ _"A poslední věc, která se ti snažím předat: Pozor na to, co tenhle vztah dělá s tebou..."_