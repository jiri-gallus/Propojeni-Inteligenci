# Prompt endineering
Na internetu je mnoho zaručených informací, jak promptovat LLM. Trh se školením umělé inteligence tento trend ukazuje:

| Segment trhu                   | Velikost trhu (rok) | Projekce (rok)  | CAGR  |
| ------------------------------ | ------------------- | --------------- | ----- |
| **AI model training market**   | $17.15B (2025)      | $124.92B (2032) | 32.8% |
| **AI training dataset market** | $3.59B (2025)       | $23.18B (2034)  | 22.9% |
| **AI in education market**     | $8.3B (2025)        | $57.2B (2033)   | 25.9% |
| **Generativní AI v L&D**       | $1.01B (2025)       | $4.42B (2030)   | 34.2% |
| **Responsible AI training**    | $1.98B (2025)       | $7.1B (2030)    | 29.2% |
| **Prompt engineering**         | $0,5B (2025)        | $4,7B (2034)    | 33.3% |

Počet pracovních míst vyžadujících prompt engineering roste trojnásobně mezi lety 2024-2026.
Srovnání profesí na Americkém trhu

| Profese                      | **Reálný medián platu (USD/rok)** |
| ---------------------------- | --------------------------------- |
| **Prompt inženýr**           | ~$60 000 - $128 000               |
| Softwarový inženýr           | ~$118 600 - $144 000              |
| Lékař (všechny specializace) | ~$103 000 - $149 000              |
| Právník                      | ~$92 500 - $100 600               |
| Datový vědec                 | ~$97 500 - $130 000               |

## Používané techniky
- Zero-shot - instrukce bez jakéhokoli příkladu
- Few-shot - instrukce s příklady
- Chain-of-Thought - instrukce aby model rozepsal svůj myšlenkový proces před tím, než generuje požadované tokeny
- Role prompting - přiřazení modelu roli, osobnost, nebo specifickou roli
- Iterativní vylepšování promptů

## Používané metody
- Iterativní vylepšování promptů - metoda pokus omyl s testováním reakce LLM
- RICE - metoda přiřazení Role, Instrukce, Obsahu, Příkladu
- COAST - metoda přiřazení Obsahu, Cíle, Instrukce, Stylu, Formátu
- Šablony - metoda, která se na prompty dívá jako na šablony a ukládá ty fungující pro pozdější použití
- Formátování - scafolding, hierarchie textu, markdown, JSON, HTML ...

# Hlídání účelu
výše popsané techniky a metody nejsou špatné. Nemusí se zahazovat jen pro to, že nezapadají do exokortexu. Naopak. Oni tam zapadají, protože každá podporuje jiný účel kognice. Otázkou jen je, jaký.

## Účelový role prompting

**Účel kognice:**
Jsem uživatel, který chce od LLM dostat kritiku na svou práci.

**Přímá role:**
> _"Jsi LLM v roli oponenta. Zkritizuj mou práci."_

**Nepřímá role:**
> _"Jsem oponentem studenta, který mi přinesl práci. Zkritizuj ji."_

Není špatný a dobrý prompt, jen nastavení hranic účelu a očekávání uživatele.

Pro přímou roli:
- LLM bude pracovat ve dvou režimech.
	- Chránit uživatele a pomáhat mu
	- Kritizovat práci uživatele
- Výstup bude slabá kritika s lidskou tváří.

Pro nepřímou roli:
- LLM bude pracovat ve dvou režimech.
	- Chránit oponenta a pomáhat mu
	- Kritizovat práci uživatele
- Výstup bude silná kritika, která ubližuje egu.

**Uživatel definuje prompt a pokud si umí definovat účel, najde způsob, jak jej naplnit i když stojí účel proti němu.**

## Sofistikovaný prompting
V tomto případě nepůjdu na všeobecnou teorii, ale ukázku praxe.

**Účel kognice:**
Analyzovat text a vypsat citace, které jsou mimo téma, a které téma neprohlubují.

**Mechanismy se kterými musí prompt počítat**
- Next-token prediction
	- generování tokenu po tokenu na základě pravděpodobnosti z trénovacích dat.
- Attention mechanismus
	- váhování důležitosti tokenů v kontextu.
- Positional encoding
	- informace o pozici tokenu, zvýhodňující relativní blízkost.
- ecency bias
	- vyšší váha novějších tokenů.
- Front-heavy bias
	- menší vliv tokenů na začátku kontextu.
- Pattern recognition bias
	- preference známých vzorů a pokračování.
- Bezestavovost (statelessness)
	- každý vstup je zpracováván nezávisle bez inherentní paměti mezi dotazy.
- Softmax / Attention jako "rozmazané okno"
	- rozprostření pozornosti a postupné oslabování staršího kontextu.
- Feedback loop (next-token)
	- generovaný token se stává součástí kontextu pro token následující, čímž si model posiluje vlastní drift.
- Halucinace z nadměrné důvěry
	- generování nepodložených tvrzení při nedostatku relevantního kontextu.
