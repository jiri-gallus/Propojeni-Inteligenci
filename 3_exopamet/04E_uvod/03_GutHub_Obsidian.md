Jaký textový editor použít pro markdovn, aby mi usnadnil formátování?

Pro markdown existuje **široká škála editorů** – od ultralehkých poznámkových bloků až po profesionální vývojová prostředí. Záleží na tom, co potřebuješ (psaní poznámek, článků, technické dokumentace, nebo knih).

Rozdělím to podle tvého **stylu práce**:

---

### 1. Pokud chceš "živý náhled" (WYSIWYG) – Nejvíc usnadní formátování

Píšeš jako ve Wordu a rovnou vidíš výsledek.

- **Typora** (nejoblíbenější) – Čistý, minimalistický. Přepínáš styly přes menu nebo klávesové zkratky. Není to klasický split-view, ale píšeš přímo ve "výsledku". (Placený, ale stojí za to.)
    
- **Zettlr** – Zdarma, open-source. Skvělý na dlouhé texty a poznámky. Má výborné vyhledávání a správu citací.
    
- **Notion / Coda** – Webové nástroje, které používají markdown jako zkratky (např. `/nadpis`). Ideální pro týmovou spolupráci.
    

---

### 2. Pokud chceš klasické "dvoupanelové" prostředí (kód vlevo / náhled vpravo)

To je nejpřehlednější pro kontrolu formátování.

- **Obsidian** – Zdarma pro osobní použití. Kromě náhledu umí propojovat poznámky (graf). Velmi oblíbený mezi pisateli.
    
- **Mark Text** – Zdarma, open-source, elegantní. Režim zdrojového kódu i náhledu.
    
- **Visual Studio Code** + rozšíření `Markdown All in One` – Pokud už ho používáš na programování, nemusíš instalovat nic nového. Náhled otevřeš přes `Ctrl+Shift+V`.
    

---

### 3. Pokud píšeš technickou dokumentaci (tabulky, matematika, diagramy)

Potřebuješ nadstandardní funkce.

- **Obsidian** (zvládá matematiku a Mermaid diagramy)
    
- **VS Code** s rozšířením `Markdown Preview Enhanced` – Umí grafy, UML, matematické vzorce (LaTeX), export do PDF/HTML.
    
- **RStudio** (pokud píšeš v R-markdownu)
    

---

### 4. Pokud chceš něco "jen na formátování" bez učení

- **Dillinger** – Online editor, stačí vložit text, on to přeformátuje a vyexportuje.
    
- **StackEdit** – Online, synchronizuje s Google Diskem / GitHubem.
    

---

### 5. Co se týče **usnadnění formátování** (klávesové zkratky)

Většina editorů podporuje:

- `Ctrl+B` = **tučně**
    
- `Ctrl+I` = _kurzíva_
    
