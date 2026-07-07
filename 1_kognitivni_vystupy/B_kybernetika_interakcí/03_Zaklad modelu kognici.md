# Biologicko-anatomický základ modelu

## 0. Úvodem: Abstrakční úroveň modelu

Tento text je **modelovým úvodem**, který definuje **abstrakční úroveň**, na níž bude kognitivní model pracovat. Cílem není popsat mozek ve vší komplexitě, ale zavést **konzistentní terminologický rámec**, který umožňuje:

- definovat funkční uzly (generátory) na základě anatomické svébytnosti,
    
- definovat komunikační kanály (bílá hmota) mezi nimi,
    
- definovat vstupy a výstupy systému.
    

Biologická přesnost je na této úrovni **obětována ve prospěch formální konzistence**. Model netvrdí, že generátory jsou ve skutečnosti homogenní – tvrdí, že **pro účely modelování** je lze na této úrovni granularity považovat za funkčně analogické jednotky s odlišnými parametry. Každá z uvedených struktur je sama o sobě složitým systémem; model tuto vnitřní složitost **zapouzdřuje** do parametrů (rychlost plasticity, poměr excitace/inhibice, topologie, latence vstupů/výstupů).

Model je cílen na fenomény na úrovni **interakce mezi neokortexem a subkortikálními strukturami** – nikoli na vnitřní kortikální zpracování. Konkrétně jde o:

1. **Rozdíl mezi vědomým a nevědomým jednáním** – souhra pyramidové a extrapyramidové dráhy, přebírání řízení, potlačování automatických reakcí.
    
2. **Vznik inspirace, múzy, intuice** – jak se nevědomé výstupy (z amygdaly, hipokampu, mozečku) dostávají do neokortexu a stávají se podkladem pro vědomé myšlenky.
    
3. **Konflikt mezi afektivní a kognitivní reakcí** – soutěž mezi extrapyramidovým a pyramidovým systémem o společný efektor.
    

Pro tyto fenomény **není třeba rozlišovat interní kortikální hierarchii** – stačí modelovat neokortex jako celek, který přijímá vstupy, integruje je a vysílá výstupy. Vnitřní kortikální specializace (např. zraková vs. motorická kůra) je pro tyto fenomény **irelevantní**, protože fenomény samy operují na úrovni celého neokortexu.

---

## 1. Šedá a bílá hmota – definice pro model

**Šedá hmota** je v modelu definována jako **výpočetní uzel** – místo, kde probíhá integrace signálů, rozhodování a plasticita. Jsou v ní obsažena těla neuronů, dendrity a synapse. Z hlediska modelu je nositelem **stavu** a **vnitřní dynamiky**.

**Bílá hmota** je v modelu definována jako **komunikační infrastruktura** – myelinizované axony, které spojují uzly navzájem a s periferií. Pro účely modelu nemá vlastní výpočetní kapacitu ve smyslu integrace signálů; její funkční role je omezována na **přenos** s definovanými **latencemi** (zpožděními), které jsou určeny délkou a myelinizací příslušných svazků. Tyto latence jsou v modelu explicitními parametry, neboť časování je pro kognici kritické (synchronizace, binding).

_Poznámka:_ Model záměrně zanedbává difúzní neurotransmisi (volume transmission) a roli extracelulárního prostoru – tyto jevy jsou na zvolené úrovni granularity nahrazeny modulačními vstupy, které vstupují do generátorů jako parametry.

---

## 2. Generátor – definice a zdůvodnění

**Generátor** je v modelu definován jako **anatomicky svébytná populace neuronů v šedé hmotě**, která splňuje pět kritérií:

1. **Definované vstupy** – aferentace z jiných generátorů a/nebo ze senzorických rozhraní.
    
2. **Definované výstupy** – eferentace do jiných generátorů a/nebo do efektorových drah.
    
3. **Vlastní vnitřní dynamika** – šíření aktivace po preferovaných trajektoriích daných vnitřní konektivitou.
    
4. **Vlastní plasticita** – přepisování parametrů na základě zkušenosti.
    
5. **Neprůhlednost (opacity)** – výstup generátoru není plně predikovatelný z jeho vstupů bez znalosti jeho vnitřního stavu.
    

Generátory jsou analogické **nikoli strukturou, ale funkcí v rámci modelu**. Všechny jsou definovány jako **iniciátoři výstupů** – tj. zdroje signálů, které vstupují do efektorových drah nebo do jiných generátorů. Jejich analogie spočívá v tom, že:

- Každý z nich **iniciuje** své výstupy na základě svých vstupů a vnitřního stavu.
    
- Každý z nich má **vlastní parametry** (rychlost plasticity, typický vzor aktivace, latence vstupů/výstupů, poměr excitace/inhibice).
    
- Každý z nich je **neprůhledný** – ostatní generátory vidí pouze jeho výstup, nikoli jeho vnitřní dynamiku.
    

**Model pracuje se sedmi generátory.** Tento počet není dán funkcí, ale **anatomickou svébytností**:

