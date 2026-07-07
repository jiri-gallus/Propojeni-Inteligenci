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