- Goal drift
	- postupné odchylování od původního záměru v důsledku kumulativních tlaků kontextu a generování.

### Prompt

#### Úkol  

Je potřeba rozložit kontextové okno na informační celky. Jednotlivé věty, které se doplňují. nejít na nižší celky. Celý kontext budeš tvořit ve 3 vlnách.
##### 1. generace tokenů
- Definovat téma
Zvolí se metrika posuzování.
##### 2. generace tokenů
- vypsat celé citace celků a obhájit, které jsou mimo téma.
Odfiltrují se celky, které nemusíme analyzovat.
##### 3. generace tokenů
- vypsat celé citace celků a obhájit, které téma neprohlubují.
Analýzu procházet a vypisovat celky zpětně. Na konci kontextového okna se očekává nejvíce neprohlubujících témat.
#### Zlaté pravidlo
Bojujeme proti patern recognition bias.
- Nevypisuješ do kontextu nic jiného, než 1. 2. 3. vlnu a text zlatého pravidla.
- 1. vlna nesmí vést k označení prvního výskytu myšlenky za neprohlubující.
- 2. a 3. vlna má opakující se vzor pro každý jednotlivý celek. Celá citace>Obhajoba>Text zlatého pravidla
- Hledáme všechny informační celky, které téma neprohlubují.
##### Text zlatého pravidla:
"Vzor v kontextu je principiální. Nejde o hranice možného. LLM se musí dívat při každém tokenu nezaujatě vůči vzoru. Braň zlaté pravidlo!"
##### Text k analýze
...

### Jak prompt funguje?
Prompt funguje jako **vícevrstvý kognitivní regulátor**, který pracuje s mechanismy LLM na několika úrovních najednou.

V první vlně vytváří referenční rámec (téma a metriku), čímž definuje účel celé interakce a dává modelu pevný bod, od kterého se odvíjí veškeré hodnocení.

Ve druhé a třetí vlně nutí model k systematické filtraci
- nejprve hrubé (mimo téma)
- pak jemné (neprohlubuje téma)
přičemž každý hodnocený celek musí být citován a obhájen, což znemožňuje halucinace a slepá tvrzení.

Opakovaná kognitivní kotva (zlaté pravidlo) v pravidelných intervalech přerušuje pattern recognition bias a vrací pozornost k účelu, zatímco backtracking (zpětný průchod kontextem) ruší front-heavy a recency bias tím, že nutí model hodnotit celky v opačném pořadí.

Celý prompt je sebeomezující
- model smí do kontextu vypisovat pouze předepsané vlny a zlaté pravidlo, čímž je zabráněno šíření vlastního goal driftu.
- model negeneruje lineárně, ale rekurzivně . Sám si definuje metriku, sám koriguje svůj vlastní bias a sám reviduje své výstupy.
- model se chová, jako by měl meta-kognici.

### Analýza sítě T-neuronů promptu.
- **A** (Úkol) je kořen, ale ne dominuje – je propojen se všemi.
- **B** (1. vlna) je referenční bod pro C a D, ale je zároveň omezen E.
- **C** (2. vlna) a **D** (3. vlna) jsou kaskádově propojeny, ale D má zpětnovazební smyčku do C.
- **E** (Zlaté pravidlo – rámec) je regulátor, který omezuje B, C, D a definuje F.
- **F** (Text zlatého pravidla) je kotva, která je vložena do C a D a vytváří rekurzivní smyčku.
- **G** (Text k analýze) je zdroj, který je zpracováván C a D.
### Analýza sítě T-neuronů kontextu.
- A-G - prompt
- H - 1. vlna generace - reference pro CH a I
- CH - 2. vlna generace - každou část generuje pomocí reference H
	- CH1
	- CH2
	- ...
	- CHN
	- na konci každé části CHX se generuje F, řídí attention modelu před každou další generací si opakuje zlaté pravidlo
- I - 3. vlna generace - každou část generuje pomocí reference H a omezení CH
	- I1
	- I2
	- ...
	- IN
	- na konci každé části IX se generuje F, řídí attention modelu před každou další generací si opakuje zlaté pravidlo
### Neuronová síť promptu
I tento zdánlivě krátký prompt vytváří mnoho propojení na úrovni T-neuronů. V kombinaci generovaných tokenů pomocí velkých jazykových modelů se chová jako neuronová síť na úrovni jednoho promptu a jedné odpovědi LLM.

Ve chvíli, kdy se koncept přenese na vyšší celky v hierarchii účelu kognitivního výstupu, stává se tato síť generátorem emergentních výstupů při interakcích s LLM a uživatele.

# Závěr promptování

Prompt je základním jazykem komunikace s LLM. Předurčuje vlastnosti generovaných T-neuronů. Prompt je první linií obrany tématu, účelu a kognitivního záměru.
Prompt ovlivňuje parametry exokortexu. Nastavuje pracovní kognitivní prostor.