|Generátor|Zdůvodnění zařazení|
|---|---|
|**Neokortex**|Jednotný embryologický původ, společná šestivrstevná architektura, společné výstupní kanály. Vnitřní specializace (senzorické, motorické, asociační oblasti) je zachycena jako odlišné trajektorie aktivace v rámci téhož generátoru.|
|**Bazální ganglia**|Anatomicky ucelený komplex subkortikálních jader se společnou vstupní strukturou (striatum) a výstupní strukturou (pallidum). Vnitřní organizace (přímá/nepřímá dráha) je v modelu parametrizována jako poměr excitace/inhibice a rychlost gatingu.|
|**Mozeček**|Samostatný anatomický celek s vlastní korovou architekturou a hlubokými jádry. Jeho výpočetní principy (např. časování, predikce) jsou v modelu parametrizovány (rychlost plasticity, typ vstupů).|
|**Amygdala**|Anatomicky ucelený komplex jader v temporálním laloku. Vnitřní diferenciace (bazolaterální vs. centromediální jádra) je v modelu zachycena jako rozdíl v parametrech (rychlost plasticity, typ výstupů).|
|**Hypotalamus**|Anatomicky vymezený soubor diencefalických jader se společnou výstupní funkcí (autonomní a neuroendokrinní regulace).|
|**Hipokampus**|Hipokampální formace (vlastní hipokampus – CA1–CA3, gyrus dentatus, subiculum) je modelována jako jeden generátor. Entorinální kůra – ačkoli je funkčním vstupem/výstupem – je z modelového hlediska **součástí propojovací infrastruktury** mezi neokortexem a hipokampem, nikoli součástí generátoru. Tím se model vyhýbá anatomickému stírání mezi archikortexem a mezokortexem.|
|**Retikulární formace**|Ačkoli je anatomicky difúzní, vykazuje jednotné funkční charakteristiky (regulace bdělosti, svalového tonu) a difúzní projekce do všech ostatních generátorů. V modelu je parametrizována jako zdroj modulačních vstupů.|

**Thalamus není generátor.** Je modelován jako **přepojovací a modulační uzel** (relé a gate), jehož výstup je silně závislý na kortikální a subkortikální modulaci (zejména retikulárního jádra thalamu – TRN). Ačkoli TRN vykazuje vlastní dynamiku, je v modelu zahrnuta pod parametry vstupů do neokortexu (gain control, selektivní pozornost). Thalamus tak v modelu **není nositelem vlastního stavu** – jeho funkce je redukována na přenos s modulovatelným ziskem. Dynamika thalamu (např. spánková vřeténka, rytmogeneze) je v modelu zachycena jako **změna parametrů vstupů do neokortexu** – neokortex vnímá thalamus jako proměnný zdroj vzruchů, jehož parametry (frekvence, amplituda, synchronizace) se mění v závislosti na stavu systému (bdělost, spánek, pozornost).

---

## 3. Vstupy do systému

Model rozlišuje dvě třídy vstupů:

**Podle původu:**

- **Interoceptivní** – signály z vnitřního prostředí (homeostatické parametry, viscerální stavy, propriocepce, vestibulární informace). Kortikální reprezentace je distribuována – zahrnuje insulární kůru, přední cingulární kůru (ACC), orbitofrontální kůru a somatosenzorickou kůru. Pro účely modelu je tato distribuce nahrazena **agregovaným interoceptivním vstupem** do neokortexu s rozlišením modality.
    
- **Exteroceptivní** – signály z vnějšího světa prostřednictvím smyslových orgánů (zrak, sluch, hmat, chuť, čich, teplota, bolest).
    

**Podle charakteru signálu:**

- **Vzruchové (driving)** – rychlé, přenášejí obsah (glutamát, GABA). Mění okamžitý výstup generátoru.
    
- **Modulační (neuromodulační)** – pomalé, přenášejí nastavení (dopamin, noradrenalin, serotonin, acetylcholin). Mění parametry generátoru (práh, plasticita, poměr signál/šum).
    

---

## 4. Výstupy ze systému

Model pracuje se dvěma efektorovými kanály:

### 4.1 Somatomotorický systém

Ovládá příčně pruhované svalstvo. Inervace probíhá přes motoneurony v míše a hlavových jádrech. Pro účely modelu rozlišujeme **dvě sestupné dráhy**, které se liší **zdrojem iniciace** a **časovou charakteristikou**:

||**Pyramidová**|**Extrapyramidová**|
|---|---|---|
|**Zdroj iniciace**|Neokortex|Podkorové generátory (mozeček, bazální ganglia, amygdala, retikulární formace)|
|**Cesta**|Přímá (neokortex → motoneuron)|Nepřímá (přes mozkový kmen)|
|**Latence**|Delší|Kratší|
|**Typ pohybu**|Vědomé, deliberativní, naučené, jemné|Nevědomé, automatické, afektivní, posturální, plynulé|
|**Příklad**|Dobrovolný úsměv, psaní, artikulace|Spontánní smích, úlek, mimika, tón hlasu|

**Oba systémy konvergují na společném motoneuronu** v míše (resp. v motorických jádrech hlavových nervů), kde dochází k integraci a soutěži signálů. Model tento souboj zachycuje jako parametrický konflikt – neokortex může extrapyramidový příkaz potlačit (zesílením vlastního pyramidového příkazu), ale nemůže ho zrušit, neboť běží na pozadí.

**Toto dělení je v modelu vztaženo ke zdroji iniciace, nikoli k anatomické dráze.** Moderní neurověda zná překryvy a interakce mezi oběma systémy; pro účely modelu však toto dělení slouží k rozlišení dvou odlišných zdrojů iniciace a dvou odlišných časových charakteristik.

### 4.2 Visceromotorický (autonomní) systém

Ovládá hladké svalstvo, srdeční sval a žlázy. Hlavním supraspinálním centrem je hypotalamus, modulován amygdalou a retikulární formací. V modelu je autonomní výstup reprezentován jako samostatný kanál s parametry (rychlost, intenzita, trvání).

---

## 5. Emoce a afektivní stavy

Model **důrazně odmítá představu**, že by emoce disponovaly vlastním, specializovaným výstupním kanálem směrem do vnějšího světa.

