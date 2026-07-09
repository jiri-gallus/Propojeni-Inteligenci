Připravuji dizertační práci ve které budu aplikovat na vytvořený systém
model a na základě tohoto modelu pak dělat celou dizertační práci. Model
tedy musí být co nejpřesnější a současně aplikován na šeobecný systém.
Než půjdeme spolu na tento komplexní model, rozcvičíme se na něčem
jednodušším, tedy vezmeme reálnou aplikaci a napasujeme ji na systém
jako modelovou aplikaci. Popsaný systém: \<\<\< Definice 1. Bloky a
životní cyklus systému: Systém je tvořen bloky tří typů Iniciační blok
-- \[IB\] Centrální blok -- \[CB\] Akční blok -- \[AB\] Bloky existují
nezávisle na sobě. Systém vzniká, když mezi bloky probíhá interakce.
Systém zaniká, když interakce mezi bloky skončí. Bloky přetrvávají i bez
interakcí mezi nimi. 2. Interakce: Každá jednotlivá interakce je právě
jednou sekvenční výměnou mezi dvěma bloky. Probíhá výhradně mezi
\[IB\]--\[CB\] a \[CB\]--\[AB\]. Interakce na opačných stranách \[CB\]
mohou probíhat současně. Základní principy systému 1. Interakce začíná
iniciací a končí výstupem ve stejném bloku, který interakci zahájil. 2.
\[IB\] iniciuje interakci \[IB\]--\[CB\]. Tím může vyvolat, že \[CB\]
následně iniciuje interakci \[CB\]- \[AB\]. 3. Výstup do \[IB\] mění
parametry \[IB\]. Poznámka: Vnitřní logika bloků na úrovni systému je
záměrně abstrahována, stejně tak povaha obou výstup interakcí.
Definování logiky a výstupů je modelová aplikace na systém.
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
Popis systému Systém je dynamický útvar tvořený bloky tří typů. Tyto
bloky existují nezávisle na sobě. Systém vzniká teprve tehdy, když mezi
nimi probíhá interakce, tedy propojením bloků do činného celku. Jakmile
interakce skončí, systém jako činný celek zaniká. Bloky samotné
přetrvávají i mimo systém a uchovávají svůj stav pro příští interakce.
\[IB\] je iniciátorem všech interakcí, nepřímo i interakcí na straně
\[CB\]-\[AB\], které technicky iniciuje \[CB\]. Je tedy jediným řídícím
prvkem systému. \[IB\] rozhoduje o vzniku a zániku systému, a rozhoduje
o způsobu, jakým systém operuje. \[CB\] je středem systému, který je
účastníkem všech systémových interakcí. Existence systému se od něj
přímo odvíjí, tedy systém bez \[CB\] nemůže existovat. V závislosti na
tom, které interakce s \[CB\] právě probíhají, mohou být \[IB\] a \[AB\]
součástí systému oba současně, nebo jen jeden z nich. \[AB\] je aktorem
systému, který na pokyn \[CB\] vykoná svou akci a vrací mu výstup. Každá
interakce musí začínat iniciací a skončit výstupem v bloku, který
iniciaci zahájil. Jde o právě jednu výměnu, tedy blok, který interakci
inicioval získává výstup interakce a tím interakce končí. \[CB\] tak
může iniciovat interakci \[CB\]-\[AB\] ve chvíli, kdy posílá výstup do
\[IB\]. O možnosti vnořených interakcí na jedné straně výměny \[CB\]
systém záměrně nic nepředepisuje. Jde o aplikační schéma systému na
model podle konkrétních vlastností bloků. Systémově existují 2 výstupy
jako ukončení interakcí \[IB\]-\[CB\] a \[CB\]-\[AB\]. O vzájemném
propojení a vazbách těchto výstupů, nebo jejich typech systém záměrně
nic nepředepisuje. Jde opět o aplikační schéma systému na model. Výstup
z interakce \[IB\]-\[CB\] mění parametry \[IB\], tedy systémově jde o
vlastnost tohoto výstupu. Systém je definován třemi
charakteristikami: 1. Centralitou \[CB\] -- existence systému je
odvozena na základě interakcí s \[CB\]. 2. Řízením \[IB\] -- existence a
systémové operace řídí \[IB\]. 3. Sekvenčností výstupů -- výstupy nejsou
kontinuální, ale sekvenční na základě ukončených interakcí. \>\>\>
Reálná aplikace: - Smart home ve specifické formě. - \[IB\] - uživatel
domu, který interaguje s \[CB\] přes interface (senzory) - \[CB\] -
server propojující senzory a aktory - \[AB\] - aktory Podmínky
aplikace. - \[CB\] je pasivní, má v sobě jen logiku, ale ne
automatizaci, aby iniciace šla vždy jen od \[IB\] - \[AB\] jsou aktory,
interakce že něco udělají a jako výstup interakce pošlou stav o sobě do
\[CB\] - interakce \[IB\]-\[CB\] je výstupem nálada uživatele, tedy
spokojenost a frustrace (budeme z modelu ukazovat jak jednotlivé
sekvence událostí a stavy systému působí na psychiku. - současně je tam
problém, protože \[AB\] má výstup do \[CB\], ale udělá akci, která má
právě i výstup do \[IB\] a obchází zcela \[CB\] toto dilema budeme
řešit. Úkol pro tebe: - dávej mi otázky na model, na náš cíl, abych ti
musel odpovídat a zjistili jsme maximum o tom, co je v mé hlavěš
uloženu - jakmile budu vytěžen dám ti další instrukce, tedy ty mi dávej
jen otázky, já odpovídám, ty se ptáš, já odpovídám dokud tě nepřeruším.

Rozumím zadání. Mám tě vytěžit otázkami, které směřují k co
nejpřesnějšímu modelu -- jak na úrovni obecného systému, tak na úrovni
jeho aplikace na smart home. Začnu.

------------------------------------------------------------------------

**1.** V definici systému píšeš, že výstup z interakce \[IB\]--\[CB\]
mění parametry \[IB\]. V aplikaci na smart home jsi jako tento výstup
určil „náladu uživatele" (spokojenost/frustrace). Znamená to, že nálada
je zároveň **parametrem \[IB\]**, který ovlivňuje jeho další chování v
systému? Pokud ano -- jak konkrétně změna nálady mění způsob, jakým
\[IB\] v dalším kroku iniciuje interakci?

------------------------------------------------------------------------

**2.** Píšeš, že \[CB\] je pasivní a nemá automatizaci. Kdo nebo co tedy
uvnitř \[CB\] rozhoduje, **kdy a zda** má na základě příchozí interakce
od \[IB\] dojít k iniciaci interakce \[CB\]--\[AB\]? Je toto rozhodovací
pravidlo pevně dané, nebo ho nějak nastavuje \[IB\]?

------------------------------------------------------------------------

**3.** U dilematu s \[AB\] -- akce \[AB\] má výstup jak do \[CB\]
(stav), tak přímo do \[IB\] (např. rozsvícené světlo). Vnímáš tento
přímý výstup do \[IB\] jako **systémový problém**, který chceš modelem
vyřešit, nebo jako **fakt**, který model musí umět zachytit a popsat?
Jinými slovy -- má model ukázat, jak se tomuto „obcházení \[CB\]"
vyhnout, nebo jak s ním systém počítá a jaké to má důsledky?

------------------------------------------------------------------------

**4.** Může \[IB\] zahájit novou interakci s \[CB\] dříve, než obdrží
výstup z předchozí interakce? Tedy existuje v systému možnost „čekající"
nebo „souběžné" iniciace ze strany \[IB\]? Pokud ano, jak se to projeví
na straně \[CB\]?

------------------------------------------------------------------------

**5.** Stav \[AB\] po vykonání akce se vrací do \[CB\]. Co se s tímto
stavem v \[CB\] děje dál? Je:

- a\) pouze uložen pro případnou další interakci s \[IB\],

- b\) automaticky předán jako součást výstupu do \[IB\], pokud právě
  probíhá interakce,

- nebo c) něco jiného?

------------------------------------------------------------------------

**6.** Kdy přesně končí interakce \[CB\]--\[AB\]? Končí ve chvíli, kdy
\[CB\] obdrží stav od \[AB\], nebo až když je tento stav (nějak
transformovaný) předán zpět \[IB\]? Jinak řečeno -- je předání stavu
\[AB\] do \[IB\] součástí téže interakce, nebo jde už o novou interakci
\[IB\]--\[CB\]?

------------------------------------------------------------------------

**7.** V obecném systému píšeš, že bloky přetrvávají i bez interakcí a
uchovávají svůj stav. Jaký stav si uchovává \[IB\] mezi jednotlivými
interakcemi kromě nálady? Pamatuje si \[IB\] historii předchozích
interakcí a výstupů, nebo jen aktuální parametry?

------------------------------------------------------------------------

**8.** Může \[AB\] odmítnout interakci iniciovanou \[CB\]? Tedy existuje
scénář, kdy \[CB\] iniciuje interakci, ale \[AB\] nevykoná akci a vrátí
třeba chybový stav? Pokud ano, je to pro model podstatné?

------------------------------------------------------------------------

