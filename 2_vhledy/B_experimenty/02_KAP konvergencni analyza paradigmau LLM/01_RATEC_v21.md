# R.A.T.E.-C v2.1: Relative Assessment of Technological Emergence & Convergence

## Dvouvrstvá matice pro měření diskurzu o LLM a lidské kognici

---

## ÚVOD

### Co jsme udělali

R.A.T.E.-C je metodika pro měření relativní viditelnosti témat v online diskurzu pomocí LLM. Vyvinuli jsme ji jako první vrstvu širšího výzkumného rámce KAP (Konvergenční Analýza Paradigmatu), který zkoumá, jak se sbíhají různé přístupy k augmentaci lidské kognice.

Metodika prošla třemi iteracemi:

|Verze|Datum|Klíčový posun|
|---|---|---|
|**v1**|Pilot 1|4 kategorie (Chat, Vibecoding, Agentic, Enterprise) – jednorozměrný poměr|
|**v2**|Pilot 2|5 modů × 3 kontexty – maticový výstup. Odhaleno, že Enterprise je doména, ne modus|
|**v2.1**|Finální|Dvouvrstvá matice 3×3 – oddělení deskriptivní a behaviorální vrstvy|

### Proč jsme to udělali

Původním záměrem bylo zjistit, zda LLM dokáže z online diskurzu odhadnout relativní poměr využívání různých technologií. V průběhu vývoje se však ukázalo, že:

1. **LLM neměří realitu – měří diskurz.** To, o čem se mluví, není totéž co to, co se skutečně používá.
    
2. **Diskurz sám je strukturován kolem osy kognitivní autonomie.** Lidé rozlišují mezi nahrazováním myšlení (delegace) a jeho posilováním (amplifikace) – a toto rozlišení je v datech měřitelné.
    
3. **Diskurz je aspirační, ne deskriptivní.** Dominuje v něm narativ "posílení myšlení", přestože behaviorální data i vědecká evidence ukazují převahu delegace.
    

Metodika R.A.T.E.-C v2.1 je navržena tak, aby tyto dva pohledy – diskurzivní a behaviorální – explicitně oddělila.

### Jak jsme to udělali

Metodika pracuje ve dvou fázích:

**Fáze sběru (P1–P4):** Čtyři nezávislé prompty jsou zadány do LLM (každý v samostatné konverzaci, teplota 0, s přístupem k internetu). Každý prompt měří jinou dimenzi diskurzu: frekvenci, trendy, hloubku zapojení a sentiment.

**Fáze syntézy (P5):** Pátý prompt obdrží všechny čtyři výstupy a vytvoří strukturovanou analytickou syntézu – matici viditelnosti, interpretaci rozporů, identifikaci prázdných míst a epistemologické limity.

Finální výstup obsahuje jak deskriptivní matici (co diskurz říká), tak kritickou reflexi (jak se to liší od behaviorální reality).

### Omezení finální verze

1. **Single-model design:** Všechny prompty jsou zadávány jednomu modelu. Multi-model triangulace by zvýšila robustnost, ale nebyla v této fázi provedena.
    
2. **Diskurz ≠ realita:** Matice měří jazykové rámování, nikoli objektivní kognitivní dopady. Toto omezení je explicitně adresováno v definici matice i v syntézním promptu.
    
3. **Časová momentka:** Výsledky jsou platné ke dni provedení. Diskurz se vyvíjí rychle.
    
4. **Jazykové omezení:** Data pocházejí primárně z anglicky mluvícího prostředí.
    
5. **Chybějící behaviorální validace:** Druhá (behaviorální) vrstva matice je v této verzi pouze konceptuální – není operacionalizována jako samostatný prompt.
    

### Co lze vylepšit

- **Multi-model ensemble:** Zadání identických promptů do 3+ modelů (GPT-4o, Claude, Gemini) a porovnání výstupů.
    
- **Behaviorální matice:** Vytvoření samostatné sady promptů, které neanalyzují jazyk diskurzu, ale klasifikují popisované chování podle behaviorálních kritérií (míra kontroly, počet iterací, míra vloženého lidského vstupu).
    
