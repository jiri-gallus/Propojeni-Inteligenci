> Dodnes se vedou spory o to, kdo byl předkem Homo erectus.
> Australopithecus?
> Homo habilis?
> Paleoatropologové se dělí na dva nesmiřitelné tábory.
> Australopithékové tvrdí, že Homo habilis měl 3 milióny let, než zvládnul rozdělat oheň.
> Habilisané tohle nepřijímají. "Člověk je chytřejší!" řvou na své kolegy a říkají, že to trvalo jen 1,4 miliónu let.
> Obě strany svou pozici opírají o písmo.
> Co na to Homo erectus?
> "Chlapi, já jsem ten oheň rozdělal, abych upekl maso. Nenaučil jsem se číst!"

# Synapse engineering
Synapse engineering není ničím novým, ve větší či menší míře tohle uživatelé a společnosti používají. Nová je terminologie, diagnostika a způsob uvažování nad textem. Synapse engineering se dělí na diagnostickou a aplikační rovinu.

## Kontextová diagnostika interakcí
Před zavedením diagnostiky textu interakcí dojde k sjednocení a popis důležitých pojmů:
- Interakce - jedna výměna mezi uživatelem a LLM
- Kontext - text diagnostiky dělení na
	- Prompt - text uživatele
	- Generované tokeny - text LLM
- T-neuron - informační celek textu nesoucí myšlenku. Minimální velikost je jedna věta textu.
- Téma - Referenční téma vůči němuž se posuzuje myšlena T-neuronu.
- Účel - důvod pro který se vstupuje do interakce s LLM. Může být složeno z více témat.

### Příprava dat
Diagnostika se dělá na úrovni křivek interakcí, které se skládají z jednotlivých bodů. Body křivek interakcí jsou určeny počtem znaků textu. Pro přípravu je text dělen podle 3 základních parametrů:
- P1 (délka textu) - celkový počet znaků jedné interakce
- P2 (text mimo téma) - počet znaků, které se zabývají jiným tématem v jedné interakci
- P3 (tex prohlubující téma) - počet znaků, které prohlubují dané téma v jedné interakci

**Základní filtry:**
- F1 - označí se T-neurony, které jsou pro jiné téma
- F2 - označí se T-neurony, které téma neprohlubují
Účel sofistikovaného promptu v kapitole [02_Prompt_engineering] je aplikovat F1 a F2 na T-neurony zadaného textu podle tématu a metodiky. F1 probíhá v 2. vlně generace a F2 ve 3. vlně generace.

### Křivky interakcí
Celý kontext se dělí na interakce, tedy [prompt > generace tokenů], které se vynášení na jednotlivé řádky. Tímto se zobrazí časová posloupnost, která umožňuje diagnostikovat trendy.

Každý řádek, interakce, je osou rozdělenou na 200 bodů, které jsou rozloženy jako 100 - 0 - 100 kdy 100 - 0 je zastoupení poměrů znaků uživatele a 0 - 100 je zastoupení poměrů znaků LLM.

![[Pasted image 20260718135909.png]]




**4. Synapse engineering**

- **Funkce:** Diagnostická a pokročilá vrstva – emergence jako vedlejší produkt.
    
- **Obsah:** Zavedení diagnostických nástrojů:
    
    - **P1** – počet symbolů vnesených uživatelem a LLM.
        
    - **P2** – počet symbolů mimo téma.
        
    - **P3** – počet symbolů téma prohlubujících.
        
    - **P4** – techniky pro diagnostiku propojení T-neuronů (pouze zmínka, bez podrobného popisu, jako extrémní téma).
        
    - Z P1–P3 se odvozují **ideální křivky pro různé účely**, které slouží jako zpětná vazba pro LLM i pro inženýra.
        
- Propojování K-agentů, emergence jako neplánovaný, ale využitelný jev.

### Spektrum propojení inteligencí
Tento diagnostický nástroj popisuje poměr kognitivního příspěvku ve společném výstupu lidské a umělé inteligence. Umožňuje kvantifikovat míru kognitivního vlivu obou aktérů, predikovat pravděpodobnost halucinací, optimalizovat vstupy spolupráce a identifikovat charakteristiky lidského uživatele i jazykového modelu.
Spektrum je vymezeno dvěma limitními póly, kterých však ve spolupráci dvou inteligencí nelze nikdy plně dosáhnout.
- Pól [AB] - kognitivní výstup je zcela generován umělou inteligencí.
- Pól [IB] - kognitivní výstup je zcela tvořen lidskou inteligencí.
Spektrum pro model T-Ex je děleno na 100 dosažitelných bodů ležících na ose [AB]---[IB].
### Křivka interakcí
Spolupráce inteligencí v modelu T-Ex generuje textový výstup, který má podobu sekvenční výměny interakcí. Každou z těchto interakcí lze vyjádřit poměrem kognitivního příspěvku, tj. číslem v rozsahu 1–100 na spektru [AB]---[IB].
Spolupráce inteligencí generuje sekvenci dílčích příspěvků na spektru [AB]---[IB], které v souhrnu definují tvar křivky interakcí.
Právě tato křivka představuje základní diagnostický nástroj. Umožňuje identifikovat vzorce spolupráce, asymetrie v kognitivní zátěži a potenciální rizikové body interakce.
## Křivka účelu interakce
Paradigma současné doby staví kontext na 1. místo ve spolupráci člověka s LLM. Jde dokonce tak daleko, že tam, kde to je možné, odstraňuje uživatele z pozice spolutvůrce kontextu, aby agentic systémy dosahovaly lepších výsledku a uživatel s nimi interagoval jen na nejvyšší úrovni.

Model T-Ex zaměřuje pozornost od kontextu k jeho účelu, od spolupráce s LLM k propojení inteligencí a začleňuje agentic přístup do exokortexu.

Účel spolupráce mají oba aktéři jiný. Definuje kontext, specializaci modelu a ovlivňuje uživatele. Křivka účelu interakce popisuje vlastnosti a dynamiku propojených inteligencí.