- `Ctrl+K` = [odkaz](https://url/)
    
- `Ctrl+Shift+]` = nadpis (v Typora / Obsidianu)
    

---

### Můj osobní tip na začátek:

**Obsidian** – je zdarma, má náhled, zkratky, propojování a milion pluginů. Až ho zvládneš, přejdi na **Typora**, pokud ti vadí dvoupanelový režim.

---

**A nakonec – pokud píšeš markdown jen příležitostně (např. do komentářů na fóra), stačí ti i obyčejný poznámkový blok + tahák s formátováním. Na složité tabulky a seznamy ale doporučuji jeden z výše jmenovaných.**

Potřebuješ poradit s konkrétním úkolem (např. export do PDF, vkládání obrázků, matematika)?

Proč má obsidian interaktivní graf?

Skvělá otázka. Ten graf (oficiálně **"Graph View"**) není žádná zbytečná "vychytávka" – je to **jádro filozofie Obsidianu**.

Obsidian totiž není jen textový editor, ale **nástroj na budování "druhého mozku" (Zettelkasten)**. Ten graf tam je z těchto zásadních důvodů:

---

**1. Ukazuje souvislosti, které jsi neplánoval**  
Když jen píšeš do složek, vidíš lineární seznam souborů. Graf ti ale vizuálně ukáže, že tvoje poznámka o "motivaci" je propojená s poznámkou o "spánku" a ta zase s "cirkadiánními rytmy".  
Často tak objevíš **nové nápady a vztahy mezi tématy**, které by tě jinak nenapadly – prostě je uvidíš.

---

**2. Odhalí "osamělé" a "zapadlé" poznámky**  
V grafu si všimneš **ostrovů** (skupinek propojených poznámek) a **osamělých bodů** (poznámek bez jediného odkazu). To je okamžitá vizuální zpětná vazba: _"Tuhle poznámku jsi napsal před rokem a nikdy ses k ní nevrátil – možná je k ničemu, nebo naopak stojí za to ji propojit."_

---

**3. Umožňuje "procházet" myšlenky jako web**  
Místo abys klikal zpět a vpřed v historii, můžeš v grafu chytit myší uzel (poznámku) a přetáhnout ho. Otevřeš si centrální téma a sleduješ, kam tě "odkazy" zavedou – podobně jako bloudíš po internetu, ale jen ve svém vlastním know-how.

---

**4. Vizuální reprezentace rozsahu projektu**  
Když píšeš diplomku nebo knihu, graf ti na první pohled ukáže, jestli máš 50 izolovaných nápadů, nebo jeden velký propojený celek. Velké shluky = témata, která máš dobře zpracovaná.

---

**5. Není to jen "hezká hračka" – dá se s ním pracovat**  
Můžeš si graf **filtrovat**:

- Zobrazit jen poznámky s konkrétními tagy (#projekt, #osoba).
    
- Obarvit uzly podle složek (např. modře = pracovní, zeleně = osobní).
    
- Zapnout **"local graph"** (lokální graf) – ten ukazuje jen propojení _aktuálně otevřené_ poznámky, což je při psaní mnohem užitečnější než celý obří graf.
    

---

**A upřímně – psychologický efekt:**  
Když vidíš, jak se ti ten "pavučinový vesmír" rozrůstá, dodává to pocit, že na tom, co píšeš, záleží a že to dává smysl. Je to **motivace pokračovat**.

---

**Ale pozor – past na začátečníky:**  
Spousta lidí si Obsidian pořídí **kvůli tomu grafu**, pak do něj nahází 500 poznámek bez odkazů, graf vypadá jako "hvězdná obloha" (samé nespojené tečky) a jsou zklamaní.

**Správný přístup:** Graf je jen **vizualizace odkazů** – aby byl užitečný, musíš mezi poznámkami **dělat interní odkazy** (např. `[[název jiné poznámky]]`). Čím víc odkazů, tím smysluplnější graf.

Zettelkasten znám. Jak to funguje v obsidiánu? Propojuji to sám?

Perfektně, jestli Zettelkasten znáš, půjdeme rovnou na věc.

Odpověď na tvou otázku zní: **ANO, ty propojuješ naprosto vše sám.** Obsidian **žádné** propojení negeneruje automaticky (na rozdíl od např. Notion AI nebo logických databází).

Tady je přesný návod, jak Zettelkasten v Obsidianu funguje a jak ho ručně propojovat, včetně "tajných zbraní", které ti to usnadní:

---

**1. Hlavní nástroj: "Wikilinky" (dvojité hranaté závorky)**  
Propojení vytvoříš tak, že napíšeš `[[název jiné poznámky]]`.

- Obsidian ti při psaní automaticky nabízí existující názvy (autocomplete).
    
- Když napíšeš název poznámky, která **ještě neexistuje**, Obsidian ji vytvoří jako novou prázdnou stránku (to je geniální na zachycení nových nápadů – napíšeš `[[teorie motivace]]` a hned máš místo, kam to zařadit).
    

---

**2. Kde se ten Zettelkasten bere? (Struktura)**  
Nemusíš používat žádné složky (i když můžeš). Zettelkasten v Obsidianu je **čistě síť odkazů**, ne stromová struktura.

- **Hlavní poznámka (Map of Content - MoC):** Vytvoříš si např. poznámku `[[Psychologie]]` a do ní dáš odkazy na všechny dílčí pojmy (`[[motivace]]`, `[[kognitivní disonance]]`). Tohle je tvůj "rozcestník".
    
- **Trvalé poznámky (literature/permanent):** Každá obsahuje jednu myšlenku a na konci má sekci "Související", kde ručně vyjmenuješ další `[[odkazy]]`.
    

---

**3. Usnadnění propojování (aby tě to nebavilo)**  
Obsidian má 3 funkce, které ti pomáhají propojovat _rychleji_, ale pořád je to na tobě:

- **Backlinks (Zpětné odkazy):** Otevřeš poznámku o "spánku" a Obsidian ti v postranním panelu ukáže **všechny ostatní poznámky**, které na tuto stránku odkazují. Nemusíš tak složitě hledat, kam všude tvůj nápad patří.
    
- **Unlinked Mentions (Neodkázané zmínky):** **Tohle je zlatý důl.** Obsidian prohledá _všechny_ tvé poznámky a najde slova, která se přesně shodují s názvem tvé aktuální otevřené poznámky, ale zatím **nejsou** v `[[závorkách]]`. Stačí kliknout na tlačítko a on ti je tam automaticky vloží. Ušetří to hodiny ručního hledání.
    
- **Horké klávesy:** Nastav si zkratku `Ctrl+O` (otevřít poznámku) a `Ctrl+Shift+F` (vyhledat text). Když píšeš a vzpomeneš si na starou poznámku, rychle ji najdeš a vložíš odkaz.
    

---

**4. Jak to celé drží pohromadě (Zettelkasten logika v praxi)**

Místo složek a čísel (jako u Luhmanna) používáš v Obsidianu **jedinečné názvy** (např. `20260307_teorie_motivace`).

Když vytvoříš novou poznámku, postupuješ takto:

1. Napíšeš myšlenku.
    
2. Do zápatí napíšeš: **"Navazuje na:"** a dáš `[[starší_poznámka]]`.
    
3. Napíšeš: **"Rozpor s:"** a dáš `[[jiná_poznámka]]`.
    
4. Napíšeš: **"Definice:"** a dáš `[[zdrojová_literatura]]`.
    

---

**Stručné shrnutí:**  
Obsidian ti **dodá motyku a mapu** (graf, backlinks, vyhledávání), ale **kopat a spojovat musíš ty**. Nic se nepropojí automaticky podle klíčových slov – musíš vědomě říct _"tahle myšlenka souvisí s tamtou"_ a zapsat to pomocí `[[ ]]`.

Právě tohle **aktivní ruční propojování** je podle Zettelkastenu ten klíčový akt učení – nutí tě to přemýšlet nad obsahem, ne ho jen pasivně ukládat.

Máš už nějakou svou osvědčenou strukturu názvů (např. s datem, nebo pojmenováváš sémanticky), nebo s tím teprve začínáš? Můžu ti poradit, co se osvědčilo.

Potřebuji na úvot práci jen s markdown, Další funkce budu dělat později. Jak začít? Mám text v docx, ale chci ho formátovat v Markdown.

Rozumím. Půjdeš na to chytře – **jen čistý markdown**, žádné zásuvné moduly, žádné grafy, žádné propojování. Na úvodní práci to stačí a Obsidian v tomto režimu funguje jako **nadstandardní poznámkový blok**.

Tady je **krok za krokem**, jak převést tvůj `.docx` do čistého markdownu v Obsidianu (a pak se k tomu vrátit):

---

## 1. Založ si "prázdnou" vault (trezor)

- Otevři Obsidian → **Create new vault**
    
- Dej mu jméno např. `Prace` a ulož ho někam na disk.
    
- **Důležité:** Hned po otevření vypni všechny "chytré" funkce, které teď nepotřebuješ:
    
    - Nastavení → Core plugins → vypni **Backlinks**, **Graph view**, **Outgoing links** (nebo je nech, ale ignoruj je).
        
    - Vypni **Staré soubory** (Settings → Files & Links → Detect all file extensions = vypni).
        

Teď máš **čistý textový editor** bez rušivých prvků.

---

## 2. Převod `.docx` do `.md` (Markdown)

Obsidian **neumí otevřít docx** – musíš ho převést. Máš 3 možnosti:

|Možnost|Výhoda|Nevýhoda|
|---|---|---|
|**Copy-paste + ruční formátování**|Úplná kontrola|Pracné u delších textů|
|**Pandoc** (nejlepší)|Zachová nadpisy, tučnost, kurzívu|Vyžaduje instalaci (příkazová řádka)|
|**Online konvertor** (např. CloudConvert, Zamzar)|Rychlé, bez instalace|Nemusí zachovat diakritiku a složité tabulky|

**Doporučuju:**

1. Zkus **Pandoc** (pokud umíš pracovat s příkazovou řádkou):
    
    bash
    
    pandoc vstup.docx -o vystup.md
    
2. Nebo jednoduše: **zkopíruj text do Obsidianu** a formátuj ručně podle bodu 3.
    

---

## 3. Jak formátovat v čistém Markdownu (stačí tohle)

Pro úvodní práci ti bohatě postačí **základní syntaxe**:

|Prvek|Zápis v Markdownu|
|---|---|
|**Nadpis 1**|`# Název kapitoly`|
|**Nadpis 2**|`## Podkapitola`|
|**Nadpis 3**|`### Další úroveň`|
|**Tučný text**|`**tučně**`|
|_Kurzíva_|`*kurzíva*`|
|Seznam (odrážky)|`- položka`|
|Číslovaný seznam|`1. první`  <br>`2. druhá`|
|Odkaz|`[popis](url)`|
|Citace|`> Toto je citace`|
|Kód (uvnitř textu)|`` `proměnná` ``|
|Odrážka s odsazením|`- položka`  <br>`- odsazená` (mezery)|

**Tabulky** už jsou složitější – na začátek se jim vyhni, nebo si pomoz online generátorem (např. [Table Generator](https://www.tablesgenerator.com/markdown_tables)).

---

## 4. Kam to uložit v Obsidianu

- Stačí vytvořit v tvém vaultu nový soubor (klikni na **New File**).
    
- Pojmenuj ho např. `uvod_prace.md` (přípona `.md` je důležitá).
    
- Vlož převedený text a začni formátovat.
    
- Ukládej průběžně (`Ctrl+S`) – Obsidian ukládá automaticky, ale je to jistota.
    

---

## 5. Živý náhled (jak to bude vypadat)

V Obsidianu máš dva režimy:

- **Edit mode** (píšeš kód) – výchozí.
    
- **Reading mode** (ukáže výsledek) – klikni na ikonu knížky vpravo nahoře nebo zmáčkni `Ctrl+E` (přepínání).
    

Pro začátek pracuj v Edit mode a občas přepni do Reading mode pro kontrolu.

---

## 6. Co dělat, až budeš chtít pokračovat

Až zpracuješ úvod, můžeš:

- Rozdělit text do více souborů (např. `kapitola1.md`, `kapitola2.md`).
    
- Postupně přidávat propojení (`[[název jiné kapitoly]]`), až se k tomu dostaneš.
    
- Exportovat do PDF/HTML přes Obsidian (Export → PDF) nebo použít pandoc na zpětný převod do docx.
    

---

**Stručně:**

1. Založ prázdný vault.
    
2. Převeď docx → md (Pandoc nebo copy-paste).
    
3. Formátuj pomocí `#`, `**`, `*`, `-`, `>`.
    
4. Ulož jako `.md`.
    
5. Občas zkontroluj náhled (`Ctrl+E`).
    

Až to budeš mít, napiš, jestli máš problém s konkrétním prvkem (tabulky, obrázky, citace) – poradím.

Je to pro mne neintuitivní. Kde se ukládá, kde najdu nastavení? Je ten soubor jen v obsidiánu, nebo mohu propojivat soubory na disku?

Chápu, že přechod z Wordu do Obsidianu je na začátku **mimořádně neintuitivní**. Word je hotový "balík", zatímco Obsidian je jen "průzkumník souborů" s textovým editorem.

Rozklíčuju ti to úplně od podlahy:

---

### 1. Kde se to ukládá? (Nejdůležitější odpověď)

**Obsidian nemá žádnou vlastní databázi ani "cloud" (pokud si neplatíš Sync).**

- Všechny tvé soubory jsou **obyčejné `.md` (textové) soubory** uložené **někde na tvém disku**.
    
- Když vytvoříš "Vault" (trezor), Obsidian si jen **pamatuje cestu** k té složce. Např. `C:/Users/TvéJméno/Dokumenty/MojePrace/`
    
- **Můžeš otevřít Průzkumníka Windows (nebo Finder na Macu), jít do té složky a uvidíš tam všechny své `.md` soubory.** Můžeš je otevírat v Poznámkovém bloku, Wordu, nebo je posílat mailem.
    

---

### 2. Kde najdu nastavení?

- Vlevo dole je **ikona ozubeného kola** (⚙️) – klikni a otevře se Nastavení.
    
- **Důležité:** Nastavení se dělí na dvě části:
    
    - **Nastavení (Settings):** Platí pro celou aplikaci (vzhled, klávesové zkratky).
        
    - **Nastavení trezoru (Vault Settings):** Platí jen pro aktuální složku. Zde najdeš např. cestu k souborům.
        

---

### 3. Mohu propojovat soubory na disku? (Áno, a to je ta superschopnost!)

**Ano, a to je přesně ten důvod, proč je Obsidian tak oblíbený mezi programátory a pisateli.**

Protože jsou to jen textové soubory na disku, můžeš dělat dvě zásadní věci:

- **Propojení s jinými programy:** Můžeš otevřít stejný `.md` soubor **současně** v Obsidianu a např. ve VS Code (programátorském editoru). Když uložíš změny v jednom, druhý se automaticky aktualizuje.
    
- **Synchronizace přes cloud (Zdarma):** Stačí, když svůj Vault (složku) umístíš do **Google Disku**, **OneDrivu**, **Dropboxu** nebo **GitHubu**. Pak můžeš na stejném textu pracovat z PC, notebooku i mobilu (stačí na mobilu nainstalovat Obsidian a otevřít tu samou složku z cloudu).
    

---

### 4. Co dělat, když se mi to nelíbí a chci zpět do Wordu?

**Žádný problém.** Protože to jsou jen texty:

1. Otevři složku na disku.
    
2. Otevři svůj `.md` soubor v **Poznámkovém bloku**.
    
3. Zkopíruj celý text.
    
4. Vlož ho do nového dokumentu Wordu.
    
5. (Nepovinné) Můžeš si nechat formátování – Word umí otevřít `.md` soubory přímo (i když to občas hází chyby u tabulek).
    

---

### 5. Moje rada pro tebe, ať se v tom neztratíš:

1. Vytvoř si na ploše (nebo v Dokumentech) **novou prázdnou složku** s názvem např. `MARKDOWN`.
    
2. V Obsidianu klikni na **"Open folder as vault"** a vyber tuto složku.
    
3. Teď víš, že **všechno, co vytvoříš, leží přesně v téhle složce na ploše**. Můžeš si ji otevřít průzkumníkem a kontrolovat, jestli tam soubory přibývají.
    
4. Dej si dole v Obsidianu zobrazit **souborový panel** (ikona dvou obdélníků vlevo nahoře) – uvidíš tam přesně stejný seznam souborů, jako vidíš v Průzkumníkovi Windows.
    

---

**Proč je to tak "divné"?**  
Obsidian je postavený na principu _"důvěřuj svému souborovému systému"_. Není to aplikace, která ti schovává soubory do černé skříňky (jako Word nebo Notion). Jsou **tvoje** a ty s nimi můžeš dělat cokoliv – i když Obsidian zítra přestane existovat, ty texty máš pořád na disku.

Teď už víš, kde to fyzicky leží. Zkus si vytvořit nový soubor (`New file`), něco do něj napiš, ulož (automaticky) a pak otevři tu složku v Průzkumníkovi – uvidíš ho tam jako `název.md`. Je to jednodušší, než to na první pohled vypadá! 😉

Už jsem se zorientoval. Použil jsem složku Git repozitáře a vidím tam vše, tedy mám otevřený vault. Jak teď s Markdowny? Jak vidět náhleda text?

Super! Když už máš otevřený vault v Gitu, jsi ve správné pozici – všechny soubory máš pod kontrolou.

Teď k **náhledu a práci s Markdowny** v Obsidianu:

---

## 1. Přepínání mezi editem a náhledem

Obsidian má **dva režimy** pro každý soubor:

|Režim|Vzhled|Zkratka|
|---|---|---|
|**Edit mode** (zdrojový kód)|Vidíš surový markdown s `#`, `**`, `-`|`Ctrl+E` (přepíná)|
|**Reading mode** (náhled)|Vidíš **výsledek** – nadpisy, tučný text, seznamy|`Ctrl+E` (stejná zkratka)|

- Klikni na ikonku **knihy/knížky** v pravém horním rohu (u názvu souboru) – přepneš mezi režimy.
    
- Nebo použij **`Ctrl+E`** – to je nejrychlejší.
    

---

## 2. Jak zobrazit **vedle sebe** (Edit i náhled současně)

Pokud chceš mít **kód vlevo** a **výsledek vpravo** (jako v programu):

1. Otevři soubor.
    
2. Vpravo nahoře klikni na **ikonu tří teček** (`...`) → vyber **"Split right"** (rozdělit okno).
    
3. V novém okně otevři **ten samý soubor** (stačí ho najít v seznamu vlevo a kliknout na něj).
    
4. V jednom okně dej **Edit mode**, ve druhém **Reading mode**.
    

Teď píšeš vlevo a hned vidíš výsledek vpravo.

---

## 3. Jak vidět **všechny soubory** najednou

- Vlevo nahoře je ikona **dvou obdélníků** (File Explorer) – tam vidíš seznam všech `.md` souborů ve tvém vaultu.
    
- Kliknutím na soubor ho otevřeš.
    

Pokud nevidíš soubory:

- Stiskni `Ctrl+O` (otevře se vyhledávací pole) a začni psát název souboru – Obsidian ho najde.
    

---

## 4. Jak editovat Markdown (základní přehled)

**V Edit mode** píšeš přímo syntaxi:

|Chceš|Napiš|
|---|---|
|Nadpis 1|`# Název`|
|Nadpis 2|`## Název`|
|Nadpis 3|`### Název`|
|Tučné|`**tučné**`|
|Kurzíva|`*kurzíva*`|
|Seznam|`- položka`|
|Číslovaný seznam|`1. první`  <br>`2. druhá`|
|Citace|`> text`|
|Obrázek|`![popis](cesta/obrazek.png)`|
|Odkaz|`[text](url)`|
|Horizontální čára|`---`|

**Když přepneš do Reading mode**, uvidíš to hezky naformátované.

---

## 5. Užitečné zkratky (ušetří ti klikání)

|Akce|Zkratka|
|---|---|
|Přepnout Edit/Reading|`Ctrl+E`|
|Otevřít soubor (vyhledávání)|`Ctrl+O`|
|Rychlé uložení|`Ctrl+S` (automaticky, ale jistota)|
|Tučné|`Ctrl+B` (označí text a dá do `**`)|
|Kurzíva|`Ctrl+I`|
|Nadpis|označ text → `Ctrl+1` (až `Ctrl+6`)|

---

## 6. Co dělat, když nevidíš náhled obrázků?

- Obrázky fungují, jen pokud je máš **uložené ve vaultu** (ne na internetu).
    
- Napiš:
    
    text
    
    ![popis](slozka/obrazek.png)
    
- V Reading mode se obrázek zobrazí.
    

---

## 7. Export do PDF / HTML (až budeš chtít)

Až doděláš text:

- Otevři soubor v **Reading mode**.
    
- Klikni na tři tečky (`...`) → **Export to PDF**.
    
- Nebo použij pandoc z příkazové řádky (pokud ho máš nainstalovaný):
    
    bash
    
    pandoc soubor.md -o soubor.pdf
    

---

**Teď už stačí:** otevři svůj `.md` soubor, dej `Ctrl+E` a uvidíš náhled. Když chceš oba pohledy vedle sebe, rozděl si okno (ikona tří teček → Split right) a dej jedno na Edit, druhé na Reading.

Máš nějaký konkrétní prvek (tabulka, obrázek, citace), který ti v náhledu nefunguje? Napiš, hned to vyřešíme.

pokud mám trezor, vytvořilo mi to složku .obsidian a tím mi to zahltilo git. Je možné tuto složku odstranit, nebo je to nutná podmínka trezoru? Můžu pak nekomitnout jen obsidian složku?

Skvělá otázka, tohle trápí každého, kdo používá Obsidian s Gitem.

Odpověď zní: **Ano, složku `.obsidian` můžeš z Gitu úplně vynechat (a dokonce je to doporučený postup).**

Rozdělím to na dvě části:

---

### 1. Je `.obsidian` nutná pro chod trezoru?

**ANO, je nutná.** Obsidian si tam ukládá:

- Nastavení trezoru (které pluginy máš zapnuté, vzhled, klávesové zkratky).
    
- Poslední otevřené soubory, pozici okna atd.
    

**Bez této složky** ti Obsidian při otevření trezoru vytvoří novou s výchozím nastavením. Ale tvoje **textové `.md` soubory** zůstanou v pořádku – `.obsidian` neobsahuje žádný tvůj obsah, jen **preference**.

---

### 2. Můžu ji nekomitnout do Gitu?

**ANO, a to je správný postup.**

Přidej do svého repozitáře soubor **`.gitignore`** a napiš do něj:

text

.obsidian/

Pak udělej:

bash

git add .gitignore
git commit -m "Přidán .gitignore pro Obsidian"

Od této chvíle Git **bude ignorovat** celou složku `.obsidian` – nic se nebude commitovat ani nahrávat na GitHub.

---

### 3. Co když už jsem `.obsidian` omylem commitnul?

Žádný problém – odeber ji z Gitu, ale **nech ji na disku** (aby ti Obsidian fungoval):

bash

git rm -r --cached .obsidian
echo ".obsidian/" >> .gitignore
git add .gitignore
git commit -m "Odstranění .obsidian z Gitu"
git push

- `--cached` znamená "odeber z Gitu, ale smaž to **pouze** z indexu, ne z disku".
    
- Složka zůstane na tvém počítači, ale Git ji přestane sledovat.
    

---

### 4. Výhody ignorování `.obsidian`

- **Repozitář je čistý** – obsahuje jen tvé `.md` soubory.
    
- **Žádné konflikty** při práci s více lidmi (každý má jiné nastavení pluginu, jinou barevnou paletu).
    
- **Můžeš sdílet** repozitář s jinými lidmi a oni si nastaví Obsidian podle sebe.
    

---

### 5. Co když chci sdílet i nastavení? (např. pluginy)

Pokud chceš, aby všichni ve tvém týmu měli **stejné pluginy a vzhled**:

- Můžeš `.obsidian` komitnout, ale pak musíš řešit konflikty.
    
- Nebo lépe: použij **Obsidian Sync** (placený) a nastavení se synchronizuje automaticky.
    
- Pro tvoji úvodní práci **důrazně doporučuji ignorovat**.
    

---

### 6. Co když chci mít nastavení pod kontrolou, ale nezahlcovat Git?

Existuje kompromis – ignoruj **všechno** v `.obsidian` **kromě**:

- `.obsidian/app.json` (globální nastavení)
    
- `.obsidian/community-plugins.json` (seznam nainstalovaných pluginů)
    

Pak do `.gitignore` napiš:

text

.obsidian/*
!.obsidian/app.json
!.obsidian/community-plugins.json

Tím se do Gitu dostanou jen **konfigurační soubory**, ale ne dočasné soubory (workspace.json, cache apod.).

---

### Shrnutí pro tebe:

1. **Přidej `.obsidian/` do `.gitignore`**.
    
2. **Pokud už je commitnutá**, odeber ji příkazem výše.
    
3. **Složka zůstane na disku** a Obsidian bude fungovat normálně.
    
4. Git bude sledovat **pouze tvé `.md` soubory** – tedy to, co máš v repozitáři.
    

Tím budeš mít repozitář čistý a přehledný. Každý, kdo si ho naklonuje, si vytvoří vlastní `.obsidian` s výchozím nastavením.

Až budeš chtít, můžeme se podívat na **automatické commitování** (např. pomocí skriptu nebo Obsidian Git pluginu) – ale to až později, teď je důležité mít čistý Git.

Co znameá subor .gitignore a dát jej do repozotáře? Jakou má příponu? Do jaké složky? Nebo tohle mám udělat jako setup v hubu?

Skvělá otázka. Tohle je základ práce s Gitem, ale pro začátečníka úplně jasný není.

Rozložím ti to na úplné detaily, abys věděl **přesně**, co to je a kam to patří.

---

### 1. Co je soubor `.gitignore`?

Je to **obyčejný textový soubor**, který říká Gitu: _"Hele, tyhle soubory nebo složky ignoruj – neukazuj je, nestahuj je, nepropisuj je do historie."_

- Nemá žádný "obsah" kromě seznamu cest.
    
- Každý řádek je jedna položka (složka, soubor, nebo maska jako `*.log`).
    

---

### 2. Jakou má příponu?

**Nemá žádnou příponu.**

Jmenuje se přesně:

text

.gitignore

- **Tečka na začátku** je důležitá – označuje skrytý soubor.
    
- **Žádné** `.txt`, `.md` nebo něco podobného.
    

---

### 3. Do jaké složky ho dát?

**Do kořenové složky tvého Git repozitáře** – tedy tam, kde je zároveň složka `.git` (ta je skrytá).

Příklad:

text

C:/Users/TvéJméno/Dokumenty/MojePrace/   ← tohle je kořen repozitáře
│
├── .git/                (skrytá, tam má Git svoji databázi)
├── .gitignore           ← SEM ho vlož
├── uvod_prace.md
├── kapitola1.md
├── .obsidian/           (složka, kterou chceme ignorovat)
└── README.md

---

### 4. Jak ho vytvořit a vložit?

**Na Windows:**

1. Otevři Poznámkový blok.
    
2. Napiš tam:
    
    text
    
    .obsidian/
    
3. Klikni na **Soubor → Uložit jako**.
    
4. Do pole **Název souboru** napiš přesně:
    
    text
    
    ".gitignore"
    
    (s uvozovkami – Poznámkový blok je jinak přidá příponu `.txt`)
    
5. Jako **Typ souboru** vyber _Všechny soubory_.
    
6. Ulož ho do kořenové složky repozitáře (tam, kde máš `.md` soubory).
    

**Na Mac / Linux:**

- Otevři terminál v kořenu repozitáře a napiš:
    
    bash
    
    echo ".obsidian/" > .gitignore
    

---

### 5. Co do něj napsat?

Pro tvoje potřeby (ignorování `.obsidian` složky) stačí:

text

.obsidian/

Pokud chceš ignorovat i jiné věci (např. dočasné soubory operačního systému), přidej další řádky:

text

.obsidian/
.DS_Store
Thumbs.db
*.log

---

### 6. Tohle mám udělat jako setup na GitHubu, nebo lokálně?

**Lokálně.**

- `.gitignore` je soubor, který leží **v tvém lokálním repozitáři** (na tvém disku).
    
- Když ho vytvoříš, přidáš ho do Gitu a commitneš, pak se **nahraje na GitHub** spolu s ostatními soubory.
    
- Každý, kdo si tvůj repozitář naklonuje, bude mít stejný `.gitignore` a bude ignorovat stejné soubory.
    

**Postup:**

1. Vytvoř `.gitignore` lokálně (podle bodu 4).
    
2. Přidej ho do Gitu:
    
    bash
    
    git add .gitignore
    git commit -m "Přidán .gitignore"
    git push
    

---

### 7. Co se stane, když už `.obsidian` běží na GitHubu?

Pokud už jsi `.obsidian` commitnul a nahrál na GitHub:

- `.gitignore` zabrání **budoucím** změnám, ale **už existující** soubory zůstanou na GitHubu.
    
- Abys je odstranil z GitHubu, ale nechal je na disku, použij:
    
    bash
    
    git rm -r --cached .obsidian
    git commit -m "Odstranění .obsidian z Gitu"
    git push
    

---

### 8. Co když nechci řešit žádné příkazové řádky?

Můžeš použít **GitHub Desktop** (grafické rozhraní):

1. V repozitáři klikni na **Repository → Repository settings**.
    
2. V záložce **Ignored files** můžeš přidat `.obsidian/` do seznamu.
    
3. Aplikace vytvoří `.gitignore` automaticky.
    

---

### Shrnutí pro tebe:

|Co|Odpověď|
|---|---|
|**Název souboru**|`.gitignore` (s tečkou, bez přípony)|
|**Kam ho dát**|Do kořenové složky repozitáře (vedle `.md` souborů)|
|**Co do něj napsat**|`.obsidian/`|
|**Kdy to udělat**|Hned teď, než začneš commitovat|
|**Musíš ho nahrát na GitHub?**|Ano, aby ho měli i ostatní (ale je to text, takže nic nehrozí)|

**Praktický tip:** Pokud používáš GitHub Desktop, stačí kliknout pravým tlačítkem na `.obsidian` složku → **Ignore** a udělá to za tebe.

Pokud chceš, můžeme teď pokračovat tím, že si vytvoříš `.gitignore` a ověříš, že Git už `.obsidian` nevidí (příkaz `git status` ti ukáže jen `.md` soubory).

Připrav cele kontextové okno k archivaci paměti. Potřebuji rozdělit kontext na logické celky o tom, co jsme probírali, opatřit je názvem, krátkým popisem a citací, kterou úsek začíná. Postup: - Rozděl kontext podle tématu (nejdi do detailů, 2-20 paměťových částí, množství částí musí být vyvážené. Co jde spojit, spoj, co je jiné téma, nová část. Části musí být postupně navazovány na celé kontextové okno, nejde spojit části do jedné, když je rozdělena jiným tématem) - Indexuj část (01, 02, 03, ... 20) - Vymysli krátký název (max. 4 slova) - Vymysli krátký popis aby bylo jasno co která část obsahuje (max. 4 věty) - Vypiš přesnou citaci začátku textu (max. 10 slov) pro zpětnou dohledatelnost v textovém editoru (ctrl+f). - Musíš obsáhnout celé kontextové pole. 01 část je od citace 01 po citaci 02.

Na základě naší konverzace vytvářím kontextové okno pro archivaci paměti. Rozdělil jsem celý průběh do logicky navazujících celků.

---

## KONTEXTOVÉ OKNO – ARCHIVACE PAMĚTI

**Datum:** 2026-07-03 až 2026-07-09  
**Téma:** Práce s Markdown, Obsidian a Git

---

### 01 – Úvod do editorů Markdown

**Název:** Výběr Markdown editoru  
**Popis:** Probrali jsme širokou škálu editorů pro Markdown – od Typora přes Obsidian až po VS Code. Rozdělili jsme je podle stylu práce (WYSIWYG, dvoupanelové, technické, online). Doporučil jsem Obsidian jako zdarma dostupný nástroj pro začátek.  
**Citace začátku:** _"Pro markdown existuje široká škála editorů..."_

---

### 02 – Grafová vizualizace v Obsidianu

**Název:** Interaktivní graf a jeho smysl  
**Popis:** Vysvětlil jsem funkci Graph View v Obsidianu – nejde o vychytávku, ale o nástroj pro objevování souvislostí, odhalování osamělých poznámek a vizuální reprezentaci rozsahu projektu. Upozornil jsem na past začátečníků (nespojené poznámky) a důležitost interních odkazů.  
**Citace začátku:** _"Skvělá otázka. Ten graf (oficiálně 'Graph View')..."_

---

### 03 – Zettelkasten v praxi

**Název:** Ruční propojování poznámek  
**Popis:** Vysvětlil jsem, že propojování v Obsidianu je výhradně ruční pomocí `[[wikilinků]]`. Představil jsem koncept Map of Content (MoC), Backlinks (zpětné odkazy) a Unlinked Mentions (neodkázané zmínky) jako nástroje pro usnadnění práce. Zdůraznil jsem aktivní roli uživatele při budování sítě poznámek.  
**Citace začátku:** _"Perfektně, jestli Zettelkasten znáš, půjdeme rovnou na věc..."_

---

### 04 – Převod DOCX do Markdown

**Název:** První kroky s dokumentem  
**Popis:** Řešili jsme, jak převést existující `.docx` soubor do Markdown. Doporučil jsem Pandoc (nejlepší zachování formátování) nebo copy-paste s ručním formátováním. Představil jsem základní syntaxi Markdown (nadpisy, tučnost, seznamy, citace) a práci v Edit/Reading mode.  
**Citace začátku:** _"Rozumím. Půjdeš na to chytře – jen čistý markdown..."_

---

### 05 – Orientace v uživatelském rozhraní

**Název:** Umístění souborů a nastavení  
**Popis:** Vysvětlil jsem, že Obsidian ukládá soubory jako obyčejné `.md` textové soubory na disk (žádná vlastní databáze). Ukázal jsem, kde najít nastavení (ikona ozubeného kola), a potvrdil možnost propojovat soubory na disku (Google Disk, OneDrive, GitHub). Zdůraznil jsem, že jde o "průzkumník souborů s textovým editorem".  
**Citace začátku:** _"Chápu, že přechod z Wordu do Obsidianu je na začátku mimořádně neintuitivní..."_

---

### 06 – Práce s náhledem a editací

**Název:** Zobrazení a formátování textu  
**Popis:** Popsal jsem přepínání mezi Edit mode a Reading mode (`Ctrl+E`), možnost rozdělení okna pro současný náhled a editaci (Split right). Uvedl jsem základní klávesové zkratky pro formátování (`Ctrl+B`, `Ctrl+I`, `Ctrl+1-6`) a export do PDF.  
**Citace začátku:** _"Super! Když už máš otevřený vault v Gitu..."_

---

### 07 – .gitignore a správa Gitu

**Název:** Ignorování Obsidian složky  
**Popis:** Vysvětlil jsem, že složka `.obsidian` je nutná pro chod trezoru, ale nemusí být commitována do Gitu. Ukázal jsem, jak vytvořit soubor `.gitignore` (bez přípony, do kořene repozitáře), co do něj napsat (`.obsidian/`) a jak odstranit již commitnutou složku z Gitu (`git rm -r --cached`). Doporučil jsem ignorovat `.obsidian` pro čistý repozitář a prevenci konfliktů.  
**Citace začátku:** _"Skvělá otázka, tohle trápí každého, kdo používá Obsidian s Gitem..."_

---

### 08 – Praktická tvorba .gitignore

**Název:** Vytvoření a umístění souboru  
**Popis:** Podrobně jsem popsal, jak vytvořit soubor `.gitignore` v Poznámkovém bloku (s uvozovkami pro správný název), kam ho umístit (kořen repozitáře) a jak ho přidat do Gitu (`git add`, `commit`, `push`). Uvedl jsem i alternativu přes GitHub Desktop pro uživatele, kteří nechtějí používat příkazovou řádku.  
**Citace začátku:** _"Skvělá otázka. Tohle je základ práce s Gitem..."_

---

## SOUHRN

|Část|Název|Klíčové téma|
|---|---|---|
|01|Výběr Markdown editoru|Úvod do editorů|
|02|Interaktivní graf a jeho smysl|Graph View|
|03|Ruční propojování poznámek|Zettelkasten|
|04|První kroky s dokumentem|Převod DOCX→MD|
|05|Umístění souborů a nastavení|Souborový systém|
|06|Zobrazení a formátování textu|Edit/Reading mode|
|07|Ignorování Obsidian složky|.gitignore princip|
|08|Vytvoření a umístění souboru|Praktická tvorba .gitignore|

---

**Poznámka pro tebe:** Kontextové okno pokrývá celou naši konverzaci od prvního dotazu na Markdown editory až po poslední otázku o `.gitignore`. Jednotlivé části na sebe logicky navazují – od teorie (editory, graf) přes praxi (převod, formátování) až po správu verzí (Git, .gitignore).