Emoce, motivace a afektivní stavy nejsou "spouštěče", které by samy o sobě produkovaly behaviorální efekt. Jsou to **emergenční fenomény** vznikající v sítích generátorů na základě konvergence interoceptivních a exteroceptivních signálů. Tento přístup je v souladu s teorií konstruované emoce (Barrett, 2017a, 2017b; Barrett & Bliss-Moreau, 2009) a s teorií somatických markerů (Damasio, 1994).

Jejich **manifestace navenek** se proto vždy realizuje výhradně jako modulace dvou fyziologických kanálů:

- **Visceromotorická složka emoce** – autonomní koreláty (zrychlený tep, pocení, zrudnutí, třes, změny dechového rytmu). Tyto projevy jsou primárně výstupem prediktivního udržování homeostázy.
    
- **Somatomotorická složka emoce** – výrazové a akční projevy. Zde model rozlišuje dvě sub-složky:
    
    - **Afektivní (extrapyramidová)** – spontánní, mimovolní projevy (úsměv jako reakce na vtip, smích, pláč, úlek, výraz strachu). Tyto jsou spouštěny afektivními generátory (amygdala, retikulární formace) a realizovány extrapyramidovou cestou. Jsou plynulé, přirozené a svalově koordinované.
        
    - **Kognitivní (pyramidová)** – volní, záměrné projevy (dobrovolný úsměv, vědomé dosmání, potlačení smíchu). Tyto jsou řízeny neokortexem a realizovány pyramidovou cestou. Jsou méně plynulé, mohou působit uměle a často vykazují mikro-záškuby či neplynulé přechody.
        

**Shrnutí:** Emoce nemají vlastní výstupní kanál. Jejich projevy navenek jsou vždy realizovány prostřednictvím dvou existujících kanálů – somatomotorického (pyramidového nebo extrapyramidového) a visceromotorického (autonomního).

---

## 6. Komunikace mezi generátory – tři principy

Komunikace mezi generátory je v modelu založena na třech principech:

1. **Vzruchová komunikace** – přímý přenos signálu mezi generátory prostřednictvím axonových svazků. Mění okamžitou aktivitu cílového generátoru.
    
2. **Modulační komunikace** – difúzní přenos nastavení prostřednictvím neuromodulátorů. Mění parametry cílového generátoru.
    
3. **Eferentní kopie (efference copy, corollary discharge)** – v modelu je tento princip **omezen na specifické okruhy, kde je biologicky doložen**:
    
    - Z neokortexu do mozečku a bazálních ganglií (kortiko-ponto-cerebelární a kortiko-striatální kolaterály).
        
    - Z mozečku do neokortexu (přes thalamus).
        
    - Z motorického systému do senzorických oblastí (pro predikci senzorických důsledků).
        
    
    Model **netvrdí**, že každý generátor distribuuje eferentní kopie do všech ostatních. Tento princip je v modelu **parametrizován** – každé spojení má definováno, zda přenáší eferentní kopii, a s jakou latencí.
    

---

## 7. Ukázkový příklad: Přechod mezi afektivní a kognitivní somatomotorikou

Uvažujme situaci, kdy jedinec zareaguje smíchem na humornou situaci. Tento příklad ilustruje mechanismy popsané v kapitolách 4 a 5.

### Fáze 1: První vlna (extrapyramidová)

- Amygdala vyhodnotí situaci jako příjemnou a spustí automatický motorický program pro smích.
    
- Signál putuje extrapyramidovou drahou: amygdala → retikulární formace → mícha → svaly.
    
- Dochází k mimovolní kontrakci bránice, mimických svalů a hlasivek.
    
- Projev je plynulý, přirozený, afektivní – typický "opravdový" smích.
    
- **Latence:** krátká (řádově desítky ms).
    
- **Zdroj iniciace:** amygdala (podkorový generátor).
    

### Fáze 2: Detekce neokortexem

- Neokortex detekuje, že běží motorický program, a to prostřednictvím:
    
    - **Eferentní kopie** z retikulární formace do neokortexu.
        
    - **Zpětnovazební propriocepce** ze svalů.
        
- Spouští se kognitivní hodnocení: _"Směju se už několik vteřin, začíná to být trapné – ztlumit / ukončit."_
    
- Neokortex si začíná přivlastňovat probíhající výstup: _"Já se směju."_ – vzniká iluze vědomého řízení.
    

### Fáze 3: Druhá vlna (pyramidová)

- Motorická kůra (neokortex) přebírá řízení téhož svalového aparátu.
    
- Signál putuje pyramidovou drahou: neokortex → mícha → svaly.
    
- Neokortex se snaží prodloužit nebo usměrnit smích, aby působil přirozeně.
    
- **Latence:** delší (řádově stovky ms).
    
- **Zdroj iniciace:** neokortex.
    

### Fáze 4: Výsledek

- Protože pyramidová dráha není optimalizována pro jemnou afektivní mimiku (je stavěna pro účelné, volní pohyby), výsledek působí **uměle, s mikro-záškuby a neplynulými přechody**.
    
- Extrapyramidový příkaz stále běží na pozadí (v amygdale, mozečku) – neokortex ho potlačil na výstupu, ale nezrušil.
    
- Když vědomá kontrola povolí, extrapyramidový příkaz se může vrátit – např. záchvat smíchu, který "přijde znovu".
    

**Klíčový závěr:** V obou fázích (afektivní i kognitivní) se používá **tentýž svalový aparát**. Nejde o dva různé výstupní kanály, ale o jeden kanál (somatomotorika), který je aktivován různými generátory (amygdala vs. neokortex) a dvěma různými sestupnými drahami (extrapyramidová vs. pyramidová).

---

## 8. Shrnutí – co model definuje a co zanedbává

