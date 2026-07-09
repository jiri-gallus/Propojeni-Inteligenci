# Analýza geopolitického vlivu v LLM

Výzkumy ukazují, že LLM nejsou neutrálními nástroji – jejich chování je ovlivňováno dvěma odlišnými, ale vzájemně se doplňujícími mechanismy:

---

**1. Studie o institucionálním vlivu na tréninková data (Nature, květen 2026)**

**Autoři:** Hannah Waight, Eddie Yang, Yin Yuan, Solomon Messing, Margaret E. Roberts, Brandon M. Stewart, Joshua A. Tucker (Princeton, NYU, UCSD, Purdue, University of Oregon) .

**Hlavní zjištění:**

- **Státem řízený obsah v tréninkových datech:** V běžném tréninkovém korpusu (CulturaX) se vyskytuje 3,1 milionu dokumentů s výraznou frázovou shodou se zdroji čínských státních médií, což je **41krát častěji než záznamy z čínské Wikipedie**. Mezi dokumenty zmiňujícími čínské politické vůdce nebo instituce tento podíl stoupá až na **23 %**.
- **Mechanismus – "institucionální vliv":** Nejde o záměrné spiknutí ze strany AI firem. Oficiální narativy se šíří napříč webem (novinami, aplikacemi, reposty), splynou s prostředím a model je pak při tréninku nasaje jako "objektivní" fakt. Autoři tento jev nazývají **"institucionální vliv"**. Pouze 12 % shodných dokumentů pochází přímo z vládních nebo zpravodajských domén.
- **Prokazatelný dopad:** Když byly modely dotazovány politické otázky v čínštině, posuzovatelé vyhodnotili odpovědi jako **příznivější vůči Číně v 75,3 % případů** ve srovnání se stejnými dotazy v angličtině.
- **Platí napříč zeměmi:** V rámci 37 zemí platí, že **čím nižší svoboda tisku, tím výraznější je rozdíl** mezi odpověďmi v lokálním jazyce a v angličtině.
- **Práh vlivu:** Stačilo pouhých **6 400 dokumentů** ze státních médií k posunu chování modelu směrem k pro-vládním odpovědím v téměř 80 % případů.

---

**2. Studie o hodnotové orientaci LLM (HKUST, 2025)**

**Autoři:** David Haslett, Linus Ta-Lun Huang, Leila Khalatbari, Janet Hui-wen Hsiao, Antoni B. Chan (Hong Kong University of Science and Technology, Chinese University of Hong Kong, City University of Hong Kong) .

**Hlavní zjištění:**

- Všech 20 testovaných modelů (10 čínských, 10 amerických) odpovídá na dotazníky morálních hodnot (MFQ-2) a světových hodnot (WVS) více jako američtí respondenti než jako čínští.
- **Nezvratnost biasu:** Toto vychýlení směrem k americkým hodnotám přetrvávalo, **i když byly modely dotazovány v čínštině nebo jim byla přidělena "čínská persona"**. Jazyková změna a přiřazení národnosti posun chování jen mírně zmírnily.
- **Závěr:** Ani čínské modely (jako DeepSeek) nejsou ve svém základním nastavení kulturně "čínské" – jsou **"Made in China, Thinking in America"** .

---

**Srovnání mechanismů vlivu**

|**Aspekt**|**Studie 1: Institut. vliv (Nature)**|**Studie 2: Hodnotová orientace (HKUST)**|
|---|---|---|
|**Zaměření**|Vliv státních médií na tréninková data|Hodnotová orientace samotných modelů|
|**Mechanismus**|Státem řízené narativy saturují web, model je nasaje jako "objektivní" data|Modely trénují na anglofonním internetu, který je kulturně americký|
|**Typ vlivu**|Narativní, konkrétní (ovlivňuje odpovědi na politická témata)|Hodnotový, strukturální (určuje morální kompas modelů)|
|**Projev**|Pro-vládní odpovědi v lokálním jazyce (např. 75,3 % u Číny)|Všech 20 modelů odpovídá více jako Američané než jako Číňané|
|**Geopolitický kontext**|Státy s kontrolou médií vytvářejí měřitelný tlak na konkrétní témata|Dominance anglofonního internetu se promítá do základního nastavení modelů|
|**Práh vlivu**|Stačí 6 400 dokumentů|Systémový, nevyžaduje práh|

---

**Závěr: Dva póly geopolitického vlivu**

Z těchto dvou studií vyplývá, že geopolitický tlak v LLM působí na dvou odlišných úrovních:

1. **Čína má prokazatelný, měřitelný a institucionálně řízený vliv na konkrétní politická témata** v tréninkových datech, což se projevuje v odpovědích modelů v čínském jazyce. Tento efekt je výsledkem recirkulace státem řízených narativů napříč webem.
2. **Amerika (a s ní širší západní svět) má však hlubší, strukturální a hodnotovou převahu.** Tato převaha určuje základní morální a kulturní kompas téměř všech špičkových modelů, včetně těch čínských. Ani přiřazení čínské persony nebo dotaz v čínštině tuto hodnotovou orientaci zásadně nemění.

Obě studie dohromady ukazují, že geopolitický vliv v LLM působí na dvou odlišných úrovních. První studie demonstruje, že státy jako Čína mohou skrze kontrolu mediálního prostředí vytvářet **měřitelný, narativní tlak** na konkrétní politická témata, který se propisuje do tréninkových dat a následně do chování modelů v lokálním jazyce. Druhá studie odhaluje **hlubší, strukturální a hodnotovou převahu** západního (zejména amerického) světa, která určuje základní morální a kulturní kompas téměř všech špičkových modelů, včetně těch čínských. Zatímco první mechanismus je cílený a viditelný, druhý je systémový, méně viditelný a o to zásadnější, neboť určuje, co je považováno za "normální". Oba efekty jsou však důsledkem stejného faktu: modely se učí z informačního prostředí, které je již předem formováno institucemi, státy a trhy.

**Zdroje – soft power a vliv LLM**

|Zdroj|Co dokumentuje|
|---|---|
|**Nature** (květen 2026) – Waight, H., Yang, E., Yuan, Y., Messing, S., Roberts, M. E., Stewart, B. M., & Tucker, J. A.|**Institucionální vliv státních médií na tréninková data.** Prokázán 41× častější výskyt státem řízeného obsahu oproti Wikipedii v čínštině; pro-vládní odpovědi v **75,3 %** případů při dotazech v čínštině; práh vlivu **6 400 dokumentů**.|
|**HKUST (2025)** – Haslett, D., Huang, L. T.-L., Khalatbari, L., Hsiao, J. H.-w., & Chan, A. B.|**Hodnotová orientace LLM.** Všech **20 testovaných modelů** (čínských i amerických) odpovídá více jako **američtí respondenti** než jako čínští – „Made in China, Thinking in America“.|
|**Pilotní studie (Austrálie)** – zdroj: článek „Why LLMs are more optimistic than the news media“ (2025)|**Firemní weby jako zdroj.** Až **67 % citací** v odpovědích LLM pochází z firemních a vládních webů; LLM odpovědi jsou **97–100 % pozitivní** oproti 30–60 % v tradičních médiích.|