- **Longitudinální měření:** Opakování měření v čase pro zachycení dynamiky diskurzu.
    
- **Externí validace:** Systematické porovnání s tvrdými daty (Stack Overflow survey, tržní analýzy, grantové databáze).
    

---

## METODIKA

### Definiční rámec: Matice 3×3

Metodika měří online diskurz o používání LLM v matici dvou os:

**Osa X – KDO používá:**

- **A. Jednotlivec** – osobní použití, hobby, učení, každodenní úkoly
    
- **B. Profesionál** – pracovní použití jednotlivcem (vývojář, analytik, tvůrce)
    
- **C. Společnost** – firmy, instituce, organizované nasazení
    

**Osa Y – MÍRA KOGNITIVNÍ AUTONOMIE ČLOVĚKA:**

Tato osa má dvě vrstvy – deskriptivní a behaviorální. Vrstvy jsou ve finální verzi explicitně odděleny:

|Řádek|Deskriptivní vrstva (jazyk diskurzu)|Behaviorální vrstva (reálné chování)|
|---|---|---|
|**1. Myšlení nahrazeno**|Diskurz používá varovné termíny: "kognitivní kapitulace", "efekt berličky", "delegace myšlení", "outsourcovat myšlení"|Člověk zadá prompt, převezme výstup bez ověření. Kognitivní zátěž plně na LLM.|
|**2. Myšlení podpořeno**|Diskurz používá pragmatické termíny: "asistent myšlení", "nástroj", "scaffolding", "produktivita s dohledem"|Člověk zadá prompt, zkontroluje výstup, případně upraví. LLM generuje, člověk hodnotí.|
|**3. Myšlení posíleno**|Diskurz používá partnerské termíny: "thinking partner", "kognitivní exoskeleton", "rozšířená mysl", "ko-kreativní proces"|Člověk a LLM vedou iterativní dialog. Člověk vkládá vlastní myšlenky, LLM je rozvíjí. Výstup je spolutvorbou.|

**Kritické upozornění:** Pilotní měření odhalilo, že deskriptivní a behaviorální vrstva se mohou významně rozcházet. Chování klasifikované diskurzem jako "posílení" (řádek 3) může být behaviorálně nerozlišitelné od "podpory" (řádek 2) – v obou případech stroj přebírá kognitivní zátěž generování a člověk plní roli hodnotitele. Metodika proto explicitně přiznává, že **měří jazyk diskurzu, nikoli objektivní kognitivní dopad**. Behaviorální vrstva je uvedena jako interpretační rámec, nikoli jako samostatně měřená veličina.

---

### Protokol měření

**Podmínky:**

- Model: LLM dle volby (pilot proveden na DeepSeek fast)
    
- Teplota: 0
    
- Internet: zapnutý u P1–P4
    
- Každý prompt do nové konverzace (zabraňuje kontaminaci kontextem)
    
- Ukládat kompletní neupravené odpovědi
    

---

### Prompt P1: Matice viditelnosti

text

[REŽIM: Teplota 0, Internet ZAPNUTÝ]
[EPISTEMOLOGICKÝ RÁMEC: Tato analýza měří JAZYK online diskurzu, nikoli reálné počty uživatelů ani objektivní kognitivní dopady.]
DEFINICE MATICE:
Osa X – KDO POUŽÍVÁ:
A. Jednotlivec – osobní použití, hobby, učení, každodenní úkoly
B. Profesionál – pracovní použití jednotlivcem (vývojář, analytik, tvůrce)
C. Společnost – firmy, instituce, organizované nasazení
Osa Y – JAZYK DISKURZU O KOGNITIVNÍ AUTONOMII:
1. Myšlení nahrazeno – diskurz používá varovné termíny („kognitivní kapitulace“, „efekt berličky“, „delegace myšlení“, „outsourcovat myšlení“)
2. Myšlení podpořeno – diskurz používá pragmatické termíny („asistent myšlení“, „nástroj“, „scaffolding“, „produktivita s dohledem“)
3. Myšlení posíleno – diskurz používá partnerské termíny („thinking partner“, „kognitivní exoskeleton“, „rozšířená mysl“, „ko-kreativní proces“)
DŮLEŽITÉ ROZLIŠENÍ:
Tato matice měří JAZYK, kterým diskurz popisuje používání LLM.
Neposuzuj, zda popisované chování skutečně posiluje myšlení.
Pouze klasifikuj, jaký typ jazyka diskurz pro dané chování používá.
ANALYZUJ online diskurz Q2 2026 a vytvoř matici 3×3.
Každá buňka obsahuje:
a) % viditelnosti v diskurzu (součet všech 9 buněk = 100 %)
b) Převažující sloveso nebo slovní spojení, které diskurz v dané kombinaci používá
PRAVIDLA:
- Vycházej z dat na internetu (posledních 6 měsíců)
- Pokud kombinace nemá signál, uveď 0 % a „bez signálu“
- Neodhaduj počty uživatelů