|Definuje|Zanedbává (metodologicky)|
|---|---|
|7 generátorů jako uzly s parametry|Vnitřní heterogenitu generátorů (nahrazeno parametry)|
|Bílou hmotu jako komunikační infrastrukturu s latencemi|Difúzní neurotransmisi, roli extracelulárního prostoru|
|Vzruchové a modulační vstupy|Molekulární mechanismy plasticity|
|Dva efektorové kanály (somatomotorický, visceromotorický)|Detailní dělení motorických drah (překryvy pyramidové/extrapyramidové)|
|Eferentní kopii na specifických okruzích|Globální distribuci eferentních kopií (není biologicky doložena)|
|Thalamus jako přepojovací uzel s modulovatelným ziskem|Vlastní dynamiku TRN (nahrazena parametry vstupů)|
|Emoce jako emergenční fenomény bez vlastního výstupu|Detailní fenomenologii afektivních stavů|

---

## 9. Predikce modelu

Model generuje následující netriviální predikce, které plynou přímo z jeho architektury:

|Predikce|Mechanismus v modelu|Testovatelnost|
|---|---|---|
|Afektivní reakce má kratší latenci než kognitivní hodnocení|Extrapyramidová dráha (kratší latence) vs. pyramidová (delší latence)|EEG, reakční časy|
|Potlačená automatická reakce běží na pozadí a vrací se při oslabení kontroly|Soutěž dvou drah na motoneuronu; pyramidový výstup může extrapyramidový přebít, nikoli zrušit|EMG, behaviorální experimenty|
|Vědomý úsměv je méně plynulý než spontánní|Pyramidová dráha optimalizována pro účelné pohyby, nikoli pro afektivní mimiku|Analýza pohybů obličeje (např. FACS)|

---

## 10. Použité zdroje

- Barrett, L. F. (2017a). _How Emotions Are Made: The Secret Life of the Brain_. Houghton Mifflin Harcourt.
    
- Barrett, L. F. (2017b). The theory of constructed emotion: An active inference account of interoception and categorization. _Social Cognitive and Affective Neuroscience_, 12(1), 1–23.
    
- Barrett, L. F., & Bliss-Moreau, E. (2009). Affect as a psychological primitive. _Advances in Experimental Social Psychology_, 41, 167–218.
    
- Brodmann, K. (1909). _Vergleichende Lokalisationslehre der Grosshirnrinde_. Leipzig: Barth.
    
- Carpenter, M. B., & Sutin, J. (1983). _Human Neuroanatomy_ (8th ed.). Williams & Wilkins.
    
- Damasio, A. R. (1994). _Descartes' Error: Emotion, Reason, and the Human Brain_. Putnam.
    
- Kandel, E. R., Schwartz, J. H., Jessell, T. M., Siegelbaum, S. A., & Hudspeth, A. J. (2013). _Principles of Neural Science_ (5th ed.). McGraw-Hill.
    
- Mai, J. K., Majtanik, M., & Paxinos, G. (2015). _Atlas of the Human Brain_ (4th ed.). Academic Press.
    
- Nieuwenhuys, R., Voogd, J., & van Huijzen, C. (2008). _The Human Central Nervous System_ (4th ed.). Springer.

# Model generátoru: Membrána a pole

## Návaznost na biologicko-anatomický model

Tento text rozšiřuje model sedmi generátorů o popis vnitřní dynamiky šedé kůry mozkové. Zatímco biologicko-anatomický model definuje architekturu systému (sedm generátorů, vstupy, výstupy, komunikační kanály), tento text odpovídá na otázku: **co se děje uvnitř každého generátoru?**

Všechny generátory jsou tvořeny šedou hmotou – populacemi neuronů s excitačními a inhibičními synapsemi, plasticitou a vnitřní dynamikou. Liší se parametry, nikoli principem. Proto zavádíme jednotný model generátoru, který je společný pro všech sedm instancí.

---

## Část 1: Biologická dynamika šedé kůry

### 1.1 Šedá a bílá hmota – funkční dělení

**Šedá hmota** je výpočetní substrát. Obsahuje těla neuronů, dendrity a synapse. Zde probíhá integrace signálů, rozhodování, ukládání paměti a tvorba predikcí. Je nositelem stavu a vnitřní dynamiky.

**Bílá hmota** je komunikační infrastruktura – myelinizované axony spojující oblasti šedé hmoty navzájem a s periferií. Nemá vlastní výpočetní kapacitu ve smyslu integrace signálů. Její funkční role je přenos s definovanými latencemi, které jsou určeny délkou a myelinizací příslušných svazků.

Pro účely tohoto textu se soustředíme výhradně na dynamiku šedé hmoty. Bílá hmota je relevantní jako nositel propojení mezi generátory – to je však popsáno v biologicko-anatomickém modelu.

### 1.2 Neuronové pole

Šedá hmota tvoří fyzický substrát pro **neuronové pole** – dynamický systém, kde každý neuron ovlivňuje ostatní skrze excitační a inhibiční synapse.

Základní vlastnosti pole:

- **Excitace** – neuron vystřelí a excituje neurony, se kterými je propojen.
    
- **Inhibice** – interneuron vystřelí a potlačí aktivitu okolních neuronů.
    
- **Integrace** – každý neuron sčítá excitační a inhibiční vstupy za určitý časový úsek.
    
- **Práh** – když integrovaný signál překročí práh, neuron vystřelí (akční potenciál).
    
- **Plasticita** – váhy synapsí se mění podle toho, jak často a v jakém sledu neurony společně vystřelují (Hebbovo pravidlo, STDP).
    
- **Reverberace** – signál krouží v uzavřených okruzích, dokud nevyhasne nebo není potlačen inhibicí.
    

### 1.3 Krajina atraktorů

Neuronové pole lze popsat jako fázový prostor – krajinu.

