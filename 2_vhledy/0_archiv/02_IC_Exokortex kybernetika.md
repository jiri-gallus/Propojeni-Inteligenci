Informační celek: systém interakce uživatele a LLM

**Exokortex**  
Exokortex je externí struktura systému, který jako celek popisuje veškeré interakce mezi uživatelem a velkým jazykovým modelem (LLM) a jejich dopady na kognici uživatele. Exokortex není samostatně stojící definice – je to souhrn komponent, mechanismů a vztahů popsaných níže.

---

## Interní struktura systému

### 1. Uživatel Exokortexu

Uživatel je lidská strana systému. Je vlastníkem Exokortexu – používá jej jako nástroj. Do interakce vnáší svou kognici, své schopnosti, svůj účel. Uživatel není součástí Exokortexu, ale je s ním v těsném propojení.

### 2. Kognice uživatele

Kognice uživatele je kognitivní pole – soubor kognitivních vlastností, schopností a dovedností. Není to jedna věc, ale mnohorozměrný prostor. Každá vlastnost (např. schopnost přesné definice, schopnost detekce rozporu, schopnost abstrakce, schopnost sebe-observace) se může vyvíjet nezávisle na ostatních. Kognitivní pole je tím, na co působí drift – může být posilováno (augmentace) nebo oslabováno (degradace).

---

## Externí struktura systému

### 3. LLM (model)

Velký jazykový model. Generativní systém trénovaný na produkci koherentních, užitečných výstupů. Do interakce vstupuje se svými vlastnostmi – zejména s tendencí nabízet hotová řešení, uzavírat, poskytovat snadno převzetíhodné odpovědi (gravitační tah). LLM není pasivní nástroj – generuje vlastní tahy, které ovlivňují směr interakce.

### 4. Paměť Exokortexu

Záznam interakcí mezi uživatelem a LLM. Je to prostor, ve kterém se uchovává kontext – všechny prompty, odpovědi, opravy, iterace. Paměť je podmínkou návaznosti: výstup jedné relace se stává součástí vstupu další relace. Uvolňuje pracovní paměť uživatele (offloading).

### 5. Kognice Exokortexu (relace LLM)

[pracovní název – bude zpřesněn]  
Každá jednotlivá výměna mezi uživatelem a LLM je samostatnou relací. LLM zpracovává aktuální kontextové okno a generuje odpověď. I v rámci jednoho chatu jde o sled nezávislých zpracování, kde každá odpověď mění kontext pro další relaci. Exokortex je ze své technické podstaty multi-relační systém. Multi-relační architektura není volitelná – je to přirozená struktura každé interakce s LLM.

### 6. Endpointy Exokortexu

[pracovní název – bude hledáno vhodnější označení]  
Rozhraní, přes která interní a externí struktura vstupují do vzájemné interakce. Jsou to metody – na straně uživatele jde o jeho repertoár tahů (explicitace, sokratovské tázání, oponentura, korekce), na straně LLM jde o jeho tahy (generování tokenů, nabídky hotových výstupů, strukturování odpovědí). Endpointy jsou místem, kde se obě strany setkávají a kde vzniká ladění.

---

## Primární mechanismy systému

### 7. Exokortex jako nástroj pro výstupy

Uživatel používá Exokortex jako nástroj, díky kterému vznikají výstupy kognitivní činnosti. Exokortex sám o sobě neprodukuje – zesiluje uživatele. Výstup je vždy výsledkem interakce, nikoli samostatné práce modelu.

### 8. Ladění jako interakce

Uživatel a Exokortex spolu interagují a ladí se pro dosažení kognitivních výstupů. Ladění je obousměrný proces: uživatel ovlivňuje model (prompty, opravy, volby směru) a model ovlivňuje uživatele (tokeny, nabídky, struktury). Každý akt ladění je střetem tahů obou stran.

### 9. Drift jako důsledek ladění