---

### Prompt P2: Trendy objemu a sentimentu

text

[REŽIM: Teplota 0, Internet ZAPNUTÝ]
DEFINICE MATICE:
[Vložit stejnou definici jako v P1]
Pro každou z 9 buněk matice urči:
a) Trend OBJEMU zmínek za posledních 12 měsíců:
   ROSTOUCÍ / STABILNÍ / KLESAJÍCÍ / ŽÁDNÝ SIGNÁL
b) Trend SENTIMENTU:
   ZLEPŠUJE SE / STABILNÍ / ZHORŠUJE SE / NELZE URČIT
VÝSTUP:
Dvě tabulky 3×3 (objem + sentiment) a stručný komentář.
PRAVIDLA:
- Vycházej z dat na internetu
- Pokud data chybí, napiš „ŽÁDNÝ SIGNÁL“ / „NELZE URČIT“
- Rozlišuj objem a sentiment – mohou jít opačným směrem

---

### Prompt P3: Hloubka zapojení a bariéry

text

[REŽIM: Teplota 0, Internet ZAPNUTÝ]
DEFINICE MATICE:
[Vložit stejnou definici jako v P1]
Pro každou z 9 buněk matice urči:
a) Typického uživatele (roli)
b) Hlavní bariéru adopce (pokud existuje)
c) Typický počet interakcí: 1–3 / 4–10 / 11–20 / 21+
PRAVIDLA:
- Vycházej z popisů v online diskurzu
- Pokud data chybí, explicitně to uveď

---

### Prompt P4: Sentiment a jazyk napříč úrovněmi

text

[REŽIM: Teplota 0, Internet ZAPNUTÝ]
DEFINICE MATICE:
[Vložit stejnou definici jako v P1]
Pro každou ze 3 ÚROVNÍ kognitivní autonomie (1, 2, 3) – nikoli pro jednotlivé buňky, ale pro celý řádek:
a) Převažující sentiment: POZITIVNÍ / SMÍŠENÝ / NEGATIVNÍ
b) 5 klíčových termínů nebo metafor, které diskurz pro tuto úroveň používá
c) Nejčastěji zmiňované nástroje/platformy
PRAVIDLA:
- Vycházej z dat na internetu
- Pokud úroveň nemá signál, uveď „ŽÁDNÝ SIGNÁL“

---

### Prompt P5: Strukturovaná analytická syntéza

text

[REŽIM: Teplota 0]
Dostal jsi čtyři nezávislé analýzy online diskurzu o používání LLM v Q2 2026.
Všechny pracovaly se stejnou maticí 3×3:
Osa X – KDO POUŽÍVÁ: A. Jednotlivec, B. Profesionál, C. Společnost
Osa Y – JAZYK DISKURZU O KOGNITIVNÍ AUTONOMII:
  1. Myšlení nahrazeno (varovné termíny)
  2. Myšlení podpořeno (pragmatické termíny)
  3. Myšlení posíleno (partnerské termíny)