- **Údolí** jsou snadno dosažitelné stavy (pravděpodobné konfigurace aktivity).
    
- **Vrcholy** jsou těžko dosažitelné stavy (nepravděpodobné konfigurace).
    
- **Atraktor** je údolí – jakmile se signál dostane na jeho svah, systém se sveze k jeho dnu.
    

Když do krajiny vstoupí signál, systém konverguje k nejbližšímu atraktoru. To je mechanismus rozhodování, vybavování i percepce – signál je interpretován podle existujících atraktorů.

#### Vznik stabilních oblastí

Ze začátku (novorozenec, začátečník) je krajina plochá – žádné výrazné atraktory, signál bloudí, systém zkouší všechno.

Když systém opakovaně zpracovává podobné signály a dostává potvrzení (predikce sedí, odměna přichází), posilují se synaptické váhy mezi neurony, které vystřelovaly současně. Tím se v krajině vytváří prohlubně – atraktory.

Čím častěji je určitá dráha použita, tím hlubší je údolí, tím snazší je do něj spadnout, tím pravděpodobnější je, že příští podobný signál skončí ve stejném údolí.

**To je paměť.** Není to uložený soubor. Je to změna pravděpodobnosti, že se určitá skupina neuronů znovu excituje ve stejném sledu. Paměť je změna krajiny atraktorů.

#### Zapomínání

Krajina není zabetonovaná. Nepoužívané atraktory se zanášejí – váhy slábnou (LTD – long-term depression), údolí se vyrovnává. Používané atraktory se prohlubují (LTP – long-term potentiation).

Zapomínání je systémová nutnost. Kdyby všechny dráhy zůstaly navždy posílené, krajina by zkameněla a systém by se nemohl učit nic nového.

#### Traumatické přepsání krajiny

Když přijde extrémně silný signál (trauma), nastane kaskáda predikčních chyb tak velká, že:

- Staré atraktory se rozbijí (dráhy vedoucí k pocitu bezpečí vedou do prázdna).
    
- Vytvoří se nové, extrémně hluboké atraktory (hypervigilance, strachové dráhy).
    
- Krajina se přetvoří během krátké doby.
    

To je mechanismus krátkodobé i dlouhodobé změny osobnosti – staré projevy zmizí, nové se stanou dominantními. V modelu sedmi generátorů se na tomto procesu podílí zejména amygdala (rychlé strachové podmiňování), hipokampus (epizodický záznam traumatu) a neokortex (konsolidace traumatických vzorců).

### 1.4 Průchod signálu

Signál je základní jednotka interakce systému se světem a mezi generátory navzájem. Bez signálů systém nefunguje – nemá co zpracovávat, nemá z čeho se učit.

#### Vstup signálu do generátoru

Signál přichází z:

- **Vnějšího světa** přes smyslové dráhy a thalamus (exterocepce).
    
- **Těla** přes interoceptivní dráhy (propriocepce, viscerální stavy, homeostatické signály).
    
- **Jiných generátorů** přes bílou hmotu (vzruchová komunikace) nebo přes difúzní modulační systémy (modulační komunikace).
    

Tyto vstupy jsou definovány v biologicko-anatomickém modelu. Zde se soustředíme na to, co se děje po vstupu signálu do generátoru.

#### Kontinuální transformace

Signál není transformován "na vstupu" a pak zpracován. Transformace a zpracování je **jeden proces**, který probíhá po celou dobu průchodu signálu neuronovou sítí generátoru.

Každý neuron, kterým signál prochází:

1. Přijímá vstup z předchozích neuronů (excitační i inhibiční).
    
2. Integruje tyto vstupy v čase.
    
3. Pokud integrovaný signál překročí práh, vystřelí.
    
4. Jeho synapse se mění (plasticita) – váhy se posilují nebo oslabují.
    
5. Vysílá signál dál do dalších neuronů.
    

Každý krok je současně:

- **Transformací signálu** – signál je filtrován, zesilován, zeslabován, tvarován podle aktuálních vah.
    
- **Potenciální změnou sítě** – synapse se přepisují, atraktory se posilují nebo oslabují.
    

#### Operace během průchodu

Během průchodu polem probíhají tyto operace:

- **Integrace** – signál se skládá z mnoha zdrojů (různé vstupy, různé modality).
    
- **Predikce** – vyšší vrstvy (v rámci generátoru) posílají očekávání směrem dolů (top-down signál).
    
- **Porovnání** – predikce se porovnává s přicházejícím signálem (bottom-up).
    
- **Predikční chyba** – rozdíl mezi predikcí a realitou. Pokud je chyba nulová, signál se dál nešíří. Pokud je velká, chyba putuje dál a spouští přepisování vah.
    
- **Reverberace** – signál krouží v uzavřených okruzích (myšlení, pracovní paměť, vybavování).
    
- **Rozhodování** – soutěž atraktorů. Vítězná populace potlačí ostatní prostřednictvím laterální inhibice.
    
- **Výstup** – signál opouští generátor a putuje do jiných generátorů nebo do efektorových drah (pyramidová, extrapyramidová – viz biologicko-anatomický model).
    

#### Zpětná vazba

Výstup generátoru způsobí změnu – buď ve světě (pohyb, řeč), nebo v těle (autonomní reakce), nebo v jiném generátoru. Tato změna je zachycena jako nový signál a vstupuje zpět do systému.

Tím se uzavírá smyčka: **signál → transformace → výstup → změna → nový signál**.

Tato smyčka je základem učení i adaptace. Každý průchod signálu mění krajinu atraktorů, a tím mění i to, jak bude příští signál transformován.

### 1.5 Paměť jako rekonstrukce

