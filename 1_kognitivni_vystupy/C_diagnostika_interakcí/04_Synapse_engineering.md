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
Diagnostika se dělá na úrovni křivek interakcí, které se skládají z jednotlivých bodů. Body křivek interakcí jsou určeny počtem znaků textu. Pro přípravu je text dělen podle tématu interakcí na 3 základní parametry:
- P1 (délka textu) - celkový počet znaků jedné interakce
- P2 (text mimo téma) - počet znaků, které se zabývají jiným tématem v jedné interakci
- P3 (tex prohlubující téma) - počet znaků, které prohlubují dané téma v jedné interakci

**Základní filtry:**
- F1 - označí se T-neurony, které jsou pro jiné téma
- F2 - označí se T-neurony, které téma neprohlubují
Účel sofistikovaného promptu v kapitole [02_Prompt_engineering] je aplikovat F1 a F2 na T-neurony zadaného textu podle tématu a metodiky. F1 probíhá v 2. vlně generace a F2 ve 3. vlně generace.

### Křivky interakcí
Celý kontext se dělí na interakce, tedy [prompt > generace tokenů], které se vynášení na jednotlivé řádky. Tímto se zobrazí časová posloupnost, která umožňuje diagnostikovat trendy.

Každý řádek, interakce, je osou rozdělenou na 200 bodů, které jsou rozloženy pro oba aktéry na 100 - 0 - 100 kdy 100 - 0 je zastoupení poměrů znaků uživatele a 0 - 100 je zastoupení poměrů znaků LLM.

Z celkového rozložení na interakce a aktéry se vybere parametr P1, který má nejvyšší počet znaků, a slouží jako reference pro parametry křivek interakcí. Ty jsou:
- KI_1 - znaky prohlubující téma (KI_1=P3) - na obrázku zobrazeno zeleně.
- KI_2 - znaky, které téma opakují (KI_2=P1-P2-P3) - na obrázku zobrazeno modře.
- KI_3_ znaky, které jsou k jinému tématu (KI_3=P2) - na obrázku zobrazeno červeně.

![[Pasted image 20260718135909.png]]

Pro obrázek výše byla reference 3772 znaků ve třetí interakci uživatele. KI_1 je referenční hodnotou. Všechny ostatní se vůči ni poměřují.

Všeobecně existuje minimálně jedna interakce konkrétního aktéra s nejvyšším množstvím znaků P1 rozloženým mezi KI_1, KI_2, a KI_3 a slouží jako reference pro všechny body křivek interakcí.

### Diagnostika křivek interakcí
Zatímco křivky interakcí se tvořily pro jedno téma, diagnostika křivek by měla brát v úvahu všechna témata pro daný účel. Záleží na tom, jak velkého detailu potřebuje diagnostika dosáhnout.

V případě křivek na obrázku byl popis a účel interakce následující:
- Interakce využívala sokratovské dotazování, kdy LLM se mělo ptát a uživatel odpovídat.
- Účel byl prohloubit téma a dostat z uživatele vše, co o tématu ví a jak jej může prohloubit. (téma bylo exokortex a stalo se základem pro kapitolu [04_Model_T_Ex])
- Sekundárním účelem bylo vytvořit kontext, který se plní jen uživatelovým myšlením a informacemi o tématu, které je uživatel schopen rozšířit a zapsat. (více o tomto účelu v sekvencích)