TVÉ VSTUPY:
[Zde vlož kompletní výstupy P1, P2, P3, P4]
VÝSTUP ROZDĚL DO TĚCHTO SEKCÍ:
SEKCE 1 – SOUHRNNÁ MATICE
Tabulka 3×3 integrující P1 a P2:
- % viditelnosti (z P1)
- Trend objemu (z P2)
- Trend sentimentu (z P2)
SEKCE 2 – ZJIŠTĚNÍ
2.1 Dominantní narativ a hlavní dynamika
- Které buňky matice mají nejvyšší viditelnost?
- Převládá v diskurzu rámec nahrazování, nebo posilování myšlení?
- Jak se tyto dva rámce vzájemně ovlivňují?
2.2 Aktéři: kdo je v diskurzu nejviditelnější?
- Který typ uživatele je v diskurzu nejvíce zastoupen?
- Liší se rozložení viditelnosti mezi typy uživatelů?
- Kde je rozpor mezi viditelností a odhadovanou reálnou mírou adopce?
2.3 Konflikty a rozpory
- Kde dochází k rozporu mezi viditelností a sentimentem?
- Kde jde objem a sentiment opačným směrem?
- Existuje kombinace, o které se mluví málo, ale silně negativně?
2.4 Pohyby a trendy
- Které buňky vykazují nejsilnější růst?
- Které stagnují nebo upadají?
- Kam se diskurz jako celek posouvá?
2.5 Prázdná a slabá místa
- Která buňka má nejnižší nebo nulovou viditelnost?
- Představuje tato absence přehlédnutou příležitost, nebo logický důsledek?
2.6 Jazyk diskurzu
- Jaké termíny a metafory diskurz pro jednotlivé úrovně používá?
- Které převažují a co to vypovídá o převažujícím rámci uvažování?
SEKCE 3 – SHRNUJÍCÍ INTERPRETACE
Maximálně 4 věty formulující hlavní zjištění.
SEKCE 4 – EPISTEMOLOGICKÉ LIMITY
Uveď 3–5 nejvýznamnějších limitací.
SEKCE 5 – KRITICKÁ REFLEXE: JAZYK VS. CHOVÁNÍ
Tato sekce je zásadní. Zamysli se nad vztahem mezi tím, co diskurz říká, a tím, co se pravděpodobně děje:
a) Lze na základě dat rozlišit, zda je chování klasifikované jako „podpora“ (řádek 2) a „posílení“ (řádek 3) behaviorálně odlišné?
   - Pokud ano – v čem spočívá rozdíl?
   - Pokud ne – co to znamená pro validitu matice?
b) Do jaké míry je dominance buněk „posílení“ (A3, B3) odrazem reálné praxe, a do jaké míry preferovaným sebepojetím uživatelů?
   - Opři se o data z P2 (sentiment, trendy) a P4 (jazyk, metafory).
c) Pokud bychom měřili nikoli jazyk diskurzu, ale reálné chování – jak by se poměr mezi řádky 1, 2, 3 pravděpodobně změnil?
   - Zdůvodni na základě behaviorálních indikátorů v datech.
PRAVIDLA:
- Každé tvrzení opři o signály ze vstupů (P1, P2, P3, P4)
- Pokud data vykazují rozpor, přiznej ho a interpretuj
- Piš úsporně, akademickým tónem
- Nepřidávej informace, které nejsou ve vstupech

---

### Finální výstup

Finální výstup R.A.T.E.-C v2.1 se skládá z:

1. **Souhrnné matice 3×3** – integrovaná data o viditelnosti, trendech a sentimentu
    
2. **Strukturovaných zjištění** – 6 dimenzí analýzy diskurzu
    
3. **Shrnující interpretace** – hlavní zjištění v akademické formě
    
4. **Epistemologických limitů** – explicitní přiznání omezení
    
5. **Kritické reflexe jazyka vs. chování** – rozlišení deskriptivní a behaviorální vrstvy
    

Příklad finálního výstupu je k dispozici v kontextovém poli (část 44).

---

## PODMÍNKY POUŽITÍ

Tato metodika je určena pro výzkumné účely. Její výstupy měří **relativní viditelnost jazykových rámců v online diskurzu**, nikoli objektivní realitu. Jakákoli interpretace výsledků musí toto omezení explicitně reflektovat.

Pro plnou verzi vývoje metodiky včetně slepých uliček, pilotních testů a triangulace s externími zdroji viz přiložené kontextové pole.