Paměť není sklad. Když si vybavujeme, systém nepřehrává uložený soubor. Místo toho spustí stejné predikční mechanismy, ale bez vnějšího vstupu. Vyšší oblasti generátoru posílají predikce dolů a nižší oblasti je zpětně potvrzují. Vzniká uzavřená smyčka – reverberace.

Paměť je běžící výpočet, ne zmrazený soubor.

#### Proč paměť slábne a sílí

- **Slábne**, když nejsou atraktory používány – jiné dráhy je přerůstají, váhy se oslabují (LTD).
    
- **Sílí pro jednu věc**, když je dráha opakovaně používána – prohlubuje se, stačí částečný podnět k excitaci. Expert vidí víc, protože jeho atraktory jsou hlubší a užší.
    

#### Řešení katastrofického zapomínání

Čistě hebbovský model naráží na problém katastrofického zapomínání – když se síť učí nové vzorce, přepisuje staré váhy a staré atraktory se rozbijí. Biologické mozky tento problém řeší několika mechanismy:

1. **Komplementární systémy učení** – hipokampus se učí rychle (epizodicky), neokortex pomalu (konsolidace). Rychlé učení nepřepisuje neokortex přímo, ale ukládá se v hipokampu a do neokortexu se konsoliduje postupně během spánku. Tento mechanismus je v modelu sedmi generátorů zachycen interakcí mezi hipokampem a neokortexem.
    
2. **Ochranná inhibice** – silné, konsolidované atraktory jsou chráněny před přepsáním inhibičními mechanismy (např. perineuronální sítě). To je parametr pole – míra ochrany existujících atraktorů.
    
3. **Oddělené fáze učení a konsolidace** – během dne probíhá ukládání (posilování drah), během spánku probíhá konsolidace (přehrávání, integrace do existující sítě bez přepsání). To je zachyceno v modelu jako změna parametrů pole mezi bdělým a spánkovým režimem.
    

### 1.6 Kognitivní funkce jako provozní režimy

Kognitivní funkce nejsou samostatné moduly. Jsou to různá nastavení dynamiky téhož pole:

|Funkce|Nastavení pole|
|---|---|
|**Rychlost myšlení**|Nízký práh excitace, vysoká rychlost propagace|
|**Hloubka myšlení**|Dlouhá reverberace, vysoká integrace v čase|
|**Kreativita**|Nízká laterální inhibice, signál bloudí, zkouší nové kombinace|
|**Soustředění**|Vysoká laterální inhibice, signál drží úzkou stopu|
|**Vybavování**|Aktivace starých atraktorů bez vnějšího vstupu (reverberace)|
|**Učení**|Vysoká plasticita, přepisování vah, tvorba nových atraktorů|

Tyto režimy jdou často proti sobě. Když usilovně myslíme (silná frontální aktivita, vysoká inhibice), nemůžeme si rychle vybavovat – silné excitační vlny přehluší jemné signály z paměťových atraktorů. To je důvod, proč odpověď často přijde, až když přestaneme hledat.

---

## Část 2: Dva funkční bloky – Membrána a Pole

Na výše popsané biologické realitě definujeme dva funkční bloky. **Nejsou to oddělené anatomické struktury.** Jsou to dvě vrstvy popisu téže neuronové sítě. Každý generátor v modelu sedmi generátorů je popsán touto dvojicí.

### 2.1 Membrána (Kognitivní membrána)

Membrána odpovídá na otázku: **"Jak systém reaguje?"**

Je to souhrn stabilních oblastí, atraktorů, pravděpodobností excitací. Je to **stav** generátoru.

**Co membrána je:**

- Pravděpodobnost, že při daném vstupu se excituje určitá skupina neuronů.
    
- Souhrn naučených vzorů – ustálené dráhy, které definují typické reakce.
    
- Projev vlastností – to, co vidíme, měříme, pozorujeme na výstupu generátoru.
    
- Transformace signálu během průchodu – signál je tvarován existujícími atraktory.
    
- Osobnost generátoru – flegmatický, cholerický, rigidní, tvárný.
    

**Co membrána není:**

- Není vstupní brána do generátoru (vstupy definuje biologicko-anatomický model – thalamus, smyslové dráhy, projekce z jiných generátorů).
    
- Není samostatný anatomický blok – je to funkční vlastnost neuronové sítě.
    
- Nemá vlastní dynamiku změny – je to zmrazený stav, momentka.
    

### 2.2 Pole (Pole kognicí)

Pole odpovídá na otázku: **"Jak se systém mění?"**

Je to dynamika, proces, přepisování. Je to **proces** běžící v generátoru.

**Co pole je:**

- Plasticita – jak rychle se přepisují váhy synapsí.
    
- Způsoby, jak se síť propojuje – architektura, hustota spojů, dosah propojení.
    
- Kognitivní funkce – rychlost, hloubka, inhibice, reverberace, top-down/bottom-up poměr.
    
- Schopnost vytvářet nové atraktory a rozbíjet staré.
    
- Rychlost změny parametrů membrány.
    

**Co pole není:**

- Není výstupní modulátor (výstupy definuje biologicko-anatomický model – pyramidová a extrapyramidová dráha, projekce do jiných generátorů).
    
- Není samostatný anatomický blok – je to funkční vlastnost neuronové sítě.
    

### 2.3 Vztah mezi membránou a polem

**Pole definuje membránu.** Konfigurace pole (parametry plasticity, inhibice, reverberace) určuje, jaké atraktory existují, jak jsou hluboké, jak pravděpodobné jsou jednotlivé reakce.

**Membrána omezuje pole.** Existující atraktory určují, kudy signál poteče příště. Čím silnější atraktory, tím těžší je pro pole přepsat je na něco jiného. To je mechanismus setrvačnosti osobnosti.