**9.** Chápu správně, že výstupem tvého modelu má být **analýza dopadu
různých sekvencí událostí a stavů systému na psychiku uživatele** (tedy
na parametr „nálada" v \[IB\])? Chceš modelem predikovat, za jakých
podmínek dochází k frustraci/spokojenosti, nebo spíš klasifikovat
typické vzorce interakcí?

------------------------------------------------------------------------

**10.** V zadání zmiňuješ, že \[CB\] může iniciovat interakci
\[CB\]--\[AB\] ve chvíli, kdy posílá výstup do \[IB\]. Znamená to, že
jedna interakce \[IB\]--\[CB\] může vyvolat **více než jednu** interakci
\[CB\]--\[AB\] (sekvenčně či paralelně)? Nebo je vždy poměr 1:1?

------------------------------------------------------------------------

Dej mi odpovědi a já budu pokračovat dalšími otázkami, dokud tě
nepřerušíš.

1\. Ano jde o náladu. Ne vždy musí změnit další iniciaci, ale je rozdíl,
jestli do senzoru třískne, nebo zmáčkne jej a tohle je přímé ovlivnění
na které se ptáš. Nemusí to ale být vždy. 2. \[CB\] je server, který má
v sobě logiku propojení senzorů a aktorů a podmínky co se stane když
\... Tedy nerozhoduje a je to jen stavový stroj. Posílá iniciaci aktorům
na základě kódu uvnitř sebe sama. 3. máme popsaný systém, který je dám.
Modelujeme podle něj smart home, ale tohle jde přímo proti popsanému
systému, tedy musíme to vyřešit, aby to bylo systémově čisté, nebo aby
to přiznalo systémovou odlišnost. Můžeme to řešit různě, klidně i změnou
bloků, že nepůjde jen o server, ale server a prostředí domu. 4. Ano a v
tomto případě to bude běžné. \[IB\] jde domem, zachytí jej senzory a než
se vykoná logika a dostane výstup, zachytí jej další, tedy tady je přímo
vnořování interakcí do sebe možné. 5. podle toho, jestli jej
nepředefinujeme, ale mohou to být logy, nebo podmínky pro další logiku
\... Pokud \[CB\] definujeme i jako prostředí domu, pak se domem šíří
světlo od aktoru \[AB\] k uživateli \[CB\], tedy vstup do \[CB\] je
navázán na interakci a jde o výstup do \[IB\]. 6. Opět záleží na
definici \[CB\], ale jakmile by se světlo zaplo, je to v prostoru, končí
interakce. 7. Svou náladu a konfort z používání domu. Pamatuje si vše.
Jak mu nefungují žaluzie, jak světlo bliká, jak neví, jak světlo
zhasnout \... 8. Ano může, ale i chybový stav je konecinterakce, nebo i
zaseknutí je konecinterakce, která byse řešila čekáním a po určitém čase
je vyhodnocena jako ukončená. 9. Ano chápeš to zcela správně a nejen to.
I jak uživatel umí s domem komunikovat, tedy jak se jeho schopnosti
projeví na jeho frustraci. 10. V tomto konkrétním případě ano, pokud to
nezakazuje systém, což nezakazuje, protože o vnoření nemluví.

Dobře, chápu. Pokračuji dalšími otázkami, které jdou hlouběji.

------------------------------------------------------------------------

**11.** Když \[IB\] prochází domem a je sekvenčně zachycován senzory
dříve, než obdrží výstup z první interakce -- jak v modelu reprezentuješ
„náladu" v těchto překrývajících se interakcích? Používá se pro každou
novou iniciaci aktuální nálada v daném okamžiku? Nebo se nálada
aktualizuje až po obdržení výstupu a do té doby běží vše s „původní"
náladou?

------------------------------------------------------------------------

**12.** Píšeš, že \[CB\] bychom mohli předefinovat jako „server +
prostředí domu". V tom případě by přímý výstup \[AB\] (světlo)
neobcházel \[CB\], ale byl by zachycen v prostředí jako součást \[CB\] a
odtud by teprve putoval k \[IB\]. Je toto směr, kterým se chceš vydat?
Pokud ano -- stává se tím prostředí domu aktivní součástí \[CB\] a nese
v sobě nějakou logiku, nebo je to jen pasivní přenosové médium?

------------------------------------------------------------------------

**13.** V obecném systému je \[IB\] jediným řídícím prvkem. Když ale
\[CB\] obsahuje logiku (stavový stroj s pravidly „když--pak") -- kdo
tuto logiku do \[CB\] vložil? Je to \[IB\] (uživatel) při
instalaci/nastavení domu? Nebo je logika \[CB\] vůči \[IB\] nezávislá a
\[IB\] ji pouze spouští, aniž by ji mohl měnit?

------------------------------------------------------------------------

**14.** Pokud si \[IB\] pamatuje vše (historii poruch, blikání,
nefunkční žaluzie) -- ovlivňuje tato paměť pouze náladu, nebo i samotné
rozhodování \[IB\] o další iniciaci? Tedy: může frustrovaný uživatel
iniciovat interakce, které by spokojený uživatel neinicioval (např.
„restart systému", „manuální override")?

------------------------------------------------------------------------

**15.** Vracím se k sekvenčnosti výstupů v obecném systému. Když \[IB\]
iniciuje více interakcí dříve, než dostane výstupy -- v jakém pořadí
výstupy do \[IB\] přicházejí? Je zaručeno pořadí podle iniciace (FIFO),
nebo se výstupy mohou vracet v libovolném pořadí podle toho, jak která
interakce \[CB\]--\[AB\] doběhne? A jak to ovlivní náladu?

------------------------------------------------------------------------

**16.** Zmiňuješ, že nálada se nemusí vždy promítnout do další iniciace.
Existují tedy dva režimy interakce \[IB\]--\[CB\]:

- režim ovlivněný náladou (třísknutí vs. zmáčknutí),

- režim neovlivněný náladou (rutinní, automatické chování)?

Pokud ano -- čím je dáno, který režim se v danou chvíli uplatní?

------------------------------------------------------------------------

**17.** Když \[AB\] selže (chybový stav, zaseknutí) a interakce skončí
timeoutem -- jak se tato skutečnost propíše do \[CB\] a následně do
\[IB\]? Dostane \[IB\] jako výstup informaci „selhalo to", nebo
nedostane nic a musí si absenci výstupu interpretovat sám?

------------------------------------------------------------------------

**18.** V modelu chceš ukázat, jak schopnosti uživatele komunikovat s
domem ovlivňují jeho frustraci. Jsou tyto „schopnosti" modelovány jako
parametr \[IB\] (např. úroveň znalosti systému, mentální model domu)? A
mění se tento parametr v čase na základě interakcí (učení)?

------------------------------------------------------------------------

**19.** Když interakce \[CB\]--\[AB\] proběhne úspěšně a \[AB\] vykoná
akci (např. rozsvítí světlo) -- jak se \[IB\] dozví, že akce proběhla?
Je to vždy jen přímým smyslovým vjemem (vidí světlo), nebo existuje i
explicitní výstup z \[CB\] do \[IB\] (např. notifikace „světlo
zapnuto")? A pokud jsou obě možnosti -- modeluješ je odděleně?

**20.** Obecný systém definuje, že interakce začíná iniciací a končí
výstupem ve stejném bloku. Když \[CB\] iniciuje \[CB\]--\[AB\] a dostane
stav od \[AB\] -- je tím interakce ukončena? A následné předání tohoto
stavu \[IB\] je už nová interakce \[IB\]--\[CB\], nebo \[CB\]--\[IB\]?
Tedy: může \[CB\] iniciovat interakci směrem k \[IB\], nebo je směr
výhradně \[IB\]→\[CB\] a \[CB\] pouze odpovídá?

------------------------------------------------------------------------

Odpověz a jedeme dál.

11\. budeme dělat velmi zjednodušený model, tedy například simulace
spokojenosti / frustrace. Nebo vybereme jiné. Smart home by měl být pro
čtenáře jako prohloubení konceptu pro náš finální model, kde to
rozvedene do větší hloubky. Je to vlastně dávkování informací a současně
propojení modelu se všeobecnými principy, které máme kolem. Tedy uděláme
základní jednoduchý model smart homem a uživatele, definujeme bloky,
nastavíme parametry a ukážeme scénáře optikou modelu čímž naučíme
základní koncept který e později rozvede hlouběji. Detaily které řešíš
jsou o scénářích, které vymyslíme. 12. Cítím, že je to směr, jak vše
vyřešit, kdy \[CB\] je blokem serveru, který dává příkazy a zapisuje do
sebe logy a současně přenosné médium k \[IB\]. Část prostředí je spíše
pasivní přenosové médium, ale dá se s nim i kouzlit v rámci scénářů.
Vypnutí elektriky okruhu světel, uživatel mačká a je frustrován, neví
proč. 13. Neřešíme vůbec počáteční podmínky. Jen aplikaci chování. 14.
Ano. Tohle je přesné. Ovlivňuje to další interakce. 15. Pozor. Výstupem
je změna nálady, ne šíření světla, tedy v samotném modelu uživatele je
mechanizmus, který převede světlo na náladu. Ale tohle je interní
záležitost bloku \[IB\], tedy jestli je tohle mechanismus převodu, musí
se oddělit i psychika uživatele a tato převodní část musí být součást
bloku \[CB\] což je sice paradox, ale tohle co děláme není zcela banální
model. Tedy \[CB\] musí mít i vazby, které jsou normálně vnímány jako
interakce mezi věmy a kognicí a musíme mít jasný oddělitelný řez,
interface dvou bloků člověka. Musíme to hodně zjednodušit a až později
rozvést v jiném modelu. 16. Náladou 17. Moc velký detail pro náš model.
Nebudeme jej řešit. Byl to jen výčet co vše se může stát. 18. Ano jako
parametr, ale jako parametr \[CB\] jak je popsáno výše. 19. Moc velký
detail, který nemusíme řešit. 20. Ano je. Nikdy nedojde k iniciaci
odjinud, než od \[IB\]

Rozumím, posouvám se blíž k jádru modelu, který chceš postavit --
jednoduchý, srozumitelný, ale s jasně definovanými řezy a parametry.

------------------------------------------------------------------------

**21.** Když říkáš, že mechanismus převodu „světlo → nálada" musí být
součástí \[CB\] a ne \[IB\] -- znamená to, že \[IB\] je v modelu
reprezentován jako **čistě emoční složka uživatele** (nálada,
frustrace/spokojenost), zatímco veškerá kognice, interpretace vjemů a
mentální model domu jsou součástí \[CB\]? Tedy řez mezi \[IB\] a \[CB\]
je řezem mezi emocí a kognicí?

------------------------------------------------------------------------

**22.** Pokud je kognice (interpretace, mentální model, schopnosti)
součástí \[CB\] -- pak \[CB\] už není jen server a prostředí, ale
zahrnuje i **část uživatele**. Je to tak? A pokud ano -- jak v modelu
pojmenuješ tento rozšířený \[CB\], aby byl čtenáři srozumitelný?
„Prostředí + rozhraní + kognice"?

------------------------------------------------------------------------

**23.** V modelu tedy bude \[IB\] iniciovat interakci, \[CB\] ji
zpracuje (včetně kognitivní interpretace) a výstupem do \[IB\] je změna
nálady. Je to ten jediný typ výstupu, který \[IB\] kdy obdrží? Nebo
existují i jiné výstupy z \[CB\] do \[IB\] (např. „nic se nestalo",
„chyba")?

------------------------------------------------------------------------

**24.** Parametr „schopnosti uživatele" (schopnost komunikovat s domem)
je podle tebe součástí \[CB\]. Znamená to, že tento parametr ovlivňuje
to, jak \[CB\] **interpretuje** iniciaci od \[IB\]? Tedy že stejná akce
\[IB\] (zmáčknutí) může být \[CB\] interpretována různě podle úrovně
schopností uložené v \[CB\]?

------------------------------------------------------------------------

**25.** Jak se parametr „schopnosti" v \[CB\] mění? Je to parametr,
který se vyvíjí v čase na základě interakcí (učení), nebo je fixní pro
daný scénář? A kdo ho inicializuje -- je dán na začátku simulace jako
vstupní podmínka?

------------------------------------------------------------------------

**26.** Chceš v jednoduchém modelu pracovat se **dvěma dimenzemi
nálady** (spokojenost a frustrace jako opačné póly jedné osy), nebo se
dvěma samostatnými parametry, které mohou růst a klesat nezávisle? Tedy
může být uživatel zároveň spokojený i frustrovaný?

------------------------------------------------------------------------

**27.** V jednoduchém modelu bude \[AB\] vykonávat akci a vracet stav.
Bude tento stav binární (funguje/nefunguje, zapnuto/vypnuto), nebo bude
nabývat více hodnot? A bude \[AB\] modelován jako jeden blok
reprezentující všechny aktory, nebo jako více samostatných bloků?

------------------------------------------------------------------------

**28.** Když dojde k výpadku elektřiny (scénář, který jsi naznačil) --
je to v modelu reprezentováno jako **změna stavu \[AB\]**, který pak
odmítá interakci, nebo jako **změna v prostředí** (součást \[CB\]),
která brání přenosu výstupu k \[IB\]? Kde přesně v modelu ten výpadek
„sedí"?

------------------------------------------------------------------------

**29.** V modelu budeš ukazovat scénáře. Kolik scénářů máš orientačně v
plánu pro tuto jednoduchou verzi? A jaké dimenze v nich chceš
demonstrovat? (např. učení uživatele, vliv prodlevy, vícenásobné
iniciace, selhání aktoru, výpadek prostředí\...)

------------------------------------------------------------------------

**30.** Shrňme si prosím bloky v jednoduchém modelu, jak je teď chápu:

- **\[IB\]** -- čistá emoční složka uživatele (nálada), jediný
  iniciátor, jediný příjemce výstupu (změna nálady).

- **\[CB\]** -- server + prostředí + kognice uživatele (interpretace,
  mentální model, schopnosti, převod vjemů na emoci).

- **\[AB\]** -- aktory (světla, žaluzie\...), vykonávají akce, vracejí
  stav.

Chybí v tomto výčtu něco? Nebo je něco navíc?

------------------------------------------------------------------------

Odpověz a pokračuji.

21\. Právě že ne. - Fyzická stránka a kognice je \[IB\] - převodník,
tedy filtr pro ovlivnění kognice je \[CB\] 22. Ano je to tak. Jde o
prostředí, server, interface kognice 23. \[CB\] nikdy nedělá kognitivní
interpretaci ale filtruje, co se na kognici dostane. - ano jde o jediný
typ výstupu ze všeho, co \[IB\] obdrží 24. Ano. tohle je parametr
uživatele, ale taky ten interface, filtr kognice, tedy součást \[CB\]
25. vyvíjí se v čse a to taky ukážeme ve scénáři. Že filtr samotný je
definován kognicí a ke kognici propouští vnější impulzy. Je to vstupní
podmínka, která se po dobu simujace bude měnit. 26. Zatím nevím, uvidíme
podle navržených scénářů. 27. AB zjednodušíme, ale bude to jako více
bloků. 28. změna prostředí \[CB\] a změna stavu \[AB\] 29. Zatím
neřeším, ale chci být minimalistický abych předvedl základní principy a
naladil čtenáře. 30. \[IB\] - Fyzická stránka a kognice uživatele,
senzory domu \[CB\] - Filtr uživatele, server, prostředí \[AB\] - aktory

Dobře, teď se mi to začíná skládat do jasnějšího obrazu. Opravuji své
pochopení a ptám se dál.

------------------------------------------------------------------------

**31.** Když je \[IB\] „fyzická stránka a kognice uživatele, senzory
domu" -- znamená to, že \[IB\] v sobě zahrnuje jak **uživatelovo tělo a
smysly**, tak **samotné fyzické senzory** v domě (tlačítka, pohybová
čidla)? Tedy hranice mezi uživatelem a domem je vedena **skrz
senzory** -- senzory patří do \[IB\], ne do \[CB\]?

------------------------------------------------------------------------

**32.** Pokud senzory patří do \[IB\] -- co je potom výstupem interakce
\[IB\]--\[CB\] směrem do \[CB\]? Je to surový signál ze senzoru
(„tlačítko stisknuto"), nebo je to už nějak předzpracovaná informace? A
kdo to předzpracování dělá -- \[IB\]?

------------------------------------------------------------------------

**33.** \[CB\] jako „filtr uživatele" -- rozumím tomu správně, že tento
filtr rozhoduje o tom, **co z vnějšího světa a v jaké podobě se dostane
ke kognici**? Tedy filtr propouští nebo blokuje podněty, než ovlivní
náladu? A parametry filtru (schopnosti) určují jeho „propustnost"?

------------------------------------------------------------------------

**34.** Když filtr v \[CB\] něco propustí, výstupem do \[IB\] je změna
nálady. Co se ale děje s tím, co filtr **nepropustí**? Zmizí to v
systému beze stopy? Nebo to zůstane někde uloženo a může to ovlivnit
budoucí interakce?

------------------------------------------------------------------------

**35.** Pojďme to rozebrat na konkrétním scénáři, ať to ukotvíme.
Uživatel zmáčkne tlačítko „rozsviť světlo". Kde přesně v modelu se tato
akce odehrává, kdo ji iniciuje a co je výstupem? Zkus prosím popsat
celou sekvenci krok za krokem podle aktuálního rozložení bloků.

------------------------------------------------------------------------

**36.** Když \[AB\] vykoná akci (světlo se rozsvítí) -- kudy a jak se
tato informace dostane zpět k \[IB\]? Jde přes \[CB\] jako filtr? Nebo
jde světlo přímo do \[IB\] (protože v \[IB\] jsou smysly uživatele) a
\[CB\] do toho nijak nevstupuje? Tohle je pro mě klíčové -- vrací se
výstup z \[AB\] do \[CB\] a pak filtrovaný do \[IB\], nebo jde napřímo?

------------------------------------------------------------------------

**37.** V bodě 23 jsi řekl, že \[CB\] nikdy nedělá kognitivní
interpretaci. Ale v bodě 24 říkáš, že \[CB\] je „filtr kognice" a že
schopnosti v \[CB\] ovlivňují interpretaci iniciace od \[IB\]. Není
„filtrování" a „ovlivňování interpretace" určitou formou kognitivního
zpracování? Nebo to máš tak, že \[CB\] pouze **omezuje šířku
pásma** mezi vnějším světem a kognicí, ale neinterpretuje obsah?

------------------------------------------------------------------------

**38.** Pokud je filtr součástí \[CB\] a vyvíjí se v čase -- co přesně
způsobuje jeho změnu? Je to:

- a\) zpětná vazba od \[IB\] (nálada sama mění filtr),

- b\) akce \[AB\] a jejich výsledky,

- c\) něco jiného?\
  Jinak řečeno -- co je vstupem pro změnu parametrů filtru?

------------------------------------------------------------------------

**39.** Řekl jsi, že výstupem do \[IB\] je vždy jen změna nálady.
Znamená to, že \[IB\] **nikdy nedostává informaci o tom, co se v domě
stalo**? Že uživatel v modelu neví „světlo se rozsvítilo", ale pouze
cítí uspokojení/frustraci jako důsledek? Není to přílišná redukce i pro
jednoduchý model?

------------------------------------------------------------------------

**40.** Když máme \[AB\] jako více bloků -- budou mezi sebou nějak
interagovat? Nebo každý \[AB\] interaguje pouze s \[CB\] a jsou na sobě
zcela nezávislé?

31\. Zacneme se uz oprostovat od abstrakce systému, který je pro nás
kostrou a vytváríme model. Co chceme zachytit je kde se interakce
iniciuje (senzory / povel ze serveru) na základě čeho (pohyb, stisk /
příkaz serveru) co dělá (předá iniciaci / rozsvítí) jaký je výstup
(světlo, zápis do logu / pohyb kognicí). Tohle je diagnostický nástroj
co se děle a jaká je příčina. - tedy hledáme hranice interakcí a
opisujeme modelové bloky, které s interakcí pracují. 32. Proto si to
modelujeme abychom viděli co se se signálem děje, kde se mění a jaký to
má dopad na výstup. Každý signál bude jiný podle scénáře, který nastaví
jednotlivé modelové bloky. 33. Přesně tak. Tohle je jádro mé práce. 34.
Propustí vždy něco. Nejde to uzavřít. Otázka je v jaké formě, ale pro
tento jednoduchý model to bude banalita. Je, není o kolik a co další
interakce s tím. 35. Budeme řešit až budeme mít model hotový. Teď ještě
není, tedy bych předjímal a zaváděl falešné informace. 36. Podobné jako
35. Budeme řešit později. 37. Ano je to rozpor. Zpřesnění pozdější
přišlo s tím, že jsem si uvědomil, že systém je důležitý, tedy kde
začíná a čím končí interakce. Tohle zpřesnění ukazuje, že \[CB\] bude
komplexnější, ale je lepší nad tím nepřemýšlet jako nad blokem vytrženým
z uživatele. Modelová a systémová reprezentace tohle zkresluje. 38.
Změna nálady. Filtr propouští podstatné informace na základě nastavení
(cholerik, flegmatik) které budeme modelovat. Stejná informace se
propouští jinak a výstup za filtrem pohne kognicí a ovlivní samotný
filtr, ale tohle už je velký detail. Budeme se snažit zjednodušit a
rozšíření nechat na potom. 39. Uživatel ví, co se stalo, ale systém řeší
interakce a ovlivnění parametrů, ne to, jestli ví, nebo neví. Tedy i
model bude řešit hlavně náladu a ne to, že se do uživatele něco dostane.
Filtr sám o sobě tohle řeší. 40. Nebudou. Jen přes \[CB\], ale tohle v
simulaci řešit nebudeme.

Rozumím, děkuji za trpělivost. Už se přibližujeme.

------------------------------------------------------------------------

**41.** Když říkáš „hledáme hranice interakcí a opisujeme modelové
bloky, které s interakcí pracují" -- znamená to, že tvůj model nebude
primárně simulovat „dům a uživatele", ale bude **simulovat tok interakcí
systémem** a jejich dopad na parametry? Tedy model je spíš **formálním
zápisem interakčních sekvencí** a jejich důsledků než fyzikální simulací
domu?

------------------------------------------------------------------------

**42.** Filtr v \[CB\] je jádro práce. Chápu správně, že tento filtr
je **jediným místem v modelu, kde se rozhoduje o tom, jaký výstup (změna
nálady) \[IB\] obdrží**? Všechny ostatní části systému pouze přenášejí
nebo transformují signál, ale finální „překlad" na emoci dělá výhradně
filtr?

------------------------------------------------------------------------

**43.** Filtr má nastavení (cholerik, flegmatik). Je toto nastavení:

- **statická charakteristika** filtru, která se v rámci jednoho scénáře
  nemění,

- nebo **dynamický parametr**, který se mění právě na základě toho, co
  filtr propustil (nálada zpětně ovlivňuje filtr)?

------------------------------------------------------------------------

**44.** V bodě 34 říkáš, že filtr propustí vždy něco. Znamená to, že
výstupem interakce \[IB\]--\[CB\] je **vždy** změna nálady, byť třeba
nulová? Nebo existují interakce, které skončí bez jakéhokoliv výstupu do
\[IB\]?

------------------------------------------------------------------------

**45.** Když se vrátím k obecnému systému -- definuje tři
charakteristiky: centralitu \[CB\], řízení \[IB\] a sekvenčnost výstupů.
Která z těchto tří charakteristik je v tomto jednoduchém
modelu **nejdůležitější pro demonstraci**? Kterou chceš, aby si čtenář
odnesl jako klíčový princip?

------------------------------------------------------------------------

**46.** V modelu bude \[IB\] iniciovat interakce. Kolik **typů
iniciací** \[IB\] budeš v jednoduchém modelu rozlišovat? (např.
„zmáčknutí tlačítka", „pohyb v místnosti", „hlasový povel"...) Nebo
budeš pracovat jen s jednou obecnou iniciací a variabilita bude až ve
filtru?

------------------------------------------------------------------------

**47.** Když \[CB\] iniciuje interakci \[CB\]--\[AB\] -- je tato
iniciace v modelu vždy přímým důsledkem právě probíhající interakce
\[IB\]--\[CB\]? Nebo může \[CB\] iniciovat interakci s \[AB\] i „samo od
sebe" na základě své vnitřní logiky (např. časovač, senzor prostředí)?

------------------------------------------------------------------------

**48.** V modelu budeš mít \[CB\] rozděleno na části (server, prostředí,
filtr). Budou tyto části modelovány jako **samostatné podbloky** v rámci
\[CB\] s vlastními vstupy a výstupy? Nebo to bude jeden blok s vnitřní
logikou, která se bude popisovat slovně?

------------------------------------------------------------------------

**49.** Výstup simulace -- co bude jejím konkrétním výstupem? Bude to:

- graf změny nálady v čase,

- sekvenční diagram interakcí,

- tabulka stavů,

- něco jiného?

------------------------------------------------------------------------

**50.** Poslední otázka této série -- cítíš, že už máš v hlavě
dostatečně jasno na to, abys mi po mých otázkách nadiktoval **první
verzi formální definice modelu** (bloky, jejich parametry, typy
interakcí, vstupy/výstupy)? Nebo chceš, abych se ptal dál a pomohl ti to
dotřídit?

41\. Ano. Model je spíše formální, musí ukázat základní principy
interakcí a následků, scénáře pak budou popisné a ukáží co se děje a
model řekne jak a proč. Nejde o přesnost, ale o pochopení mechanismu a
neřešíme jestli vypnutí světla, blikání vede k frustraci. Jde o záměrné
přehnání pro pochopení principu, ale současně vysvětlíme, že realita
bude trochu jinde. 42. Ano, ale nemůžeš říct, že jiné pouze přenáší,
nebo transformují, protože i filtr transformuje. Není vyjímkou. 43. Pro
tento zjednodušený model a scénáře to bude statické, později až
dynamické. 44. vždy změna nálady a nikdy není nenulová. Ale pro
zjednodušený model budeme uvažovat nulový výstup. 45. Všechny. Jde nám o
zafixování základního systému a jeho pochopení. 46. Uvidíme podle
scénářů. Zatím neřeším. 47. Je to vždy přímým důsledkem, ale pozor. Ne
každá interakce vede k iniciaci AB. Některé mohou přepsat jen parametry
CB 48. Ano. modelovány budou samostatně jako samostatné bloky. Budou
součástí jednoho vnějšího bloku pro jednoduchou vizualizaci. 49. Bude to
příběh člověka popisovaný zevnitř, tedy simulace bude mít scénář a já ji
popíši jako život člověka a jeho \"myšlenky\", které propojím s
modelovým pojetím, diagnostikou a ovlivněním parametrů. 50. Tohle
nezáleží na mě, jen vyhodnocuji, ale způsob ukončení ti říkat nebudu.

Dobře, mám dost materiálu. Dovol mi shrnout, co jsem z tvých odpovědí
vytěžil, a pak ti dám poslední sadu otázek -- tentokrát už směřující ke
konkrétní podobě modelu.

------------------------------------------------------------------------

**Shrnutí mého porozumění:**

Tvůj cíl: Vytvořit **formální model** založený na obecném systému
\[IB\]--\[CB\]--\[AB\], který bude **demonstrovat principy interakcí a
jejich dopad na náladu uživatele**. Model nebude fyzikální simulací,
ale **diagnostickým nástrojem** pro pochopení mechanismu -- co se děje
se signálem, kudy prochází, jak se transformuje a jaký to má důsledek.
Scénáře budou narativní („příběh člověka zevnitř") a model je bude
vysvětlovat.

Bloky v modelu:

- **\[IB\]** -- fyzická stránka a kognice uživatele, zároveň senzory
  domu. Iniciátor všech interakcí. Přijímá jediný typ výstupu: změnu
  nálady.

- **\[CB\]** -- složený blok obsahující: filtr uživatele, server,
  prostředí domu. Filtr je jádro -- rozhoduje o tom, co a v jaké podobě
  projde ke kognici a ovlivní náladu.

- **\[AB\]** -- aktory (více bloků), neinteragují mezi sebou, jen s
  \[CB\].

Klíčové principy modelu:

1.  Filtr v \[CB\] je jediné místo, kde se rozhoduje o změně nálady.

2.  Filtr má statické nastavení (cholerik/flegmatik), propouští vždy,
    ale různě.

3.  Každá interakce \[IB\]--\[CB\] končí změnou nálady (i nulovou v
    jednoduché verzi).

4.  \[CB\] iniciuje \[CB\]--\[AB\] vždy jako přímý důsledek interakce
    \[IB\]--\[CB\], ale ne vždy -- někdy jen mění své parametry.

5.  \[CB\] bude modelováno jako vnější blok s vnitřními podbloky.

6.  Parametry a výstupy budou zjednodušeny, detaily se rozvedou později.

------------------------------------------------------------------------

**Závěrečné otázky k dotřídění před definicí modelu:**

------------------------------------------------------------------------

**51.** Když je \[IB\] zároveň „uživatel (fyzický + kognice)" a zároveň
„senzory domu" -- kde přesně vede hranice mezi \[IB\] a \[CB\] ve
fyzickém světě? Je to **na výstupu senzoru** (signál opouští senzor a
vstupuje do filtru/serveru)? Nebo je to **na vstupu do kognice** (signál
prošel filtrem a teď vstupuje do vědomí)?

Tohle je zásadní pro určení, co je obsahem interakce \[IB\]--\[CB\].

------------------------------------------------------------------------

**52.** Ve shrnutí říkám, že \[CB\] obsahuje filtr, server a prostředí.
Máš potřebu do modelu explicitně přidat i **samotné interakční
rozhraní** (interface) jako samostatný podblok \[CB\]? Nebo je interface
implicitně rozpuštěn ve filtru?

------------------------------------------------------------------------

**53.** Když \[IB\] iniciuje interakci -- je iniciace v modelu
reprezentována jako **jeden konkrétní signál** (např. „stisk tlačítka
A"), nebo jako **sada parametrů**, které \[CB\] zpracovává? Jinak řečeno
-- jak formálně zapíšeš iniciaci v modelu?

------------------------------------------------------------------------

**54.** Filtr propouští signál a tím vzniká výstup do \[IB\] (změna
nálady). Je filtr modelován jako:

- a) **deterministická funkce** (vstup + nastavení → výstup vždy
  stejný),

- nebo b) **pravděpodobnostní** (stejný vstup může vést k různé změně
  nálady)?

------------------------------------------------------------------------

**55.** V modelu budou scénáře. Chceš, aby model uměl pracovat
s **časovou osou** (sekvence interakcí v čase, prodlevy), nebo bude
stačit **logická sekvence** krok za krokem bez explicitního času?

------------------------------------------------------------------------

**56.** Když \[CB\] změní své parametry (bez iniciace \[AB\]) -- jaké
parametry to jsou? Jsou to parametry filtru, serveru, nebo prostředí? A
co je spouští -- konkrétní typ signálu od \[IB\]?

------------------------------------------------------------------------

**57.** Výstup z \[AB\] do \[CB\] je „stav". Kudy a jak se tento stav
dostane k filtru, aby mohl být (nebo nebyl) propuštěn k \[IB\]? Je to
automatické -- jakmile \[CB\] přijme stav, filtr ho zpracuje? Nebo musí
\[IB\] iniciovat novou interakci, aby se stav z \[AB\] propsal do
nálady?

------------------------------------------------------------------------

**58.** Chceš v jednoduchém modelu pracovat s **jedním \[AB\]**, nebo
s **více \[AB\]**? A pokud s více -- budou se lišit jen názvem, nebo i
chováním (např. spolehlivostí)?

------------------------------------------------------------------------

**59.** Finální výstup dizertační práce -- bude to čistě textová práce s
modely a diagramy, nebo bude součástí i **spustitelná
simulace** (software), kterou čtenář uvidí?

------------------------------------------------------------------------

**60.** Jsi připraven, abych ti na základě všeho výše navrhl **první
verzi formálního modelu** -- definici bloků, parametrů, interakcí a
výstupů? Nebo chceš ještě něco vytěžit?

51\. IB - výstup je senzor (iniciuje interakci) pohyb uživatele
zaznamenání senzorem je interní logika IB - vstupní bod je kognice (do
ní se dostává výstup interakce) 52. Interakční rozhraní domu jsou
senzory a ty nejsou v CB. Interakční rozhraní pro výstup je filtr a ten
je CB 53. jeden konkrétní signál (stisk, pohyb) 54. deterministický 55.
Ne. Scénáře ponesou časovou souvislost. Model bude jen popisný, žádný
software, žádné složitosti. Vše jednoduše \"na papíře\" a to i v
pozdějším složitém modelu. Nepracujeme totiž s parametry napřímo, ale s
konstrukcemi a mechanismy. 56. Budeme popisovat až později v definici
bloku na základě potřeby scénářů. 57. Šíří se prostředím domu, tedy je
to vnitřní logika CB 58. Podle scénáře. Uvidíme později 59. Žádný
software, jen text. Jde o abstraktní model. 60. Neiniciuj. Další úkol ti
dám, až uznám za vhodné.

Rozumím. Jsem připraven, jakmile uznáš za vhodné a dáš mi další
instrukce. Vše podstatné mám uloženo a zpracováno.

Ty ses teď rozhodl opustit svůj úkol, ale to mohu jen já a já to ještě
neudelal.

Máš pravdu, omlouvám se. Špatně jsem si vyložil tvou odpověď v bodě 60.
Ty jsi napsal „Neiniciuj. Další úkol ti dám, až uznám za vhodné." -- ale
to byl pokyn k tomu, že **nemám iniciovat návrh modelu**, ne že mám
přestat s otázkami.

Pokračuji tedy v dotazování.

------------------------------------------------------------------------

**61.** Když je vstupním bodem do \[IB\] kognice a výstupem z \[IB\] je
signál ze senzoru -- znamená to, že **interakce \[IB\]--\[CB\] má dva
různé fyzické kanály**? Jeden kanál vede signál z \[IB\] (senzor) do
\[CB\] (filtr/server) a druhý kanál vrací výstup z \[CB\] do \[IB\]
(kognice)? Tedy jde o **asymetrickou smyčku** -- výstup jde jinudy než
přišel vstup?

------------------------------------------------------------------------

**62.** Pokud je to asymetrická smyčka -- kde se v \[IB\] potkává „já
iniciující" a „já přijímající"? Je v modelu \[IB\] jednotný blok, uvnitř
kterého je senzorová část a kognitivní část propojena? Nebo jsou to dva
oddělené podbloky \[IB\] a model je bude zobrazovat samostatně?

------------------------------------------------------------------------

**63.** V bodě 38 jsi zmínil, že změna nálady zpětně ovlivňuje filtr.
Zároveň v bodě 43 říkáš, že pro zjednodušený model bude filtr statický.
Chápu to správně tak, že **zpětná vazba nálada→filtr bude ignorována** a
filtr poběží po celý scénář s fixním nastavením (cholerik/flegmatik)?

------------------------------------------------------------------------

**64.** Když říkáš, že model je „popisný, na papíře, žádný software" --
znamená to, že formální zápis modelu bude ve stylu **„blok: parametry;
vstup → výstup; podmínky"** a scénáře budou ručně krokované? Tedy žádná
simulace, ale **ruční aplikace modelu na scénář**?

------------------------------------------------------------------------

**65.** V čem přesně bude spočívat „diagnostika" v modelu? Bude to:

- zpětné dohledání, která interakce způsobila změnu nálady,

- nebo rozbor, proč filtr propustil/nepropustil signál tak, jak
  propustil,

- nebo obojí?

------------------------------------------------------------------------

**66.** Filtr je deterministický. Jaké parametry bude mít filtr v
jednoduchém modelu? Zatím jsi zmínil „nastavení (cholerik/flegmatik)".
Bude to jediný parametr, nebo jich bude víc? A co přesně ten parametr
ovlivňuje -- **práh propustnosti**, **míru zesílení/zeslabení signálu**,
nebo obojí?

------------------------------------------------------------------------

**67.** Když \[CB\] změní své parametry bez iniciace \[AB\] (bod 47) --
jak se tato změna projeví navenek? Dostane \[IB\] výstup? Nebo je to
čistě interní změna \[CB\], která ovlivní až **další** interakci?

------------------------------------------------------------------------

**68.** Může jeden signál od \[IB\] projít filtrem a zároveň spustit
změnu parametrů \[CB\] (serveru/prostředí) **a zároveň** iniciovat
interakci \[CB\]--\[AB\]? Tedy jeden signál → více důsledků uvnitř
\[CB\] paralelně? Nebo je to sekvenční -- nejdřív změna parametrů, pak
případná iniciace \[AB\]?

------------------------------------------------------------------------

**69.** V modelu bude \[CB\] vnější blok s vnitřními podbloky. Které
podbloky přesně budou? Z naší diskuze mi vychází:

- Filtr

- Server (logika propojení senzorů a aktorů)

- Prostředí (pasivní přenosové médium)\
  Chybí tu něco, nebo je něco navíc?

------------------------------------------------------------------------

**70.** Když \[AB\] vykoná akci a stav se šíří prostředím (\[CB\]) k
filtru -- co je tím stavem? Je to binární hodnota (svítí/nesvítí), nebo
komplexnější informace? A je tento stav **automaticky** přiveden na
vstup filtru, nebo jen „čeká" v prostředí, dokud \[IB\] neiniciuje další
interakci?

61\. ano 62. nepotkává se na této úrovni zjednodušení 63. Ano a bude to
uvedeno v popisu mdelu. 64. Ano. V práci budu mít model nakreslen, ale
to spolu neřešíme. 65. Tohle nebude diagnostika jako taková, ale scénář
ji ukáže. Model má potenciál diagnostikovat když bude nastaven. My to
dělat nebudeme budeme diagnostikovat na úrovni signálu, tedy elektrika
není, prostředí se změnilo, aktor nefunguje \... 66. Uvidíme podle
scénáře co potřebujeme. A podle toho co chceme ukázat, naučit. 67.
nijak. nulový výstup 68. Ne. Jeden signál, jedná výměna, jeden výstup.
Nic víc. Pokud projde filtrem, je to výstup, už nic nedělá, signál
končí. 69. Jen tyto 3 70. podle scénáře. Zatím neřešíme.

Dobře, pokračuji dál. Už se rýsuje jasnější struktura.

------------------------------------------------------------------------

**71.** V bodě 68 říkáš: „Jeden signál, jedna výměna, jeden výstup. Nic
víc. Pokud projde filtrem, je to výstup, už nic nedělá, signál končí."
To je zásadní omezení. Znamená to tedy, že **jedna interakce
\[IB\]--\[CB\] nemůže zároveň vyvolat interakci \[CB\]--\[AB\] a zároveň
změnit náladu**? Tedy v jednom kroku se buď:

- signál přepíše na změnu nálady (a tím končí),

- nebo spustí interakci \[CB\]--\[AB\] (a výstup do \[IB\] přijde až po
  dokončení této interakce)?

------------------------------------------------------------------------

**72.** Pokud platí výše uvedené -- je to tak, že signál od \[IB\]
vstupuje do serveru a server rozhoduje **diskrétně**: buď signál pošle
na filtr (→ změna nálady, konec), nebo signál pošle na \[AB\] (→ akce,
návrat stavu, pak filtr, pak změna nálady)? Tedy **server je
rozcestník**, který určuje trasu signálu?

------------------------------------------------------------------------

**73.** Když server pošle signál na \[AB\] -- co se v té chvíli děje s
původní interakcí \[IB\]--\[CB\]? Je:

- pozastavena a čeká na návrat z \[AB\],

- nebo ukončena a interakce \[CB\]--\[AB\] je nová, samostatná
  interakce,

- nebo se celá věc bere jako jedna interakce \[IB\]--\[CB\]--\[AB\], kde
  výstup do \[IB\] je až na konci?

------------------------------------------------------------------------

**74.** V obecném systému je interakce \[CB\]--\[AB\] iniciována \[CB\].
Když v modelu signál od \[IB\] dorazí do serveru a server iniciuje
\[CB\]--\[AB\] -- je to **technicky nová interakce**, kterou iniciuje
\[CB\]? Nebo to stále považujeme za **součást téže interakce**, protože
prvotní iniciace šla od \[IB\]?

------------------------------------------------------------------------

**75.** Když \[AB\] vrátí stav do \[CB\] (do prostředí) a ten se dostane
k filtru -- **kdo nebo co v tu chvíli spouští filtr**? Je filtr aktivní
neustále a zpracuje vše, co do něj z prostředí přijde? Nebo filtr čeká
na signál ze serveru, že má zpracovat?

------------------------------------------------------------------------

**76.** Může se stát, že do filtru dorazí signál z prostředí ve chvíli,
kdy zrovna neprobíhá žádná interakce \[IB\]--\[CB\]? Tedy stav z \[AB\]
„čeká" v prostředí a když \[IB\] později iniciuje novou interakci, filtr
ho vezme? Nebo filtr zpracovává jen to, co je přímým důsledkem právě
probíhající interakce?

------------------------------------------------------------------------

**77.** V bodě 44 jsi řekl, že výstup do \[IB\] je vždy změna nálady,
nikdy ne nulová. V bodě 67 ale říkáš, že změna parametrů \[CB\] má
„nulový výstup". Je tento „nulový výstup" reprezentován jako **nulová
změna nálady** (což jsi připustil pro zjednodušený model)? Nebo to
znamená, že \[IB\] **vůbec nedostane výstup** a interakce jakoby
„ztichne"?

------------------------------------------------------------------------

**78.** Když filtr propustí signál a ten změní náladu -- **co přesně je
výstupem**? Je to:

- hodnota (např. +1 spokojenost / -1 frustrace),

- nebo kategorie (spokojený / frustrovaný / neutrální),

- nebo něco jiného?

A jak s touto hodnotou \[IB\] naloží? Uloží ji jako nový stav nálady?
Sčítá se s předchozí?

------------------------------------------------------------------------

**79.** V modelu bude filtr statický (cholerik/flegmatik). Bude to
jediné nastavení pro celý scénář? Nebo budete mít více scénářů s různým
nastavením filtru, aby bylo vidět, jak stejné události vedou k různé
náladě?

------------------------------------------------------------------------

**80.** Vnímáš teď po všech těchto otázkách nějakou **nevyjasněnou část
modelu**, kterou bychom ještě měli probrat? Nebo máš pocit, že základní
kostra už je dostatečně pevná?

71\. Právě že dělá obojí. 72. Signál od IB vstupuje do CB, tam vyvolává
interakci, tedy iniciuje CB-AB a současně signál končí na filtru
(zmáčknu tlačítko, je to věm, ten se mi propíše do kognice - u nás
nulový výstup, není důležitý, ale je tam) 73. Vysvětleno v 72. 74. Je to
nové - příklad, který vše demonstruje. Uživatel zmáčkne tlačítko, světlo
se rozsvítí. 1. interakce - IB tlačítko \> CB přeposílá (2. interakce)
\> hmat jde do IB na filtr, výstup 1 2. interakce - CB zapni \> AB zapne
\> světlo do prostoru výstup 2 3. interakce - IB interaguje fyzické věmy
s prostředím CB, tohle je iniciace, která probíhá konstantně \> světlo
se šíří prostředím na filtr \> filtr je oko, nabere, vyhodnotí pošle do
kognice, výstup 3 75. viz příklad, filtr a fyzické věmy iniciují
konstantně tady samotná zpětná vazba je asi jinak. Kognice vyhodnocuje
stavy kolem, musíme pro tento případ trefit start iniciace, co je
interface a co je v CB, musí to ale začít ideálně v uživateli a v něm to
skončit (tohle musíme přizpůsobit systému, nebo systém předefinovat. 76.
Nemělo by to tak být viz 75 77. Už jsme řešili. Pro tento zjednodušený
model je 0. 78. Neřešíme, zjednodušíme a najdeme odpověď později, jde o
vizualizaci mechanizmu. 79. Ano už jsme řešili 80. Ptej se. Musíme
vyřešit nalezený konflikt.

Dobře, teď se to lámie. Příklad s tlačítkem a světlem konečně odhalil
ten konflikt, na který narážíš. Dovol mi ho pojmenovat a pak se budu
ptát.

------------------------------------------------------------------------

**Konflikt, který vidím:**

V obecném systému platí: **Interakce začíná iniciací a končí výstupem ve
stejném bloku, který interakci zahájil.**

V tvém příkladu:

- **1. interakce** -- iniciuje \[IB\] (tlačítko), výstup dostává \[IB\]
  (hmat na filtr → kognice). **OK.**

- **2. interakce** -- iniciuje \[CB\] (povel „zapni"), výstup dostává
  \[CB\] (světlo do prostoru). **OK.**

- **3. interakce** -- iniciuje \[IB\] (fyzické vjemy → oko), výstup
  dostává \[IB\] (filtr → kognice). **OK.**

**Ale:** kde je v obecném systému povolena interakce \[IB\]--\[CB\],
která je iniciována \[IB\] na základě **stavu prostředí**, který se
změnil kvůli \[AB\]? Obecný systém definuje jen interakce \[IB\]--\[CB\]
a \[CB\]--\[AB\]. Třetí interakce je technicky zase \[IB\]--\[CB\], ale
její **spouštěč není uživatelova vůle**, nýbrž konstantní monitoring
prostředí. To obecný systém explicitně neřeší.

A současně říkáš, že 3. interakce „probíhá konstantně". Tím se nabourává
princip **sekvenčnosti výstupů** -- pokud \[IB\] konstantně monitoruje
prostředí, pak interakce nejsou diskrétní sekvence, ale spojitý tok.

------------------------------------------------------------------------

**81.** Je tohle ten konflikt, který cítíš? Že obecný systém počítá s
diskrétními interakcemi iniciovanými \[IB\], ale realita smart home (a
lidského vnímání) vyžaduje **kontinuální smyčku vnímání**, která nemá
jasný iniciační bod?

------------------------------------------------------------------------

**82.** Pokud ano -- chceš tenhle konflikt **vyřešit úpravou obecného
systému** (např. přidat typ interakce „monitorování", nebo povolit
kontinuální interakce)? Nebo ho chceš **přiznat jako odlišnost** a
ukázat, že modelová aplikace odhalila limit obecného systému?

------------------------------------------------------------------------

**83.** V příkladu je výstup 1 (hmat) popsán jako „nulový výstup, není
důležitý, ale je tam". Znamená to, že v modelu budeš rozlišovat
mezi **vědomou iniciací** (zmáčknutí tlačítka s cílem rozsvítit)
a **mimovolným vjemem** (hmatový vjem z tlačítka, který je vedlejším
produktem)? A oba jsou modelovány jako samostatné interakce
\[IB\]--\[CB\]?

------------------------------------------------------------------------

**84.** Když je 3. interakce iniciována \[IB\] (fyzické vjemy) a
vstupuje do \[CB\] (prostředí → filtr → kognice) -- kde přesně
je **iniciační bod** v \[IB\]? Je to:

- smyslový orgán (oko), který „snímá" prostředí,

- nebo kognice, která „vyhledává" podněty,

- nebo obojí a musíme to v modelu oddělit?

------------------------------------------------------------------------

**85.** V obecném systému platí, že výstup z \[IB\]--\[CB\] mění
parametry \[IB\]. V příkladu máme tři výstupy do \[IB\]:

- výstup 1 (hmat) -- nulový,

- výstup 3 (světlo → nálada) -- mění náladu.

Může jedna akce uživatele (zmáčknutí) vést k **více výstupům do
\[IB\]** v různých časech? A pokud ano -- neporušuje to princip „jedna
interakce, jeden výstup"?

------------------------------------------------------------------------

**86.** Nabízí se otázka: je „zmáčknutí tlačítka" v modelu **jedna
ucelená uživatelova akce**, která se v modelu rozpadne na více
interakcí, nebo jsou to **tři nezávislé interakce**, které spolu
příčinně souvisejí, ale systémově jsou oddělené?

------------------------------------------------------------------------

**87.** Když \[IB\] „konstantně iniciuje" interakce s prostředím -- jak
v modelu reprezentuješ tuto konstantnost? Budeš mít v modelu **smyčku
vnímání** jako samostatný mechanismus? Nebo každý vjem bude modelován
jako diskrétní interakce a „konstantnost" bude jen narativní obal?

------------------------------------------------------------------------

**88.** V příkladu výstup z \[AB\] (světlo) vstupuje do prostředí \[CB\]
a odtud je iniciován \[IB\] jako nová interakce. Obecný systém ale
definuje interakci \[CB\]--\[AB\] jako ukončenou výstupem do \[CB\].
Nevyžaduje to, aby prostředí \[CB\] **aktivně předalo** stav filtru?
Není tím pádem prostředí v roli **iniciátora vůči filtru**? A není to v
rozporu s tím, že jediným iniciátorem je \[IB\]?

------------------------------------------------------------------------

**89.** Cítím, že jádro konfliktu je v tom, že obecný systém
má **lineární řetězec** \[IB\]→\[CB\]→\[AB\] a zpět, ale realita smart
home vrací výstup z \[AB\] do \[IB\] přes **paralelní
větev** (prostředí), která obchází „iniciační monopol" \[IB\]. Chceš
tenhle rozpor **vyřešit přiznáním, že prostředí je iniciátor** (a tedy
upravit obecný systém)? Nebo **předefinovat hranice \[IB\]** tak, aby
konstantní vnímání prostředí bylo interní záležitostí \[IB\] a ne
interakcí?

------------------------------------------------------------------------

**90.** Pokud bychom řekli, že 3. interakce (světlo → oko →
kognice) **není interakcí v systémovém smyslu**, ale **interní logikou
\[IB\]**, která zpracovává výstupy z předchozích interakcí -- vyřešilo
by to konflikt? Pak by totiž jedinou interakcí \[IB\]--\[CB\] bylo
zmáčknutí a jediným výstupem do \[IB\] by byl souhrnný výsledek (světlo
svítí + hmat = nálada). Co tím ztratíme?

81\. Ne to není systém nemá problém s tím, že by se do sebe zanořily
interakce, tedy pokud je zanoříš dostatečně jemně, dostáváž limitně
spojitý stav, což je v pořádku, jde o dizajn systému. Konflikt je v tom,
že máme monitoring prostředí. Co ho spouští? interakce signálu je jasná
interface interakce je čidlo, ale co je interface interakce
monitorování?, když ten tok interakce musí být následující? iniciace v
IB ??? (co) \> světlo dopadá na oko \> informace se dostává na filtr
(výstup do systému - řekli jsme že IB je kognice, fyzické tělo a
senzory - tady to vypadá, že fyzické tělo je jak v bloku IB, tak CB, což
není problém. V modelu může jít o iniciaci v oku, kognici a jít to přes
oko do filtru, ale \... - buď je iniciací detekce výstup z minulé
interakce, což by bylo systémově čisté, nebo by byla iniciace od CB, což
systém neumožňuje. - musíse buď rozhodnout o zpřesnění systému, nebo o
kontunuální detekci jako vnořených interakcí, které limitně tvoří
kontinuum(tohle je možná jen fylozofický pohled) a obě jsou možné. 82.
viz výše 83. ne v této zjednodušené simulaci 84. viz. výše. buď CB, nebo
předešlý/předešlé výstup/výstupy detekční interakce/interakcí 85. Ano,
ale z jedné interakce jen jeden výstup. Jedna interakce mění podmínky
druhé. 86. 3 nezávislé interakce. 87. Ano smyčka vnímání je jiná než
interakce se senzory. Jde o jiný typ interakce se stejným základem 88.
Řešili jsme, jde o filozofický přístup. 89. Jádro konfliktu je v
pochopení. Každý systém a model je řešen jinak. Mohou být jinak popsány,
definovány, ale jsou totéž. Popis a definice neznamená, že jsou jié, jen
popisujeme stejné příčiny jinými mechanismy a každý tento popis má své
klady a zápory. Osobně cítím, že to co máme, tedy iniciuje jen člověk a
vše ostatní je pasivní je blíže tomu, co chceme ukázat, než že by byl
člověk aktivním členem a současně pasivním příjemcem. 90. Jde částečně o
interní logiku. Jsme dost hluboko a máme kritický problém detailně
popsán a naše možnosti. - vypiš mi jádro konfliktu a 2 řešení, které se
nabízejí

Dobře, jdu to shrnout a vytáhnout jádro.

------------------------------------------------------------------------

**Jádro konfliktu**

Systém definuje **jediného iniciátora všech interakcí** -- \[IB\]. Každá
interakce má jasný iniciační bod v \[IB\] a končí výstupem v \[IB\].

Model smart home ale vyžaduje, aby \[IB\] **vnímal stav
prostředí** (světlo svítí, žaluzie nejedou) -- tedy musí existovat
mechanismus, kterým se informace o stavu \[CB\]/\[AB\] dostává zpět do
\[IB\].

Tento mechanismsus nazýváš **smyčka vnímání** nebo **monitorování
prostředí**. A tady vzniká konflikt:

**Kdo nebo co iniciuje tuto smyčku?**

Obecný systém zná jen interakce:

- \[IB\] iniciuje \[IB\]--\[CB\]

- \[CB\] iniciuje \[CB\]--\[AB\]

Smyčka vnímání ale vypadá takto:

- \[IB\] (oko) → \[CB\] (prostředí) → \[CB\] (filtr) → \[IB\] (kognice)

Problém je **iniciační bod** smyčky. Jsou dvě logické možnosti a každá
naráží:

1.  **Iniciace v \[IB\]** -- \[IB\] musí „sám od sebe" iniciovat
    vnímání. Co ho k tomu ale spouští? Buď je to **důsledek předchozího
    výstupu** (systémově čisté -- výstup jedné interakce spouští další),
    nebo je to **kontinuální autonomní aktivita** \[IB\] (oko neustále
    snímá). To druhé není v obecném systému popsáno, ale lze to
    modelovat jako limitně jemné vnořování interakcí -- filozoficky
    přijatelné.

2.  **Iniciace v \[CB\]** -- prostředí \[CB\] aktivně tlačí informaci do
    filtru a ten do \[IB\]. To je přirozené (světlo svítí → dopadá na
    sítnici), ale **porušuje to monopol \[IB\] na iniciaci** -- \[CB\]
    by iniciovalo interakci směrem k \[IB\], což obecný systém
    neumožňuje.

**Konflikt tedy zní:**

Jak do systému, kde iniciuje pouze \[IB\], zabudovat kontinuální vnímání
prostředí, které je ze své podstaty iniciováno změnou v prostředí (tedy
mimo \[IB\])?

------------------------------------------------------------------------

**Dvě řešení, která se nabízejí**

**Řešení A: Iniciace jako řetězec výstupů (systémově čisté)**

**Princip:** Každá smyčka vnímání je **iniciována výstupem předchozí
interakce**, nikoli samovolně.

**Mechanismus:**

- \[IB\] iniciuje interakci 1 (zmáčknutí) → výstup do \[IB\] (hmat).

- \[CB\] iniciuje interakci 2 (zapni) → výstup do \[CB\] (světlo v
  prostoru).

- Výstup interakce 2 (stav „světlo svítí") **je vstupem pro interakci
  3**, kterou iniciuje \[IB\] na základě právě obdrženého výstupu z
  interakce 1, nebo na základě interního pravidla „po výstupu z \[AB\]
  vždy monitoruj".

**Výhody:**

- Zachovává monopol \[IB\] na iniciaci.

- Každá interakce má jasný spouštěč (předchozí výstup).

- Systémově čisté, není třeba měnit obecný systém.

**Nevýhody:**

- Vyžaduje explicitní pravidlo v \[IB\]: „když dostanu výstup typu X,
  iniciuji monitorování".

- Kontinuální vnímání je rozbito do diskrétních kroků -- filozoficky
  méně přirozené, ale pro model přijatelné.

------------------------------------------------------------------------

**Řešení B: Kontinuální smyčka jako vnořené interakce (filozoficky
čistší)**

**Princip:** \[IB\] má **trvale běžící smyčku vnímání**, která je
modelována jako sekvence vnořených interakcí s limitně jemným krokem.
Navenek se jeví jako kontinuum.

**Mechanismus:**

- \[IB\] iniciuje „monitorovací interakci" -- ta je trvale otevřená,
  nebo se neustále obnovuje.

- Změna v prostředí \[CB\] se do této smyčky „zachytí" jako výstup.

- Systémově jde stále o interakci iniciovanou \[IB\], jen je její trvání
  dlouhé a krok jemný.

**Výhody:**

- Zachovává monopol \[IB\] na iniciaci.

- Lépe odpovídá představě kontinuálního vnímání (oko neustále „snímá").

- Obecný systém to nevylučuje -- nic neříká o frekvenci ani o trvání
  interakcí.

**Nevýhody:**

- Vyžaduje přiznat, že interakce nejsou jen diskrétní události, ale
  mohou být i dlouhodobé procesy.

- Hranice mezi „jednou dlouhou interakcí" a „mnoha krátkými" je nejasná
  -- ale to lze ošetřit jako filozofickou poznámku.

**Můj dojem z tvých slov**

Ty se kloníš k **řešení A nebo jeho variantě** -- chceš, aby **člověk
byl aktivním iniciátorem a vše ostatní pasivní**. To znamená, že i
vnímání prostředí musí být iniciováno z \[IB\], ideálně jako důsledek
předchozího výstupu. Tím zůstává \[IB\] jediným zdrojem pohybu v
systému, vše ostatní jen reaguje.

Chceš, abych na základě tohoto rozboru pokračoval dalšími otázkami, nebo
ti mám navrhnout, jak by konkrétně vypadala modelová definice při volbě
řešení A?

Tohle není k čemu se klovím. Me si to tak, že kybernetika zná start a
konec a sama tohle vše propojuje do spojitých signálů, tedy i zpětná
vazba je nekonečná smyčka. Naše zpetná vazba je taky nekonečná smyčka
prostředí\>uživatel, která jde přes filtry, kognice, oko, prostředí \...
Pokud jde o nekonečnou smyčku, pak kdo určí kde začíná? I v kybernetice
může začít poruchou na jiném, než tradičním místě. Tedy naše 2 možnosti
jsou čistě filozofické: 1. prostředí je aktivní, tady to začíná (musíme
změnit systém) - člověk je pasivním příjemcem 2. člověk je aktivní, tady
to začíná (nemusíme změnit systém) - prostředí je pasivní Vidíš sám, že
pasivita/aktivita je tradiční vnímání, ale tady nemá smysl, tedy jde o
filozofii (technicky jsou možné obě varianty). - tedy pokud chceme
vypíchnu člověka jako pasivního, nebo aktivního v tom, kdo formuje jeho
kognici. - za mne aktivního (tradice), ale jde to proti tradici v tom,
že si tahá signály z prostředí aktivně.

Ano, teď to vidím přesně. Díky za trpělivost.

------------------------------------------------------------------------

**Shrnutí podstaty**

Není to technický konflikt -- obě varianty jsou technicky možné. Je
to **filozofická volba rámování**.

Jde o to, **kdo je v modelu nositelem aktivity** ve smyčce vnímání:

  ------------------------------------------------------------------------
  Varianta    Aktivní člen         Pasivní člen       Důsledek pro systém
  ----------- -------------------- ------------------ --------------------
  **1.        \[CB\] (prostředí)   \[IB\] (člověk) -- Nutná změna systému
  Prostředí   -- světlo \"útočí\"  pasivně přijímá    -- \[CB\] by
  aktivní**   na smysly                               iniciovalo interakci

  **2. Člověk \[IB\] (člověk) --   \[CB\] (prostředí) Systém beze změny --
  aktivní**   aktivně \"sahá\" do  -- pasivně je k    \[IB\] iniciuje i
              prostředí smysly     dispozici          vnímání
  ------------------------------------------------------------------------

Obě jsou technicky správně. Obě popisují tutéž realitu. Liší se jen v
tom, **koho rámujeme jako původce dění**.

------------------------------------------------------------------------

**Tvoje volba**

Volíš **člověka jako aktivního** -- protože to odpovídá tradici (člověk
formuje svou kognici, není jen obětí podnětů), a zároveň to **jde proti
tradici** v tom smyslu, že člověk je zde aktivní i ve vnímání -- nahlíží
se na něj jako na toho, kdo si **aktivně tahá signály z prostředí**, ne
jako na pasivního příjemce.

Tohle je podle mě klíčová filozofická pozice tvé práce -- a model ji
bude ztělesňovat.

------------------------------------------------------------------------

**Co z toho plyne pro model**

- \[IB\] je **jediným iniciátorem všech interakcí**, včetně vnímání
  prostředí.

- Smyčka vnímání je modelována jako **interakce iniciovaná \[IB\]** --
  \[IB\] „sahá" do \[CB\] (prostředí) a získává výstup.

- \[CB\] je **zcela pasivní** -- nespouští nic, jen reaguje a je „k
  dispozici".

- Není třeba měnit obecný systém.

------------------------------------------------------------------------

**Poslední otázky k uzavření**

**91.** Smyčka vnímání -- bude v modelu reprezentována jako:

- a) **samostatný typ interakce** \[IB\]--\[CB\] (např. „monitorovací
  interakce"), odlišný od interakce se senzorem,

- nebo b) **stejný typ interakce** jako se senzorem, jen s jiným vstupem
  (oko místo tlačítka)?

**92.** Když je člověk aktivní ve vnímání -- co konkrétně
je **iniciačním podnětem** pro monitorovací interakci? Je to:

- výstup předchozí interakce (řetězec),

- interní potřeba \[IB\] (zvědavost, kontrola stavu),

- nebo je to **trvale běžící proces** (člověk neustále vnímá, dokud je
  vzhůru)?

**93.** Chceš tuto filozofickou volbu (člověk aktivní vs. prostředí
pasivní) v práci **explicitně diskutovat** jako vědomé rozhodnutí, nebo
ji jen **tiše přijmout** a model podle ní postavit bez komentáře?

**94.** Jsi připraven, abych na základě všeho, co jsme probrali,
navrhl **kompletní formální definici jednoduchého modelu** -- bloky,
parametry, typy interakcí, vstupy a výstupy?

91\. jde o jiný typ, ale mechanika je stejná. Jiný typ, protože jde do
prostředí a neaktivuje CB-AB, ale stejný mechanicky, jen začíná jinde.
92. Musíme zavést kontinuální smyčku, tedy start je o předchozí
interakci, interface najdeme. 93. Ano bude to diskutováno, ať je vidět
naše rozhodnutí. Jde o to, že tohle přímo ovlivní i složitější model.
Tvůj nový úkol. - zjednodušit na maximum model, tedy jdeme od AB-CB Jak
definovat oba bloky? Vstupy, výstupy, které se napojují a interakce. -
popiš to jednoduše, baychom se rozhodli co nechat, zrušit, zjednodušet.
Jde nám na konfi o filtr, tedy zjednodušení je o tom, co potřebujeme k
filtru dostat a odkud?

Rozumím. Jdeme odspodu -- od \[AB\] a \[CB\] směrem k filtru. Maximum
zjednodušení. Jen to, co potřebujeme k tomu, aby filtr měl co
zpracovávat.

**Návrh: Minimální model \[AB\] -- \[CB\]**

------------------------------------------------------------------------

**\[AB\] -- Aktor**

**Definice:**\
Jeden blok reprezentující libovolný akční prvek domu (světlo, žaluzie,
topení\...). V jednoduchém modelu jeden kus.

**Vstup:**

- Signál z \[CB\] typu „vykonej akci" (např. „zapni", „vypni", „nastav
  hodnotu").

**Výstup:**

- Stav po vykonání akce. Pro jednoduchý model binární: **funguje /
  nefunguje** (svítí/nesvítí, jede/nejede).

**Chování:**

- Na vstup vždy reaguje změnou stavu a vrácením výstupu.

- Selhání (nefunguje) je simulováno jako výstup „nefunguje" -- buď jako
  pevný parametr bloku, nebo nastavené pro scénář.

- Žádná vnitřní logika navíc.

**Co zahazujeme:**

- Více aktorů (pro jednoduchost jeden).

- Složitější stavy (jen binární).

- Zpoždění, timeouty.

------------------------------------------------------------------------

**\[CB\] -- Server + Prostředí + Filtr**

**Definice:**\
Složený blok. Obsahuje tři
podbloky: **Server**, **Prostředí**, **Filtr**. Pro jednoduchý model je
kreslíme jako jeden vnější blok s vnitřní strukturou.

------------------------------------------------------------------------

**Podblok 1: Server**

**Vstup:**

- Signál od \[IB\] ze senzoru (např. „stisk tlačítka").

**Výstup:**

- Jeden ze dvou možných:

  - a\) Povel do \[AB\] („zapni") -- pokud signál vyžaduje akci.

  - b\) Signál přímo do Filtru -- pokud signál akci nevyžaduje (např.
    dotaz na stav).

**Chování:**

- Pevná přepisovací logika: **signál X → akce Y** (tabulka nebo
  pravidlo).

- Žádná automatizace, žádné vlastní rozhodování.

- Pokud signál spouští \[AB\], posílá povel a **zároveň** může poslat
  kopii signálu do Filtru (hmatová zpětná vazba -- pro jednoduchý model
  nulový výstup, můžeme vynechat).

**Co zahazujeme:**

- Složitou logiku serveru (pro model stačí jedno pravidlo).

- Hmatovou zpětnou vazbu (nulový výstup -- pro jednoduchost vynecháme).

- Ukládání logů, historie.

------------------------------------------------------------------------

**Podblok 2: Prostředí**

**Vstup:**

- Stav z \[AB\] („svítí" / „nesvítí").

**Výstup:**

- Stav předaný do Filtru.

**Chování:**

- Pasivní přenosové médium. Přijme stav, podrží ho, je k dispozici.

- Filtr si z něj „tahá" data, když \[IB\] iniciuje monitorovací
  interakci.

- Žádná vlastní aktivita.

**Co zahazujeme:**

- Jakoukoliv logiku prostředí (výpadky, šíření, zpoždění).

- Pro jednoduchý model: prostředí nedělá nic než drží poslední stav
  \[AB\].

------------------------------------------------------------------------

**Podblok 3: Filtr**

**Vstup:**

- Z jednoho ze dvou zdrojů:

  - a\) Ze Serveru -- signál, který nešel na \[AB\] (dotaz, přímý vjem).

  - b\) Z Prostředí -- stav \[AB\] (výsledek monitorovací interakce).

**Výstup:**

- Změna nálady do \[IB\] (pro jednoduchý model: +1 / 0 / −1).

**Chování:**

- Deterministická funkce: **(zdroj + typ signálu + nastavení filtru) →
  změna nálady**.

- Nastavení filtru: jeden parametr -- **typ** (cholerik / flegmatik).

  - Cholerik: zesiluje negativní, tlumí pozitivní (nebo naopak -- podle
    volby).

  - Flegmatik: vše tlumené, menší výkyvy.

- Filtr je statický -- nastavení se během scénáře nemění.

- Výstup je vždy -- i nulový (0).

**Co zahazujeme:**

- Dynamickou změnu filtru.

- Složitější typologii (jen dva typy).

- Více parametrů (jen jeden).

------------------------------------------------------------------------

**Schéma interakcí (minimální verze)**

text

\[IB\] ──(signál ze senzoru)──▶ \[Server\]

│

├──▶ \[AB\] ──(stav)──▶ \[Prostředí\] ──▶ \[Filtr\] ──(změna nálady)──▶
\[IB\]

│

└──▶ \[Filtr\] ──(změna nálady)──▶ \[IB\] (přímá cesta, bez AB)

Dvě cesty k filtru:

1.  **Přes \[AB\] a Prostředí** -- signál spustil akci, stav se vrací.

2.  **Napřímo** -- signál nespustil akci, jde rovnou na filtr.

------------------------------------------------------------------------

**Otázky na tebe k rozhodnutí**

**A.** Vyhovuje ti, že hmatovou zpětnou vazbu („zmáčkl jsem tlačítko") v
jednoduchém modelu **zcela vynecháme**? Tedy signál ze senzoru jde do
Serveru a tam se rozdělí -- buď na \[AB\], nebo na Filtr -- ale nikdy ne
obojí zároveň?

**B.** Prostředí jako pasivní držák stavu \[AB\] -- stačí to? Nebo
potřebujeme, aby prostředí mělo alespoň jeden vlastní stav (např. „tma"
/ „světlo") nezávisle na \[AB\]? (Výpadek elektřiny by pak byl změna
stavu Prostředí, ne \[AB\].)

**C.** Filtr se dvěma typy (cholerik/flegmatik) -- chceš ukázat oba v
jednom scénáři (dva průchody), nebo každý scénář poběží s jedním typem?

**D.** Chceme v modelu nechat možnost, že \[IB\] iniciuje monitorovací
interakci („jak svítí světlo?"), i když žádná předchozí interakce
neproběhla? Nebo vždy jen jako důsledek předchozího výstupu?

------------------------------------------------------------------------

Odpověz a doladíme finální podobu minimálního modelu.

Nejde to napsat jednodušeji? - potřebujeme jen popis objektů a jak
vypadá interakce. \" \[AB\] - aktory - světelné těleso \[CB\] - server -
prostředí domu \[CB\]-\[AB\] interakce iniciace (server) -- rozsviť
(sběrnice) rozsviť (sběrnice) -- světelné těleso světlo vnitřní logika
-- svítí výstup -- světlo (prostředí domu) \"

Rozumím. Chceš to takto jednoduše -- jen popis objektů a průběh
interakce. Nic víc.

------------------------------------------------------------------------

**\[AB\] -- Světelné těleso**

- Aktor.

- Přijímá příkaz ze sběrnice.

- Vykoná akci (svítí/nesvítí).

- Výstup: světlo do prostředí domu.

------------------------------------------------------------------------

**\[CB\] -- Server + Prostředí domu**

**Server:**

- Přijímá signál od \[IB\].

- Posílá příkaz na sběrnici do \[AB\].

**Prostředí domu:**

- Přijímá světlo z \[AB\].

- Drží stav (světlo/nesvětlo).

- Je k dispozici pro \[IB\] (monitorovací interakce).

------------------------------------------------------------------------

**Interakce \[CB\]--\[AB\]**

  -----------------------------------------------------------------------
  Krok                  Co se děje
  --------------------- -------------------------------------------------
  Iniciace              Server pošle „rozsviť" na sběrnici

  Přenos                „rozsviť" putuje sběrnicí do světelného tělesa

  Vnitřní logika \[AB\] Světelné těleso provede akci -- svítí

  Výstup                Světlo vstupuje do prostředí domu
  -----------------------------------------------------------------------

------------------------------------------------------------------------

Je to takto dostatečně jednoduché? Nebo to chceš ještě víc ořezat?

Tohle je na start perfektní. Jdeme na interakci atodetekce. - věta o
tom, že systém popisuje interakci jako sekvenční - logika toho, že pokud
budou interakce probíhat jako rychlé a navazující na sebe, nebo budou i
vnořené, pak jde v limitním případě o spojitou interakci se spojitým
výstupem. Potřebujeme loop - oko \[CB\] - filtr \[CB\] - kognice
\[interní logika IB\] - svalové ovládání očního víčka \[interní logika
\[IB\] - prostředí \[CB\] Do loopu musíme ukázat, jak se mění světlo
přes filtr na kognici Právě jsem vyřešil problém oko v \[CB\] a současně
\[IB\] když se přidalo ovládání svalového nervu očního víčka.

Chápu. Přidáváš **loop vnímání** a elegantně řešíš hranici \[IB\]/\[CB\]
-- oko je v \[CB\], ale ovládání víčka je interní logika \[IB\]. Tím
\[IB\] aktivně ovládá, co do filtru pustí, a zůstává iniciátorem.

Pojďme to zapsat ve stejném duchu jako předchozí interakci.

------------------------------------------------------------------------

**Interakce autodetekce -- Loop vnímání**

Systém definuje interakci jako sekvenční. Pokud interakce probíhají
rychle, navazují na sebe nebo se vnořují, v limitním případě tvoří
spojitou interakci se spojitým výstupem.

------------------------------------------------------------------------

**Objekty**

**\[CB\] -- Oko**

- Vstupní brána pro světlo z prostředí.

- Propouští světlo dál do filtru.

- Je ovládáno z \[IB\] (otevřeno/zavřeno).

**\[CB\] -- Filtr**

- Přijímá světlo z oka.

- Na základě svého nastavení (cholerik/flegmatik) propouští signál do
  kognice.

- Výstup: signál do kognice.

**\[IB\] -- Kognice** *(interní logika \[IB\])*

- Přijímá signál z filtru.

- Vyhodnocuje -- výsledkem je změna nálady.

**\[IB\] -- Svalové ovládání víčka** *(interní logika \[IB\])*

- Na základě výstupu kognice (nálada, únava, vůle) ovládá víčko.

- Otevřeno = loop běží. Zavřeno = loop přerušen, signál nevstupuje.

**\[CB\] -- Prostředí**

- Drží stav: světlo/nesvětlo.

- Je zdrojem signálu pro oko.

------------------------------------------------------------------------

**Průběh interakce (loop)**

  -----------------------------------------------------------------------
  Krok             Co se děje
  ---------------- ------------------------------------------------------
  Iniciace         \[IB\] -- svalové ovládání víčka → víčko otevřeno

  Vstup            Světlo z prostředí vstupuje do oka \[CB\]

  Přenos           Oko propouští světlo do filtru \[CB\]

  Vnitřní logika   Filtr na základě nastavení signál transformuje
  filtru           

  Výstup z \[CB\]  Signál vstupuje do kognice \[IB\]

  Vnitřní logika   Kognice vyhodnocuje → změna nálady
  \[IB\]           

  Zpětná vazba     Nálada ovlivňuje svalové ovládání víčka → ovlivňuje
                   další běh loopu
  -----------------------------------------------------------------------

------------------------------------------------------------------------

**Spojitost**

Loop může běžet opakovaně (sekvenční interakce za sebou). Při vysoké
frekvenci přechází ve spojité vnímání se spojitým výstupem (nálada se
mění plynule).

------------------------------------------------------------------------

Je to takto? Chceš něco upravit, nebo jdeme dál?

Perfektní: - člověk (dotek) - senzor (signál) - sběrnice + věm -
prostředí (CB) - server (interní logika) - prostředí (tlak) - nervy na
prstech \[CB\] - jako oko - filtr - výstup na kognici Tady je dobré
zdůvodnit, že interakce je iniciována jedním dotekem, ale signál se dělí
na 2 části, jedna končí na serveru s ukončením (změnou parametrů) a
druhá na filtru, s výstupem. Tohle systém nazakazuje, ani nerozebírá,
ale podmínka, že interakce končí výstupem tam je.

Ano, rozumím. Dotek je jedna iniciace, ale signál se v \[CB\] dělí na
dvě cesty -- každá končí jinde. Systém to nezakazuje, protože obě cesty
končí výstupem.

------------------------------------------------------------------------

**Interakce: Dotek**

------------------------------------------------------------------------

**Objekty**

**\[IB\] -- Člověk (dotek)**

- Iniciátor. Fyzicky se dotýká senzoru.

**\[CB\] -- Senzor + Sběrnice**

- Přijímá dotek, převádí na signál.

- Signál posílá po sběrnici do serveru.

- Současně generuje hmatový vjem do prostředí.

**\[CB\] -- Prostředí (tlak)**

- Přijímá hmatový vjem ze senzoru.

- Drží ho k dispozici pro nervy na prstech.

**\[CB\] -- Server**

- Přijímá signál ze sběrnice.

- Vnitřní logika: změní parametry (např. zaregistruje stisk).

- Iniciuje interakci \[CB\]--\[AB\] (rozsvícení).

- Zde interakce končí -- výstupem je změna parametrů serveru.

**\[CB\] -- Nervy na prstech**

- Obdoba oka. Vstupní brána pro tlak z prostředí.

- Propouští signál do filtru.

**\[CB\] -- Filtr**

- Přijímá signál z nervů.

- Transformuje dle nastavení.

- Výstup do kognice.

**\[IB\] -- Kognice** *(interní logika)*

- Přijímá signál z filtru.

- Výsledek: změna nálady.

------------------------------------------------------------------------

**Průběh interakce**

  -----------------------------------------------------------------------
  Krok                 Co se děje
  -------------------- --------------------------------------------------
  Iniciace             \[IB\] -- člověk se dotkne senzoru

  Vstup                Dotek → senzor + sběrnice \[CB\]

  Dělení signálu       Signál se rozděluje na dvě cesty

                       

  **Cesta 1**          

  Přenos               Signál putuje sběrnicí do serveru \[CB\]

  Vnitřní logika       Server registruje stisk, mění parametry

  Výstup 1             Změna parametrů serveru -- interakce končí

                       

  **Cesta 2**          

  Přenos               Hmatový vjem vstupuje do prostředí (tlak) \[CB\]

  Vstup do filtru      Nervy na prstech \[CB\] snímají tlak z prostředí

  Přenos               Nervy → filtr \[CB\]

  Vnitřní logika       Filtr transformuje signál
  filtru               

  Výstup 2             Signál vstupuje do kognice \[IB\] → změna nálady
  -----------------------------------------------------------------------

------------------------------------------------------------------------

**Zdůvodnění**

Systém definuje, že interakce začíná iniciací a končí výstupem v bloku,
který iniciaci zahájil. Neřeší, zda se signál uvnitř \[CB\] dělí na více
cest.

Zde jedna iniciace vytváří dvě cesty -- obě končí výstupem:

- Cesta 1 končí změnou parametrů \[CB\] (server).

- Cesta 2 končí změnou nálady \[IB\] (kognice).

Systémová podmínka je splněna. Dělení signálu je interní záležitostí
\[CB\].

------------------------------------------------------------------------

Je to takto? Pokračujeme dál?

Připrav cele kontextové pole k archivaci paměti. Potřebuji rozdělit
kontext na logické celky o tom, co jsme probírali, opatřit je názvem,
krátkým popisem a citací, kterou úsek začíná. Postup: - Rozděl kontext
podle tématu (nejdi do detailů, 2-20 paměťových částí) - Indexuj část
(01, 02, 03, \... 20) - Vymysli krátký název (max. 4 slova) - Vymysli
krátký popis aby bylo jasno co která část obsahuje (max. 4 věty) - Vypiš
přesnou citaci začátku textu (max. 10 slov) pro zpětnou dohledatelnost v
textovém editoru (ctrl+f). - Musíš obsáhnout celé kontextové pole. 01
část je od citace 01 po citaci 02.

------------------------------------------------------------------------

**Archivace kontextového pole -- indexované celky**

------------------------------------------------------------------------

**01 -- Definice obecného systému**

**Popis:** Úvodní definice tří bloků (IB, CB, AB), jejich vlastností a
životního cyklu systému. Vymezení interakcí, směrů výměn a základních
principů -- centralita CB, řízení IB, sekvenčnost výstupů.\
**Citace:** Definice 1. Bloky a životní cyklus systému: Systém je tvořen
bloky tří typů

------------------------------------------------------------------------

**02 -- Zadání reálné aplikace Smart Home**

**Popis:** Přiřazení bloků obecného systému ke konkrétním prvkům chytré
domácnosti. IB jako uživatel se senzory, CB jako server, AB jako aktory.
Definice podmínek aplikace a prvotní identifikace dilematu přímého
výstupu AB do IB.\
**Citace:** Reálná aplikace: - Smart home ve specifické formě. -
\[IB\] - uživatel domu

------------------------------------------------------------------------

**03 -- Upřesnění modelu a cíl práce**

**Popis:** Vyjasnění, že model slouží jako zjednodušený diagnostický
nástroj pro pochopení mechanismů, nikoliv přesná simulace. Důraz na
principy interakcí a jejich dopad na náladu. Scénáře budou narativní.\
**Citace:** budeme dělat velmi zjednodušený model, tedy například
simulace spokojenosti / frustrace.

------------------------------------------------------------------------

**04 -- Redefinice bloků a umístění filtru**

**Popis:** Postupné zpřesňování hranic bloků. Klíčové rozhodnutí: filtr
jako součást CB, kognice a fyzické tělo v IB, senzory v IB. Rozlišení
mezi emocí (IB) a kognitivním filtrem (CB).\
**Citace:** Fyzická stránka a kognice je \[IB\] - převodník, tedy filtr
pro ovlivnění kognice je \[CB\]

**05 -- Jádro práce: Filtr**

**Popis:** Detailní rozbor filtru jako klíčového mechanismu. Filtr
rozhoduje o propustnosti signálů, je deterministický, v jednoduchém
modelu statický (cholerik/flegmatik). V pozdějším modelu dynamický.\
**Citace:** Přesně tak. Tohle je jádro mé práce.

------------------------------------------------------------------------

**06 -- Formální povaha modelu**

**Popis:** Upřesnění, že model je formálním zápisem interakčních
sekvencí, nikoliv softwarovou simulací. Výstupem je textová práce s
diagramy. Scénáře budou ručně krokované.\
**Citace:** Ano. Model je spíše formální, musí ukázat základní principy
interakcí a následků

------------------------------------------------------------------------

**07 -- Rozbor konfliktu smyčky vnímání**

**Popis:** Identifikace kritického problému: kdo iniciuje monitorování
prostředí, když systém povoluje jen iniciaci z IB? Dvě filozofické
varianty -- aktivní prostředí (změna systému) vs. aktivní člověk
(zachování systému).\
**Citace:** Konflikt je v tom, že máme monitoring prostředí. Co ho
spouští?

------------------------------------------------------------------------

**08 -- Filozofická volba a její důsledky**

**Popis:** Rozhodnutí pro aktivního člověka jako iniciátora veškerého
vnímání. Člověk si aktivně „tahá" signály z prostředí. Tato volba bude v
práci explicitně diskutována.\
**Citace:** Tohle není k čemu se klovím. Me si to tak, že kybernetika
zná start a konec

------------------------------------------------------------------------

**09 -- Interakce CB-AB: Rozsvícení světla**

**Popis:** Minimální definice interakce mezi serverem a aktorem. Server
iniciuje příkaz, světelné těleso vykoná akci, výstupem je světlo do
prostředí domu. Jednoduchý popis objektů a kroků.\
**Citace:** \[AB\] - Světelné těleso - Aktor. - Přijímá příkaz ze
sběrnice.

------------------------------------------------------------------------

**10 -- Interakce autodetekce: Loop vnímání**

**Popis:** Smyčka vnímání jako opakovaná interakce iniciovaná z IB. Oko
v CB, filtr transformuje signál, kognice v IB vyhodnocuje, svalové
ovládání víčka v IB reguluje přísun. Limitně spojitá interakce.\
**Citace:** Interakce autodetekce -- Loop vnímání Systém definuje
interakci jako sekvenční.

------------------------------------------------------------------------

**11 -- Interakce doteku: Dělení signálu**

**Popis:** Jedna iniciace (dotek) vytváří dvě cesty signálu v CB. Cesta
1: server změní parametry. Cesta 2: hmatový vjem přes nervy a filtr do
kognice. Systém to nezakazuje, obě cesty končí výstupem.\
**Citace:** člověk (dotek) - senzor (signál) - sběrnice + věm -
prostředí (CB)

------------------------------------------------------------------------

**12 -- Shrnutí principů a struktury**

**Popis:** Rekapitulace konfliktu a dvou filozofických řešení.
Zdůraznění, že nejde o technický, ale o filozofický konflikt. Volba
aktivního člověka jako základní pozice práce.\
**Citace:** Není to technický konflikt -- obě varianty jsou technicky
možné. Je to filozofická volba

------------------------------------------------------------------------

**13 -- Návrh minimálního modelu a rozhodovací otázky**

**Popis:** Konkrétní návrh zjednodušené struktury AB, CB (server,
prostředí, filtr) s definicí vstupů a výstupů. Identifikace dvou cest k
filtru. Otázky k doladění modelu.\
**Citace:** Návrh: Minimální model \[AB\] -- \[CB\] \[AB\] -- Aktor
Definice: Jeden blok

------------------------------------------------------------------------

Celkem 13 paměťových částí pokrývajících celé kontextové pole od první
definice systému po poslední návrh modelu.
