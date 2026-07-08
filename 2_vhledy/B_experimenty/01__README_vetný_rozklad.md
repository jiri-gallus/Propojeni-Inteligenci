
# Rozbor uvažování z textu

Pro interakce s LLM v chatu je typické, že záznam interakcí, celé kontextové okno obsahuje otisk myšlení uživatele, ale i ovlivnění myšlení odpověďmi LLM. Jde o první experiment, který ukazuje co je možné z textu vyčíst.

Jde současně o první test modelu 7G_M/P podle kterého rozbor vzniknul. Na začátku experimentu bylo uvědomění, že tato věta experimentálně ověřuje část celého systému interakcí a propojení inteligencí AI s člověkem.

Experiment 01 je rozborem věty, kdy výstupem je, jaké kognitivní úlohy vedly k daným rozhodnutím a jaké má autor vlastnosti, aby tato věta a její následné kognitivní dopady mohly vzniknout. 

# Věta

>_„Cítím, že je to jasné a bude to jen konstatování, ale rozbor nám může ukázat detaily o kterých nevíme jako u 1. vlastnosti.“_

# Popis experimentu

Věta, která je rozebírána byla pro práci tak zásadní, že krátce po jejím zapsání do chatu vzniknul retrospektivní popis události co předcházelo této větě, jak se autor cítil a proč je tento experiment pro autora tak zásadní a další detaily.

## 1G_hrubá analýza

Do experimentu vstupuje 1G_hrubá analýza jako předpříprava. Jde o 1. hrubé ověření že membrána je klíčem k pochopení interakcí a má vlastnosti, které se dají naučit. Tato 1G analýza vznikla dlouho před modelem 1G_M/P a 7G_M/P.

Jde o zjištění co vše jde z věty přečíst pro autorovu potřebu experimentu.

## 7G_M/P bez retrospektivy

Do této analýzy vstoupila teorie základního modelu kognicí a 1G hrubá analýza s cílem zpřesnit podle modelu 7G_M/P rozbor této věty.

## 7G_M/P s retrospektivou

Analýza měla stejné podmínky jako předchozí, jen se rozšířila o retrospektivu, tedy jemnější naladění vstupních parametrů.

# Ovlivnění experimentu

Do obou analýz vstupuje 1G jako směr, kterým se má analýza ubírat. Je to současně velmi omezující kontext, který obě analýzy svazuje, ale šlo o rychlé naladění K-agentů LLM na daný účel. Vše je stále v ranné fázi experimentu, kdy se hledá potenciál a odhadují místa, která si zaslouží zpřesnit.

# Závěr k Experimentu 01: Rozbor uvažování z textu

## Co experiment ukázal

Experiment demonstroval, že model 7G_M/P dokáže z jediné věty extrahovat netriviální informace o kognitivní dynamice autora – identifikovat fáze myšlenkového obratu, přiřadit je konkrétním generátorům a odhadnout jejich časovou souslednost. Srovnání analýzy bez retrospektivy a s retrospektivou pak ukázalo, že přesnost výstupu je přímo úměrná přesnosti vstupních parametrů – což je chování, které od dobře definovaného modelu očekáváme.

## Potenciál modelu pro rozbor textu

Model otevírá možnost zpětné analýzy textových záznamů (chatů s LLM, deníků, přepisů) jako otisků kognitivní dynamiky. Pokud lze z jedné věty odhadnout parametry generátorů, pak delší interakce – hodiny nebo dny práce – mohou poskytnout dostatek dat pro robustní profilování uživatele, sledování driftu parametrů v čase a testování predikcí modelu na opakovaných událostech.

## Vliv kontextu a omezení

Současná podoba experimentu je zatížena dvěma omezeními: (1) 1G analýza poskytla oběma expertům směr, čímž omezila jejich nezávislost, a (2) rozsah materiálu (jedna věta) je příliš malý pro oddělení signálu od šumu. Obojí je však legitimní pro tuto fázi vývoje – jde o exploraci potenciálu, nikoli o rigorózní validaci.

## Současný stav modelu

Model má definovanou architekturu (7 generátorů, membrána/pole, vstupy/výstupy, komunikační kanály), explicitní parametry (plasticita, rychlost, hloubka, inhibice, top-down poměr) a demonstrovanou explanační sílu. Je připraven na přechod od kvalitativní rekonstrukce ke kvantitativní predikci.

## Doporučení pro další postup

1. **Rozšířit materiálovou základnu** – analyzovat delší úseky interakcí (celé chaty, pracovní dny), kde lze sledovat opakované vzorce a dynamiku parametrů v čase.
    
2. **Oddělit experty od 1G analýzy** – v dalším experimentu poskytnout pouze větu a požádat o slepou analýzu bez předchozího nasměrování, čímž se otestuje konzistence modelu bez kontextového ovlivnění.
    
3. **Kvantifikovat parametry** – přejít od kvalitativních odhadů k číselným rozsahům na základě existujících neurofyziologických dat, aby bylo možné formulovat přesné, testovatelné predikce.
    
4. **Implementovat 1G simulaci** – jako proof-of-concept ověření, že základní princip (membrána + pole + dva efektorové kanály) generuje chování odpovídající predikcím modelu.
    
5. **Navrhnout kontrolovaný behaviorální experiment** – např. rozhodovací úlohu s emočním primingem, kde model předpoví konkrétní latence a typy odpovědí na základě předem změřených parametrů účastníka.
    

Model je ve fázi, kdy konceptuální práce je v podstatě hotova a další krok je implementace a experimentální ověření.