**Pole přepisuje membránu.** Když polem prochází signál, mění váhy synapsí, a tím mění krajinu atraktorů. Každý průchod signálu zanechá stopu.

**Je to jeden systém, dvě vrstvy popisu:**

- Membrána = stav (momentka).
    
- Pole = proces (dynamika změny stavu).
    

### 2.4 Dynamika v čase

text

Čas T0 (klidový stav):
  Konfigurace pole = K0 (parametry plasticity, inhibice, reverberace...)
  Membrána = souhrn atraktorů daných konfigurací K0
Čas T1 (přichází signál S1):
  S1 vstupuje do generátoru (vstupy definovány biologicko-anatomickým modelem)
  Signál je transformován membránou (existujícími atraktory) → S1'
  S1' prochází polem (zpracování, predikce, reverberace, soutěž)
  Zpracovaný signál přepisuje konfiguraci pole: K0 → K1
  Tím se mění i membrána pro příští signál
Čas T2 (přichází signál S2):
  Membrána je nyní jiná (protože K1 ≠ K0)
  S2 je transformován jinak → S2'
  S2' přepisuje konfiguraci dál: K1 → K2
A tak dále...

**Každý signál projde membránou, která je výsledkem všech předchozích signálů. Každý signál změní pole, a tím změní membránu pro signály budoucí.**

---

## Část 3: Osobnost, emoce, vědomé a nevědomé

### 3.1 Osobnost jako statistický průměr atraktorů

Když řekneme, že někdo je flegmatik, neříkáme, že jeho neurony zpracovávají všechno stejně. Říkáme, že jeho krajina atraktorů je statisticky vychýlená určitým směrem.

- **Flegmatik** – široká, mělká údolí. Reakce pomalé, energie se šetří, výstupy tlumené.
    
- **Cholerik** – ostré, hluboké jámy. Reakce bleskové, silné, impulzivní.
    
- **Neurotik** – hypercitlivé atraktory na hrozbu. Malý podnět spustí silnou reakci.
    

Tyto krajiny nejsou fixní. Jsou to jen hustotní mapy toho, jak často která dráha vyhrála v minulosti. Když flegmatik dostane podnět, který nezapadá do žádného z jeho mělkých údolí (např. ohrožení života), systém vytvoří novou dráhu – a ta může být cholerická.

Osobnost je **modální hodnota** – nejčastější odpověď, ne jediná možná.

V modelu sedmi generátorů má každý generátor svou vlastní "osobnost" – své typické atraktory a parametry pole. Celková osobnost systému je výsledkem interakce všech sedmi generátorů.

### 3.2 Emoce

Model důrazně odmítá představu, že by emoce disponovaly vlastním, specializovaným výstupním kanálem. Tento princip je převzat z biologicko-anatomického modelu a zde je rozšířen o vnitřní dynamiku generátorů.

Emoce jsou **emergenční fenomény** vznikající v sítích generátorů na základě konvergence interoceptivních a exteroceptivních signálů. V tomto modelu popisujeme, jak se emoce projevují uvnitř generátoru:

- Emoce není "konfigurace pole" – je to **globální přepnutí parametrů** napříč více generátory současně.
    
- Neokortex (a tedy jeho pole) se na emocích podílí, ale negeneruje je sám. Amygdala, hypotalamus a retikulární formace jsou generátory, které emoce spouštějí a modulují.
    
- Membrána a pole popisují, jak neokortex emoce **zpracovává a moduluje**, nikoli jak je vytváří.
    

**Transformační složka emocí** – jak emoce změní parametry pole a tím i membránu:

|Emoce|Plasticita|Rychlost|Hloubka|Inhibice|Top-down poměr|
|---|---|---|---|---|---|
|**Strach**|Zvýšená (rychlé učení hrozeb)|Vysoká|Nízká (jednej!)|Vysoká (tunel na hrozbu)|Vysoký (očekávám nebezpečí)|
|**Vztek**|Snížená (fixace na cíl)|Vysoká|Nízká (jednej!)|Vysoká (tunel na cíl)|Vysoký (vím, kdo za to může)|
|**Radost**|Střední|Střední|Nízká (užívej!)|Nízká (otevřenost)|Nízký (jsem otevřený)|
|**Smutek**|Zvýšená (přehodnocování)|Nízká|Vysoká (přehodnocuji)|Nízká (bloudění)|Vysoký (vše je ztraceno)|

**Dynamická složka emocí** – jak rychle emoce nastoupí a jak dlouho trvají – závisí na parametrech pole:

- **Rychlost nástupu** – jak rychle se parametry přepnou. Závisí na plasticitě a síle spouštěče.
    
- **Doba trvání** – jak dlouho emoční konfigurace drží. Závisí na hloubce reverberace a schopnosti pole přepsat se zpět.
    
- **Intenzita** – jak silně jsou parametry přepsány. Závisí na síle paměťových atraktorů spojených s emocí.
    

Projevy emocí navenek jsou vždy realizovány prostřednictvím dvou existujících kanálů – somatomotorického (pyramidového nebo extrapyramidového) a visceromotorického (autonomního). To je detailně popsáno v biologicko-anatomickém modelu.

### 3.3 Vědomé a nevědomé výstupy

Biologicko-anatomický model definuje dva efektorové kanály s odlišnými zdroji iniciace:

- **Pyramidová dráha** – iniciace v neokortexu. Delší latence. Vědomé, deliberativní, volní pohyby.
    
- **Extrapyramidová dráha** – iniciace v subkortikálních generátorech (amygdala, mozeček, bazální ganglia, retikulární formace). Kratší latence. Nevědomé, automatické, afektivní pohyby.
    