#### Vyhodnocení křivek
Na křivky s těmito základními parametry P1-P3 se dá dívat z mnoha úhlů. Předně jde o textové analýzy na úrovni T-neuronů k danému tématu a tedy o textové analýzy jak uživatel a LLM naplňují daný účel interakce.
1. Uživatel držel účel interakce po celou dobu, kdy u všech osmi interakcí prohlubuje téma a drží se jej. Z pohledu uživatele ještě nebyl důvod ukončovat interakci, prtože měl k tématu více co říct.
2. LLM držel účel po celou dobu interakcí. menší červené texty mimo téma jdou zdvořilostní fráze mimo otázky. Konec, kdy převládá opakování v jeho otázkách oproti prohlubování tématu ukazuje trend, kdy LLM ztrácí prohloubení a otázkami se jen opakuje. Tohle byl signál pro uživatele k ukončení tématu, která se dále neprohlubovalo.
3. Na straně LLM jde vidět vzor, které si vytvořilo. Součet zelené a modré má skoro v každé interakci stejnou hodnotu. Otázky, které kladl byly stejně dlouhé, kdy jde vidět, že jakmile LLM v kontextu bude mít vzor, následuje jej o podobných úkolů.
4. Je vidět negativní vliv dlouhého dotazování LLM, tedy poměr mezi znaky uživatele a LLM. Tohle jde přímo proti sekundárnímu účelu interakce, kdy kontext měl být zaplněn co možná největším objemem uživatelova myšlení oproti generaci LLM. Uživatel pokládal tyto interakce za velmi efektivní podle jeho zkušenosti, ale až tato diagnostika a konfrontace s účely interakcí ukázala potenciál jak změnit úvodní prompt, kdy po změně je LLM méně ukecané, nemluví už mimo téma a účel interakce je plněn daleko čistěji.

#### Ideální křivky podle účelu interakcí
Každý účel interakce bude mít zcela jinou ideální křivku a jinou diagnostiku.
- Sokratovské dotazování - musí dominovat zelená
- 7 why metoda - musí dominovat zelená a tazatel otázek Why musí být umlčen, ideálně pár znaků na interakci.
- Učitel > žák - pro přejímání znalostí učitel mluví více, než žák, téma se nesmí prohlubovat dominantně, zelená je daleko nižší, než modrá. Zelená znamená nové znalosti, modrá je opakování a fixace znalostí. Pokud necháte žáka interagovat s LLM, uvidíte, jestli se učil, nebo probíral s LLM něco jiného, dominovala by červená. Současně byste viděli jak moc student zkouší nové a jak moc fixuje poznatky. U diagnostiky více témat pro jeden účel už půjde vidět které téma rozvíjí, které prohlubuje a na jaké zatím nedošel.
- Objevování - účel pro který je vhodné mít dynamické změny a červená křivka v tuto chvíli není na škodu, když nejde o trend, ale postupně se vrací modré a zelené. Opět analýzy více témat pro tento účel ukáží propojení.
- Vibecoding - ukázal by kvalitu agenta, LLM, kdy červená by byla nastavená na chybové kódy, zelená za prohlubující a modrá za opakující. Tato diagnostika ukáže efektivitu užvatele.
- ...

### Aplikace diagnostiky
Aplikace je na dvou úrovních:
1. Synapse engineering
	- Optimalizace prompt engineerngu
	- Optimalizace kontext engineeringu
	- Řízení sekvencí
	- Řízení emergentních výstupů
2. Automatizace - zpětná vazba
	- Triggery pro ukončení agenta nekonečného loopu
	- Zpětná vazba agentů, aby drželi účel interakce řízením s ideální křivkou
	- Softwarové řízení agentic systémů
	- Softwarové řízení RAG ...

### Aplikace i mimo T-Ex model
Jde o textové analýzy, které se dají aplikovat různě
- Jaký objem textu je prohlubující, opakující, mimo téma?
	- Věda chce práce, kterým bude dominovat zelená?
	- Závěrečné studentské práce? Neměla by dominovat zelená v tématu studenta a modrá v teorii?
	- Učebnice. Jaký je poměr témat, zelené a modré?
	- Knihy. Jaký má kniha účel?
- Při rozšíření na audio je možné separovat pyramidální a extrapyramidální dráhu.
- Jaké další parametry mimo P1-P3 se dají hledat?

## Sekvence






- Propojování K-agentů, emergence jako neplánovaný, ale využitelný jev.