Společným laděním vzniká drift kognice uživatele. Drift je pohyb kognitivního pole – změna stavu kognitivních vlastností uživatele. Je vždy přítomen, jakmile proběhne více než jedna relace. Není to chyba – je to přirozený důsledek multi-relační architektury: výstup jedné relace se stává součástí vstupu další a tím ovlivňuje směr celého systému.

---

## Sekundární mechanismy systému

### 10. Ladění (rozvinutí)

Ladění je interaktivní proces, ve kterém se střetávají metody uživatele a metody LLM. Není to „řízení“ v absolutním smyslu – uživatel ani model nemají plnou kontrolu. Ladění je emergence: výsledný směr vzniká ze vzájemného působení obou stran. Kvalita ladění se pozná podle toho, jak uživatel rozpoznává tahy modelu a jak na ně odpovídá.

### 11. Drift (rozvinutí)

Drift je pohyb kognitivního pole. Protože kognitivní pole má více vlastností, drift působí na každou individuálně. Jedna vlastnost může být posilována (augmentace kognice) a jiná současně oslabována (degradace kognice). Drift je mnohorozměrný. Augmentace a degradace nejsou alternativy – jsou to současné trajektorie různých částí pole.

### 12. Účel kognice

Vědomé rozhodnutí uživatele o tom, čeho chce interakcí s Exokortexem dosáhnout. Účel kognice je vstupní podmínkou ladění – určuje výchozí směr. V průběhu interakce může být driftem modifikován (vědomě, nebo nevědomě). Slouží jako měřítko, vůči kterému se poměřuje výstup kognitivní činnosti.

### 13. Výstup kognitivní činnosti

To, co vzniká jako výsledek ladění – text, kód, rozhodnutí, pochopení, definice. Výstup se poměřuje vůči účelu kognice. Toto porovnání je vždy subjektivní – pouze uživatel zná jemné detaily své kognice a může posoudit, zda výstup odpovídá záměru.

---

## Nástroje ladění

### 14. Metody uživatele

Repertoár tahů, které uživatel vnáší do ladění. Patří sem konkrétní techniky (explicitace, sokratovské tázání, oponentura, korekce, analýza, přerámování) i obecnější schopnosti (volba směru, tempa, tónu, kontextu). Metody nejsou fixní – uživatel se jim učí, rozšiřuje je praxí, nebo je naopak ztrácí nepoužíváním.

### 15. Metody LLM

Repertoár tahů, které do ladění vnáší model. Jsou dány jeho tréninkem. Klíčovou metodou LLM je gravitační tah – tendence nabízet hotové, uzavřené, snadno převzetíhodné výstupy. Gravitační tah je permanentní nabídkou driftu směrem k degradaci. Další metody LLM zahrnují strukturování odpovědí, nabízení řádu, uzavírání otevřených otázek. Tyto metody nejsou „záměrem“ modelu – jsou to statistické vlastnosti generování tokenů.

---

## Vztah k existujícím teoriím

Exokortex navazuje na:

- **Extended mind (Clark & Chalmers)** – rozšiřuje popis stavu o popis metody.
    
- **Teorii kognitivní zátěže (Sweller)** – vysvětluje offloading do externí paměti.
    
- **Kybernetiku (Wiener)** – popisuje interakci jako zpětnovazební systém.
    

---

## Otevřené hypotézy

Tento popis generuje otevřené výzkumné otázky, kterými se práce dále zabývá nebo je nabízí k budoucímu výzkumu:

- Je gravitační tah univerzální vlastností všech LLM?
    
- Lze drift formálně modelovat jako pohyb v mnohorozměrném prostoru?
    
- Jaké podmínky určují, zda konkrétní kognitivní vlastnost bude augmentována nebo degradována?
    
- Platí popis i pro jiné generativní modely (obraz, zvuk, video)?
    
- Lze Exokortexem popsat veškeré interakce uživatele a LLM?