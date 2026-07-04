# Systém interakcí člověk-stroj

Jedná se o systémovou architekturu interakcí. Vnitřní logika bloků na úrovni systému je záměrně abstrahována, stejně tak povaha obou výstupů interakcí a jedné akce. Definování logiky a výstupů je modelová aplikace na systém.

## Definice

1. **Bloky a životní cyklus systému:**

Systém je tvořen bloky tří typů  
Iniciační blok – [IB]
Centrální blok – [CB]
Akční blok – [AB]

Bloky existují nezávisle na sobě.  
Systém vzniká, když mezi bloky probíhá interakce, nebo akce.  
Systém zaniká, když mezi bloky neprobíhá žádná interakce ani akce.  
Bloky přetrvávají i bez interakcí a akcí mezi nimi.

2. **Interakce:**

Každá jednotlivá interakce je právě jednou sekvenční výměnou mezi dvěma bloky.  
Probíhá výhradně mezi [IB]–[CB] a [CB]–[AB].  
Interakce na opačných stranách [CB] mohou probíhat současně.

3. **Akce:**

Jde o vazbu mezi [IB]>[CB], která končí výstupem do [CB].

## Základní principy systému

1. Interakce začíná iniciací a končí výstupem ve stejném bloku, který interakci zahájil.
2. [IB] iniciuje interakci [IB]–[CB].
3. Iniciací interakce [IB]–[CB] může vzniknout akce [IB]>[CB], která nutí [CB] k iniciaci interakce [CB]-[AB].
4. Výstup do [IB] mění parametry [IB].

## Popis systému

Systém je dynamický útvar tvořený bloky tří typů. Tyto bloky existují nezávisle na sobě. Systém vzniká teprve tehdy, když mezi nimi probíhá interakce nebo akce, tedy propojením bloků do činného celku. Jakmile všechny interakce a akce skončí, systém jako činný celek zaniká. Bloky samotné přetrvávají i mimo systém a uchovávají svůj stav pro příští interakce.

[IB] je iniciátorem všech interakcí, nepřímo i interakcí na straně [CB]-[AB], které technicky iniciuje [CB]. Je tedy jediným řídícím prvkem systému. [IB] rozhoduje o vzniku a zániku systému, a rozhoduje o způsobu, jakým systém operuje.

[CB] je středem systému, který je účastníkem všech systémových interakcí. Existence systému se od něj přímo odvíjí, tedy systém bez [CB] nemůže existovat. V závislosti na tom, které interakce s [CB] právě probíhají, mohou být [IB] a [AB] součástí systému oba současně, nebo jen jeden z nich.

[AB] je aktorem systému, který na pokyn [CB] vykoná svou akci a vrací mu výstup.

Každá interakce musí začínat iniciací a skončit výstupem v bloku, který iniciaci zahájil. Jde o právě jednu výměnu, tedy blok, který interakci inicioval získává výstup interakce a tím interakce končí. [CB] tak může iniciovat interakci [CB]-[AB] ve chvíli, kdy posílá výstup do [IB]. O možnosti vnořených interakcí na jedné straně výměny [CB] systém záměrně nic nepředepisuje. Jde o aplikační schéma systému na model podle konkrétních vlastností bloků.

Systémově existují 2 výstupy jako ukončení interakcí [IB]-[CB] a [CB]-[AB]. O vzájemném propojení a vazbách těchto výstupů, nebo jejich typech systém záměrně nic nepředepisuje. Jde opět o aplikační schéma systému na model. Výstup z interakce [IB]-[CB] mění parametry [IB], tedy systémově jde o vlastnost tohoto výstupu.

Iniciace [IB]-[CB] může vyvolat akci, která představuje druhou cestu signálu. Akce je řídící vazba mezi [IB]>[CB], jejíž výstup končí v [CB] a nutí [CB] k iniciaci interakce [CB]–[AB]. Obě cesty vznikají současně z jediné iniciace [IB].

## Vlastnosti systému

Systém se dá definovat pomocí 3 vlastností:

1. **Centralitou [CB]** – existence systému je odvozena na základě interakcí s [CB].
2. **Řízením [IB]** – existenci systému a systémové operace řídí [IB].
3. **Sekvenčností výstupů** – výstupy jsou sekvenční na základě ukončených interakcí.

## Rozšíření systému

Systém je v základní konfiguraci pro popis interakcí mezi člověkem a strojem. Může se nacházet i ve zcela jiných konfiguracích. Uvádím 3 další možné interakce pro inspiraci.

- [IB]-[CB]-[IB] - interakce člověk-člověk, nebo člověk-zvíře
- [AB]-[CB]-[AB] - interakce strojů
- [IB]-[CB]-[IB]/[IB]/[IB] - interakce člověk-skupina, nebo člověk-sociální tlak