V kontextu membrány a pole to znamená:

- Membrána a pole jsou uvnitř neokortexu – podílejí se tedy přímo na **pyramidových (vědomých) výstupech**.
    
- Extrapyramidové výstupy jdou mimo neokortex – jsou generovány jinými generátory s vlastními membránami a poli.
    
- Neokortex může extrapyramidový výstup **potlačit** (zesílením vlastního pyramidového příkazu na společném motoneuronu), ale nemůže ho **zrušit** – extrapyramidový příkaz běží na pozadí.
    

To vysvětluje fenomény jako:

- Spontánní smích, který se pokoušíme potlačit (pyramidový výstup přebíjí extrapyramidový, ale extrapyramidový stále běží).
    
- Mikro-výrazy – krátké průniky extrapyramidových signálů přes pyramidovou inhibici.
    
- Návrat automatické reakce při oslabení vědomé kontroly (únava, překvapení).
    

---

## Část 4: Nasazení modelu na generátory

### 4.1 Jeden model, sedm instancí

Všechny generátory v modelu sedmi generátorů jsou tvořeny šedou hmotou. Všechny mají:

- Excitační a inhibiční neurony.
    
- Synaptickou plasticitu.
    
- Atraktory (stabilní konfigurace).
    
- Vstupy a výstupy (definované v biologicko-anatomickém modelu).
    
- Vnitřní dynamiku (reverberace, soutěž populací, integrace signálu).
    

Liší se v **parametrech pole**, nikoli v principu. Každý generátor je instancí téhož modelu (membrána + pole) s jiným výchozím nastavením parametrů.

### 4.2 Parametry sedmi generátorů

|Generátor|Plasticita|Rychlost|Hloubka|Inhibice|Top-down|Atraktory|Role v systému|
|---|---|---|---|---|---|---|---|
|**Neokortex**|Střední|Střední|Vysoká|Vysoká|Vysoký|Velmi vysoká|Vědomé myšlení, predikce, integrace|
|**Bazální ganglia**|Nízká|Vysoká|Nízká|Vysoká|Nízký|Střední|Selekce akcí, návyky|
|**Mozeček**|Vysoká|Velmi vysoká|Nízká|Nízká|Nízký|Střední|Časování, predikce, jemné ladění|
|**Amygdala**|Velmi vysoká|Velmi vysoká|Nízká|Nízká|Vysoký|Nízká|Rychlé emoční podmiňování|
|**Hypotalamus**|Nízká|Nízká|Nízká|Nízká|Vysoký|Velmi nízká|Homeostáza, setpointy|
|**Hipokampus**|Velmi vysoká|Vysoká|Střední|Nízká|Nízký|Vysoká|Epizodická paměť, rychlé učení|
|**Retikulární formace**|Velmi nízká|Nízká|Nízká|Nízká|Nízký|Velmi nízká|Bdělost, tonus, modulace|

Každý generátor má stejnou strukturu (membrána + pole), ale jiné výchozí parametry. Tím vzniká sedm různých "osobností" generátorů, které společně tvoří komplexní chování systému.

### 4.3 Dva režimy modelu: 1G a 7G

Architektura umožňuje dva režimy podle požadované úrovně detailu:

#### Model 1G (Jeden generátor, dva výstupy)

Celý mozek modelujeme jako **jeden generátor** s parametry pole a membrány. Vstupy jsou smyslové a interoceptivní. Výstupy jsou pyramidový a extrapyramidový.

**Výhody:**

- Extrémně jednoduchý – jeden generátor, jedna sada parametrů.
    
- Zachycuje základní dynamiku: vědomé vs. nevědomé, konflikt drah.
    
- Rychle ověřitelný – jde simulovat na malém výpočetním výkonu.
    
- Vhodný pro první prototyp a ověření principu.
    

**Omezení:**

- Nerozlišuje zdroje nevědomých výstupů (amygdala vs. mozeček vs. bazální ganglia).
    
- Nedokáže modelovat komplexní interakce mezi generátory (např. inspirace z mozečku, konsolidace hipokampem).
    
- Osobnost je jen jedna sada parametrů – hrubý odhad.
    

**Použití:** Když potřebujeme rychle ověřit princip. Když modelujeme jednoduché chování (reakce na podnět, konflikt automatické a volní reakce). Když učíme model základním fenoménům.

#### Model 7G (Sedm generátorů, dva výstupy)

Každý generátor je samostatná instance membrána/pole s vlastními parametry. Generátory komunikují přes bílou hmotu (definované kanály s latencemi). Výstupy konvergují na společných efektorech (pyramidová a extrapyramidová dráha).

**Výhody:**

- Zachycuje komplexní dynamiku (inspirace z mozečku do neokortexu, strachová reakce amygdaly, konsolidace paměti hipokampem).
    
- Umožňuje modelovat konflikty mezi generátory.
    
- Věrohodnější – odpovídá známé anatomii.
    

**Omezení:**

- Výpočetně náročnější – sedm generátorů, každý s vlastní dynamikou.
    
- Více parametrů k ladění.
    
- Složitější na implementaci a validaci.
    

**Použití:** Když potřebujeme modelovat komplexní fenomény (emoce, trauma, intuice, konsolidace paměti, konflikt mezi generátory).

#### Vztah mezi modely

Model 1G je **speciálním případem** modelu 7G – stav, kdy všechny generátory mají stejné parametry a nulové latence mezi sebou. Je to limitní zjednodušení, které umožňuje rychlé prototypování.

Model 7G je **plnou verzí** – rozlišuje generátory a jejich interakce. Umožňuje zachytit bohatost biologické reality.

Oba používají **stejný základní princip**: generátor = membrána + pole.