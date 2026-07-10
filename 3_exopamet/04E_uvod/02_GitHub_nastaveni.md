Jak funguje GitHub, povolí G, další mechanismy. Co GitHub umožňuje.

Hledání zastaveno

Jak funguje GitHub, pooling, další mechanismy. Co GitHub umožňuje.

Přečteno 12 webových stránek

GitHub je v podstatě sociální síť pro vývojáře postavená na verzovacím systému Git. Není to jen místo pro ukládání kódu, ale především **komunikační kanál**, který týmům umožňuje spolupracovat, diskutovat o změnách a plánovat práci [](https://github.com/ucdavisdatalab/adventures_in_data_science/blob/main/chapters/week10/working-with-github.qmd)[](https://ucdavisdatalab.github.io/workshop_research_computing/chapters/git-for-teams/02_working-with-github.html).

### 🔧 Základní princip fungování

Základem je Git, který sleduje změny v souborech. GitHub přidává uživatelské rozhraní a nástroje pro usnadnění spolupráce [](https://docs.github.com/en/enterprise-server@3.16/get-started/start-your-journey/about-github-and-git):

- **Repozitář (repository)**: "Složka" pro váš projekt na GitHubu, kde je uložen kód a jeho historie [](https://docs.github.com/en/enterprise-server@3.16/get-started/start-your-journey/about-github-and-git).
    
- **Větvení (branching)**: Umožňuje vytvořit si vlastní kopii kódu (větev), kde můžete pracovat na nové funkci, aniž byste ovlivnili hlavní verzi (`main`) [](https://docs.github.com/en/enterprise-server@3.16/get-started/start-your-journey/about-github-and-git).
    
- **Pull Request (PR)**: Způsob, jak navrhnout začlenění změn z vaší větve do jiné (např. do `main`). PR je centrálním bodem pro **diskusi, kontrolu kódu (code review) a schvalování** změn [](https://github.com/ucdavisdatalab/adventures_in_data_science/blob/main/chapters/week10/working-with-github.qmd)[](https://docs.github.com/en/enterprise-server@3.16/get-started/start-your-journey/about-github-and-git)[](https://hsf-training.github.io/git-novice/16-collab-branch-and-pr.html).
    
- **Fork (vidlička)**: Vytvoření osobní kopie cizího repozitáře na GitHubu. Používá se, když chcete přispět do projektu, ke kterému nemáte přístup pro přímý zápis. Změny pak navrhujete zpět přes Pull Request [](https://github.com/ucdavisdatalab/adventures_in_data_science/blob/main/chapters/week10/working-with-github.qmd)[](https://ucdavisdatalab.github.io/workshop_research_computing/chapters/git-for-teams/02_working-with-github.html)[](https://hsf-training.github.io/git-novice/16-collab-branch-and-pr.html).
    
- **Synchronizace**: Pravidelně stahujete (`pull`) změny od ostatních a nahráváte (`push`) své vlastní. Git tyto změny inteligentně spojuje [](https://docs.github.com/en/enterprise-server@3.16/get-started/start-your-journey/about-github-and-git)[](https://pages.nist.gov/git-novice-MSE/08-collab/index.html).
    

### 🛠 Co GitHub umožňuje (klíčové funkce)

GitHub nabízí širokou škálu nástrojů, které sahají daleko za pouhé ukládání kódu [](https://github.com/ucdavisdatalab/adventures_in_data_science/blob/main/chapters/week10/working-with-github.qmd)[](https://ucdavisdatalab.github.io/workshop_research_computing/chapters/git-for-teams/02_working-with-github.html):

- **Komunikace a plánování**:
    
    - **Issues (Úkoly)**: Systém pro **hlášení chyb, zadávání úkolů a sledování práce**. Pull Requesty jsou ve skutečnosti speciálním typem issue [](https://github.com/ucdavisdatalab/adventures_in_data_science/blob/main/chapters/week10/working-with-github.qmd)[](https://ucdavisdatalab.github.io/workshop_research_computing/chapters/git-for-teams/02_working-with-github.html).
        
    - **Projektové tabule (Project Boards)**: Pro dlouhodobé **plánování a správu projektu** (např. ve stylu Kanban) [](https://github.com/ucdavisdatalab/adventures_in_data_science/blob/main/chapters/week10/working-with-github.qmd)[](https://ucdavisdatalab.github.io/workshop_research_computing/chapters/git-for-teams/02_working-with-github.html).
        
    - **Wiki a dokumentace**: Pro podrobnější dokumentaci, často doplňující hlavní `README.md` soubor [](https://github.com/ucdavisdatalab/adventures_in_data_science/blob/main/chapters/week10/working-with-github.qmd)[](https://ucdavisdatalab.github.io/workshop_research_computing/chapters/git-for-teams/02_working-with-github.html).
        
- **Sledování a zapojení**: Můžete **sledovat (Watch)** projekt pro novinky, dát mu **hvězdu (Star)** jako oblíbený, nebo si ho **naklonovat (Fork)** [](https://github.com/ucdavisdatalab/adventures_in_data_science/blob/main/chapters/week10/working-with-github.qmd)[](https://ucdavisdatalab.github.io/workshop_research_computing/chapters/git-for-teams/02_working-with-github.html).
    

### 💡 "Pooling" a efektivní workflow

Váš dotaz na "pooling" pravděpodobně směřuje k technikám, jak zefektivnit práci s Pull Requesty.

1. **Stacked Pull Requests (Vrstvené PR)**:  
    Místo jednoho obřího PR, který se špatně kontroluje, se velká funkce rozdělí na **malé, na sobě závislé PR (stack)**. První PR je základ, druhý na něj navazuje, a tak dále. To umožňuje **rychlejší a snazší code review** [](https://pypi.org/project/jeeves-pr-stack/0.1.3/)[](https://dev.to/heraldofsolace/how-to-stack-pull-requests-on-github-without-losing-your-mind-54p8#comments)[](https://gigazine.net/gsc_news/en/20260416-github-stacked-pr#gsc.tab=0).
    
    - **Výzva**: Ruční správa těchto závislostí je složitá (zejména "rebase").
        
    - **Řešení**: Existují nástroje, které to automatizují. Jedním z nich je **Graphite CLI**, které umožňuje snadno vytvářet a spravovat stacky příkazem `gt submit --stack` [](https://dev.to/heraldofsolace/how-to-stack-pull-requests-on-github-without-losing-your-mind-54p8#comments).
        
    - **Oficiální řešení**: GitHub tuto funkci zavádí jako **"GitHub Stacked PRs"**. V současnosti je v soukromé preview. Umožňuje zobrazit mapu stacku přímo v rozhraní GitHubu a automaticky rebase vyšší PR, když se změní nižší [](https://gigazine.net/gsc_news/en/20260416-github-stacked-pr#gsc.tab=0)[](https://gigazine.net/news/20260416-github-stacked-pr/).
        
2. **Harmonizace review procesu (Harmony)**:  
    Nástroj **Harmony** pomáhá týmům s efektivním přidělováním reviewerů. Heuristicky vybírá člena týmu s **nejnižším aktuálním pracovním vytížením** na základě počtu otevřených review. To zjednodušuje rozhodování, koho požádat o kontrolu PR [](https://www.npmjs.com/package/@mattpolzin/harmony?activeTab=dependencies).
    

Stručně řečeno, GitHub funguje jako centrální centrum pro váš kód, kde se prolíná verzování, spolupráce a komunikace. Kromě základního flow s PR nabízí i pokročilé mechanismy pro zvládání složitějších projektů, ať už pomocí vrstvení PR, nebo chytrého přidělování reviewerů.

Jaká komunita se tam objevuje? Má každý přístup k GitHub, nebo jen na pozvání k projektu?

Přečteno 10 webových stránek

Na GitHubu se setkáte s obrovskou a různorodou komunitou, od jednotlivých vývojářů a open-source projektů až po celé organizace a firmy. A co se týče přístupu – **není to výhradně na pozvání**. Přístup se odvíjí od jednoduchého pravidla: je repozitář **veřejný**, nebo **soukromý**?

### 👥 Kdo tvoří komunitu na GitHubu?

Komunita je velmi široká a zahrnuje:

- **Individuální vývojáře a studenty**, kteří si na GitHubu zakládají profily a ukládají své projekty.
    
- **Open-source projekty**, jako je Linux, React nebo Python, kde spolupracují tisíce dobrovolníků z celého světa.
    
- **Firmy a organizace všech velikostí**, které na GitHubu hostí svůj komerční kód a řídí přístup členů svých týmů [](https://learn.microsoft.com/en-ie/training/modules/manage-git-repositories/12-configure-source-control-repository-permissions-use-github).
    

### 🔓 Veřejné repozitáře: Přístup pro všechny

Pokud je repozitář **veřejný (public)**, přístup k němu má **opravdu každý na internetu**.

- **Kdokoli si ho může prohlížet, stahovat a vytvářet si jeho kopie (fork)** [](https://learn.microsoft.com/en-ie/training/modules/manage-git-repositories/12-configure-source-control-repository-permissions-use-github)[](https://docs.github.com/en/enterprise-server@3.16/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/setting-repository-visibility)[](https://imperialcollegelondon.github.io/docs/repositories/repositories).
    
- Kdokoli může přispívat tím, že navrhne změny pomocí Pull Requestu. Veřejné repozitáře jsou základním kamenem open-source světa.
    
- To znamená, že ke GitHubu jako platformě má přístup každý, kdo si vytvoří účet. Pro veřejné repozitáře neexistuje žádné "pozvání".
    

### 🔒 Soukromé repozitáře: Přístup jen pro vybrané

V případě **soukromého (private)** repozitáře je situace opačná. Přístup je striktně omezen.

- **Pouze majitel (nebo správce organizace) rozhoduje**, kdo má k repozitáři přístup [](https://learn.microsoft.com/en-ie/training/modules/manage-git-repositories/12-configure-source-control-repository-permissions-use-github)[](https://imperialcollegelondon.github.io/docs/repositories/repositories).
    
- Přístup se uděluje explicitně, buď přímo, nebo přes týmy v rámci organizace [](https://learn.microsoft.com/pt-br/training/modules/manage-git-repositories/12-configure-source-control-repository-permissions-use-github)[](https://learn.microsoft.com/zh-cn/training/modules/manage-git-repositories/12-configure-source-control-repository-permissions-use-github?ns-enrollment-id=learn.wwl.az-400-work-git-for-enterprise-devops&ns-enrollment-type=learningpath). V soukromém repozitáři, který vlastní osobní účet, lze přidat až tři spolupracovníky [](https://learn.microsoft.com/en-ie/training/modules/manage-git-repositories/12-configure-source-control-repository-permissions-use-github).
    
- **Nikdo nemůže nahlížet do soukromého repozitáře ani navrhovat změny bez výslovného povolení.** [](https://github.com/orgs/community/discussions/174347)
    

### 🏢 Organizace a "Interní" repozitáře

Organizace (např. firmy nebo univerzity) mohou mít i **interní (internal)** repozitáře [](https://imperialcollegelondon.github.io/docs/repositories/repositories).

- Jsou viditelné pro všechny členy dané organizace (např. všechny zaměstnance firmy), ale ne pro veřejnost [](https://imperialcollegelondon.github.io/docs/repositories/repositories).
    
- Slouží pro sdílení kódu uvnitř většího celku, aniž by byl dostupný světu.
    

### 🔐 Různé úrovně přístupu (Role)

Kromě samotného viditelného/neviditelného nastavení existují i různé **role**, které určují, co smí daný uživatel dělat. Mezi hlavní patří [](https://learn.microsoft.com/en-ie/training/modules/manage-git-repositories/12-configure-source-control-repository-permissions-use-github)[](https://learn.microsoft.com/pt-br/training/modules/manage-git-repositories/12-configure-source-control-repository-permissions-use-github):

|Role|Typická oprávnění|
|---|---|
|**Read**|Prohlížení kódu, diskuzí a issue.|
|**Triage**|Správa issue a Pull Requestů bez možnosti zapisovat kód.|
|**Write**|Aktivní přispívání – nahrávání kódu (push) a vytváření větví.|
|**Maintain**|Správa repozitáře včetně nastavení, ale bez přístupu k nejcitlivějším akcím.|
|**Admin**|Plná kontrola, včetně mazání repozitáře a správy bezpečnosti.|

Zjednodušeně: GitHub je otevřený všem, kdo si založí účet. Zda uvidíte a budete moci upravovat konkrétní kód, závisí čistě na tom, jestli je repozitář veřejný, nebo zda vám majitel soukromého repozitáře udělil práva. Veřejné repozitáře slouží jako základna pro celosvětovou open-source spolupráci, zatímco soukromé jsou určeny pro uzavřené týmy a firemní projekty.

Jak Git řeší autorská práva pro veřejný repozitář?

Přečteno 9 webových stránek

To je velmi důležitá a častá otázka. Zjednodušeně řečeno: **samotný GitHub autorská práva neřeší; poskytuje pouze technickou platformu. Práva a povolení určuje výhradně autor tím, že ke svému kódu přidá (nebo nepřidá) licenci.**[](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository?from_column=20423)[](https://ospo.library.jhu.edu/learn-grow/public-code-repository-best-practices/)[](https://raw.githubusercontent.com/Harish-Gundapu/opensource.guide/refs/heads/main/_articles/zh-hans/legal.md)

### 🔒 Výchozí stav: Bez licence = Všechna práva vyhrazena

Pokud váš veřejný repozitář **neobsahuje** žádný licenční soubor (např. `LICENSE`), automaticky to neznamená, že je kód volně k dispozici. Naopak, platí standardní autorský zákon (copyright).

- **Vy (autor)** si ponecháváte **všechna výhradní práva** ke svému kódu[](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository?from_column=20423)[](https://ospo.library.jhu.edu/learn-grow/public-code-repository-best-practices/)[](https://docs.github.com/enterprise/2.5/user/articles/licensing-a-repository).
    
- Nikdo jiný **nesmí váš kód legálně používat, kopírovat, upravovat ani dále šířit** bez vašeho výslovného svolení[](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository?from_column=20423)[](https://ospo.library.jhu.edu/learn-grow/public-code-repository-best-practices/)[](https://opensource.guide/zh-hans/legal/#%e4%b8%ba%e4%bb%80%e4%b9%88%e4%ba%ba%e4%bb%ac%e8%bf%99%e4%b9%88%e5%85%b3%e5%bf%83%e5%bc%80%e6%ba%90%e7%9a%84%e6%b3%95%e5%be%8b%e6%96%b9%e9%9d%a2%e9%97%ae%e9%a2%98).
    

**Důležitá výjimka – prohlížení a forkování:** GitHub ve svých [podmínkách služby](https://docs.github.com/en/site-policy/github-terms-of-service) uděluje uživatelům právo **prohlížet a forkovat (vytvořit kopii)** veřejné repozitáře na své vlastní účty[](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository?from_column=20423)[](https://raw.githubusercontent.com/Harish-Gundapu/opensource.guide/refs/heads/main/_articles/zh-hans/legal.md)[](https://docs.github.com/enterprise/2.5/user/articles/licensing-a-repository). To však **nenahrazuje licenci** – forknutí projektu bez licence vám stále nedává právo kód upravovat, používat v jiném projektu nebo ho dále distribuovat[](https://raw.githubusercontent.com/Harish-Gundapu/opensource.guide/refs/heads/main/_articles/zh-hans/legal.md)[](https://opensource.guide/zh-hans/legal/#%e4%b8%ba%e4%bb%80%e4%b9%88%e4%ba%ba%e4%bb%ac%e8%bf%99%e4%b9%88%e5%85%b3%e5%bf%83%e5%bc%80%e6%ba%90%e7%9a%84%e6%b3%95%e5%be%8b%e6%96%b9%e9%9d%a2%e9%97%ae%e9%a2%98).

### 📜 Správná cesta: Přidejte jasnou open-source licenci

Aby ostatní věděli, co s vaším kódem smějí dělat, je nezbytné zvolit a přidat do repozitáře licenci[](https://ospo.library.jhu.edu/learn-grow/public-code-repository-best-practices/)[](https://raw.githubusercontent.com/Harish-Gundapu/opensource.guide/refs/heads/main/_articles/zh-hans/legal.md)[](https://opensource.guide/zh-hans/legal/#%e4%b8%ba%e4%bb%80%e4%b9%88%e4%ba%ba%e4%bb%ac%e8%bf%99%e4%b9%88%e5%85%b3%e5%bf%83%e5%bc%80%e6%ba%90%e7%9a%84%e6%b3%95%e5%be%8b%e6%96%b9%e9%9d%a2%e9%97%ae%e9%a2%98). GitHub přímo doporučuje použít web [choosealicense.com](https://choosealicense.com/), který přehledně vysvětluje nejpoužívanější licence[](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository?from_column=20423)[](https://docs.github.com/enterprise/2.5/user/articles/licensing-a-repository).

Nejběžnější typy licencí zahrnují:

|Typ licence|Charakteristika|Příklady|
|---|---|---|
|**Permisivní (volnější)**|Umožňují téměř cokoliv, včetně použití v komerčních projektech. Vyžadují pouze uvedení autora.[](https://ospo.library.jhu.edu/learn-grow/public-code-repository-best-practices/)|MIT, Apache 2.0, BSD[](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository?from_column=20423)[](https://ospo.library.jhu.edu/learn-grow/public-code-repository-best-practices/)[](https://raw.githubusercontent.com/Harish-Gundapu/opensource.guide/refs/heads/main/_articles/zh-hans/legal.md)|
|**Copyleft (zavazující)**|Umožňují úpravy a šíření, ale **vyžadují**, aby odvozená díla byla zveřejněna pod stejnou licencí.[](https://ospo.library.jhu.edu/learn-grow/public-code-repository-best-practices/)|GPL, AGPL[](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository?from_column=20423)[](https://ospo.library.jhu.edu/learn-grow/public-code-repository-best-practices/)|
|**Veřejná doména**|Vzdáváte se všech svých autorských práv a dílo dáváte volně k užití.[](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository?from_column=20423)|CC0, Unlicense[](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository?from_column=20423)|

**Jak na to:** Stačí vytvořit v kořenové složce vašeho repozitáře soubor s názvem `LICENSE` a vložit do něj plné znění vybrané licence[](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository?from_column=20423)[](https://ospo.library.jhu.edu/learn-grow/public-code-repository-best-practices/). GitHub tuto volbu automaticky nabízí už při zakládání nového repozitáře.

Dá se použít Git na psaní vědecké knihy, která je úzce spojena s LLM, ale zaměřuje se na interakce více, než na technologii.

Přečteno 7 webových stránek

Ano, Git (a platforma jako GitHub) se dá výborně použít i na psaní vědecké knihy, a to i když není o programování. Jeho principy verzování a spolupráce jsou univerzální a pro textový obsah fungují skvěle.

### 💡 Proč je Git vhodný pro psaní knihy?

Základní výhody, které Git přináší, jsou pro autorskou práci velmi užitečné:

- **Kompletní historie změn**: Git uchovává **každou verzi** vašeho textu. Můžete se tak bez obav vrátit k libovolné předchozí verzi kapitoly, zjistit, co a kdy jste změnili, a experimentovat bez rizika ztráty původního textu.
    
- **Práce na větvích**: Hlavní myšlenka "větví" (branches) je vynikající pro organizaci práce. Můžete si vytvořit samostatnou větev pro recenze, jednu pro novou kapitolu a hlavní větev (`main`) udržovat vždy ve stabilním stavu.
    
- **Bezproblémová spolupráce**: Pokud na knize spolupracujete s dalšími lidmi (korektory, spoluautory), Git elegantně sloučí vaše změny. Pomocí nástrojů, jako jsou Pull Requesty na GitHubu, můžete o každé navrhované změně diskutovat a schvalovat ji, podobně jako ve vědeckém recenzním řízení [](https://biblioteca.izt.uam.mx/vufind/Record/978-1-4842-0076-6/Details?lng=fr).
    
- **Podpora pro textové soubory**: Git je optimalizován pro **plain text** (např. ve formátech jako Markdown, LaTeX, nebo docx). Pro tyto formáty umí Git skvěle zobrazovat rozdíly mezi verzemi a efektivně je slučovat.
    

### 🚀 Výhody pro vaše specifické téma (LLM a interakce)

Vaše kniha se zaměřuje na **interakce**, nikoliv na technologii. To je pro použití Gitu skvělá zpráva.

- Git se soustředí na **text a jeho změny**, ne na to, o čem text pojednává. Ať už píšete o lingvistice, sociologii, filozofii nebo technických detailech LLM, pro Git je to stále jen text.
    
- Své výzkumy, poznámky, rozhovory nebo myšlenkové mapy můžete mít přehledně uspořádané v adresářích a verzovat je společně s rukopisem.
    

### 📝 Praktické tipy pro začátek

1. **Zvolte formát**: Pro vědecké knihy je ideální kombinace **Markdown** (pro jednoduché formátování) a **LaTeX** (pro složité rovnice a reference) [](https://biblioteca.izt.uam.mx/vufind/Record/978-1-4842-0076-6/Details?lng=fr). Oba jsou to čisté textové formáty.
    
2. **Organizace složek**: Vytvořte si adresáře jako `kapitoly/`, `obrazy/`, `bibliografie/` a `poznamky/`.
    
3. **Pravidelně ukládejte (commit)**: Uložte své změny do Gitu vždy, když dokončíte smysluplný celek (např. odstavec, tabulku, myšlenku).
    
4. **Využijte platformu**: Když svůj repozitář umístíte na platformu jako GitHub, získáte nejen bezpečné online zálohování, ale i nástroje pro spolupráci a snadné sledování úkolů (Issues). Navíc získáte přehled o tom, jak se vaše kniha vyvíjela. [](https://mzk.knihovny.cz/Record/mzk.MZK01-001080854?sid=608821&lng=cs&print=1)[](https://www.knihovny.cz/Record/ntk.STK01-000672721/Details#tabnav)[](https://vufind-test.katalog.k.utb.cz/SummonRecord/FETCH-LOGICAL-c1145-cd377157441ab1bee8811be74ce2c106f7dfa49f1a2ca9e2ce085601117c9fb63?sid=2775220)
    

Stručně řečeno, Git není jen nástroj pro programátory, ale univerzální pomocník pro každého, kdo pracuje s textem a chce mít nad svou prací plnou kontrolu a přehled. Zkuste to – vaše budoucí já vám za kompletní historii každé kapitoly poděkuje.

Jde mi spíše o komunitu, kterou zatím nemám. Mám zcela nový způsob práce s LLM, který by většinaidi uvítala. Kromě knihy tam mohou být ukázky mých chatu jako tréninková a experimentální data pro budoucí experimenty. Návody jak dosáhnout augmentace, bezpečné sekvence ...

Přečteno 14 webových stránek

Chápu, vaše otázka směřuje k jádru věci – **jak na GitHubu vybudovat komunitu** pro váš zcela nový přístup k práci s LLM. GitHub je k tomu skvěle uzpůsobený, není to jen úložiště kódu, ale přímo platforma pro otevřenou spolupráci a budování komunit [](https://github.com/features/discussions?hmsr=joyk.com&utm_source=joyk.com&utm_medium=referral)[](https://docs.github.com/en/enterprise-server@3.12/get-started/using-github/communicating-on-github).

Vaše kniha, ukázky chatů a experimentální data zde najdou ideální domov. Zde je konkrétní návod, jak na to.

### 🏛️ Položte pevné základy projektu

Než pozvete první zájemce, mějte vše připravené. Klíčová je **transparentnost a otevřenost** [](https://raw.githubusercontent.com/NeverSight/skills_feed/refs/heads/main/data/skills-md/jonathimer/devmarketing-skills/open-source-marketing/SKILL.md)[](https://github.com/worldbank/ifc_gender_datahub).

- **Šablona projektu**: Začněte s tzv. **šablonou repozitáře** (repository template). Ta vám dá perfektní rozjezd – vytvoří předpřipravenou strukturu složek pro vaši knihu (`docs/`), ukázky chatů (`data/`), návody (`notebooks/`) a kód (`src/`). Ušetří to čas a navede vás to k osvědčeným postupům [](https://github.com/worldbank/ifc_gender_datahub)[](https://worldbank.github.io/template/README.html).
    
- **Jasné soubory na úvod**: Nezapomeňte na tyto tři zásadní dokumenty, které tvoří "vizitku" vašeho projektu:
    
    - **`README.md`**: Podrobný úvod. Co je vaším cílem? Co je váš nový přístup zač a komu je určen? Proč by se měl kdokoli zapojit? A hlavně: **jak začít**? [](https://github.com/worldbank/ifc_gender_datahub)[](https://worldbank.github.io/template/README.html)
        
    - **`LICENSE`**: Jasně určete, jak může kdokoli s vaším dílem nakládat. Bez licence máte automaticky všechna práva vyhrazena a nikdo nesmí váš kód ani text použít [](https://github.com/worldbank/ifc_gender_datahub)[](https://worldbank.github.io/template/README.html).
        
    - **`CODE_OF_CONDUCT`**: **Zásadní dokument!** Pravidla chování, která vytvoří bezpečné a respektující prostředí. Chrání vás i vaši komunitu před nevhodnými příspěvky [](https://github.com/worldbank/ifc_gender_datahub)[](https://zenodo.org/records/12117430/files/CSCCE%20Tech%20Case%20Study-%20rOpenSci.pdf?download=1#1#1).
        

### 💬 Otevřete prostor pro komunikaci a nápady

Toto je srdce vaší komunity. GitHub k tomu dává dva skvělé nástroje:

1. **GitHub Discussions (Diskuze)**: Založte je jako **hlavní fórum pro vaši komunitu** [](https://github.com/features/discussions?hmsr=joyk.com&utm_source=joyk.com&utm_medium=referral). Je to prostor pro:
    
    - **Otevřené diskuze** o vaší knize, nápadech a filozofii [](https://docs.github.com/en/enterprise-server@3.12/get-started/using-github/communicating-on-github).
        
    - **Q&A (Otázky a odpovědi)**, kde mohou zájemci klást dotazy [](https://github.com/features/discussions?hmsr=joyk.com&utm_source=joyk.com&utm_medium=referral).
        
    - **Ankety (Polls)**, kterými můžete zjišťovat, o co má komunita největší zájem, nebo která témata knihy jsou nejžádanější [](https://docs.github.com/en/discussions/collaborating-with-your-community-using-discussions/participating-in-a-discussion)[](https://github.com/features/discussions?hmsr=joyk.com&utm_source=joyk.com&utm_medium=referral).
        
    - **Oznamování novinek** a pokroků [](https://docs.github.com/en/enterprise-server@3.12/get-started/using-github/communicating-on-github).
        
    
    > Diskuze jsou ideální pro "otevřené" rozhovory, které nemají jedno správné řešení [](https://docs.github.com/en/enterprise-server@3.12/get-started/using-github/communicating-on-github)[](https://docs.github.com/en/enterprise-server@3.16/issues/tracking-your-work-with-issues/learning-about-issues/about-issues).
    
2. **GitHub Issues (Úkoly)**: Používejte je pro **konkrétní, akční úkoly** ve vašem projektu [](https://github.blog/developer-skills/github/github-for-beginners-getting-started-with-github-issues-and-projects/?utm_source=youtube-episode-1&utm_medium=social&utm_campaign=gfb-s3-2026)[](https://docs.github.com/en/enterprise-server@3.16/issues/tracking-your-work-with-issues/learning-about-issues/about-issues). Skvěle se hodí pro:
    
    - **Sledování chyb** v kódu nebo v textu knihy [](https://esciencecenter-digital-skills.github.io/python-intermediate-development/51-managing-software.html).
        
    - **Návrhy na vylepšení** od komunity [](https://github.blog/developer-skills/github/github-for-beginners-getting-started-with-github-issues-and-projects/?utm_source=youtube-episode-1&utm_medium=social&utm_campaign=gfb-s3-2026).
        
    - **Plánování konkrétních kapitol nebo experimentů**, kde můžete úkol přiřadit sobě nebo zájemci z komunity [](https://esciencecenter-digital-skills.github.io/python-intermediate-development/51-managing-software.html)[](https://docs.github.com/en/enterprise-server@3.16/issues/tracking-your-work-with-issues/learning-about-issues/about-issues).
        
    - **"První úkoly pro nováčky" (`good first issue`)**. Označte tak jednoduché úkoly (např. oprava překlepu, návrh jednoduché ukázky), abyste povzbudili nové přispěvatele [](https://raw.githubusercontent.com/NeverSight/skills_feed/refs/heads/main/data/skills-md/jonathimer/devmarketing-skills/open-source-marketing/SKILL.md)[](https://esciencecenter-digital-skills.github.io/python-intermediate-development/51-managing-software.html).
        

### 🤝 Aktivně pozvěte komunitu k zapojení

Komunita nepřijde sama, musíte ji pozvat.

- **Využijte "Issue" šablony**: Vytvořte šablony pro Issues. Když někdo bude chtít nahlásit chybu nebo navrhnout novou ukázku, formulář ho provede a vy získáte všechny potřebné informace hned na začátku [](https://zenodo.org/records/12117430/files/CSCCE%20Tech%20Case%20Study-%20rOpenSci.pdf?download=1#1#1)[](https://esciencecenter-digital-skills.github.io/python-intermediate-development/51-managing-software.html).
    
- **Sledujte a reagujte**: Komunita roste tam, kde se jí dostává pozornosti.
    
    - Označujte diskuze nebo Issues štítky (labels) jako `idea`, `approved` nebo `working on it`, aby všichni viděli, co se děje [](https://zenodo.org/records/12117430/files/CSCCE%20Tech%20Case%20Study-%20rOpenSci.pdf?download=1#1#1).
        
    - Na otázky a návrhy reagujte, klidně i jednoduchou zprávou, že se jimi zabýváte. Stanovte si například lhůtu 48 hodin pro odpověď [](https://raw.githubusercontent.com/NeverSight/skills_feed/refs/heads/main/data/skills-md/jonathimer/devmarketing-skills/open-source-marketing/SKILL.md).
        
    - Za kvalitní odpovědi v diskuzích je označujte jako **"odpověď" (Mark as answer)** [](https://docs.github.com/en/discussions/collaborating-with-your-community-using-discussions/participating-in-a-discussion).
        
- **Zviditelněte důležité informace**: Diskuze, které jsou klíčové (např. "Jak začít", "Vize projektu"), si můžete **připnout (pin)** na začátek [](https://docs.github.com/en/enterprise-server@3.12/get-started/using-github/communicating-on-github)[](https://github.com/features/discussions?hmsr=joyk.com&utm_source=joyk.com&utm_medium=referral).
    

### 📈 Udržujte a rozvíjejte komunitu

- **Sledujte metriky**: GitHub nabízí přehledy (Insights), kde vidíte aktivitu v diskuzích, počty přispěvatelů a zhlédnutí stránek. Uvidíte, co funguje [](https://github.com/features/discussions?hmsr=joyk.com&utm_source=joyk.com&utm_medium=referral).
    
- **Buďte transparentní**: Sdílejte s komunitou svůj plán, ať už přes Milníky (Milestones) v Issues nebo přes samostatnou diskuzi [](https://raw.githubusercontent.com/NeverSight/skills_feed/refs/heads/main/data/skills-md/jonathimer/devmarketing-skills/open-source-marketing/SKILL.md)[](https://esciencecenter-digital-skills.github.io/python-intermediate-development/51-managing-software.html).
    
- **Oslavujte přispěvatele**: Když někdo pošle užitečný Pull Request nebo dá skvělý nápad, poděkujte mu veřejně. To buduje loajalitu [](https://raw.githubusercontent.com/NeverSight/skills_feed/refs/heads/main/data/skills-md/jonathimer/devmarketing-skills/open-source-marketing/SKILL.md).
    

Až vaše komunita povyroste a bude aktivní, otevřou se vám další možnosti, jako je například finanční podpora projektů, na kterých vaše komunita závisí (GitHub Sponsors), nebo dokonce možnost žádat o granty na bezpečnost open-source projektů, což by mohlo být relevantní, pokud by váš přístup zahrnoval i vlastní kódové nástroje [](https://github.com/open-source/sponsors)[](https://github.com/open-source?trk=article-ssr-frontend-pulse_little-text-block)[](https://github.com/open-source/github-secure-open-source-fund?utm_source=github&utm_medium=blog&utm_campaign=FY26Q3-oss-security-funding).

GitHub má všechny nástroje, které potřebujete. Záleží jen na vás, jak je nastavíte a jak do nich vložíte svou energii. Přeji vám, ať se vaše komunita brzy rozroste!

Git je pro geeky. Je to jen struktura složek a texty a není user friendly. Dá se propojit s mou HTML a tahat si do ní texty? Grafický to vylepšit? Co s verzi sním? Dá se natáhnout statická verze textu?

Přečteno 14 webových stránek

Chápu tu frustraci, Git opravdu může na první pohled působit jako nástroj pro "geeky". Dobrá zpráva ale je, že **pro vaše potřeby – psaní knihy a její převedení na hezkou stránku – existují cesty, jak se vyhnout příkazové řádce a využít přitom všechny výhody verzování.** Vaše myšlenka propojit to s HTML je naprosto správná a je to standardní postup.

### 🖥️ Od textu k webové stránce bez programování

Ano, Git a GitHub jdou s HTML a hezkým vzhledem skvěle dohromady. Funguje to na principu **"dokumenty jako kód" (docs-as-code)** [](https://www.linkedin.com/posts/joeladewole_for-technical-writers-who-are-new-to-github-activity-7384894697837862912-asEp). Vy píšete text v jednoduchém formátu (např. Markdown) a GitHub z něj automaticky vyrobí profesionální webovou stránku. Zde je postup:

1. **Pište v Markdownu**: Je to jednoduchý formátování textu (např. `#` pro nadpisy, `**` pro tučný text), který se snadno čte i bez znalosti HTML. GitHub ho umí automaticky zobrazit pěkně naformátovaný [](https://dev.to/nikhilajain/github-for-writers-no-git-commands-needed-51l8#comments).
    
2. **Nechte to vygenerovat**: Ke svému repozitáři na GitHubu stačí zapnout službu **GitHub Pages** [](https://docs.github.com/en/enterprise-server@3.15/pages/#main-content)[](https://jekyllrb.com/docs/github-pages/)[](https://heardlibrary.github.io/digital-scholarship/manage/control/github/pages/). Ta pak z vašich textových souborů udělá ostrý web. Za tím stojí nástroj jménem **Jekyll** [](https://docs.github.com/en/enterprise-server@3.15/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll#plugins)[](https://docs.github.com/en/enterprise-server@3.13/pages/setting-up-a-github-pages-site-with-jekyll/#main-content)[](https://learn.microsoft.com/zh-tw/training/modules/create-host-web-sites-github-pages/2-what-is-github-pages).
    
    - Jekyll je tzv. "generátor statických stránek". Vezme vaše Markdown soubory a podle vámi zvolené šablony (template) vytvoří kompletní HTML stránky [](https://docs.github.com/en/enterprise-server@3.15/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll#plugins)[](https://learn.microsoft.com/zh-tw/training/modules/create-host-web-sites-github-pages/2-what-is-github-pages). Díky šablonám můžete mít jednotný vzhled, navigaci a nemusíte řešit HTML kód pro každou kapitolu zvlášť.
        
    - Výsledkem je **statická verze textu** – tedy hotový, připravený web, který si může kdokoli prohlížet [](https://learn.microsoft.com/zh-tw/training/modules/create-host-web-sites-github-pages/2-what-is-github-pages)[](https://heardlibrary.github.io/digital-scholarship/manage/control/github/pages/). To je přesně to, co jste chtěl.
        

### 🚀 Jak na to uživatelsky přívětivě (bez příkazů)

Nemusíte se bát černé obrazovky. Pro práci s GitHubem existují přehledné vizuální nástroje:

- **GitHub Desktop**: Aplikace pro váš počítač, která má přehledné tlačítko pro stažení (`Pull`), nahrání změn (`Push`) a zobrazení historie. Veškeré složité příkazy dělá za vás [](https://www.linkedin.com/posts/joeladewole_for-technical-writers-who-are-new-to-github-activity-7384894697837862912-asEp)[](https://dev.to/nikhilajain/github-for-writers-no-git-commands-needed-51l8#comments)[](https://articulatedmedia.com/the-writers-guide-to-using-github-for-true-version-control/#respond).
    
- **[GitHub.com](https://github.com/) (webové rozhraní)**: Na webu si můžete prohlížet soubory, upravovat je přímo v prohlížeči (stačí kliknout na tužku) a vytvářet nové verze (commity) [](https://www.linkedin.com/posts/joeladewole_for-technical-writers-who-are-new-to-github-activity-7384894697837862912-asEp)[](https://dev.to/nikhilajain/github-for-writers-no-git-commands-needed-51l8#comments).
    
- **Vizuální Git klienti**: Existují i další nástroje jako GitKraken, které celý proces a historii zobrazují graficky jako mapu. Pomáhá to pochopit, co se s vašimi texty děje [](https://www.gitkraken.com/gitkon/git-for-writers).
    

### 🧩 Co se všemi verzemi a statickým textem?

- **Verze (commity)**: Každou uloženou verzi vaší knihy můžete v GitHubu vidět jako "záznam v historii". Můžete se k ní vrátit, porovnat rozdíly mezi verzemi, nebo ji označit jako stabilní vydání (např. "první kapitola"). Pro vaše potřeby to funguje jako nekonečná historie změn, ke které se snadno dostanete kliknutím [](https://dev.to/nikhilajain/github-for-writers-no-git-commands-needed-51l8#comments)[](https://www.gitkraken.com/gitkon/git-for-writers).
    
- **Statická verze**: Když zmáčknete tlačítko pro nahrání změn (Push), GitHub Pages automaticky spustí Jekyll a přebuduje celý váš web s novým obsahem [](https://learn.microsoft.com/zh-tw/training/modules/create-host-web-sites-github-pages/2-what-is-github-pages)[](https://jekyllrb.com/docs/github-pages/). Vy tak máte k dispozici jak "pracovní verzi" (texty v repozitáři), tak "ostrou verzi" (živý web pro čtenáře).
    

### 💡 Užitečné tipy na závěr

- Můžete začít s **připravenou šablonou (template)** pro GitHub Pages, která už má vše přednastavené [](https://github.com/joshualinog/eleventy-tailwind-githubpages-template).
    
- Všechny tyto nástroje (GitHub Desktop, GitHub Pages) jsou **zdarma** pro veřejné repozitáře. Pro soukromý repozitář, kde si chcete knihu nejdříve připravit, to také funguje [](https://articulatedmedia.com/the-writers-guide-to-using-github-for-true-version-control/#respond).
    
- Vaše kniha o interakcích s LLM je pro tento přístup ideální – technologie je tu jen jako nástroj, který vám usnadní psaní, verzování a publikování, aniž byste se museli stát programátorem [](https://www.geeksforgeeks.org/git/how-could-non-developers-benefit-from-using-git/#practical-examples-of-git-for-nondevelopers)[](https://www.gitkraken.com/gitkon/git-for-writers).
    

Já myslel pracovat na Gitu a přenést to na vlastní doménu.

Přečteno 9 webových stránek

Ano, jde to. Přesně takhle to dělá většina lidí, kteří chtějí mít vlastní web – pracují na Gitu a výsledek zobrazí na vlastní doméně.

Děje se to ve dvou krocích: **nastavíte GitHub Pages**, aby z vašeho repozitáře generoval web, a pak **propojíte svou doménu**.

---

### 1. GitHub Pages – váš bezplatný hosting

GitHub má vestavěnou službu **GitHub Pages**, která umí z vašeho repozitáře udělat živý web zcela zdarma. Funguje to tak, že soubory (HTML, Markdown, CSS) nahrajete do repozitáře a GitHub je automaticky zveřejní na adrese `https://vasjmeno.github.io` nebo `https://vasjmeno.github.io/nazev-repozitare` [](https://developer.baidu.com/article/detail.html?id=4627366)[](https://developer.baidu.com/article/detail.html?id=4627470)[](https://www.udacity.com/blog/how-to-host-your-website-for-free-using-github-pages-a-step-by-step-guide/).

**Jak to zapnout:**

1. Jděte do **Settings** vašeho repozitáře na GitHubu.
    
2. V levém menu klikněte na **Pages**.
    
3. V části **Source** (nebo **Build and deployment**) vyberte, zda chcete publikovat z konkrétní větve (např. `main`) nebo pomocí GitHub Actions [](https://github.com/joshualinog/eleventy-tailwind-githubpages-template)[](https://developer.baidu.com/article/detail.html?id=4627366).
    
4. Klikněte na **Save** a za pár okamžiků bude váš web dostupný na výchozí [github.io](https://github.io/) adrese.
    

---

### 2. Propojení s vaší vlastní doménou

Aby váš web běžel na vlastní doméně (např. `mojekniha.cz`), musíte udělat dvě věci: **nastavit GitHub** a **nastavit DNS u vašeho registrátora domény**.

#### A) Nastavení na GitHubu

1. V **Settings → Pages** najděte sekci **Custom domain**.
    
2. Zadejte svoji doménu (např. `www.mojekniha.cz`) a uložte [](https://github.com/joshualinog/eleventy-tailwind-githubpages-template)[](https://trustoverip.github.io/spec-up-t-website/docs/developer-documentation/gh-pages-to-custom-domain/)[](https://github.com/orgs/community/discussions/183121?sort=top).
    
3. GitHub automaticky vytvoří v kořeni vašeho repozitáře soubor `CNAME` s tímto údajem [](https://github.com/benchristel/dns.js.org)[](https://trustoverip.github.io/spec-up-t-website/docs/developer-documentation/gh-pages-to-custom-domain/).
    
4. Po chvíli, až se DNS propojí, zaškrtněte **Enforce HTTPS**, aby GitHub vašemu webu automaticky přidělil bezplatný SSL certifikát a stránka byla zabezpečená [](https://github.com/joshualinog/eleventy-tailwind-githubpages-template)[](https://developer.baidu.com/article/detail.html?id=4627366)[](https://www.namesilo.com/blog/en/websites-hosting/how-to-point-your-custom-domain-to-github-pages).
    

#### B) Nastavení DNS u poskytovatele domény

U svého registrátora (např. Cloudflare, Namecheap, GoDaddy) upravíte DNS záznamy. Způsob závisí na tom, zda používáte **root doménu** (`mojekniha.cz`) nebo **subdoménu** (`www.mojekniha.cz`) [](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages)[](https://www.namesilo.com/blog/en/websites-hosting/how-to-point-your-custom-domain-to-github-pages).

- **Pro subdoménu (doporučeno, např. `www`)** [](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages):
    
    - Vytvořte **CNAME záznam**, který ukazuje na vaši GitHub Pages adresu, např. `vasjmeno.github.io` [](https://github.com/orgs/community/discussions/183121?sort=top)[](https://www.udacity.com/blog/how-to-host-your-website-for-free-using-github-pages-a-step-by-step-guide/)[](https://www.namesilo.com/blog/en/websites-hosting/how-to-point-your-custom-domain-to-github-pages).
        
- **Pro root doménu (např. `mojekniha.cz`)** [](https://www.namesilo.com/blog/en/websites-hosting/how-to-point-your-custom-domain-to-github-pages):
    
    - Vytvořte **čtyři A záznamy** směřující na tyto IP adresy GitHubu:
        
        - `185.199.108.153`
            
        - `185.199.109.153`
            
        - `185.199.110.153`
            
        - `185.199.111.153` [](https://github.com/joshualinog/eleventy-tailwind-githubpages-template)[](https://developer.baidu.com/article/detail.html?id=4627366)[](https://www.namesilo.com/blog/en/websites-hosting/how-to-point-your-custom-domain-to-github-pages)
            
    - Zároveň přidejte CNAME záznam pro `www`, který bude ukazovat na `vasjmeno.github.io` [](https://www.namesilo.com/blog/en/websites-hosting/how-to-point-your-custom-domain-to-github-pages).
        

> ⏱️ **Pozor na čas:** DNS změny se neprojeví okamžitě, může to trvat několik minut až 24 hodin [](https://github.com/orgs/community/discussions/183121?sort=top)[](https://www.udacity.com/blog/how-to-host-your-website-for-free-using-github-pages-a-step-by-step-guide/)[](https://www.namesilo.com/blog/en/websites-hosting/how-to-point-your-custom-domain-to-github-pages). Teprve až se záznamy rozšíří po internetu, bude HTTPS fungovat [](https://developer.baidu.com/article/detail.html?id=4627366)[](https://www.namesilo.com/blog/en/websites-hosting/how-to-point-your-custom-domain-to-github-pages).

---

### Shrnutí

GitHub je skvělý nejen na psaní, ale i na zveřejňování. Vaše kniha bude mít perfektní zázemí – verze v Gitu, hotový web na GitHub Pages a vlastní doménu, kterou si k tomu snadno připojíte. A vše zcela zdarma.

Nehledě na to, co jsme probírali, proveďme základy GitHubu, které by měl znát každý nový uživatel.

Dobře, pojďme se na to podívat úplně od začátku. To, co jsme probírali, byly konkrétní scénáře (kniha, LLM, doména). Teď si projdeme **čisté základy GitHubu**, které opravdu potřebuje znát každý, kdo s ním začíná.

Představte si to jako **naučit se používat nástroje v dílně** – nemusíte hned umět stavět dům, ale musíte vědět, co je kladivo a šroubovák.

---

### 1. Co je co? (Základní slovník)

- **Git vs. GitHub**:
    
    - **Git** je "motor" – počítačový program, který běží u vás na disku a sleduje změny v souborech (verzuje je).
        
    - **GitHub** je "webová garáž" – internetová stránka, kam nahrajete svůj lokální repozitář, abyste ho měli zálohovaný, mohli na něm spolupracovat s ostatními a sdílet ho se světem.
        
- **Repository (Repo)**: Hlavní složka vašeho projektu. Může obsahovat složky, soubory, obrázky – prostě vše, co k projektu patří. Veřejné repo vidí každý, soukromé jen vy a ti, které pozvete.
    
- **Commit (uložení)**: Snímek vašeho projektu v určitém čase. Představte si to jako "uložení hry" – ke každému commitu přidáte krátkou zprávu (např. "přidána první kapitola"), abyste věděli, co se změnilo.
    
- **Push (odeslání)**: Odeslání vašich lokálních commitů na GitHub (do cloudu).
    
- **Pull (stažení)**: Stažení nejnovějších změn z GitHubu k vám do počítače. Používáte, když chcete mít jistotu, že pracujete s aktuální verzí.
    
- **Branch (větev)**: Nezávislá linka vývoje. Hlavní větev se obvykle jmenuje `main` nebo `master`. Větve používáte, když chcete pracovat na nové kapitole (nebo experimentu), aniž byste ohrozili hotový text v hlavní větvi.
    

---

### 2. Jak začít pracovat? (První kroky)

**Krok 1: Založte si účet** na [github.com](https://github.com/). Vyberte si uživatelské jméno – bude se objevovat u všeho, co uděláte.

**Krok 2: Vytvořte si svůj první repozitář**:

1. Klikněte na zelené tlačítko **"New"** (nový) v horní části stránky.
    
2. Pojmenujte ho (např. `moje-kniha`).
    
3. Vyberte, zda bude **veřejný** (vidí ho všichni) nebo **soukromý** (vidíte ho jen vy a pozvaní).
    
4. (Důležité!) Zaškrtněte volbu **"Add a README file"** – GitHub vám vytvoří úvodní soubor, do kterého můžete napsat popis projektu.
    
5. Klikněte na **"Create repository"**.
    

**Krok 3: Přidejte do repozitáře obsah**:  
Máte dvě možnosti:

- **Jednoduchá cesta (přes web)**: Na stránce vašeho repozitáře klikněte na **"Add file" → "Create new file"**. Napište název (např. `kapitola1.md`), napište text, dole připište krátkou zprávu o změně (commit message) a klikněte na **"Commit new file"**.
    
- **Profesionální cesta (přes počítač)**: Stáhněte si aplikaci **GitHub Desktop**. Ta vám umožní pracovat se soubory v počítači a tlačítky je odesílat na GitHub, aniž byste museli používat příkazovou řádku.
    

---

### 3. Spolupráce a komunikace – základ úspěchu

GitHub není jen úložiště, ale **sociální síť pro projekty**. K tomu slouží dva hlavní nástroje:

- **Issues (úkoly)**: Jako "to-do list" pro váš projekt. Každý issue má název, popis a diskuzi. Slouží k hlášení chyb, návrhům nových kapitol, nebo plánování úkolů. Můžete je **přiřadit** sobě nebo jinému člověku a označit štítky (např. `good first issue` pro nováčky).
    
- **Pull Requests (PR)**: Jsou srdcem spolupráce na GitHubu. Když chcete, aby se vaše změny z jedné větve dostaly do hlavní (např. `main`), **pošlete Pull Request**. Je to žádost o začlenění a zároveň prostor, kde ostatní vaše změny **zkontrolují (code review)**, napíšou k nim komentáře a nakonec je schválí nebo zamítnou. Pull Requesty jsou naprosto klíčové, pokud na projektu pracuje víc lidí.
    

---

### 4. Základní workflow (jak to celé denně používat)

Ať už pracujete sami nebo v týmu, každodenní rytmus vypadá takto:

1. **Stáhnete (pull)** nejnovější verzi z GitHubu.
    
2. **Uděláte změny** ve svých souborech (píšete novou kapitolu, upravujete chyby).
    
3. **Změny uložíte (commit)** s jasnou zprávou ("přidán odstavec o augmentaci").
    
4. **Odešlete (push)** commity na GitHub.
    
5. (V týmu) **Vytvoříte Pull Request** a požádáte o kontrolu.
    

---

### 5. Dvě zásadní věci na závěr

1. **Bez licence to nikdo nesmí použít**: Přidání licenčního souboru (např. `LICENSE`) je zásadní. Bez něho máte všechen svůj text a kód automaticky chráněný autorským právem a nikdo ho nesmí kopírovat ani upravovat.
    
2. **README.md je vaše výkladní skříň**: Každý repozitář by měl mít soubor `README.md` (píše se v lehkém formátu Markdown). Do něj napište, o čem projekt je, jak ho nainstalovat/používat a kam směřuje. Je to to první, co každý návštěvník uvidí.
    

---

GitHub se může zdát složitý, ale v základu jde jen o **ukládání souborů s historií** a **prostor pro komunikaci o nich**. Všechno ostatní je už jen vylepšení, o které se nemusíte starat, dokud nebudete připravení. Až si tyto základy osvojíte, budete mít perfektní odrazový můstek pro cokoli – knihy, kód, i budování komunit.

Takže já pracuji Vlastě ve složkách vlastního počítače. Na Hub se nahraje nová verze, tedy celý nový obsah? Nebo si Hub zkontroluje jen změny v cloud a vytvoří novou verzi jen části? Pak z Hubu poplují poslední verzi, tedy disk PC se mi přepíše, nebo se verzuji i na PC?

Skvělé otázky – tohle je přesně to, co začátečníky na Gitu nejvíc mate. Odpověď je jednoduchá a zásadní:

**Git (a tím pádem GitHub) verzuje VŠECHNO, ale chytře – nahrává a stahuje POUZE ZMĚNY, ne celé složky pokaždé znovu.**

Pojďme si to rozložit na vaše konkrétní otázky:

---

### 📤 1. "Nahraje se na Hub nová verze, tedy celý nový obsah?"

**NE.** GitHub nenahrává celý projekt znovu. Funguje to takto:

- Vy máte na disku složku (repozitář) s tisíci soubory.
    
- Změníte JEDEN soubor (např. přidáte odstavec do `kapitola3.md`).
    
- Když dáte **Push**, GitHub si spočítá otisk (hash) každého souboru a **pošle jen ty soubory (nebo jejich části), které se změnily**.
    
- Všechny ostatní soubory zůstávají na GitHubu beze změny.
    

**Příklad:** Máte knihu o 500 stránkách. Opravíte jednu překlep na straně 42. Push pošle na GitHub jen tento jeden opravený soubor (nebo dokonce jen jeho změněnou část). Zbytek knihy zůstává na serveru nedotčen.

---

### 🧠 2. "Vytvoří Hub novou verzi jen části?"

**ANO, ale s důležitou nuancí.**

GitHub negeneruje "novou kompletní verzi" jako celek. Místo toho si uchovává:

- **První commit** = celý obsah všech souborů.
    
- **Druhý commit** = pouze záznam o tom, co se v kterých souborech změnilo (např. "na řádku 42 přibylo slovo 'augmentace'").
    

Když si pak prohlížíte historii, Git umí z těchto "střípků změn" rekonstruovat celý obsah v libovolném okamžiku. Je to jako filmový střih – uchováváte jen rozdíly mezi jednotlivými snímky, ne celý film pokaždé znovu.

---

### 📥 3. "Z Hubu poplují poslední verzi, disk PC se mi přepíše?"

**ZÁLEŽÍ na tom, co máte na disku.**

Git je chytrý a dělá toto:

1. Když dáte **Pull** (stažení), Git se podívá, co máte na disku a co je na GitHubu.
    
2. **Srovná obě verze** a aplikuje POUZE ty změny, které na GitHubu přibyly od vašeho posledního stažení.
    
3. **Vaše lokální soubory se přepíší NOVÝM obsahem** – ale jen v těch místech, kde došlo ke změně. Žádné soubory, které jste nezměnili, se nedotýká.
    

**Důležité:** Git nikdy nesmaže vaše lokální změny, pokud jste je neuložili (commitu). Když máte na disku rozpracovanou kapitolu a dáte Pull, Git se vás zeptá, co dělat, pokud dojde ke konfliktu. Většinou to ale bez problémů sloučí.

---

### 💾 4. "Verzuji se i na PC?"

**ANO!** A to je klíčový bod, který spousta lidí nechápe.

Git je **distribuovaný systém** – to znamená, že **KAŽDÝ POČÍTAČ MÁ KOMPLETNÍ HISTORII VŠECH ZMĚN**.

- Když uděláte **Commit**, uloží se nová verze DO VAŠEHO LOKÁLNÍHO REPOZITÁŘE (na disku PC).
    
- Když uděláte **Push**, pošlete tuto lokální verzi na GitHub (do cloudu).
    
- Když uděláte **Pull**, stáhnete si z GitHubu změny, které ostatní nahráli.
    

**To znamená:** I když zítra GitHub zanikne, vy máte na svém disku kompletní historii celého projektu. Můžete se vrátit k libovolné verzi z minulého týdne, aniž byste byli připojeni k internetu. Git je jako stroj času, který máte u sebe v počítači.

---

### 🧩 Praktický příklad pro vaši knihu

|Krok|Co děláte|Co se děje na disku PC|Co se děje na GitHubu|
|---|---|---|---|
|1|Vytvoříte `kapitola1.md` a dáte Commit|Uloží se celý soubor do lokální historie|Zatím nic|
|2|Dáte Push|Nic se nemění|Objeví se celý soubor|
|3|Upravíte `kapitola1.md` (přidáte 2 věty) a dáte Commit|Uloží se pouze změna (2 věty) do lokální historie|Zatím nic|
|4|Dáte Push|Nic se nemění|Na GitHub přibyde záznam o 2 větách|
|5|Kolega přidá `kapitola2.md` a dá Push|Vy o tom nevíte|Na GitHubu přibude nový soubor|
|6|Vy dáte Pull|Git stáhne `kapitola2.md` a přidá ho na váš disk|Nic se nemění|

---

### ✅ Závěr pro vaši praxi

- **Verze máte VŽDY na dvou místech:** na disku (lokální historie) a na GitHubu (cloudová záloha).
    
- **Push = posílám jen to, co se změnilo.**
    
- **Pull = stahuji jen to, co se změnilo od posledního stažení.**
    
- **Nikdy nenahráváte celý projekt znovu** – jen rozdíly mezi verzemi.
    

Je to jako když píšete knihu v Google Docs, ale s tím rozdílem, že **KAŽDÁ VERZE JE ULŽENA U VÁS DOMA NA PEVNÉM DISKU** a vy máte naprostou kontrolu nad tím, co a kdy sdílíte s ostatními.

Branch je tedy nový repozitář?

Jaká je monetizacni politika GitHubu?

Přečteno 11 webových stránek

Monetizační politika GitHubu je postavena na několika pilířích, které pokrývají různé způsoby, jak na platformě vydělávat, ať už jako uživatel, vývojář, nebo provozovatel projektu.

### 💰 1. GitHub Sponsors – Finanční podpora od komunity

Toto je primární nástroj, jak mohou tvůrci open-source projektů získávat přímo od komunity finanční podporu [](https://docs.github.com/en/sponsors/getting-started-with-github-sponsors/about-github-sponsors). Politika je zde velmi transparentní:

- **Pro sponzory z osobních účtů**: GitHub si **neúčtuje žádné poplatky**. 100 % vašeho příspěvku jde přímo podporovanému vývojáři nebo organizaci [](https://docs.github.com/en/sponsors/getting-started-with-github-sponsors/about-github-sponsors).
    
- **Pro sponzory z organizačních účtů**: GitHub si účtuje poplatek **až 6 %**, který se skládá z 3 % za zpracování kreditní karty a 3 % za servisní poplatek [](https://github.com/orgs/community/discussions/153625)[](https://docs.github.com/en/sponsors/getting-started-with-github-sponsors/about-github-sponsors). Organizace mohou ušetřit 3% poplatek za kreditní kartu přechodem na fakturační billing [](https://docs.github.com/en/sponsors/getting-started-with-github-sponsors/about-github-sponsors).
    

### 🛒 2. GitHub Marketplace – Prodej aplikací a nástrojů

Pokud vyvíjíte aplikaci a chcete ji prodávat přes GitHub Marketplace, platí zde tento model:

- **Provize GitHubu**: Z každé transakce uskutečněné přes Marketplace si GitHub **ponechá 5 % z příjmů** (u transakcí po 1. lednu 2021; před tímto datem to bylo 25 %) [](https://docs.github.com/en/apps/github-marketplace/selling-your-app-on-github-marketplace/receiving-payment-for-app-purchases)[](https://docs.github.com/es/enterprise-cloud@latest/apps/github-marketplace/selling-your-app-on-github-marketplace/receiving-payment-for-app-purchases)[](https://docs.github.com/de/apps/github-marketplace/selling-your-app-on-github-marketplace/receiving-payment-for-app-purchases).
    
- **Výplata**: Výplaty jsou prováděny na konci následujícího měsíce, jakmile vaše měsíční příjmy dosáhnou **minimální hranice 500 USD** [](https://docs.github.com/en/apps/github-marketplace/selling-your-app-on-github-marketplace/receiving-payment-for-app-purchases)[](https://docs.github.com/es/enterprise-cloud@latest/apps/github-marketplace/selling-your-app-on-github-marketplace/receiving-payment-for-app-purchases).
    

### 📊 3. Účtování za služby (Plány, Action, Packages)

Pro samotné uživatele a organizace je monetizace GitHubu postavena na kombinaci **předplatného a průběžného účtování podle využití** [](https://learn.microsoft.com/zh-cn/training/modules/github-introduction-products/4-github-billing?WT.mc_id=MVP_380318&ns-enrollment-type=learningpath&ns-enrollment-id=learn.github-foundations):

- **Předplatné (Subscriptions)**: Jedná se o fixní měsíční poplatky za účty (např. GitHub Pro, GitHub Team) a další produkty jako GitHub Copilot nebo aplikace z Marketplace [](https://learn.microsoft.com/zh-cn/training/modules/github-introduction-products/4-github-billing?WT.mc_id=MVP_380318&ns-enrollment-type=learningpath&ns-enrollment-id=learn.github-foundations).
    
- **Účtování podle využití (Usage-based fees)**: Platí se za služby, jejichž cena roste s objemem využití. Typickým příkladem jsou:
    
    - **GitHub Actions**: Účtují se minuty běhu a úložiště artefaktů. Veřejné repozitáře mají neomezený běh zdarma, pro soukromé repozitáře jsou v rámci plánu zahrnuty určité volné minuty (např. 2 000 minut/měsíc na Free účtu) a za jejich překročení se platí [](https://learn.microsoft.com/zh-cn/training/modules/github-introduction-products/4-github-billing?WT.mc_id=MVP_380318&ns-enrollment-type=learningpath&ns-enrollment-id=learn.github-foundations).
        
    - **GitHub Packages**: Účtuje se za uložená data a přenesený bandwidth [](https://learn.microsoft.com/zh-cn/training/modules/github-introduction-products/4-github-billing?WT.mc_id=MVP_380318&ns-enrollment-type=learningpath&ns-enrollment-id=learn.github-foundations).
        
    - **Flexibilita**: Pro správu nákladů si lze nastavit limity výdajů. U licencí (např. GitHub Enterprise) byl zaveden model **"pay-as-you-go"**, kdy se platí pouze za aktivní uživatele v daném měsíci, čímž odpadá nutnost předplacení pevného počtu licencí [](https://learn.microsoft.com/zh-cn/training/modules/github-introduction-products/4-github-billing?WT.mc_id=MVP_380318&ns-enrollment-type=learningpath&ns-enrollment-id=learn.github-foundations).
        

### 💸 4. Poplatky a finanční práh pro vývojáře

- **Poplatek u GitHub Sponsors**: Jak bylo zmíněno výše, poplatek závisí na tom, zda sponzor platí z osobního nebo organizačního účtu [](https://docs.github.com/en/sponsors/getting-started-with-github-sponsors/about-github-sponsors). Kromě poplatku GitHubu je třeba počítat s poplatky, které si za zpracování platby účtuje **Stripe** (platební brána, kterou GitHub používá), což jsou standardní poplatky za kreditní karty a případné mezinárodní převody a konverze měn [](https://github.com/orgs/community/discussions/153625).
    
- **Minimální hranice pro výplatu (Marketplace)**: Pro výplatu z GitHub Marketplace je nutné dosáhnout měsíčního obratu alespoň **500 USD** [](https://docs.github.com/en/apps/github-marketplace/selling-your-app-on-github-marketplace/receiving-payment-for-app-purchases)[](https://docs.github.com/es/enterprise-cloud@latest/apps/github-marketplace/selling-your-app-on-github-marketplace/receiving-payment-for-app-purchases). GitHub Sponsors takový striktní práh nemá a výplaty jsou zpracovávány průběžně [](https://github.com/orgs/community/discussions/153625).
    

### 🤝 5. Partner Program a Enterprise

Pro firmy a partnery existují specifické smluvní a finanční modely. **GitHub Partner Program** umožňuje partnerům (např. resellerům) prodávat a distribuovat produkty GitHubu za provizi [](https://github.com/partners/legal?locale=es-419). Pro velké organizace je určen **GitHub Enterprise**, který zahrnuje pokročilé bezpečnostní a administrativní funkce a cení se na základě počtu uživatelů a nasmlouvaných služeb [](https://docs.github.com/en/site-policy/site-policy-deprecated/github-enterprise-server-license-agreement).

### 📌 6. Shrnutí pro vaši konkrétní situaci

Pokud vaše kniha a navazující experimenty povedou k vytvoření open-source projektu nebo komunity, dává pro vás největší smysl **GitHub Sponsors**. Umožní vám přijímat dobrovolné příspěvky od uživatelů, kteří vaši práci ocení, a to s minimálním poplatkem. Pokud byste vytvořili placený nástroj nebo aplikaci, cesta by vedla přes **GitHub Marketplace** a jeho 5% provizi. Vedení samotného repozitáře s knihou a daty je zdarma a účtování za služby (Actions, Packages) se vás pravděpodobně dotkne až ve chvíli, kdy byste začali masivně využívat například automatizované testování nebo distribuovali velké objemy dat.

Takže jediný zaručený způsob jak mít repozitář zdarma je veřejný repozitář.

Přečteno 9 webových stránek

Vaše úvaha je **správná** v tom, že bezplatné účty na GitHubu primárně staví na veřejných repozitářích. Veřejné repozitáře jsou totiž pro všechny uživatele a organizace zcela zdarma a bez omezení počtu spolupracovníků či funkcí [](https://docs.github.com/en/enterprise-server@3.16/get-started/learning-about-github/githubs-plans)[](https://github.com/orgs/community/discussions/158496)[](https://docs.github.com/en/get-started/learning-about-github/githubs-plans?apiVersion=2022-11-28).

### 📂 Možnosti bezplatných účtů

Pravda je ale o něco pestřejší, a to zejména pokud jde o soukromé repozitáře. Zde je přehled toho, co nabízí bezplatné plány [](https://docs.github.com/en/get-started/learning-about-github/githubs-plans?apiVersion=2022-11-28):

- **Veřejné repozitáře (zdarma)**: Nabízí **plný přístup ke všem funkcím** pro neomezený počet spolupracovníků [](https://docs.github.com/en/enterprise-server@3.16/get-started/learning-about-github/githubs-plans)[](https://github.com/orgs/community/discussions/158496). GitHub Actions jsou zde zdarma s neomezeným počtem minut na hostovaných běžcích [](https://learn.microsoft.com/en-us/training/modules/github-introduction-products/4-github-billing).
    
- **Soukromé repozitáře na **osobním (Free) účtu**: Jsou také zcela zdarma pro neomezený počet repozitářů a spolupracovníků [](https://docs.github.com/en/enterprise-server@3.16/get-started/learning-about-github/githubs-plans)[](https://docs.github.com/en/get-started/learning-about-github/githubs-plans?apiVersion=2022-11-28). Platí zde však **omezená sada funkcí** a **limit 2 000 minut GitHub Actions za měsíc** [](https://docs.github.com/en/enterprise-server@3.16/get-started/learning-about-github/githubs-plans)[](https://learn.microsoft.com/en-us/training/modules/github-introduction-products/4-github-billing)[](https://docs.github.com/de/enterprise-server@3.12/get-started/learning-about-github/githubs-plans#github-enterprise). Upozornění: U osobního Free účtu mohou mít spolupracovníci v soukromém repu pouze roli se **zápisem (write)** [](https://learn.microsoft.com/en-ie/training/modules/manage-git-repositories/12-configure-source-control-repository-permissions-use-github).
    
- **Soukromé repozitáře na **organizačním (Free) účtu**: Nabízejí stejné výhody jako osobní Free účet – neomezené repozitáře, neomezené spolupracovníky, ale s **omezenými funkcemi** a **2 000 minutami GitHub Actions měsíčně** [](https://learn.microsoft.com/en-us/training/modules/github-introduction-products/4-github-billing)[](https://github.com/team)[](https://docs.github.com/ko/enterprise-server@3.16/get-started/learning-about-github/githubs-plans).
    

### 💡 Proč se tedy říká, že "zaručeně zdarma" je jen veřejný repozitář?

Tato představa pramení z několika důvodů:

- **Minulost**: Dříve byly soukromé repozitáře na bezplatných účtech výrazně omezené, například počtem spolupracovníků [](https://learn.microsoft.com/en-ie/training/modules/manage-git-repositories/12-configure-source-control-repository-permissions-use-github). To už ale neplatí.
    
- **"Plná sada funkcí" (Full feature set)**: Oficiální dokumentace [](https://docs.github.com/en/enterprise-server@3.16/get-started/learning-about-github/githubs-plans)[](https://docs.github.com/en/get-started/learning-about-github/githubs-plans?apiVersion=2022-11-28) neustále zdůrazňuje, že **veřejné repozitáře** mají "plnou sadu funkcí", zatímco soukromé jen "omezenou sadu funkcí" [](https://docs.github.com/en/enterprise-server@3.16/get-started/learning-about-github/githubs-plans)[](https://docs.github.com/en/get-started/learning-about-github/githubs-plans?apiVersion=2022-11-28)[](https://learn.microsoft.com/en-ie/training/modules/manage-git-repositories/12-configure-source-control-repository-permissions-use-github).
    
- **Možnost skrytých poplatků**: V soukromých repozitářích se při překročení bezplatného limitu (např. minut GitHub Actions nebo úložiště GitHub Packages) automaticky spouští **fakturace** [](https://learn.microsoft.com/en-us/training/modules/github-introduction-products/4-github-billing). Ve veřejných repozitářích vám nikdy za překročení těchto limitů nevznikne poplatek [](https://github.com/orgs/community/discussions/195271)[](https://learn.microsoft.com/en-us/training/modules/github-introduction-products/4-github-billing).
    

### ✅ Závěr pro vás

Pro váš projekt (kniha, návody, experimentální data) platí:

- **Veřejný repozitář**: Je zcela zdarma, bez rizika skrytých poplatků a s přístupem ke všem funkcím. Navíc je ideální pro budování **komunity** a otevřenou spolupráci, jak jste zmiňoval.
    
- **Soukromý repozitář na bezplatném účtu**: Není problém a je také zdarma. Budete ale muset počítat s tím, že některé pokročilé nástroje (např. chráněné větve, vlastníci kódu) nebudou k dispozici [](https://docs.github.com/ko/enterprise-server@3.16/get-started/learning-about-github/githubs-plans) a budete si muset hlídat využití služeb, abyste nepřekročili bezplatný limit.
    

Pokud už mám na PC strukturu složek a soubory, pak zacit s depozitářem bude jen o založení nové struktury a přechod na repozitář. Mohu mít repozitář jako součást pracovní ozky, tedy dokumentů, které se do repozitare nesmí dostat?

Přečteno 14 webových stránek

Ano, je to nejen možné, ale je to i standardní a bezpečný postup. Vaše pracovní složka se může stát **repozitářem** a zároveň si můžete být naprosto jistí, že se do něj nedostanou dokumenty, které tam nepatří.

### 🗂️ Repozitář jako součást pracovní složky

Přesně tak to funguje. Git je navržen tak, aby mohl být inicializován přímo ve vaší existující pracovní složce. Základem repozitáře je pak skrytá složka `.git`, která obsahuje celou historii vašeho projektu[](https://manpages.debian.org/testing/git-man/git-init.1.en.html)[](https://manpages.ubuntu.com/manpages/focal/en/man1/git-init.1.html)[](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository#ch02-git-basics-chapter).

Váš pracovní postup by byl:

1. Otevřete terminál/příkazovou řádku a přejděte do vaší pracovní složky (např. `cd C:/Users/tvuj_ucet/Dokumenty/projekt`).
    
2. Spusťte příkaz `git init`[](https://manpages.debian.org/testing/git-man/git-init.1.en.html)[](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository#ch02-git-basics-chapter). Tím se ve složce vytvoří `git` repozitář.
    
3. Příkazem `git add .` a následně `git commit -m "První verze"` přidáte všechny soubory do repozitáře[](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository#ch02-git-basics-chapter).
    

### 🛡️ Jak zabránit nahrání "nepatřičných" dokumentů?

Vaše obava je naprosto na místě a Git na to má elegantní řešení – **ignorování souborů**. Existují tři hlavní způsoby, jak to udělat, od těch, které platí pro všechny, až po ty jen pro váš počítač [](https://manpages.debian.org/experimental/git-man/gitignore.5.en.html)[](https://docs.github.com/en/enterprise-server@3.15/get-started/git-basics/ignoring-files?platform=windows):

#### 1. `.gitignore` (Pro celý tým – doporučeno)

- Vytvořte v kořenové složce vašeho repozitáře soubor s názvem `.gitignore` [](https://learn.microsoft.com/zh-hk/previous-versions/azure/devops/repos/git/ignore-files?view=azure-devops-2019)[](https://docs.github.com/en/enterprise-server@3.15/get-started/git-basics/ignoring-files?platform=windows).
    
- Do tohoto souboru napíšete pravidla, které soubory nebo složky má Git ignorovat. Pravidla se zapisují pomocí zástupných znaků (wildcards) [](https://labex.io/questions/can-git-ignore-specific-file-types-081850).
    
- **Výhoda:** Tento soubor se commitne do repozitáře, takže ho mají všichni spolupracovníci a platí pro všechny stejně [](https://manpages.debian.org/experimental/git-man/gitignore.5.en.html)[](https://docs.github.com/en/enterprise-server@3.15/get-started/git-basics/ignoring-files?platform=windows).
    
- **Příklad obsahu `.gitignore`:**
    

text

# Ignoruje celou složku s osobními poznámkami
/osobni_poznamky/
# Ignoruje všechny soubory s příponou .log (logy)
*.log
# Ignoruje konkrétní soubor, který nesmí být v repozitáři
tajny_klic.txt

Pokud by některé soubory už byly Gitem sledovány, musíte je nejprve odtrackovat příkazem `git rm --cached <soubor>` [](https://learn.microsoft.com/zh-hk/previous-versions/azure/devops/repos/git/ignore-files?view=azure-devops-2019)[](https://manpages.debian.org/experimental/git-man/gitignore.5.en.html)[](https://labex.io/questions/how-do-i-ignore-specific-files-515364).

#### 2. `.git/info/exclude` (Pouze pro váš lokální počítač)

- Jedná se o speciální soubor `exclude` uvnitř skryté složky `.git` [](https://manpages.debian.org/experimental/git-man/gitignore.5.en.html)[](https://docs.github.com/en/enterprise-server@3.15/get-started/git-basics/ignoring-files?platform=windows).
    
- Funguje na stejném principu jako `.gitignore`, ale **tento soubor se necommitne** a platí pouze pro váš lokální repozitář [](https://manpages.debian.org/experimental/git-man/gitignore.5.en.html)[](https://docs.github.com/en/enterprise-server@3.15/get-started/git-basics/ignoring-files?platform=windows).
    
- **Kdy ho použít:** Hodí se, když chcete ignorovat soubory, které jsou specifické pro váš pracovní postup a ostatní by je ignorovat nemuseli (např. dočasné soubory vašeho textového editoru)[](https://docs.github.com/en/enterprise-server@3.15/get-started/git-basics/ignoring-files?platform=windows).
    

#### 3. Globální `.gitignore` (Pro všechny vaše projekty)

- Můžete si nastavit jeden globální soubor `.gitignore`, který se aplikuje na všechny vaše Git repozitáře na vašem počítači [](https://github.com/narsiimha19/git-training-manual/blob/main/docs/23_gitignore.md)[](https://docs.github.com/en/enterprise-server@3.15/get-started/git-basics/ignoring-files?platform=windows).
    
- Nastavuje se příkazem: `git config --global core.excludesfile ~/.gitignore_global` [](https://github.com/narsiimha19/git-training-manual/blob/main/docs/23_gitignore.md).
    
- **Kdy ho použít:** Ideální pro soubory, které generuje váš operační systém (např. `Thumbs.db` na Windows, `.DS_Store` na macOS) [](https://github.com/narsiimha19/git-training-manual/blob/main/docs/23_gitignore.md)[](https://docs.github.com/en/enterprise-server@3.15/get-started/git-basics/ignoring-files?platform=windows).
    

### 💡 Tip pro vás: `--separate-git-dir`

Pokud chcete mít pracovní složku (ty vaše "dokumenty") a složku s historií (`.git`) **fyzicky oddělené** na disku (např. pro snadnější zálohování), můžete použít příkaz:

bash

git init --separate-git-dir /cesta/k/umisteni/repozitare.git

Ten umístí celou složku `.git` na jiné místo, než je vaše pracovní složka s dokumenty[](https://github.com/orgs/community/discussions/161360)[](https://git.zx2c4.com/git/log/?id=aed0800ca68806a7bc1dc15995417b9171f22079&ofs=300&showmsg=1).

**Stručně:** Složku repozitáře vytvoříte přímo ve své pracovní složce. O tom, které soubory se do repozitáře dostanou, rozhodujete vy pomocí `.gitignore` (nebo `exclude`). Je to bezpečné a je to standardní způsob práce s Gitem.

Mám projek v něm složky, vytvořím jen novou složku repozitáře, staré alpský nebudou pro GitHub dostupné. Souhlas?

Ano, **naprostý souhlas**. Toto je nejen možné, ale i velmi častý a bezpečný přístup.

Vaše myšlenka je naprosto správná: **Git (a GitHub) vidí jen to, co leží uvnitř složky, kterou jste inicializovali jako repozitář. Všechno ostatní, co je mimo ni, je pro Git neviditelné a nedotknutelné.**

Pojďme si to potvrdit na vašem konkrétním případu:

### 🗂️ Vaše situace krok za krokem

Představte si, že váš počítač má tuto strukturu:

text

C:/Users/tvuj_ucet/Dokumenty/           (hlavní pracovní složka)
│
├── stary_projekt/                      (složka A – staré soubory)
│   ├── obrazky/
│   └── poznamky.txt
│
├── novy_projekt/                       (složka B – nový projekt)
│   ├── kapitola1.md
│   └── data/
│
└── osobni_dokumenty/                   (složka C – citlivé dokumenty)
    └── danove_priznani.pdf

**Pokud uděláte toto:**

1. Otevřete terminál a přejdete do složky `novy_projekt`.
    
2. Spustíte `git init`.
    

**Výsledek:**

- Vytvoří se repozitář **pouze** ve složce `novy_projekt` (objeví se v ní skrytá složka `.git`).
    
- Git bude sledovat **jen** `kapitola1.md` a složku `data/` (a cokoli dalšího, co do `novy_projekt` přidáte).
    
- Složky `stary_projekt` a `osobni_dokumenty` **zůstanou zcela nedotčeny**. Git o nich neví a nikdy se o nich nedozví. Když pak dáte `push` na GitHub, nahrají se **jen soubory z `novy_projekt`**.
    

---

### ✅ Co to pro vás znamená?

|Vaše obava|Skutečnost|
|---|---|
|"Staré složky nebudou pro GitHub dostupné."|**Přesně tak.** GitHub nikdy neuvidí soubory, které leží mimo váš repozitář.|
|"Musím přesouvat všechny dokumenty do jedné složky?"|**Ne.** Repozitář si založíte přesně tam, kde chcete. Zbytek vašeho disku zůstane nedotčen.|
|"Nenahrál bych omylem citlivé dokumenty?"|**Nehrozí**, pokud jsou fyzicky mimo složku repozitáře. Git je prostě nezná. (Pro jistotu si ale časem zvykněte používat `.gitignore` pro soubory uvnitř repozitáře, které nechcete sdílet.)|

---

### ⚠️ Jediná drobná výhrada

Pokud byste chtěli, aby **oba projekty** (starý i nový) byly na GitHubu, musíte vytvořit **dva samostatné repozitáře** – jeden v každé složce. Git neumí sdílet jednu historii napříč nesouvisejícími složkami.

---

### 🧠 Shrnutí

Ano, máte to naprosto správně. Repozitář je jen "kontejner", který si sami vytvoříte v libovolné složce. Všechno mimo něj je pro Git vzduch. Můžete tak klidně pracovat na nové knize v izolaci, aniž byste se museli bát, že omylem nahrajete na GitHub své staré dokumenty nebo osobní soubory.

Mám metody, které jsou extrémně náročné, nové, ale i intuitivní na pochopení. Pracují s LLM. Chci sdílet můj způsob chatování, mou paměť projektu. Kvůli výzkumům jako data jak projekt vzniká a vznikl. Pro budoucí analýzy sekvenci ... Jde svým způsobem o knihu, která předbíhá výzkum a výzkum na ni naváže. Jak ošetřit licenci, abych měl jistotu, že univerzita mi má poslat záměr výzkumu aby dostala práva na ty které části a jen pro svůj záměr?

Přečteno 15 webových stránek

Vaše myšlenka je jasná: chcete sdílet svou práci, ale mít kontrolu nad tím, jak ji univerzita použije. Musíte jim dát jasně najevo, že si vyhrazujete právo rozhodovat o využití pro výzkum, a to nejlépe **kombinací pečlivě zvolené licence a vlastního "smluvního" dodatku.**

Nejde o jeden soubor, ale o **kombinaci nástrojů**, které dohromady vytvoří právní a kulturní rámec vašeho projektu.

### 🧩 Výchozí stav: "Bez licence" je nepoužitelné

První a zásadní krok je přidat licenci. Bez ní platí, že **nikdo nesmí váš text ani data použít**, protože autorská práva máte automaticky vy vy [](https://step-up.ac.uk/blog/2025-09-29-software-licensing/#footer)[](https://ucospo.net/research-software-citable-discoverable/open-source-license.html). To by znemožnilo i univerzitě váš výzkum legálně použít.

### ⚖️ Výběr správné licence: "Pouze pro nekomerční výzkum"

Existují dvě cesty, jak dosáhnout svého cíle. Tu druhou (šitou na míru) byste zvolil, pokud je váš vztah s univerzitou složitější.

#### 1. Standardní licence se správnou kombinací podmínek

Nejjednodušší je použít některou ze standardních licencí. Pro váš případ bych doporučil **Creative Commons Attribution-NonCommercial-ShareAlike (CC BY-NC-SA)**.

- **Proč?** Tato licence přesně odpovídá vašim potřebám: umožňuje ostatním (včetně univerzity) **sdílet a upravovat** vaše dílo, ale **výhradně pro nekomerční účely** a pouze **pod podmínkou, že nová díla budou licencována stejně** [](https://www.enago.com/academy/smart-data-sharing-which-license-should-you-choose/?from_id=8538&to_id=8090).
    
- **Funguje to?** Univerzita si tak vaše dílo může stáhnout a použít ve svém výzkumu, aniž by vás musela žádat o svolení, **pokud tento výzkum zůstane nekomerční**. Tím jí dáváte jasný rámec, ve kterém se může pohybovat, aniž byste ztratili kontrolu. Datové sady se často takto licencují právě proto, aby se omezilo jejich komerční zneužití [](https://uni-tuebingen.de/en/faculties/faculty-of-humanities/departments/modern-languages/department-of-linguistics/chairs/general-and-computational-linguistics/ressources/lexica/germanet/licenses/)[](https://usm3d.github.io/S23DR/data_license.html).
    

#### 2. Vlastní licence (pro komplexnější kontrolu)

Pokud chcete mít ještě přísnější kontrolu, můžete vytvořit **vlastní licenci**. Ta by měla jednoznačně definovat, co je "akademický výzkum", a omezit použití pro komerční subjekty. Například:

"_Tento repozitář a jeho obsah smí být použit výhradně pro nekomerční akademický výzkum na akreditovaných institucích. Jakékoli jiné použití, včetně komerčního výzkumu, je přísně zakázáno bez předchozího písemného souhlasu autora._"

Takové přístupy jsou běžné u univerzitního softwaru, ale vyžadují více právní práce a mohou být hůře srozumitelné [](https://iopscience.iop.org/article/10.1088/1741-2552/adb997/pdf#6#4)[](https://www.myhkl.hkl-xray.com/hkl-2000-license-policy-academic-users).

### 🛡️ Krok navíc: "Oznámení o patentu" a rezervace práv

Výzkum na univerzitě je specifický tím, že se často potýká s patenty. Může se stát, že univerzita nebude moci vaši práci použít, protože by jí to mohlo zkomplikovat existující patentové smlouvy [](https://eprints.bbk.ac.uk/id/eprint/23469/1/2018-08-07-open-source-patents.markdown)[](https://iopscience.iop.org/article/10.1088/1741-2552/adb997/pdf#6#4).

- **Řešení**: Do repozitáře přidejte **patentové oznámení**. Například: "Části tohoto díla mohou být předmětem patentových přihlášek. Pro licenční informace kontaktujte [váš e-mail]" [](https://iopscience.iop.org/article/10.1088/1741-2552/adb997/pdf#6#4).
    
- **Rezervace práv pro univerzitu**: Můžete výslovně uvést, že si **vyhrazujete právo uzavřít s univerzitou samostatnou smlouvu** pro konkrétní výzkumné záměry. Tím jim dáváte najevo, že jste otevřeni diskuzi, ale že standardní licence nezakrývá všechny situace. Tento přístup je v akademickém prostředí poměrně běžný [](http://www.law.emory.edu/fileadmin/journals/elj/58/58.4/Lee.pdf#17#13).
    

### ⚠️ Nejdůležitější varování: Zjistěte si vlastnická práva

**Než cokoli uděláte, zjistěte si u své univerzity, komu dílo patří.**

Na mnoha univerzitách platí, že software, a obzvláště pak inovativní metodologie vytvořené zaměstnanci či studenty s využitím univerzitních zdrojů, jsou majetkem **instituce** [](https://ucospo.net/research-software-citable-discoverable/open-source-license.html)[](https://facultygov.unc.edu/wp-content/uploads/sites/261/2011/03/Res2016-11OnAmendingCopyrightPolicy.pdf#1#1).

- **Pokud je dílo majetkem univerzity**, nemůžete si sami určit licenci. Musíte jednat s jejím technologickým transferovým oddělením (Technology Transfer Office) [](https://ucospo.net/research-software-citable-discoverable/open-source-license.html).
    
- **Pokud je vaše**, některé univerzity (např. UNC-Chapel Hill) mají proceduru, kde autor **musí univerzitu informovat o svém záměru** publikovat pod otevřenou licencí. Univerzita má pak např. 30 dní na to, aby si nárokovala práva, pokud usoudí, že je dílo komerčně využitelné [](https://facultygov.unc.edu/wp-content/uploads/sites/261/2011/03/Res2016-11OnAmendingCopyrightPolicy.pdf#1#1).
    

Toto je zásadní krok, bez kterého riskujete nejen právní problémy, ale i to, že vaše snaha o kontrolu bude marná.

### ✅ Shrnutí a doporučený postup

1. **Ověřte si vlastnictví**: Kontaktujte technologické transferové oddělení vaší univerzity.
    
2. **Přidejte výchozí licenci (CC BY-NC-SA)**: Do kořenového adresáře repozitáře vložte plné znění a do `README.md` odkaz.
    
3. **Přidejte vlastní "smluvní" dodatek**: Do `README.md` (nebo jako `TERMS.md`) uveďte upřesňující prohlášení, které definuje, co považujete za "výzkumný záměr" a že si vyhrazujete právo uzavírat samostatné dohody.
    
4. **Dokumentujte a patentujte**: V repozitáři uveďte, že se jedná o originální metodologii a že si vyhrazujete práva pro budoucí patentové přihlášky.
    

Tímto způsobem vytvoříte jasný, právně konzistentní rámec, který vám umožní sdílet vaši práci, podporovat otevřenou vědu, ale zároveň si ponechat kontrolu nad tím, jak a pro jaké účely bude vaše univerzita a další instituce vaše inovace využívat.

Téma na kterém pracují je multidisciplinární. Kybernetika, IT, neurovědy, psychologie, pedagogika, politologie ... Těch univerzit může být hodně. Chci mít pod kontrolou velká témata, ne malé výzkumné projekty. Chci mít pod kontrolou propojení s autorem a dílem knihy.

Přečteno 12 webových stránek

Chápu vaši ambici. Pracujete na díle, které je svým záběrem průřezové a významově zcela nové. Standardní open-source licence, které jsme dosud probírali, jsou pro tento případ příliš hrubým nástrojem.

Potřebujete **vícevrstevný právní rámec**, který bude chránit velké koncepty, propojení s vaším autorstvím a umožní vám řídit, jak se s vaším dílem nakládá na různých úrovních.

### 📜 1. Hlavní licence: "Pouze ke čtení, bez odvozenin"

Pro samotné jádro vaší knihy a hlavní metodologii zvolte **Creative Commons Attribution-NoDerivatives (CC BY-ND)** [](https://creativecommons.org/licenses/by-nd/2.0/legalcode?trk=article-ssr-frontend-pulse_little-text-block)[](https://interoperable-europe.ec.europa.eu/licence/creative-commons-attribution-no-derivatives-40-international).

- **Proč právě tato?** Umožňuje komukoli (včetně univerzit) vaše dílo **šířit a sdílet**, ale **zakazuje vytvářet odvozená díla** (derivative works) [](https://creativecommons.org/licenses/by-nd/2.0/legalcode?trk=article-ssr-frontend-pulse_little-text-block)[](https://interoperable-europe.ec.europa.eu/licence/creative-commons-attribution-no-derivatives-40-international). To znamená, že nikdo nesmí vaše koncepty převyprávět, parafrázovat nebo je začlenit do svého vlastního díla, aniž by porušil licenci.
    
- **Záruka autorství:** Vynucuje povinné uvedení vašeho jména (attribution) [](https://creativecommons.org/licenses/by-nd/2.0/legalcode?trk=article-ssr-frontend-pulse_little-text-block)[](https://interoperable-europe.ec.europa.eu/licence/creative-commons-attribution-no-derivatives-40-international). Tím si zajišťujete, že každé použití bude trvale spojeno s vaším jménem.
    
- **Nevýhoda:** Tato licence zakazuje i **nekomerční** úpravy. To je ale přesně to, co chcete – kontrolovat, kdo a jak vaše "velká témata" rozvíjí.
    

### 🧪 2. Experimentální data: Model "Všechna práva vyhrazena"

Data z vašich chatů a experimentů jsou unikátní a cenná. Zde byste měli zvolit nejpřísnější přístup.

- **Data User Agreement (DUA):** Toto není licence, ale smlouva o užití dat, která je vhodnější pro data, která mohou obsahovat citlivé informace [](https://open-brain-consent.readthedocs.io/en/latest/gdpr/data_user_agreement.html#translations). V DUA můžete jasně stanovit, že data smí být použita **výhradně** pro ověření vašich výsledků, nikoli pro trénink jiných modelů nebo pro komerční účely [](https://open-brain-consent.readthedocs.io/en/latest/gdpr/data_user_agreement.html#translations).
    
- **Praktický důsledek:** Zveřejníte data "tak, jak jsou" (as-is), ale každý, kdo si je bude chtít stáhnout, musí **výslovně souhlasit s vašimi podmínkami**. To vám dává maximální kontrolu [](https://open-brain-consent.readthedocs.io/en/latest/gdpr/data_user_agreement.html#translations).
    

### 🔬 3. Výzkumné záměry: Dvoustupňový model

Vaše obava, že univerzita zneužije váš výzkum pro vlastní projekty, je oprávněná. Zde vstupuje do hry **dvoustupňový model**, který se osvědčil v akademickém prostředí [](https://opendl.ifip-tc6.org/db/conf/hcc/hcc2006/Dedeurwaerdere06.pdf#2#2):

1. **Veřejná (open-science) úroveň:** Pro nekomerční akademický výzkum, který se drží vašich pravidel, platí licence **CC BY-ND** (viz bod 1). To je "povolení" pro standardní vědeckou práci.
    
2. **Komerční / rozšířená úroveň:** Pokud by univerzita (nebo kdokoli jiný) chtěla vaše dílo použít způsobem, který licence CC BY-ND nepovoluje (např. vytvořit odvozené dílo, použít pro komerční výzkum, patentovat vaši metodu), musí s vámi **uzavřít samostatnou smlouvu** [](https://opendl.ifip-tc6.org/db/conf/hcc/hcc2006/Dedeurwaerdere06.pdf#2#2). V této smlouvě si můžete vyjednat podmínky – od finančního vypořádání až po kontrolu nad směřováním výzkumu.
    

### 🧠 4. Extra vrstva: "Moral Rights" a OSL-3.0

Máte zájem o propojení s autorem a dílem na hlubší úrovni. Zde mohou pomoci dva aspekty:

- **Moral Rights (Osobnostní práva):** Žádná licence na světě vám neumožňuje se jich vzdát (jsou nepřevoditelná). Dávají vám právo **bránit se jakémukoli zásahu do vašeho díla, který by poškozoval vaši pověst nebo integritu**. V případě sporu se můžete dovolávat právě jich [](https://interoperable-europe.ec.europa.eu/licence/creative-commons-attribution-no-derivatives-40-international).
    
- **Open Software License 3.0 (OSL-3.0):** Možná se to zdá jako nástroj pro software, ale pro vás je klíčová jedna jeho vlastnost: **explicitní udělení patentových práv** a specifický mechanismus ukončení licence v případě patentových sporů [](https://api.github.com/licenses/osl-3.0)[](https://pkg.go.dev/github.com/3052/blog@v0.0.0-20240601103935-e2cf438dd861/2024-01/gen-doc?tab=licenses). Zvažte použití OSL-3.0 pro jakoukoli **univerzální metodu nebo algoritmus**, který vaše dílo obsahuje. OSL-3.0 totiž vyžaduje, aby **jakékoli šíření díla bylo pod stejnou licencí (copyleft)** a zároveň poskytuje **patentovou ochranu** [](https://api.github.com/licenses/osl-3.0).
    

### 📋 Kontrolní seznam pro váš repozitář

1. `LICENSE` (kořen repozitáře): Text **CC BY-ND 4.0**.
    
2. `DATA_LICENSE.md` (ve složce s daty): Text **Data User Agreement** (vlastní verze, která zakazuje komerční využití a trénink modelů).
    
3. `README.md`: Jasný odkaz na obě licence a **krátké prohlášení o vašich autorských a výzkumných záměrech**.
    
4. `TERMS_OF_USE.md`: Detailní dokument, který definuje:
    
    - Co je "nekomerční akademický výzkum".
        
    - Že pro jakékoli **odvozené dílo** nebo **komerční využití** je vyžadován váš předchozí písemný souhlas.
        
    - Že si vyhrazujete právo na **patentovou ochranu** vašich metod (a odkaz na OSL-3.0, pokud je to relevantní).
        
5. `CONTRIBUTING.md`: Jasně uveďte, že **nepřijímáte Pull Requesty** s novelizacemi textu, ale výhradně návrhy na doplnění do samostatné sekce "Poznámky a diskuze". Tím zabráníte snahám o "forknutí" vašeho hlavního díla.
    

Tento přístup je právně konzistentní, chrání vaše "velká témata" před nekontrolovaným šířením a zároveň dává univerzitám jasný rámec, ve kterém se mohou pohybovat, aniž by vás obtěžovaly s každým drobným projektem. Zároveň si ale vyhrazujete právo rozhodovat o strategických směrech.

Jak v repozitáři měnit strukturu? Budu mít více složek, v nich více souborů, předpokládám že jde o hlavní větev, ale jak zařídit přesun z hlavní větve do délčích souborů do archivu? Jen tím, že se to šoupne do archivní složky a v commitu se to propíše jako přesun ve struktuře, ale git to bere pořád jako hlavní větev, uživatel už za mrtvou část?

Vaše úvaha je naprosto správná. **Přesun souborů do archivní složky a jejich ponechání v hlavní větvi je technicky jednoduché, ale z hlediska verzování a přehlednosti projektu to není ideální.**

Git a GitHub nabízejí k řešení této situace **dvě zcela odlišné filozofie**, z nichž každá má své výhody a nevýhody. Vyberte si podle toho, jak chcete, aby vaše historie vypadala.

---

### 1. 🗂️ Varianta "Archiv ve větvi" (Vaše představa)

Přesunete soubory do složky `archiv/` a dáte commit.

- **Ano**, Git to bere jako **přesun** (rename) souborů, nikoli jako jejich smazání a nové vytvoření. Historie souboru zůstane zachována a lze ji vysledovat (`git log --follow`).
    
- **Co se stane s uživatelem?** Uživatel, který si stáhne hlavní větev, uvidí soubory ve složce `archiv/`. Stále jsou to **aktivní soubory** v aktuální verzi, jen fyzicky leží jinde.
    

**Kdy to použít:**

- Chcete, aby archivované soubory byly stále **snadno dostupné** všem, kdo si repozitář klonují.
    
- Soubory v archivu jsou malé a nezvětšují repozitář nad doporučené limity .
    
- Nechcete komplikovat historii větvením.
    

**Nevýhoda:** Hlavní větev se časem nafukuje o soubory, které už nejsou aktivní. Pokud jich bude mnoho, může to zpomalit práci s repozitářem.

---

### 2. 🌿 Varianta "Archiv ve větvi" (True Git way)

Vytvoříte samostatnou větev (např. `archiv`) a do hlavní větve (`main`) soubory **smažete** (nebo je přesunete do archivu a smažete z `main`).

- **Jak to udělat:**
    
    1. Vytvoříte novou větev: `git checkout -b archiv`
        
    2. V této větvi necháte staré soubory beze změny (nebo je přesunete do složky `archiv`).
        
    3. Přepnete se zpět do `main`: `git checkout main`
        
    4. Smažete staré soubory z `main`: `git rm stary_soubor.md`
        
    5. Dáte commit a push.
        
- **Co se stane s uživatelem?** Uživatel, který si stáhne hlavní větev, uvidí jen aktuální, "živé" soubory. Pokud by chtěl vidět archiv, musí si stáhnout větev `archiv`.
    

**Kdy to použít:**

- Chcete udržet hlavní větev **čistou a přehlednou** pouze pro aktivní vývoj.
    
- Archivované soubory jsou velké nebo je jich hodně a nechcete, aby zatěžovaly každodenní práci.
    
- Chcete jasně oddělit **aktivní** a **historický** obsah.
    

**Nevýhoda:** Uživatelé musí vědět o existenci větve `archiv` a aktivně si ji stáhnout, pokud ji chtějí vidět. Není to tak "na první pohled" jako složka.

---

### 3. 🏷️ Varianta "Archiv jako Tag" (Pro finální verze)

Pokud chcete zachovat přesný snímek (snapshot) projektu v určitém okamžiku (např. "hotová kapitola 3"), vytvořte **Tag**.

- **Jak to udělat:** `git tag -a archiv-kapitola3 -m "Archiv kapitoly 3"` a pak `git push --tags`.
    
- **Co to je:** Tag je **neměnný** ukazatel na konkrétní commit v historii. Je to jako "záložka" v čase.
    
- **Co se stane s uživatelem?** Uživatel si může stáhnout konkrétní tag a dostane přesně tu verzi, která v tom okamžiku existovala. Hlavní větev přitom může pokračovat dál.
    

**Kdy to použít:**

- Chcete označit **milníky** (např. "verze 1.0", "kapitola 5 hotova").
    
- Nechcete, aby se historie větvila nebo se do hlavní větve ukládaly neaktivní soubory.
    

---

### ✅ Doporučení pro vaši knihu

Vzhledem k vašemu záměru (kniha, experimentální data, návody) bych doporučil **kombinaci**:

1. **Hlavní větev (`main`)** obsahuje vždy **pouze aktuální verzi knihy** a aktivní experimentální data.
    
2. **Archiv starých kapitol / metod**: Přesuňte je do složky `archiv/` v rámci **hlavní větve**, ale v `README.md` jasně označte, že tato složka obsahuje historické verze a nemusí být relevantní pro nové čtenáře.
    
3. **Finální verze knihy (PDF)** uložte jako **Release** (vydání) na GitHubu, nikoli do historie repozitáře.
    
4. **Klíčové milníky** (např. "první verze knihy hotova", "data pro studii X") označte **Tagy**.
    

Tento přístup udrží hlavní větev přehlednou, archivované soubory dostupné a zároveň umožní snadnou orientaci v historii projektu.

OK, takže když smažu soubor smaže se i v Gitu? A pak, vlastně před tím jej přesunu do vedlejší větve, kde půjde se všemi commity.

Odpověď na obě vaše otázky zní **ANO**, ale s důležitými detaily, které potřebujete znát, abyste nepřišli o svou práci.

---

### 1. "Když smažu soubor, smaže se i v Gitu?"

**ANO a NE.** Záleží na tom, **kdy** soubor smažete.

- **Smažete-li soubor, který už je v Gitu zaznamenaný (commitnutý):**
    
    - Git si ho **pamatuje ve své historii**. Smazáním ho pouze odstraníte z **aktuální verze** (z hlavní větve).
        
    - Soubor ale pořád existuje ve všech předchozích commitech. Můžete se k němu kdykoli vrátit (např. pomocí `git checkout <hash_commitu> -- smazany_soubor.txt`).
        
    - **Git ho fyzicky nevymaže z disku** (pokud nepoužijete speciální nástroje). Zůstává v databázi `.git` jako historický záznam.
        
- **Smažete-li soubor, který jste **ještě nikdy necommitnuli** (např. jen ho vytvořili a neuložili do Gitu):**
    
    - Pak ho Git **nezná** a smazáním ho ztratíte navždy (pokud ho nemáte zálohovaný jinde).
        

**Technicky vzato:** Příkaz `git rm soubor.txt` smaže soubor z pracovního adresáře **a** zaregistruje toto smazání jako změnu pro příští commit. Soubor ale zůstává v předchozích commitech uložený.

---

### 2. "Když ho před smazáním přesunu do vedlejší větve, půjde se všemi commity?"

**PŘESNĚ TAK.** A to je ten správný postup, jak si zachovat plnou historii.

#### Jak na to krok za krokem:

1. **Jste v hlavní větvi (`main`)** a chcete přesunout starou kapitolu `kapitola3.md` do archivu.
    
2. **Vytvoříte novou větev pro archiv** (ta bude obsahovat i soubor s celou jeho historií):
    
    bash
    
    git checkout -b archiv/kniha
    
    Tím jste vytvořili větev, která je v tomto okamžiku **identická** s `main`.
    
3. **V této nové větvi (`archiv/kniha`) soubor necháte** – nic s ním neděláte. Je tam přesně tak, jak byl.
    
4. **Přepnete se zpět do hlavní větve:**
    
    bash
    
    git checkout main
    
5. **Zde soubor smažete:**
    
    bash
    
    git rm kapitola3.md
    
6. **Commitnete smazání v hlavní větvi:**
    
    bash
    
    git commit -m "Přesun kapitoly 3 do archivu (větev archiv/kniha)"
    
7. **Nahrajete obě větve na GitHub:**
    
    bash
    
    git push origin main
    git push origin archiv/kniha
    

**Výsledek:**

- Hlavní větev (`main`) už soubor neobsahuje.
    
- Větev `archiv/kniha` obsahuje soubor **se všemi jeho historickými commity** (kdy byl vytvořen, upravován, atd.).
    
- Nikdo o nic nepřišel. Každý, kdo si stáhne větev `archiv/kniha`, uvidí kompletní historii daného souboru.
    

---

### ⚠️ Důležité upozornění: "Co když uživatelé mají staženou hlavní větev?"

Když vy smažete soubor v `main` a nahrajete to na GitHub, uživatelé, kteří si udělají `git pull` na své lokální `main`, **ten soubor ztratí ve svém pracovním adresáři** (protože Git ho smaže, aby odpovídal vzdálené verzi).

Pokud ale chtějí soubor znovu získat, stačí, aby si přepnuli na větev `archiv/kniha`:

bash

git checkout archiv/kniha

a soubor se jim opět objeví v pracovní složce.

---

### ✅ Shrnutí

|Akce|Výsledek|
|---|---|
|Smažete soubor v Gitu (commitnutý)|Zmizí z aktuální verze, ale zůstane v historii.|
|Smažete soubor, který není commitnutý|Ztratíte ho navždy.|
|Přesunete soubor do jiné větve a smažete v hlavní|Soubor žije dál ve vedlejší větvi **i se všemi commity**, hlavní větev zůstane čistá.|

Vaše intuice vás nezklamala – přesun do vedlejší větve je elegantní a bezpečné řešení, jak archivovat, aniž byste přišli o historii.

Jasně. Commit je jen uložení repozitáře (změn) na GitHub.

**Téměř, ale ne úplně.** Je to časté zjednodušení, ale je v tom jeden zásadní rozdíl.

Pojďme to rozlišit:

### 🔍 Commitem se NIC nenahrává na GitHub

- **Commit** je lokální operace. Uloží vaše změny **jen do vašeho počítače** (do lokálního repozitáře ve složce `.git`).
    
- Dáte-li `git commit`, vytvoří se nový snímek vašich souborů, ale **GitHub o tom zatím nemá ani tušení**. Jste stále offline, nikam se nic neposílá.
    

### ☁️ Na GitHub se nahrává až Push

- Aby se commit dostal na GitHub, musíte provést **Push** (`git push`).
    
- **Push** odešle všechny vaše lokální commity na vzdálený server (GitHub).
    

---

### 🧠 Přesná definice

|Operace|Co dělá|Kde se ukládá|
|---|---|---|
|**Commit**|Uloží snímek změn do lokální historie|**Pouze na vašem disku** (složka `.git`)|
|**Push**|Odešle všechny nové commity na GitHub|**Na GitHub server** (do cloudu)|

---

### 💡 Proč to nestačí vědět, ale musíte to chápat?

Protože to ovlivňuje vaši práci:

1. **Můžete commitovat offline:** Když jste na cestách bez internetu, můžete klidně ukládat commity. Nahrát je (push) můžete, až se připojíte.
    
2. **Commit není záloha:** Když uděláte commit ale neuděláte push, váš počítač může shořet a všechny commity jsou pryč. **Teprve push je bezpečná záloha na GitHubu.**
    
3. **GitHub nevidí vaši práci, dokud neuděláte push:** Spolupracovníci neuvidí vaše změny, dokud je neodešlete.
    

---

### ✅ Opravená věta (pro vaši knihu)

> **Commit** je uložení změn do **lokální historie na mém disku**.  
> **Push** je odeslání těchto commitů na **GitHub** (cloud).

Takže pokud chcete, aby vaše kniha, data a návody byly dostupné na GitHubu pro vaši komunitu, musíte vždy udělat **commit** (uložit lokálně) a pak **push** (nahrát na GitHub). Teprve pak je obsah online.

OK. Jak se pracuje na projektu v rámci komunity? Jsou tam komentáře? Chaty? jak to funguje? Musí být nějaký správce, nebo se předpokládá, že jsou všichni slušní?

Přečteno 9 webových stránek

Práce na projektu v rámci komunity na GitHubu se točí kolem otevřené komunikace pomocí specializovaných nástrojů a důležitou roli v ní hraje jak určitá míra samosprávy, tak i aktivní moderování.

### 🗣️ Komunikační nástroje: Komentáře, Chaty a Diskuse

GitHub není sociální síť v klasickém slova smyslu, ale nabízí **tři hlavní typy nástrojů pro komunikaci**, z nichž každý slouží k něčemu jinému[](https://docs.github.com/en/enterprise-cloud@latest/get-started/using-github/communicating-on-github)[](https://docs.github.com/en/enterprise-server@3.16/get-started/using-github/communicating-on-github#which-discussion-tool-should-i-use):

- **Issues (Úkoly):** Slouží pro **konkrétní a strukturovanou komunikaci**, která směřuje k řešení. Jsou to téměř výhradně nástroje pro hlášení chyb, návrhy na vylepšení nebo sledování úkolů[](https://docs.github.com/en/enterprise-cloud@latest/get-started/using-github/communicating-on-github)[](https://docs.github.com/en/enterprise-server@3.16/get-started/using-github/communicating-on-github#which-discussion-tool-should-i-use). Mívají jasného "vlastníka" a jejich výsledkem je zpravidla akce (např. oprava chyby)[](https://docs.github.com/en/enterprise-cloud@latest/get-started/using-github/communicating-on-github).
    
- **Pull Requests (Požadavky na stažení):** Komunikace zde probíhá **přímo nad navrženými změnami kódu nebo textu** (ve vašem případě kapitol knihy). Je to prostor pro kontrolu, připomínkování a diskuzi o konkrétních úpravách, než se stanou součástí hlavního projektu[](https://docs.github.com/en/enterprise-cloud@latest/get-started/using-github/communicating-on-github)[](https://docs.github.com/en/enterprise-server@3.16/get-started/using-github/communicating-on-github#which-discussion-tool-should-i-use).
    
- **GitHub Discussions (Diskuze):** To je to, co se nejvíce blíží **"komunitnímu fóru" nebo "chatu"**[](https://docs.github.com/en/enterprise-server@3.16/discussions/quickstart)[](https://docs.github.com/en/enterprise-cloud@latest/get-started/using-github/communicating-on-github)[](https://docs.github.com/en/enterprise-server@3.16/get-started/using-github/communicating-on-github#which-discussion-tool-should-i-use). Je to ideální prostor pro otevřené rozhovory, které nemusí nutně vést k okamžité akci – brainstorming, sdílení novinek, kladení otázek a obecná diskuze o směřování projektu[](https://docs.github.com/en/enterprise-server@3.16/discussions/quickstart)[](https://docs.github.com/en/enterprise-cloud@latest/get-started/using-github/communicating-on-github)[](https://docs.github.com/en/enterprise-server@3.16/get-started/using-github/communicating-on-github#which-discussion-tool-should-i-use). Komentáře zde mohou být volnější.
    

### 🛡️ Role Správce a Moderování

**Předpoklad, že jsou všichni slušní, by byl naivní, a GitHub s tím počítá.** Platforma proto nabízí propracovaný systém pravidel a moderátorských nástrojů. Zároveň ale nejste v tom, kdo musí vše hlídat, sami.

#### 1. Jasná Pravidla: `CODE_OF_CONDUCT.md`

Prvním krokem je vytvoření **pravidel chování** (Code of Conduct)[](https://github.com/jatinkumar11954/community/blob/main/CODE_OF_CONDUCT.md)[](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/about-community-management-and-moderation)[](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/adding-a-code-of-conduct-to-your-project). Tento dokument definuje standardy a očekávání pro zapojení v komunitě – signál, že jde o vstřícné a respektující prostředí[](https://github.com/jatinkumar11954/community/blob/main/CODE_OF_CONDUCT.md)[](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/adding-a-code-of-conduct-to-your-project). GitHub nabízí i šablony pro jeho snadné vytvoření[](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/adding-a-code-of-conduct-to-your-project). Kromě toho můžete přidat i soubor s návodem pro přispěvatele (`CONTRIBUTING.md`), aby bylo jasné, jak a kde se komunikace vede[](https://docs.github.com/en/enterprise-server@3.16/discussions/quickstart)[](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/about-community-management-and-moderation).

#### 2. Nástroje pro Moderování (na úrovni správce)

Jako správce repozitáře máte k dispozici řadu nástrojů, jak udržovat komunitu zdravou a bezpečnou[](https://docs.github.com/en/enterprise-server@3.16/discussions/quickstart)[](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/about-community-management-and-moderation):

- **Uzamčení diskuze (Locking):** Pokud konverzace přestane být produktivní a začne být vyhrocená, můžete ji zamknout a zabránit tak dalším komentářům[](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/about-community-management-and-moderation).
    
- **Skrytí komentáře (Hiding):** Komentáře, které porušují pravidla, můžete skrýt, aby je ostatní neviděli[](https://github.com/benbalter/ai-community-moderator).
    
- **Označení odpovědi (Marking as Answer):** V rámci GitHub Discussions můžete označit užitečné odpovědi, což pomáhá budovat komunitní znalostní bázi a orientaci[](https://docs.github.com/en/enterprise-server@3.16/discussions/quickstart).
    
- **Připnutí (Pinning) a Mazání (Deleting):** Důležité diskuse můžete připnout na viditelné místo, a naopak ty nežádoucí smazat[](https://docs.github.com/en/enterprise-server@3.16/discussions/quickstart).
    

#### 3. Automatizace Moderování: AI Moderátor

Velmi zajímavou možností pro vaše téma (multidisciplinarita, LLM) je využití **AI pro moderování komunity**. Na GitHubu existují nástroje, například **AI Community Moderator**, což je GitHub Action, která umí automaticky analyzovat nové příspěvky v Issues, Pull Requestech a Discussions[](https://github.com/benbalter/ai-community-moderator).

Tento nástroj:

- **Kontroluje obsah** oproti vašemu `CODE_OF_CONDUCT.md` a `CONTRIBUTING.md`[](https://github.com/benbalter/ai-community-moderator).
    
- **Hodnotí závažnost** porušení na škále 1–10 a na základě toho může automaticky reagovat – napsat výchovný komentář, skrýt nevhodný obsah nebo diskuzi uzamknout[](https://github.com/benbalter/ai-community-moderator).
    
- Můžete nastavit, jak přísný má být (např. práh pro zásah)[](https://github.com/benbalter/ai-community-moderator).
    

Tento přístup by mohl být velmi efektivní pro správu komunity a uvolnil by vám ruce pro obsahovou práci.

### 🧑‍🤝‍🧑 Kdo může co dělat?

Přístupová práva se odvíjejí od vašeho nastavení. Každý, kdo má k repozitáři přístup (např. pro veřejný repozitář je to kdokoli), může vytvářet nové diskuze a komentovat[](https://docs.github.com/en/enterprise-server@3.16/discussions/quickstart). Pro moderování a správu ale potřebujete určitá oprávnění:

- **Write přístup** k repozitáři: Umožňuje vytvářet nové kategorie diskuzí, připínat je, mazat je nebo je převádět mezi repozitáři[](https://docs.github.com/en/enterprise-server@3.16/discussions/quickstart).
    
- **Triage přístup**: Umožňuje označovat odpovědi, uzamykat diskuze nebo převádět Issues na Diskuze[](https://docs.github.com/en/enterprise-server@3.16/discussions/quickstart).
    
- **Admin přístup**: Poskytuje plnou kontrolu včetně nastavení repozitáře a správy ostatních uživatelů.
    

**Stručně řečeno:** Komunikace na GitHubu je strukturovaná, nikoli chaotická. Existují jasné nástroje pro různé typy konverzací. Spoléhat se pouze na slušnost nestačí, ale GitHub vám dává do rukou nástroje, jak si vlastní pravidla nastavit a vymáhat – a díky AI moderátorovi to můžete z velké části i automatizovat. Vaše role správce je tak spíše o nastavení rámce než o každodenním "hašení požárů".

GitHub Discussions (Diskuze): Jde o jednu diskusi, nebo o organizaci, např. přiřazení k určitému souboru?

Přečteno 11 webových stránek

GitHub Discussions (**Diskuze**) představuje mnohem víc než jen jednu konverzaci. Je to **plnohodnotné diskusní fórum, které je možné uspořádat do kategorií**, abyste měli přehled o tom, o čem se mluví [](https://docs.github.com/ru/discussions/managing-discussions-for-your-community/managing-categories-for-discussions)[](https://docs.github.com/zh/discussions/managing-discussions-for-your-community/managing-categories-for-discussions)[](https://docs.github.com/pt/discussions/managing-discussions-for-your-community/managing-categories-for-discussions).

Diskuze nejsou přímo přiřazeny k jednotlivým souborům jako komentáře v kódu. Jsou určeny pro otevřené rozhovory, které přesahují konkrétní řádky kódu [](https://docs.github.com/ru/discussions/quickstart)[](https://docs.github.com/en/discussions/quickstart)[](https://docs.github.com/ru/enterprise-server@3.10/get-started/using-github/communicating-on-github#which-discussion-tool-should-i-use).

### 🧭 Jak jsou diskuze organizovány?

Organizace diskuzí se liší podle toho, zda jsou vedeny na úrovni **celé vaší organizace** (např. pod vaším uživatelským jménem), nebo na úrovni **konkrétního repozitáře**.

**Kategorie (Categories)**  
Každá diskuze musí spadat do jedné kategorie [](https://docs.github.com/ru/discussions/managing-discussions-for-your-community/managing-categories-for-discussions)[](https://docs.github.com/zh/discussions/managing-discussions-for-your-community/managing-categories-for-discussions). Je to jako zařazení příspěvku do správné "přihrádky" v diskuzním fóru.

- **Výchozí kategorie:** GitHub automaticky vytvoří několik základních kategorií, např.:
    
    - `📣 Announcements` (Oznámení) – pouze pro správce [](https://docs.github.com/ru/discussions/managing-discussions-for-your-community/managing-categories-for-discussions)[](https://docs.github.com/pt/discussions/managing-discussions-for-your-community/managing-categories-for-discussions).
        
    - `💡 Ideas` (Nápady) – pro návrhy na vylepšení [](https://docs.github.com/ru/discussions/managing-discussions-for-your-community/managing-categories-for-discussions).
        
    - `🙏 Q&A` (Dotazy a odpovědi) – pro otázky, na které hledáte odpověď od komunity [](https://docs.github.com/ru/discussions/managing-discussions-for-your-community/managing-categories-for-discussions).
        
    - `🗳 Polls` (Ankety) – pro hlasování komunity [](https://docs.github.com/ru/discussions/managing-discussions-for-your-community/managing-categories-for-discussions)[](https://docs.github.com/zh/discussions/managing-discussions-for-your-community/managing-categories-for-discussions).
        
    - `#️⃣ General` (Obecné) – pro cokoli ostatního [](https://docs.github.com/ru/discussions/managing-discussions-for-your-community/managing-categories-for-discussions)[](https://docs.github.com/ja/enterprise-server@3.20/discussions/managing-discussions-for-your-community/managing-categories-for-discussions).
        
- **Vlastní kategorie:** Jako správce můžete vytvářet vlastní kategorie, aby lépe odpovídaly potřebám vašeho projektu (např. "Diskuze o knize", "Experimentální data", "Metodologie"). Na jeden repozitář nebo organizaci můžete mít až **25 kategorií** [](https://docs.github.com/ru/discussions/managing-discussions-for-your-community/managing-categories-for-discussions)[](https://docs.github.com/ru/discussions/quickstart).
    

**Sekce (Sections)**  
Pro ještě lepší přehlednost můžete kategorie sdružovat do **sekcí**. Představte si to jako záložky na úvodní stránce fóra. Například jedna sekce "Komunita" může obsahovat kategorie "Představení" a "Obecná diskuze" a sekce "Vývoj" kategorie "Nápady" a "Q&A" [](https://docs.github.com/ru/discussions/managing-discussions-for-your-community/managing-categories-for-discussions)[](https://github.com/orgs/community/discussions/190887).

### 🌐 Diskuze na úrovni organizace vs. repozitáře

- **Diskuze v repozitáři:** Jsou "připoutány" k jednomu konkrétnímu repozitáři. Jsou viditelné na stránce tohoto repozitáře a práva v nich (kdo může mazat diskuze apod.) se odvíjejí od práv uživatele k tomuto repozitáři [](https://docs.github.com/ru/discussions/managing-discussions-for-your-community/managing-categories-for-discussions)[](https://docs.github.com/en/discussions/quickstart).
    
- **Diskuze v organizaci:** Fungují napříč celou vaší organizací (např. pod vaším jménem). To je ideální, pokud máte více repozitářů (např. jeden pro knihu, jeden pro data) a chcete, aby komunita diskutovala o projektech dohromady. Stále se ale vážou k jednomu "zdrojovému" repozitáři, který určuje, kdo má jaká práva [](https://docs.github.com/ru/discussions/quickstart)[](https://docs.github.com/en/discussions/quickstart).
    

### 🏷️ Další možnosti organizace

Kromě kategorií a sekcí můžete pro ještě přesnější třídění používat **štítky (labels)**. Stejnou sadu štítků můžete využívat pro Issues, Pull Requesty i Diskuze [](https://docs.github.com/ru/discussions/quickstart)[](https://docs.github.com/en/discussions/quickstart).

### ✅ Shrnutí

Diskuze na GitHubu jsou víc než jedna konverzace. Jsou to **organizovaná fóra**, kde můžete:

1. **Vytvářet kategorie** (např. "Obecné", "Nápady", "Q&A") pro různé typy konverzací [](https://docs.github.com/ru/discussions/managing-discussions-for-your-community/managing-categories-for-discussions).
    
2. **Seskupovat kategorie do sekcí** pro lepší přehlednost [](https://docs.github.com/ru/discussions/managing-discussions-for-your-community/managing-categories-for-discussions).
    
3. **Využívat štítky** pro detailnější kategorizaci [](https://docs.github.com/ru/discussions/quickstart).
    

To vše vám jako správci umožňuje udržet komunikační kanály vašeho projektu přehledné a přístupné pro vaši komunitu.

Je žádoucí pokud očekávám, že repozitář může být virální zveřejnit email?

**Krátká odpověď:** **NE, není to žádoucí.** Pokud očekáváte, že váš repozitář bude "virální" (tj. získá velkou popularitu a pozornost), **rozhodně byste svůj soukromý e-mail (ať už Gmail, nebo firemní) neměl zveřejňovat v commitech ani v README.**

### 🧠 Proč ne?

1. **Cílený spam a phishing:** Automatické scrapery neustále procházejí veřejné repozitáře na GitHubu a sbírají e-mailové adresy z commitů, README a dalších souborů. Pokud váš projekt nabere na popularitě, stanete se terčem nevyžádané pošty, phishingu a pokusů o sociální inženýrství.
    
2. **Ztráta soukromí:** Vaše e-mailová adresa se stane veřejně dohledatelnou. Kdokoli si ji může spojit s vaším jménem, profilem a projektem. To může být nežádoucí z hlediska osobního i profesního života.
    
3. **Obtěžování a tlak komunity:** Velké projekty přitahují nejen nadšené přispěvatele, ale i lidi s extrémními názory, nespokojené uživatele nebo ty, kteří budou chtít, abyste řešili jejich problémy. Veřejný e-mail je pro ně snadným cílem.
    
4. **Firemní politika a právní rizika:** Pokud používáte firemní e-mail, vystavujete se riziku, že vaše komunikace bude považována za oficiální stanovisko firmy. Navíc univerzity a firmy často zakazují používání firemních e-mailů pro osobní open-source projekty kvůli autorským právům a odpovědnosti.
    

---

### ✅ Co dělat místo toho?

#### 1. Používejte GitHub `noreply` anonymní adresu (NAPŘÍKLAD)

- GitHub vygeneruje adresu ve tvaru `ID+uzivatelskejmeno@users.noreply.github.com`.
    
- Nastavte ji jako svůj `user.email` v lokálním Gitu.
    
- **Výsledek:** Veřejnost uvidí jen anonymní adresu, ale GitHub si ji interně spojí s vaším účtem (commity se zobrazí pod vaším profilem).
    

#### 2. Pro komunikaci s komunitou používejte GitHub nástroje

- **Kontakt na vás:** V `README.md` uveďte odkaz na svůj GitHub profil, nikoli e-mail.
    
- **Otázky a diskuze:** Povzbuďte komunitu, aby používala **GitHub Discussions** nebo **Issues** pro veřejnou komunikaci.
    
- **Soukromé záležitosti:** Pro opravdu důvěrné dotazy si můžete vytvořit samostatný **"kontaktní" e-mail** (např. `mujprojekt@email.cz`), který použijete pouze pro tento účel a nebudete ho používat nikde jinde. Ale i ten se může stát terčem spamu.
    

#### 3. Vytvořte si "veřejný" e-mail

Pokud opravdu potřebujete uvést e-mail (např. kvůli licenčním podmínkám), vytvořte si **novou e-mailovou adresu** určenou výhradně pro open-source projekty. Nechte ji veřejnou, ale počítejte s tím, že na ni bude chodit spam.

---

### 📋 Shrnutí pro vás

|Co dělat|Co nedělat|
|---|---|
|✅ Používat GitHub `noreply` anonymní e-mail v commitech.|❌ Zveřejňovat svůj osobní Gmail v commitech.|
|✅ V `README.md` uvádět odkaz na GitHub profil.|❌ V `README.md` uvádět osobní e-mail.|
|✅ Komunikovat přes GitHub Discussions a Issues.|❌ Používat firemní e-mail pro veřejné projekty.|
|✅ Pro důvěrné dotazy vytvořit samostatný kontaktní e-mail.|❌ Spoléhat na to, že "nikdo to nebude zneužívat".|

**Závěr:** Ve virálním projektu je veřejný e-mail časovaná bomba. GitHub vám dává všechny nástroje, abyste se tomu vyhnuli – používejte je. Vaše soukromí a bezpečnost jsou důležitější než to, že někdo bude mít snadný způsob, jak vás kontaktovat. Komunita najde cestu, jak se k vám dostat přes GitHub.

Gmail mám jako email propojený s googlem Firemní mám nastavený jako primary. Mám zaškrtnuty ON: - Keep my email addresses private - Block command line pushes that expose my email Je tohle OK, nebo command line pushes nemám blokovat?

**Vaše nastavení je naprosto perfektní a je to přesně ta "zlatá standardní" konfigurace, kterou by měl mít každý, kdo pracuje na veřejných repozitářích.** Můžete to mít zapnuté obojí, není v tom žádný konflikt.

Pojďme si říct, proč je to ideální a co přesně ta druhá volba dělá (protože je často nepochopená).

---

### ✅ 1. "Keep my email addresses private" (zapnuto) – SPRÁVNĚ

Toto je vaše **hlavní obranná linie**.

- **Co dělá:** GitHub vygeneruje vaši anonymní `noreply` adresu (`ID+jmeno@users.noreply.github.com`) a ve webovém rozhraní GitHubu (v commitech, issues, PR) **zobrazuje vždy tuto anonymní adresu, nikoli váš firemní nebo Gmail**.
    
- **Proč je to správně:** I kdybyste omylem commitnul s firemním emailem, GitHub ho na webu **překryje** touto anonymní adresou. Vaše soukromí je chráněno na úrovni serveru.
    

---

### ⚙️ 2. "Block command line pushes that expose my email" (zapnuto) – TAKÉ SPRÁVNĚ

Toto je vaše **záložní bezpečnostní síť** (druhá vrstva ochrany).

- **Co dělá:** Když se pokusíte nahrát (push) commity na GitHub a **lokální Git má nastavený jiný e-mail**, než který máte ověřený na GitHubu (např. tam omylem dáte `novy@seznam.cz`, který jste si nikdy nepřidali), GitHub **push zablokuje** a nepustí ho na server.
    
- **Proč je to správně:**
    
    - Chrání vás před **"únikem"** e-mailu, který jste zapomněli správně nastavit v Gitu.
        
    - Nutí vás, abyste měli vždy nastavený **povolený e-mail** (buď firemní, nebo `noreply`).
        
    - Zabrání tomu, aby se ve veřejné historii objevil váš Gmail, když na něj zapomenete a omylem ho commitnete.
        

---

### 🧠 Jak to celé dohromady funguje?

Máte-li obojí zapnuté, vaše lokální Git musí mít nastavený e-mail, který je **na seznamu ověřených e-mailů na GitHubu**.

Máte dvě možnosti, co si nastavit lokálně:

|Lokální nastavení (`user.email`)|Výsledek po Push|
|---|---|
|`vas@firma.cz` (firemní, ověřený)|GitHub ho na webu **překryje** `noreply` adresou (díky první volbě). Nikdo ho neuvidí.|
|`ID+jmeno@users.noreply.github.com` (anonymní)|Push projde, v commitu je rovnou anonymní adresa.|

**Blokování (`Block command line pushes`)** se spustí **pouze tehdy**, pokud byste do Gitu omylem dali `mujsoukromy@gmail.com`, který na GitHubu **nemáte ověřený**. Pak vám GitHub řekne: _"Ne, tohle sem nepustím, protože by se tam objevil e-mail, který si nechceš zveřejňovat."_

---

### ❓ Takže mám "Block command line pushes" nechat zapnuté, nebo vypnout?

**ROZHODNĚ ZAPNUTÉ (ON).**

- Je to vaše pojistka proti vaší vlastní nepozornosti.
    
- Jediný důvod, proč byste to vypínali, je, pokud byste **opravdu chtěli**, aby se v commitech objevil konkrétní veřejný e-mail (např. máte vyhrazený e-mail pro open-source projekty, který chcete, aby byl vidět).
    
- Vy ale **nechcete**, aby byl vidět váš firemní ani Gmail, takže tuto pojistku **potřebujete**.
    

---

### ✅ Závěrečné doporučení

|Vaše nastavení|Stav|Verdikt|
|---|---|---|
|`Keep my email addresses private`|**ON**|✅ Správně (skrývá e-maily na webu)|
|`Block command line pushes that expose my email`|**ON**|✅ Správně (blokuje push s neschváleným emailem)|

Máte to nastavené naprosto ideálně. Teď už jen stačí, abyste si v lokálním Gitu nastavil `user.email` buď na svůj firemní e-mail, nebo na tu `noreply` adresu (obojí je ověřené a bezpečné).

Osobně doporučuji do Gitu rovnou napsat tu **`noreply` adresu** – je to nejčistší řešení. Firemní e-mail si pak můžete nechat v nastavení GitHubu jako "primární" pro interní notifikace, ale do commitů ho nedávat.

Jsou další settings, které mne mají zajímat než založím repozitář? nebo stačí default?

Odpověď je **ANO i NE**.

**Krátká verze:** Pro samotné založení repozitáře a základní práci **stačí výchozí nastavení**. GitHub je chytře navržený tak, aby fungoval "out of the box".

**Dlouhá verze (kterou chcete slyšet):** Pokud očekáváte, že váš projekt bude virální a budete na něm spolupracovat s komunitou, **existují 3 zásadní nastavení, která byste měl udělat hned na začátku**, než začnete lákat první přispěvatele. Ušetří vám to později hodiny dohadování a nervů.

Rozdělme to na **ta, která jsou v GitHub účtu (profilu)** a **ta, která se týkají konkrétního repozitáře**.

---

### 1. 🛂 Nastavení profilu (platí pro VÁS)

Tohle už máte z minula skvěle nastavené, ale pro úplnost:

|Nastavení|Kde najít|Doporučení|Proč?|
|---|---|---|---|
|**E-maily**|Settings → Emails|✅ **Zapnuto:** `Keep my email addresses private`  <br>✅ **Zapnuto:** `Block command line pushes...`|Už máte. Chrání vás před spamem.|
|**Dvoufaktorové ověření (2FA)**|Settings → Password and authentication|✅ **Zapnout (IDEÁLNĚ)**|GitHub to letos začíná vyžadovat pro všechny, kdo přispívají kódem. Chrání váš účet před hackery.|
|**Veřejný profil**|Settings → Profile|✅ Přidat fotku, jméno, web (pokud chcete)|Když se na vás komunita podívá, vidí, že nejste "prázdný anonymní účet". Buduje to důvěru.|

---

### 2. 🏗️ Nastavení repozitáře (platí pro VÁŠ PROJEKT)

Než ho založíte nebo hned po založení (v **Settings** daného repozitáře) udělejte toto:

#### A. Obecná nastavení (General)

- **Základní popis a web:** Hned při zakládání vyplňte **popis** a **URL** (pokud už máte doménu). Nechte si zatrhnout **"Add a README file"** (vždycky).
    
- **Jazyk / .gitignore:** Pokud budete přidávat HTML, CSS nebo Python skripty, GitHub umí automaticky vygenerovat `.gitignore` (seznam souborů, které se nikdy nebudou nahrávat, např. systémové složky). To je užitečné, ale není to kritické hned na začátku.
    

#### B. 🔐 Collaboration (Spolupráce) – TOHLE JE ZÁSADNÍ

1. **Branch protection rules (Pravidla ochrany hlavní větve):**
    
    - Přejděte do **Settings → Branches** a klikněte na **"Add branch protection rule"**.
        
    - Do pole **"Branch name pattern"** napište `main` (nebo `master`).
        
    - **Zapněte (zaškrtněte):**
        
        - ☑️ **"Require a pull request before merging"** – nikdo nehodí změny do hlavní knihy jen tak, musí to být přes Pull Request.
            
        - ☑️ **"Require approvals"** (nastavte na 1) – než se PR sloučí, musí ho někdo (třeba vy) schválit.
            
    - Toto nastavení **zabrání** tomu, aby do vaší knihy někdo nahrál změnu bez vašeho vědomí, i kdyby měl práva. Vy si ponecháte plnou kontrolu nad hlavním textem.
        
2. **Code owners (Vlastníci kódu/souborů):**
    
    - V kořeni repozitáře vytvořte soubor `.github/CODEOWNERS`.
        
    - Napište do něj: `* @vasUzivatelskeJmeno`
        
    - **Výsledek:** Když někdo pošle Pull Request, GitHub vás automaticky přiřadí jako recenzenta. Vy na to nezapomenete.
        

#### C. 🧩 Komunita a šablony (TEMPLATE)

Ve složce `.github/` (kterou si vytvoříte) můžete mít připravené šablony, které se objeví, když někdo založí nový Issue nebo Pull Request.

- **Na začátku doporučuji:** Vytvořte alespoň 3 soubory:
    
    - `CODE_OF_CONDUCT.md` (pravidla chování)
        
    - `CONTRIBUTING.md` (návod, jak přispívat)
        
    - Šablona pro Issue (aby vám lidé psali strukturovaně)
        

Toto nastavení dá vašemu projektu **profesionální vzhled** a řekne komunitě: _"Tady to myslíme vážně."_

---

### 3. ⚙️ Co naopak nemusíte řešit (zůstaňte na defaultu)

- **Webhooks, Actions, Secrets (tajné klíče)**: To jsou pokročilé věci pro automatizaci (např. automatické generování PDF knihy). Nechte je defaultní, dokud nezačnete budovat build proces.
    
- **Collaborators & Teams (Spolupracovníci)**: Zatím nikoho nepřidávejte. Jakmile začnou chodit Pull Requesty, rozhodnete se, komu dáte práva na zápis.
    

---

### ✅ Shrnutí: Co udělat před prvním commitem?

|Krok|Akce|Naléhavost|
|---|---|---|
|1|Zkontrolovat e-maily (už máte OK)|✅ Hotovo|
|2|**Vypnout možnost přímého push do `main`** (Branch protection)|🔥 **Udělat HNED**|
|3|Vytvořit `CODE_OF_CONDUCT.md` a `CONTRIBUTING.md`|🔥 **Udělat HNED** (nebo do týdne)|
|4|Nastavit dvoufaktorovku (2FA)|⚠️ **Doporučuji co nejdříve**|
|5|Zbytek (Actions, Webhooks) nechat na defaultu|✅ Můžete ignorovat|

**Závěr:** GitHub je skvělý v tom, že defaultní nastavení je bezpečné. **Jediné, co je opravdu kritické udělat hned, je ochrana hlavní větve (`main`),** aby vám tam nikdo nekecal bez vašeho vědomí. Všechno ostatní můžete doladit průběžně, jak vaše komunita poroste.

Tato odpověď je generována AI Assistantem, pouze pro referenci.

Git používá recovery code. Je to stejné jako seed v kryptu? Měl bych se k tomu takto chovat? Mít uloženo mimo PC na papíře např.

Vaše intuice je **naprosto přesná**. GitHub používá pro dvoufaktorové ověření (2FA) **recovery code (záložní kódy)**.  
Z hlediska bezpečnosti a přístupu k vašemu účtu jsou **na stejné úrovni jako seed (mnemotechnická fráze) v kryptu**.

Pokud o ně přijdete, **přijdete o přístup ke svému GitHubu**. Je to poslední záchranná síť, když ztratíte telefon s aplikací (např. Google Authenticator) nebo zapomenete heslo.

**Ano, měl byste se k nim chovat naprosto stejně jako k seedu:**

- ⚠️ **Nikdy je neukládejte do počítače jako prostý text** (do Wordu, Poznámkového bloku, ani do složky na ploše).
    
- ⚠️ **Nikdy je neposílejte e-mailem ani přes chat.**
    
- ✅ **Vytiskněte si je na papír** a uložte na bezpečné místo (trezor, sejf).
    
- ✅ **Napište si je ručně** do záložního notýsku (mimo dosah cizích lidí).
    

### 🔐 Proč je to tak důležité?

1. **Recovery kód = plný přístup:** Kdokoli, kdo získá vaše recovery kódy, se může přihlásit k vašemu GitHubu, i když nemá váš telefon ani heslo. Může vám ukrást repozitář, smazat ho, nebo vydávat se za vás v komunitě.
    
2. **GitHub je vaše "digitální identita":** Pro vás, jako autora knihy a metodologie, je GitHub klíčový. Ztráta účtu znamená ztrátu kontroly nad vaším dílem a kontaktem s komunitou.
    
3. **Neexistuje "obnovení" přes support:** Na rozdíl od banky vám GitHub účet neobnoví, když mu pošlete občanku. Bez recovery kódů a přístupu k telefonu je účet nenávratně ztracený.
    

### 📋 Co přesně udělat?

1. **Při nastavování 2FA na GitHubu** vám systém ukáže sadu **jednorázových záložních kódů** (obvykle 10 kódů).
    
2. **Neklikejte na "Skip" nebo "Done"**, dokud si je neuložíte!
    
3. **Vytiskněte si je** (nebo je ručně opište na papír).
    
4. **Papír uložte do trezoru / sejfu / bezpečné obálky.**
    
5. **Nezapisujte si je do mobilu (poznámky) ani do cloudu (Google Drive, iCloud).** V případě hacknutí cloudu jsou kódy kompromitované.
    
6. **Pro jistotu:** Recovery kódy můžete později v nastavení GitHubu (Settings → Password and authentication) **vygenerovat znovu** (zrušíte staré a dostanete nové). Dělejte to, pokud máte podezření, že je někdo viděl.
    

### 🧠 Srovnání se seedem v kryptu

|Aspekt|Seed (krypto peněženka)|GitHub Recovery kód|
|---|---|---|
|**Úroveň přístupu**|Plná kontrola nad kryptoměnami.|Plná kontrola nad GitHub účtem.|
|**Ztráta**|Ztráta přístupu k penězům navždy.|Ztráta přístupu k účtu navždy.|
|**Doporučené úložiště**|Papír v trezoru, kovová destička.|Papír v trezoru, bezpečná obálka.|
|**Nedoporučené úložiště**|Cloud, screenshot, poznámky v mobilu.|Cloud, screenshot, poznámky v mobilu.|
|**Kompromitace**|Kdokoli s ním ukradne vaše coiny.|Kdokoli s ním ukradne váš účet.|

### ✅ Shrnutí

Ano, je to **naprosto stejné**. Recovery kódy nejsou jen "heslo navíc", ale **poslední klíč od dveří**. Zacházejte s nimi s maximální opatrností, vytiskněte si je a fyzicky je uschovejte. Věřte mi, že až jednou omylem smažete Google Authenticator, budete za ten papír v trezoru nesmírně vděční.

Tato odpověď je generována AI Assistantem, pouze pro referenci.

Jak otestovat recovery code než jej smažu z PC? Jde to jen tím, že udělám recovery mimo přihlášení, nebo mají možnosti jako v kryptu? Vidím tam jen že mohu recovery code generovat nový, ale tím starý zanikne.

To je **velmi chytrá a zodpovědná otázka**. Bohužel, odpověď je přesně taková, jakou jste sám tušíte.

**GitHub nenabízí žádnou možnost, jak recovery kód "otestovat", aniž byste při tom skutečně neprovedli obnovu účtu.**

Neexistuje žádné tlačítko "Ověřit platnost kódu" jako u některých krypto peněženek. Museli byste se reálně odhlásit a zkusit se přihlásit pomocí recovery kódu, čímž byste ale **spotřebovali jeden z vašich kódů** (pokud to uděláte, systém vám ho po použití škrtne).

---

### 🧠 Proč to GitHub dělá?

Důvod je prostý a bezpečnostní: Recovery kódy jsou **jednorázové**. Jejich smyslem je, že každý kód může být použit právě jednou. Kdyby existovala funkce "otestovat kód", v podstatě byste si museli být jisti, že systém kód neoznačí jako použitý, což by mohlo vést k bezpečnostním dírám. GitHub proto zvolil cestu, která je sice méně pohodlná, ale bezpečnější: **kódy buď fungují, když je opravdu potřebujete, nebo nefungují.**

---

### 🔄 Co dělat, když si nejste jistý, že máte kódy správně opsané?

Tady je postup, který je ekvivalentem "otestování" v bezpečném režimu, aniž byste se odhlašovali:

#### ✅ Řešení: Vygenerujte si NOVOU SADU kódů

Protože máte stále přístup k účtu (jste přihlášeni), můžete si jednoduše **staré kódy zneplatnit a vygenerovat zcela nové**.

1. Jděte do **Settings → Password and authentication**.
    
2. V sekci **"Recovery codes"** klikněte na tlačítko **"Generate new recovery codes"**.
    
3. GitHub vás upozorní, že **tato akce zneplatní vaše předchozí recovery kódy**.
    
4. Potvrďte a **nové kódy si vytiskněte / uložte na papír**.
    

**Výhoda:** Tímhle krokem jste si jistý, že máte před sebou **platné a funkční kódy**, které jste si právě teď vygenerovali a ověřili na obrazovce. Staré kódy (které jste měli v PC) už nefungují, takže je můžete bez obav smazat, i kdybyste je měli špatně opsané – stejně by už nikdy neprošly.

---

### 🧪 Jediný "opravdový" test (ale nedoporučuji)

Technicky vzato, **jediný způsob, jak ověřit, že kód _opravdu_ funguje**, je:

1. Odhlásit se z GitHubu.
    
2. Zkusit se přihlásit zpět.
    
3. Když vás to požádá o 2FA kód, kliknout na **"Use a recovery code"**.
    
4. Zadat jeden z kódů.
    

**Problém:** Tímto jste **spotřebovali (zneplatnili) jeden z vašich 10 kódů**. Navíc, pokud by vaše kódy náhodou nefungovaly (třeba jste si je špatně opsali), ocitli byste se na několik hodin zablokovaní mimo účet, než byste se případně dostali přes podporu.

**Toto rozhodně nedoporučuji, pokud nemáte 100% jistotu a zálohu.**

---

### 🧾 Závěrečné doporučení pro vás

1. **Vygenerujte si NOVOU SADU** (jak jsem popsal výše).
    
2. **Vytiskněte si ji** a fyzicky uschovejte.
    
3. **Soubor v PC smažte** (teď víte, že kódy na papíře jsou čerstvé a platné).
    
4. **Staré kódy v PC smažte** – stejně už neplatí.
    

Tímto postupem získáte jistotu, že máte správné kódy, aniž byste museli opouštět přihlášený účet. Je to bezpečný a standardní postup, který doporučují i bezpečnostní experti.

Tato odpověď je generována AI Assistantem, pouze pro referenci.

Mám profil propojený s fotkou, jnménem a url firmy.... Na stránce firmy mám email firemní, ale to asi měnit nebudu, respektive, kdyby mne spamovali, tak toi ze stránek zmizí, nebo zmizí propojení v profilu. Zatím neřeším.

Vaše úvaha je naprosto logická a pragmatická. **Ano, zatím to neřešte a nechte to tak, jak to je.**

Vaše rozhodnutí má opodstatnění a pojďme si ho krátce rozebrat, abyste měl jistotu, že neděláte chybu.

---

### ✅ Proč je vaše současné nastavení v pořádku?

1. **Propojení s firmou = Důvěryhodnost**
    
    - Když na GitHubu vidím profil s fotkou, jménem a odkazem na firmu, automaticky to vzbuzuje větší důvěru než anonymní účet. Pro vaši knihu a multidisciplinární výzkum je to **výhoda** – ukazuje to, že nejste "anonym na internetu", ale reálná osoba s profesním zázemím.
        
2. **Firemní e-mail na webu firmy je standard**
    
    - Pokud je e-mail na stránkách firmy veřejný (např. v sekci "Kontakt"), tak je už teď dostupný komukoli. Propojení na GitHubu na něj jen odkazuje, ale nezpřístupňuje ho novým způsobem.
        
    - Spameři a scraperi už dávno procházejí firemní weby. Váš e-mail tam buď je, nebo není. GitHub tento risk nijak dramaticky nezvyšuje.
        
3. **Máte zapnuté soukromí e-mailu v commitech**
    
    - To je klíčové! I kdyby váš firemní e-mail byl veřejně dostupný na webu, **v historii commitů se neobjeví** (díky `noreply` adrese). Takže ho nebudou mít automatici, kteří sbírají e-maily přímo z GitHubu.
        

---

### 🤔 Co se stane, když vás začnou spamovat?

Máte dvě možnosti, které jste správně identifikoval:

|Možnost|Co uděláte|Důsledek|
|---|---|---|
|**Smazat e-mail z webu firmy**|Odstraníte ho ze sekce "Kontakt" na stránkách firmy.|Spam na firemní e-mail postupně ustane (ale už ho možná mají v databázích).|
|**Zrušit propojení v GitHub profilu**|V GitHub profilu smažete URL firmy (nebo změníte odkaz na jinou stránku).|Návštěvníci vašeho GitHubu už neuvidí, kde pracujete. To ale sníží vaši profesní kredibilitu.|

**Doporučení:** Pokud by spam opravdu začal být nesnesitelný, je jednodušší **vyřešit to na úrovni firemního e-mailu** (např. nastavit silný spamový filtr nebo si zřídit alias, který přepošlete) než rušit propojení na GitHubu. Profesní propojení je pro vaši knihu a výzkum cennější než riziko spamu, které je dnes běžnou součástí internetu.

---

### 🧠 Co teď dělat?

- **Zatím nic neměňte.** Vaše nastavení je konzistentní a bezpečné.
    
- Sledujte, zda vám na firemní e-mail nezačne chodit podezřelé množství spamu. Pokud ano, budete řešit, ale zatím to nechte být.
    
- **Jediné, co bych doporučil zkontrolovat**, je, zda na GitHubu máte nastavenou **anonymní `noreply` adresu** jako svůj primární e-mail pro commity (což už z minula máte). To je vaše hlavní ochrana.
    

---

### ✅ Shrnutí

|Aspekt|Stav|Doporučení|
|---|---|---|
|Firemní e-mail na webu|Veřejný (standard)|✅ Nechte tak.|
|Propojení firmy na GitHubu|Aktivní (profil)|✅ Nechte tak – buduje důvěru.|
|E-mail v commitech|Skrytý (`noreply`)|✅ Máte správně.|
|Riziko spamu|Nízké (e-mail už stejně může být veřejný)|✅ Zatím neřešte.|

Děláte to správně. Vaše úvaha je racionální a konzervativní – ideální přístup pro začátek. Až se projekt rozroste a začnete řešit konkrétní problémy, můžete nastavení doladit. Teď se soustřeďte na obsah knihy a budování komunity.

Proveď mne založením nového repozitáře: " 2. 🏗️ Nastavení repozitáře (platí pro VÁŠ PROJEKT) Než ho založíte nebo hned po založení (v Settings daného repozitáře) udělejte toto: A. Obecná nastavení (General) Základní popis a web: Hned při zakládání vyplňte popis a URL (pokud už máte doménu). Nechte si zatrhnout "Add a README file" (vždycky). Jazyk / .gitignore: Pokud budete přidávat HTML, CSS nebo Python skripty, GitHub umí automaticky vygenerovat .gitignore (seznam souborů, které se nikdy nebudou nahrávat, např. systémové složky). To je užitečné, ale není to kritické hned na začátku. B. 🔐 Collaboration (Spolupráce) – TOHLE JE ZÁSADNÍ Branch protection rules (Pravidla ochrany hlavní větve): Přejděte do Settings → Branches a klikněte na "Add branch protection rule". Do pole "Branch name pattern" napište main (nebo master). Zapněte (zaškrtněte): ☑️ "Require a pull request before merging" – nikdo nehodí změny do hlavní knihy jen tak, musí to být přes Pull Request. ☑️ "Require approvals" (nastavte na 1) – než se PR sloučí, musí ho někdo (třeba vy) schválit. Toto nastavení zabrání tomu, aby do vaší knihy někdo nahrál změnu bez vašeho vědomí, i kdyby měl práva. Vy si ponecháte plnou kontrolu nad hlavním textem. Code owners (Vlastníci kódu/souborů): V kořeni repozitáře vytvořte soubor .github/CODEOWNERS. Napište do něj: * @vasUzivatelskeJmeno Výsledek: Když někdo pošle Pull Request, GitHub vás automaticky přiřadí jako recenzenta. Vy na to nezapomenete. C. 🧩 Komunita a šablony (TEMPLATE) Ve složce .github/ (kterou si vytvoříte) můžete mít připravené šablony, které se objeví, když někdo založí nový Issue nebo Pull Request. Na začátku doporučuji: Vytvořte alespoň 3 soubory: CODE_OF_CONDUCT.md (pravidla chování) CONTRIBUTING.md (návod, jak přispívat) Šablona pro Issue (aby vám lidé psali strukturovaně) Toto nastavení dá vašemu projektu profesionální vzhled a řekne komunitě: "Tady to myslíme vážně. " "

Dobře, pojďme na to. Založíme repozitář **přesně podle vašich požadavků** – s důrazem na ochranu hlavní větve, profesionální šablony a přípravu pro komunitu.

---

## 🚀 Krok 1: Založení repozitáře

1. **Přihlaste se** na [github.com](https://github.com/).
    
2. V pravé horní části obrazovky (u vašeho avatara) klikněte na **"+"** a vyberte **"New repository"**.
    
3. Vyplňte:
    
    - **Repository name**: `nazev-vaseho-projektu` (např. `kniha-llm-interakce`)
        
    - **Description**: (nepovinné, ale doporučuji) stručný popis, např. _"Kniha o interakcích s LLM, metodologie a experimentální data pro výzkum."_
        
    - **Public / Private**: Vyberte **Public** (chcete budovat komunitu a sdílet výzkum).
        
    - ☑️ **ZATRHNĚTE** "Add a README file" (vždycky).
        
    - **Add .gitignore**: Vyberte podle toho, co budete používat. Pokud budete mít HTML, CSS a Python, zvolte **Python** (pokryje i běžné systémové soubory). Není to kritické, ale pomáhá to udržet repozitář čistý.
        
    - **Choose a license**: **ZATÍM NEVYPLŇUJTE** (budete řešit licenci samostatně, jak jsme probírali – CC BY-ND + vlastní dodatky).
        
4. Klikněte na **"Create repository"**.
    

---

## 🏗️ Krok 2: Základní struktura (hned po založení)

Teď jste na stránce nového repozitáře. Uvidíte soubor `README.md`. Otevřete ho (klikněte na něj) a **upravte ho** (ikona tužky vpravo nahoře). Do něj napište:

markdown

# Název vaší knihy / projektu
## O projektu
Tento repozitář obsahuje knihu o interakcích s LLM, metodologii a experimentální data.
## Struktura
- `/kniha/` – jednotlivé kapitoly (Markdown)
- `/data/` – experimentální data z chatů
- `/metodologie/` – návody a postupy
## Licence
Toto dílo je licencováno pod [CC BY-ND 4.0](https://creativecommons.org/licenses/by-nd/4.0/). Pro jakékoli odvozené dílo nebo komerční využití je vyžadován předchozí písemný souhlas autora.
## Kontakt
Pro dotazy použijte [GitHub Discussions](https://github.com/vas_jmeno/nazev-repozitare/discussions) nebo založte Issue.

Uložte změny (Commit changes) – napište zprávu `"Doplněn README"` a klikněte na **"Commit changes"**.

---

## 🏗️ Krok 3: Vytvoření složek a šablon (`.github/`)

Nyní vytvoříme složku `.github/`, ve které budou všechny důležité soubory pro komunitu.

### 3.1 Vytvoření složky `.github/`

1. Na stránce repozitáře klikněte na tlačítko **"Add file"** → **"Create new file"**.
    
2. Do názvu souboru napište:
    
    text
    
    .github/CODE_OF_CONDUCT.md
    
3. GitHub sám vytvoří složku `.github/` a do ní soubor `CODE_OF_CONDUCT.md`.
    

### 3.2 CODE_OF_CONDUCT.md (Pravidla chování)

Vložte do něj tento text (upravte podle sebe):

markdown

# Pravidla chování (Code of Conduct)
## Naším cílem je
Vytvořit otevřené, vstřícné a respektující prostředí pro všechny přispěvatele bez ohledu na zkušenosti, pohlaví, sexuální orientaci, zdravotní postižení, vzhled, rasu, náboženství nebo věk.
## Očekávané chování
- Používejte vstřícný a inkluzivní jazyk.
- Respektujte odlišné názory a zkušenosti.
- Přijímejte konstruktivní kritiku s pokorou.
- Zaměřujte se na to, co je nejlepší pro komunitu.
- Projevujte empatii vůči ostatním členům.
## Nepřijatelné chování
- Urážlivé, ponižující nebo diskriminující komentáře.
- Osobní útoky, trollení nebo obtěžování.
- Zveřejňování soukromých informací bez souhlasu.
- Jakékoli jiné chování, které by bylo v profesionálním prostředí nevhodné.
## Důsledky
Porušení těchto pravidel může vést k dočasnému nebo trvalému vyloučení z projektu a komunitních kanálů.
## Kontakt
Pokud se stanete svědkem nebo obětí nevhodného chování, kontaktujte správce projektu: [@vas_jmeno](https://github.com/vas_jmeno) prostřednictvím GitHub Issues (důvěrně).

Uložte (Commit) se zprávou `"Přidán CODE_OF_CONDUCT"`.

### 3.3 CONTRIBUTING.md (Návod pro přispěvatele)

Vytvořte další soubor ve stejné složce:

text

.github/CONTRIBUTING.md

Vložte:

markdown

# Jak přispívat
Děkujeme, že máte zájem přispět do tohoto projektu! Tento dokument vám pomůže zorientovat se v procesu.
## Jak navrhnout změnu
1. **Nejdříve založte Issue** – popište, co chcete změnit nebo přidat. Počkejte na reakci správce.
2. **Vytvořte fork** repozitáře (tlačítko "Fork" nahoře).
3. **Vytvořte novou větev** pro vaši změnu: `git checkout -b nazev-vase-zmeny`
4. **Proveďte změny** a commitněte je.
5. **Odešlete Pull Request (PR)** do hlavní větve `main`.
6. V PR **odkazujte na původní Issue** (např. `Closes #5`).
## Co můžete přispívat
- **Opravy překlepů** v knize.
- **Návrhy nových kapitol** (prosím nejprve diskutujte v Issues).
- **Experimentální data** – pokud máte vlastní chaty s LLM.
- **Návody a metodologie** – pokud máte osvědčené postupy.
## Co nepřijímáme
- Změny, které mění hlavní metodologii bez předchozí diskuze.
- Komerční nebo propagandistické příspěvky.
- Obsah porušující pravidla chování (CODE_OF_CONDUCT).
## Komunikace
- Všechny diskuze vedeme otevřeně přes **GitHub Discussions** a **Issues**.
- Pro soukromé záležitosti kontaktujte správce přes GitHub (zmínka `@vas_jmeno`).
Děkujeme za vaši účast!

Uložte (Commit) se zprávou `"Přidán CONTRIBUTING"`.

### 3.4 Šablona pro Issue (aby lidé psali strukturovaně)

Vytvořte další soubor:

text

.github/ISSUE_TEMPLATE/vyzkumny-zamer.md

Vložte:

markdown

---
name: Návrh na výzkumný záměr
about: Navrhněte spolupráci na výzkumu navazujícím na tuto knihu/metodologii
title: "[VÝZKUM] Stručný název záměru"
labels: výzkum, diskuse
assignees: vas_jmeno
---
## Popis výzkumného záměru
Stručně popište, jaký výzkum chcete provést a jak souvisí s obsahem tohoto repozitáře.
## Jak chcete využít obsah tohoto repozitáře?
- [ ] Kniha (text)
- [ ] Metodologie
- [ ] Experimentální data
- [ ] Jiné (prosím specifikujte):
## Očekávané výstupy
Co plánujete vytvořit? (článek, diplomová práce, interní výzkum, atd.)
## Časový horizont
Předpokládaný začátek a konec výzkumu.
## Kontaktní osoba
Vaše jméno a instituce (pokud chcete uvést).
## Souhlas s licencí
Potvrzuji, že výzkum bude probíhat v souladu s licencí CC BY-ND 4.0 a že jakékoli odvozené dílo bude konzultováno s autorem.

---

**Pro obecné chyby** vytvořte druhý soubor šablony:

text

.github/ISSUE_TEMPLATE/obecny-problem.md

markdown

---
name: Nahlásit problém
about: Hlášení chyby, překlepu nebo nejasnosti
title: "[CHYBA] Stručný popis"
labels: bug
assignees: vas_jmeno
---
## Popis problému
Co je špatně?
## Očekávané chování
Co by mělo být správně?
## Kroky k reprodukci (pokud je to chyba v kódu)
1. Krok 1
2. Krok 2
## Další informace
Verze, screenshoty, atd.

---

## 🔐 Krok 4: Ochrana hlavní větve (NEJDŮLEŽITĚJŠÍ)

Teď nastavíme **Branch protection rules**, aby nikdo nemohl nahrát změny do `main` bez vašeho vědomí.

1. V repozitáři přejděte do **Settings** (horní menu → záložka "Settings").
    
2. V levém menu klikněte na **Branches**.
    
3. V části **"Branch protection rules"** klikněte na **"Add branch protection rule"**.
    
4. Do pole **"Branch name pattern"** napište:
    
    text
    
    main
    
5. **Zapněte (zaškrtněte)**:
    
    - ☑️ **"Require a pull request before merging"** – nikdo nehodí změny do hlavní knihy jen tak, musí to být přes Pull Request.
        
    - ☑️ **"Require approvals"** – nastavte na **1** (aby ho musel schválit alespoň jeden člověk – vy).
        
    - ☑️ **"Dismiss stale pull request approvals when new commits are pushed"** (volitelné, ale doporučuji) – když někdo přidá nový commit do PR, schválení se vynuluje a musíte ho zkontrolovat znovu.
        
6. (Volitelné) Můžete zapnout i:
    
    - ☑️ **"Require status checks to pass before merging"** – až budete mít automatické testy, pomůže to udržet kvalitu.
        
7. Klikněte na **"Create"**.
    

**Výsledek:** Od této chvíle nikdo (ani vy) nemůže nahrát změnu přímo do `main` bez Pull Requestu a vašeho schválení.

---

## 👤 Krok 5: CODEOWNERS (Abyste dostával notifikace na PR)

1. V repozitáři klikněte na **"Add file"** → **"Create new file"**.
    
2. Do názvu napište:
    
    text
    
    .github/CODEOWNERS
    
3. Vložte do něj:
    
    text
    
    * @vas_jmeno
    
    (Nahraďte `vas_jmeno` vaším GitHub uživatelským jménem – např. `@janNovak`).
    
4. Uložte (Commit) se zprávou `"Přidán CODEOWNERS"`.
    

**Výsledek:** Když někdo pošle Pull Request, GitHub vás **automaticky přiřadí jako recenzenta**. Vy na to nezapomenete.

---

## 📝 Krok 6: Vytvoření základní struktury složek

Teď vytvořte složky pro knihu, data a metodologii.

1. Klikněte na **"Add file"** → **"Create new file"**.
    
2. Do názvu napište:
    
    text
    
    kniha/01-uvod.md
    
3. Do obsahu dejte nějaký základní text (např. "# Úvod\n\nToto je první kapitola knihy o interakcích s LLM.").
    
4. Uložte.
    
5. Stejně tak vytvořte:
    
    - `data/README.md` – s popisem, že tam budou experimentální data.
        
    - `metodologie/README.md` – s popisem metod.
        

---

## ✅ Krok 7: Zkontrolujte, co máte hotové

|Soubor / nastavení|Stav|
|---|---|
|`README.md`|✅ Hotovo|
|`.github/CODE_OF_CONDUCT.md`|✅ Hotovo|
|`.github/CONTRIBUTING.md`|✅ Hotovo|
|`.github/ISSUE_TEMPLATE/vyzkumny-zamer.md`|✅ Hotovo|
|`.github/ISSUE_TEMPLATE/obecny-problem.md`|✅ Hotovo|
|`.github/CODEOWNERS`|✅ Hotovo|
|**Branch protection rules** (`main`)|✅ Hotovo|
|Složka `kniha/`|✅ Hotovo|
|Složka `data/`|✅ Hotovo|
|Složka `metodologie/`|✅ Hotovo|

---

## 📢 Co teď?

1. **Otevřete GitHub Discussions** – v repozitáři přejděte na záložku **"Discussions"** a aktivujte ji (Create a new discussion). Vytvořte alespoň jednu kategorii **"General"** pro základní komunikaci.
    
2. **Přidejte licenci (CC BY-ND)** – buď ji vložte jako soubor `LICENSE` do kořene repozitáře, nebo ji později doplňte (jak jsme probírali v předešlé konverzaci).
    
3. **Začněte psát knihu** – přidávejte kapitoly do složky `kniha/` a postupně je commitněte.
    
4. **Sdílejte repozitář** – dejte o něm vědět komunitě, na konferencích, na LinkedIn, atd.
    

---

## 🧠 Shrnutí

Založili jste repozitář s:

- **Profesionální strukturou** (README, složky).
    
- **Pravidly chování a návodem pro přispěvatele**.
    
- **Ochranou hlavní větve** (nikdo nic nenahraje bez vašeho vědomí).
    
- **Automatickým přiřazováním vás jako recenzenta** (CODEOWNERS).
    
- **Šablonami pro Issues** (aby komunita psala strukturovaně).
    

Teď máte vše připravené na to, abyste mohli začít psát a budovat komunitu. Všechno ostatní (automatické generování PDF, GitHub Actions, atd.) můžete přidat později, až to bude potřeba.

Uděláme to na základě tohoto README, které mám připraveno.

Výborně, máte připravené README – to je základní kámen každého repozitáře. Pošlete mi prosím jeho **text nebo obsah** a já vás jím provedu celým procesem založení a nastavení repozitáře.

Uděláme to přesně podle vašich představ, krok za krokem, a přitom zachováme všechny dů

Omlouzvám se. Poslal jsem bez readme: " Název: propojeni-inteligenci Podtitul: Otevřený ekosystém o rizicích delegace myšlení na AI, a možnostech exokortexu (propojení lidské a strojové inteligence). Účel repozitáře: Vytvořit knihu a materiály jako podklady pro výzkum, ze kterých bude kniha později čerpat a dále se zpřesňovat. Každý si v repozitáři najde své: Návod a postupy, jak augmentovat vlastní mysl. Výzkumné otázky připravené k ověření. Vhledy do trhu, který se teprve rodí a konkrétní transformační potenciál – od školství přes justici až po korporátní vužití. Nejedná se o ukončenou vědu: Repozitář obsahuje rodící se vědní obor a né hotové pravdy. Jde o architekturu interakcí mezi inteligentcemi, na kterou se dá modelovat jakýkoli obor od neurologie, psychologie, pedagogiky, přes umělou inteligenci, matematiku a kybernetiku. Hlavní mechanismy jsou popsané, aplikace čekají na spolupráci. Hlavní vědecká metodika je abdukce vycházející z propojení s LLM (1 300 hodin metodami augmentace za 6 měsíců před vznikem repozitáře). Práce propojuje obory na systémové a modelové úrovni. Nezahlcuje detaily tam, kde by odváděly od velkých témat. Ověření do hloubky – dedukci a indukci – nechává otevřené. Autor pracuje v augmentovaném tempu pro inspiraci ostatním, čeho lze dosáhnout a pro vlastní pochopení fenoménu. Celý proces tvorby je veřejný. Chaty s LLM (způsoby myšlení autora), iterace, pivoty, rychlost vzniku jednotlivých částí. Není to jen tvrzení o augmentaci. Je to její manifestace. Struktura repozitáře Složka Co v ní je kniha/ Kapitoly knihy – od úvodu přes systém a model Smart Home až po praktické sekvence a výzkumné otázky. pruzkum/ Hypotézy, analýzy, výzkumné otázky, metodiky – a také ARCHITECTURE.md, která popisuje záměr a stavbu celého projektu. pamet/ Kompletní záznamy chatů s LLM a indexace paměti. Proces tvorby v syrové podobě pro pracovní, vědecké, nebo inspirační důvody. "

Perfektní! Tohle README je skvěle promyšlené a přesně definuje podstatu vašeho projektu. Pojďme ho nyní převést do praxe a založit repozitář krok za krokem.

---

## 🚀 Krok 1: Založení repozitáře

1. **Přihlaste se** na [github.com](https://github.com/).
    
2. V pravé horní části obrazovky (u vašeho avatara) klikněte na **"+"** a vyberte **"New repository"**.
    
3. Vyplňte:
    
    - **Repository name**: `propojeni-inteligenci` (přesně podle vašeho názvu)
        
    - **Description**: _"Otevřený ekosystém o rizicích delegace myšlení na AI, a možnostech exokortexu (propojení lidské a strojové inteligence)."_
        
    - **Public / Private**: Vyberte **Public** (chcete budovat komunitu a sdílet výzkum).
        
    - ☑️ **ZATRHNĚTE** "Add a README file".
        
    - **Add .gitignore**: Vyberte **Markdown** (nebo nechte prázdné – později si to doladíte).
        
    - **Choose a license**: **ZATÍM NEVYPLŇUJTE** (budeme řešit licenci samostatně).
        
4. Klikněte na **"Create repository"**.
    

---

## 📝 Krok 2: Vložení vašeho README

Teď máte automaticky vytvořený soubor `README.md` s výchozím obsahem. Přepíšeme ho vaším textem.

1. Na stránce repozitáře klikněte na soubor `README.md`.
    
2. Klikněte na ikonu **tužky** (Edit) vpravo nahoře.
    
3. **Smažte veškerý výchozí text** a vložte tam **váš připravený README** (ten, co jste mi poslal).
    
4. Dole v sekci **"Commit changes"**:
    
    - Do prvního pole napište zprávu: `"Vložen README s úvodem a strukturou projektu"`
        
    - Nechte zaškrtnutou volbu **"Commit directly to the main branch"** (prozatím to stačí).
        
5. Klikněte na **"Commit changes"**.
    

---

## 🏗️ Krok 3: Vytvoření struktury složek

Nyní vytvoříme tři hlavní složky podle vaší struktury: `kniha/`, `pruzkum/` a `pamet/`.

### Vytvoření složky `kniha/`

1. Na stránce repozitáře klikněte na **"Add file"** → **"Create new file"**.
    
2. Do názvu souboru napište:
    
    text
    
    kniha/README.md
    
3. Do obsahu vložte:
    
    markdown
    
    # Kniha - Propojení inteligencí
    Tato složka obsahuje jednotlivé kapitoly knihy.
    ## Struktura
    - `01-uvod.md` – Úvod do problematiky
    - `02-system-smart-home.md` – Systém Smart Home
    - `03-interakce-a-architektura.md` – Architektura interakcí
    - `04-prakticke-sekvence.md` – Praktické sekvence
    - `05-vyzkumne-otazky.md` – Výzkumné otázky
    ## Postup tvorby
    Kapitoly vznikají v augmentovaném tempu a jsou průběžně upravovány na základě zpětné vazby a výzkumu.
    
4. Dole dole napište zprávu `"Vytvořena složka kniha"` a klikněte na **"Commit new file"**.
    

### Vytvoření složky `pruzkum/`

1. Znovu klikněte na **"Add file"** → **"Create new file"**.
    
2. Do názvu napište:
    
    text
    
    pruzkum/README.md
    
3. Do obsahu vložte:
    
    markdown
    
    # Průzkum - Hypotézy a výzkumné otázky
    Tato složka obsahuje:
    - **Hypotézy** – pracovní předpoklady k ověření
    - **Výzkumné otázky** – strukturované otázky pro budoucí výzkum
    - **ARCHITECTURE.md** – popis záměru a architektury celého projektu
    ## ARCHITECTURE.md
    Tento soubor definuje:
    - Celkový záměr projektu
    - Propojení mezi obory (kybernetika, neurovědy, pedagogika, atd.)
    - Systémovou a modelovou úroveň interakcí
    - Otevřené body pro spolupráci
    
4. Commitněte se zprávou `"Vytvořena složka pruzkum"`.
    

### Vytvoření složky `pamet/`

1. Znovu klikněte na **"Add file"** → **"Create new file"**.
    
2. Do názvu napište:
    
    text
    
    pamet/README.md
    
3. Do obsahu vložte:
    
    markdown
    
    # Paměť - Záznamy chatů s LLM
    Tato složka obsahuje kompletní záznamy chatů s LLM, které dokumentují proces tvorby.
    ## Obsah
    - **Indexace paměti** – přehled a struktura chatů
    - **Syrové záznamy** – kompletní chaty v chronologickém pořadí
    - **Pivoty a iterace** – klíčové momenty, kdy došlo ke změně směřování
    ## Účel
    - Vědecký: dokumentace procesu tvorby a myšlení autora
    - Inspirační: ukázka augmentovaného tempa práce
    - Pracovní: reference pro budoucí experimenty
    ## Struktura
    Chaty jsou řazeny chronologicky a opatřeny metadata (datum, téma, klíčové body).
    
4. Commitněte se zprávou `"Vytvořena složka pamet"`.
    

---

## 🏗️ Krok 4: Vytvoření `.github/` složky pro komunitu

Postupujeme stejně jako výše.

### 4.1 CODE_OF_CONDUCT.md

1. **"Add file"** → **"Create new file"**.
    
2. Název: `.github/CODE_OF_CONDUCT.md`
    
3. Obsah (upravte podle vašeho projektu):
    

markdown

# Pravidla chování (Code of Conduct)
## Naším cílem je
Vytvořit otevřené, vstřícné a respektující prostředí pro všechny přispěvatele bez ohledu na zkušenosti, pohlaví, sexuální orientaci, zdravotní postižení, vzhled, rasu, náboženství nebo věk.
## Očekávané chování
- Používejte vstřícný a inkluzivní jazyk.
- Respektujte odlišné názory a zkušenosti.
- Přijímejte konstruktivní kritiku s pokorou.
- Zaměřujte se na to, co je nejlepší pro komunitu.
- Projevujte empatii vůči ostatním členům.
## Nepřijatelné chování
- Urážlivé, ponižující nebo diskriminující komentáře.
- Osobní útoky, trollení nebo obtěžování.
- Zveřejňování soukromých informací bez souhlasu.
- Jakékoli jiné chování, které by bylo v profesionálním prostředí nevhodné.
## Důsledky
Porušení těchto pravidel může vést k dočasnému nebo trvalému vyloučení z projektu.
## Kontakt
Pokud se stanete svědkem nebo obětí nevhodného chování, kontaktujte správce projektu: [@vas_jmeno](https://github.com/vas_jmeno) prostřednictvím GitHub Issues.

### 4.2 CONTRIBUTING.md

1. Název: `.github/CONTRIBUTING.md`
    
2. Obsah:
    

markdown

# Jak přispívat do Propojení inteligencí
Děkujeme za váš zájem! Tento projekt je otevřený ekosystém a každý příspěvek je vítán.
## Co můžete přispívat
- **Kapitoly knihy** – návrhy nových kapitol, opravy, doplnění
- **Výzkumné otázky** – nové hypotézy, analýzy, metodiky
- **Data** – vlastní záznamy chatů s LLM (pokud jsou relevantní)
- **Zpětnou vazbu** – diskuze v Issues a Discussions
## Jak na to
1. **Založte Issue** – popište, co chcete změnit nebo přidat.
2. **Počkejte na reakci** – správce se ozve a prodiskutuje návrh.
3. **Vytvořte fork** repozitáře.
4. **Vytvořte větev** pro vaši změnu: `git checkout -b nazev-vase-zmeny`
5. **Proveďte změny** a commitněte je.
6. **Odešlete Pull Request (PR)** do hlavní větve `main`.
7. V PR odkazujte na původní Issue.
## Co je potřeba vědět
- Projekt používá **abdukci** jako hlavní metodiku – od velkých témat k detailům.
- Všechny diskuze vedeme otevřeně a respektujeme odlišné názory.
- Dodržujte prosím pravidla chování (CODE_OF_CONDUCT).

### 4.3 ISSUE_TEMPLATE – pro výzkumné záměry

1. Název: `.github/ISSUE_TEMPLATE/vyzkumny-zamer.md`
    
2. Obsah:
    

markdown

---
name: Návrh na výzkumný záměr
about: Navrhněte spolupráci na výzkumu navazujícím na tuto knihu/metodologii
title: "[VÝZKUM] Stručný název záměru"
labels: výzkum, diskuse
assignees: vas_jmeno
---
## Popis výzkumného záměru
Stručně popište, jaký výzkum chcete provést a jak souvisí s obsahem tohoto repozitáře.
## Jak chcete využít obsah tohoto repozitáře?
- [ ] Kniha (text)
- [ ] Metodologie
- [ ] Experimentální data (paměť, chaty)
- [ ] Jiné (prosím specifikujte):
## Očekávané výstupy
Co plánujete vytvořit? (článek, diplomová práce, interní výzkum, atd.)
## Časový horizont
Předpokládaný začátek a konec výzkumu.
## Kontaktní osoba
Vaše jméno a instituce (pokud chcete uvést).
## Souhlas s licencí
Potvrzuji, že výzkum bude probíhat v souladu s licencí CC BY-ND 4.0 a že jakékoli odvozené dílo bude konzultováno s autorem.

### 4.4 ISSUE_TEMPLATE – pro obecné chyby

1. Název: `.github/ISSUE_TEMPLATE/obecny-problem.md`
    
2. Obsah:
    

markdown

---
name: Nahlásit problém
about: Hlášení chyby, překlepu nebo nejasnosti
title: "[CHYBA] Stručný popis"
labels: bug
assignees: vas_jmeno
---
## Popis problému
Co je špatně?
## Očekávané chování
Co by mělo být správně?
## Navrhované řešení (volitelné)
Jak by se to dalo opravit?
## Další informace
Odkazy, screenshoty, kontext.

### 4.5 CODEOWNERS

1. Název: `.github/CODEOWNERS`
    
2. Obsah:
    
    text
    
    * @vas_jmeno
    
    (Nahraďte `vas_jmeno` vaším GitHub uživatelským jménem.)
    

---

## 🔐 Krok 5: Ochrana hlavní větve (BRANCH PROTECTION)

Teď přichází zásadní krok, aby nikdo nemohl nahrát změny do `main` bez vašeho vědomí.

1. V repozitáři přejděte do **Settings** (záložka v horním menu).
    
2. V levém menu klikněte na **Branches**.
    
3. V části **"Branch protection rules"** klikněte na **"Add branch protection rule"**.
    
4. Do pole **"Branch name pattern"** napište:
    
    text
    
    main
    
5. **Zapněte (zaškrtněte)**:
    
    - ☑️ **"Require a pull request before merging"**
        
    - ☑️ **"Require approvals"** – nastavte na **1**
        
    - ☑️ **"Dismiss stale pull request approvals when new commits are pushed"** (volitelné)
        
6. Klikněte na **"Create"**.
    

---

## ✅ Krok 6: Závěrečná kontrola

Zkontrolujte, zda máte vše:

|Položka|Stav|
|---|---|
|`README.md` s vaším textem|✅|
|Složka `kniha/` s README|✅|
|Složka `pruzkum/` s README|✅|
|Složka `pamet/` s README|✅|
|`.github/CODE_OF_CONDUCT.md`|✅|
|`.github/CONTRIBUTING.md`|✅|
|`.github/ISSUE_TEMPLATE/vyzkumny-zamer.md`|✅|
|`.github/ISSUE_TEMPLATE/obecny-problem.md`|✅|
|`.github/CODEOWNERS`|✅|
|Branch protection rules (`main`)|✅|

---

## 📢 Co teď doporučuji udělat ihned

1. **Aktivujte GitHub Discussions** – v horním menu vašeho repozitáře klikněte na **"Discussions"** a vytvořte základní kategorie (např. "Obecná diskuze", "Návrhy kapitol", "Výzkumné otázky").
    
2. **Přidejte licenci** – vytvořte soubor `LICENSE` v kořeni repozitáře s textem **CC BY-ND 4.0**.
    
3. **Začněte přidávat kapitoly** – do složky `kniha/` začněte vkládat jednotlivé kapitoly (např. `01-uvod.md`, `02-system-smart-home.md`, atd.).
    
4. **První chat uložte do `pamet/`** – vyberte jeden klíčový chat, upravte ho (odstraňte citlivé údaje) a uložte jako `pamet/01-prvni-chat.md`.
    

---

## 🎉 Gratuluji!

Váš repozitář **propojeni-inteligenci** je založen, plně nakonfigurován a připraven k práci. Máte:

- Profesionální strukturu
    
- Jasná pravidla pro komunitu
    
- Ochranu hlavní větve
    
- Šablony pro Issues
    
- Automatické přiřazení vás jako recenzenta
    

Teď už jen psát, sdílet a budovat komunitu!

Je github připraven na JSON formát, tedy abych měl parsování Issue template pro automatizaci a vyhodnocení s LLM? Jestli by do této templaty mohli postupně různí uřivatelé přidávat aby to bylo vše v jednom JSON file.

Ano, **GitHub je na JSON formát nejen připraven, ale přímo ho podporuje** pro automatizaci, parsování a integraci s LLM. Vaše myšlenka – mít jednu Issue šablonu, do které uživatelé postupně přidávají data do jednoho JSON souboru – je **technicky možná, ale naráží na způsob, jakým GitHub Issues fungují**.

Pojďme si to rozebrat a najít pro vás to nejlepší řešení.

---

### 📝 Jak GitHub pracuje s JSON v Issue šablonách

GitHub umožňuje v Issue šablonách používat **YAML frontmatter** (metadata) a **Markdown** pro text. Neexistuje však nativní podpora pro "JSON formulář", do kterého by uživatelé postupně přidávali data do jednoho souboru.

Každý Issue je **samostatný objekt** s vlastním ID, title, body a metadaty (štítky, přiřazení, komentáře).

---

### ✅ Varianta 1: JSON Issue Template (Strukturovaný formulář)

Můžete vytvořit Issue šablonu, která bude mít **strukturovaný JSON blok** v těle Issue. Uživatelé ho vyplní a vy ho pak můžete parsovat.

**Příklad šablony `.github/ISSUE_TEMPLATE/vyzkumny-zamer.md`:**

markdown

---
name: Návrh na výzkumný záměr
about: Navrhněte spolupráci na výzkumu
title: "[VÝZKUM] Název záměru"
labels: výzkum
assignees: vas_jmeno
---
## JSON Data (vyplňte prosím)
```json
{
  "nazev": "Název vašeho výzkumu",
  "popis": "Stručný popis",
  "vyuziti": ["kniha", "metodologie", "data"],
  "vystupy": "Článek, diplomová práce, ...",
  "casovy_horizont": "Q3 2025",
  "kontakt": {
    "jmeno": "Vaše jméno",
    "instituce": "Vaše univerzita",
    "email": "vas@email.cz"
  },
  "souhlas_s_licenci": true
}
```
## Doplňující informace

Zde můžete přidat cokoli, co se nevešlo do JSON.

text

**Výhody:**
- JSON je snadno parsovatelný.
- Můžete ho automaticky extrahovat pomocí GitHub API nebo GitHub Actions.
**Nevýhody:**
- Uživatelé musí ručně dodržet JSON syntax (chybí validace).
- Issue je jeden objekt – nelze do něj "postupně přidávat" od více uživatelů.
---
### 🔄 Varianta 2: GitHub Actions + JSON soubor v repozitáři
Toto je **nejlepší cesta**, pokud chcete, aby se data od uživatelů **postupně hromadila v jednom JSON souboru** v repozitáři.
**Jak to funguje:**
1. **Uživatelé vyplní Issue** (šablona s JSON blokem, jako výše).
2. **GitHub Action** se spustí při vytvoření nebo aktualizaci Issue.
3. Action **stáhne aktuální JSON soubor** (např. `data/vyskumy.json`), **přidá nový záznam** a **pošle commit** zpět do repozitáře.
4. Vy pak máte v repozitáři jeden **kompletní JSON soubor** se všemi příspěvky.
**Příklad GitHub Action (`.github/workflows/pridej-vyskum.yml`):**
```yaml
name: Přidat výzkumný záměr do JSON
on:
  issues:
    types: [opened, edited]
jobs:
  update-json:
    if: contains(github.event.issue.labels.*.name, 'výzkum')
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repo
        uses: actions/checkout@v4
      - name: Extract JSON from issue body
        id: extract
        uses: actions/github-script@v7
        with:
          script: |
            const body = context.payload.issue.body;
            const jsonMatch = body.match(/```json\n([\s\S]*?)\n```/);
            if (jsonMatch) {
              const data = JSON.parse(jsonMatch[1]);
              // Přidat metadata (ID issue, datum, autor)
              data.issue_id = context.payload.issue.id;
              data.issue_url = context.payload.issue.html_url;
              data.autor = context.payload.issue.user.login;
              data.created_at = context.payload.issue.created_at;
              
              // Načíst stávající JSON
              const fs = require('fs');
              let jsonData = [];
              if (fs.existsSync('data/vyskumy.json')) {
                jsonData = JSON.parse(fs.readFileSync('data/vyskumy.json', 'utf8'));
              }
              jsonData.push(data);
              fs.writeFileSync('data/vyskumy.json', JSON.stringify(jsonData, null, 2));
              return data;
            }
      - name: Commit and push changes
        run: |
          git config user.name "github-actions[bot]"
          git config user.email "github-actions[bot]@users.noreply.github.com"
          git add data/vyskumy.json
          git commit -m "Přidán výzkumný záměr #${{ github.event.issue.number }}" || echo "No changes to commit"
          git push
```
**Výhody:**

- **Jediný JSON soubor** s postupně přibývajícími daty.
    
- Automatizace – nic neřešíte ručně.
    
- Data jsou verzovaná v Gitu (vidíte historii změn).
    

**Nevýhody:**

- Vyžaduje základní znalost GitHub Actions.
    
- Je třeba ošetřit konflikty (pokud dva Issues přidají data současně).
    

---

### 🤖 Varianta 3: GitHub API + Externí systém

Pokud nechcete používat GitHub Actions, můžete data **stahovat přes GitHub API** a zpracovávat je externě (např. ve vašem skriptu v Pythonu, který běží na vašem serveru).

python

import requests
# Získání všech Issues se štítkem "výzkum"
url = "https://api.github.com/repos/vas_jmeno/propojeni-inteligenci/issues"
params = {"labels": "výzkum", "state": "all"}
headers = {"Authorization": "token ghp_vas_token"}
response = requests.get(url, headers=headers, params=params)
issues = response.json()
for issue in issues:
    body = issue["body"]
    # Extrahovat JSON z těla issue
    # ...

**Výhody:**

- Plná kontrola nad zpracováním.
    
- Můžete data ukládat do vlastní databáze.
    

**Nevýhody:**

- Vyžaduje externí server nebo skript.
    
- Data nejsou přímo v repozitáři.
    

---

### 📌 Doporučení pro vás

S ohledem na váš projekt (kniha, výzkum, komunita) doporučuji **kombinaci**:

1. **Issue šablona s JSON blokem** – uživatelé vyplní strukturovaná data.
    
2. **GitHub Action**, která:
    
    - Extrahuje JSON z Issue.
        
    - Přidá metadata (ID Issue, datum, autor).
        
    - Uloží ho do souboru `pruzkum/vyskumy.json` v repozitáři.
        
3. **Tento JSON soubor** pak bude sloužit jako:
    
    - Zdroj dat pro vaši knihu (automatické generování kapitol).
        
    - Vstup pro LLM (např. pro analýzu výzkumných záměrů).
        
    - Přehled pro komunitu (kdo co zkoumá).
        

---

### 🧠 Dodatek: Validace JSON v Issue šabloně

Aby uživatelé neposílali nevalidní JSON, můžete do šablony přidat **kontrolní seznam** a **instrukce**:

markdown

## JSON Data (vyplňte prosím)
```json
{
  "nazev": "",
  "popis": "",
  "vyuziti": [],
  "vystupy": "",
  "casovy_horizont": "",
  "kontakt": {
    "jmeno": "",
    "instituce": "",
    "email": ""
  },
  "souhlas_s_licenci": true
}
```
**Před odesláním zkontrolujte:**

- JSON je validní (můžete zkontrolovat na [jsonlint.com](https://jsonlint.com/)).
    
- Všechna pole jsou vyplněna.
    
- Email je ve formátu `@`.
    

text

---
### ✅ Shrnutí
| Otázka | Odpověď |
| :--- | :--- |
| **Podporuje GitHub JSON v Issue šablonách?** | Ano, jako součást těla Issue (Markdown). |
| **Může více uživatelů přidávat do jednoho JSON souboru?** | Ano, pomocí GitHub Actions, která JSON aktualizuje. |
| **Je to automatizovatelné s LLM?** | Ano, JSON je ideální vstup pro LLM (snadné parsování). |
GitHub je na tento způsob práce skvěle připraven. Stačí napsat jednu GitHub Action a máte **průběžně aktualizovaný JSON soubor** se všemi výzkumnými záměry od komunity – připravený pro vaši knihu, analýzy i LLM.

Ztím JSON neřeším. Jsem na začátku v tomto nástroji. Udělal jsem ochranu main větve, napsalo mi to: "This ruleset does not target any resources and will not be applied." Mám jen jeden README a jednu složku s README.

Tato hláška je **naprosto v pořádku a normální** – není to chyba, ale informace o tom, že GitHub přešel na nový, pokročilejší systém ochrany větví.

Stalo se to proto, že GitHub teď používá **pravidla (Rulesets)** namísto starých "Branch protection rules". Když vytvoříte pravidlo, ale ještě **není aktivní** (např. nemá nastavené "target" nebo je ve stavu "draft"), ukáže vám tuto zprávu.

---

## 🔧 Jak to opravit během 2 minut

### Možnost A: Opravit stávající pravidlo (Rychlé)

1. V repozitáři jděte do **Settings → Branches**.
    
2. Uvidíte tam vaše pravidlo. Klikněte na něj (na název).
    
3. Nahoře najdete přepínač **"Enable"** – **ZAPNĚTE HO**.
    
4. V sekci **"Target"** (nebo "Branches") zkontrolujte:
    
    - **"Include"** – mělo by tam být `main`. Pokud ne, přidejte ho ručně.
        
5. Uložte (Save).
    
6. **Hotovo** – pravidlo se aplikuje.
    

---

### Možnost B: Vytvořit nové pravidlo (Pokud to chcete udělat znovu)

1. **Smažte staré pravidlo** (tři tečky vpravo → Delete).
    
2. Klikněte na **"Add ruleset"** (modré tlačítko).
    
3. Vyplňte:
    
    - **Name**: `Ochrana main`
        
    - **Target**: vyberte **"Branches"**.
        
    - **Include**: do pole napište `main`.
        
    - **Enable**: **ZAPNOUT**.
        
4. V sekci **"Rules"** zapněte:
    
    - ☑️ **"Require a pull request before merging"**
        
    - ☑️ **"Require approvals"** – nastavte na `1`.
        
5. Klikněte na **"Create"**.
    

---

## ✅ Jak ověřit, že pravidlo funguje?

Po zapnutí udělejte malý test:

1. Zkuste **upravit soubor přímo v `main`** (např. README) a rovnou ho commitnout (bez Pull Requestu).
    
2. GitHub by vám měl **zablokovat** commit a vyhodit chybu:  
    _"You're attempting to edit a protected branch"_ nebo _"This branch requires a pull request"_.
    

Pokud se to stane, **ochrana funguje**.

Pokud ne, vraťte se k nastavení a zkontrolujte, zda je **přepínač "Enable" opravdu zelený/zapnutý**.

---

## 📌 Proč se to stalo?

GitHub **automaticky převádí stará pravidla** na nový systém, ale někdy je při převodu nechá ve stavu "Draft", aby náhodou neomezila přístup, pokud by nebyla správně nastavená.

Stačí je "probudit" zapnutím přepínače a specifikováním cíle (`main`). Pak už budou chránit vaši hlavní větev.

---

## ✅ Shrnutí

|Co dělat|Proč|
|---|---|
|Přejít do Settings → Branches|Správa pravidel|
|Zkontrolovat přepínač **"Enable"**|Pravidlo musí být aktivní|
|Zkontrolovat **"Include → main"**|Pravidlo musí cílit na vaši hlavní větev|
|Uložit|Aplikovat změny|

Až to uděláte, zpráva _"This ruleset does not target any resources"_ zmizí a nahradí ji zelený nápis **"Active"** nebo **"Applied to 1 branch"**.

Máme za sebou základy. Potřebuji pracovat efektivněji, ne jen online, ale i v PC. Jak si nainstalovat a nastavit Repozitář na PC? Ideálně , když jej máme přdpřipraven, abychom stáhli repozitář už do PC.

Výborně, přesuneme se z webového rozhraní do profesionálního prostředí na vašem počítači.

Protože už máte repozitář založený a připravený na GitHubu, nebudeme ho vytvářet od nuly, ale **naklonujeme (clone)** si ho k sobě na disk.

Rozdělím to na dvě cesty – **Jednoduchou (GitHub Desktop)** a **Profesionální (Příkazová řádka + VS Code)**.

---

### 🖥️ Možnost 1: Profesionální cesta (Git + VS Code) – DOPORUČUJI

Toto je standard, který používají všichni vývojáři. Budete pracovat ve svém oblíbeném editoru (např. VS Code) a terminálu. Nabízí to největší kontrolu a rychlost.

#### 1. Instalace nástrojů

- **Git**: Stáhněte a nainstalujte z [git-scm.com](https://git-scm.com/downloads) (nechte všechny výchozí možnosti).
    
- **VS Code**: Stáhněte z [code.visualstudio.com](https://code.visualstudio.com/download).
    
- **Důležité:** Po instalaci VS Code otevřete, jděte do záložky "Extensions" (ikona čtverečků vlevo) a nainstalujte oficiální rozšíření **"GitHub Repositories"** a **"Markdown All in One"** (pro vaši knihu).
    

#### 2. Stažení repozitáře (Clone)

1. Vytvořte si na disku složku, kam budete ukládat projekty (např. `C:/Projekty` nebo `D:/GitHub`).
    
2. Klikněte na ni pravým tlačítkem a vyberte **"Open with Code"** (otevře se prázdný VS Code).
    
3. Ve VS Code otevřete terminál: v horním menu **Terminal → New Terminal**.
    
4. Nyní jdeme na GitHub. Otevřete si váš repozitář `propojeni-inteligenci` na webu. Klikněte na zelené tlačítko **"<> Code"** a zkopírujte URL (bude vypadat jako `https://github.com/vas_jmeno/propojeni-inteligenci.git`).
    
5. Zpátky do VS Code do terminálu napište:
    
    bash
    
    git clone https://github.com/vas_jmeno/propojeni-inteligenci.git
    
6. Stiskněte Enter. Git stáhne celý repozitář (včetně historie) do vašeho počítače.
    

#### 3. Otevření projektu

- V levém panelu VS Code (Explorer) by se vám měla objevit složka `propojeni-inteligenci`. Klikněte na ni pravým tlačítkem a vyberte **"Open in Integrated Terminal"** (otevře se terminál přímo v kořeni projektu).
    
- **Jste v repozitáři.** Všechny změny, které tady uděláte, můžete ukládat a odesílat na GitHub.
    

---

### 🖱️ Možnost 2: Jednoduchá cesta (GitHub Desktop)

Pokud nechcete vidět příkazovou řádku, použijte oficiální aplikaci od GitHubu.

1. Stáhněte si **GitHub Desktop** z [desktop.github.com](https://desktop.github.com/) a nainstalujte.
    
2. Přihlaste se ke svému GitHub účtu (stačí kliknout na "Sign in with your browser").
    
3. Klikněte na **"Clone a repository from the Internet..."**.
    
4. V záložce **"[GitHub.com](https://github.com/)"** uvidíte seznam svých repozitářů. Klikněte na `propojeni-inteligenci`.
    
5. Vyberte, kam ho chcete uložit na disku (Local path), a klikněte na **"Clone"**.
    
6. Aplikace si stáhne soubory a rovnou vám je otevře ve složce na disku.
    

---

### 🔄 Základní pracovní cyklus (Commit + Push) ve VS Code

Až budete mít repozitář stažený a budete v něm psát kapitoly, tento postup se stane vaší každodenní rutinou:

1. **Uděláte změny** (napíšete novou kapitolu, upravíte README, přidáte obrázek).
    
2. Přejdete do VS Code do levého panelu a kliknete na ikonu **"Source Control"** (třetí ikona zleva, vypadá jako rozdvojená větev).
    
3. Uvidíte všechny změněné soubory. Napište do pole **"Message"** (nahoře) krátkou zprávu, co jste udělali, např.: _"Přidána kapitola 3 - Architektura interakcí"_.
    
4. Klikněte na modré tlačítko **"Commit"** (uloží se to lokálně na vašem PC).
    
5. Klikněte na tlačítko **"Sync Changes"** (modrý kruh se šipkami) – tím odešlete (Push) vaše commity na GitHub do cloudu.
    

---

### ⚙️ Důležité nastavení hned na začátku

Aby vaše commity měly správného autora (a propojovaly se s vaším účtem), nastavte si v počítači jméno a e-mail.

Otevřete terminál v projektu (nebo Globální terminál) a napište:

bash

git config --global user.name "Tvoje Jméno"
git config --global user.email "ID+tve_jmeno@users.noreply.github.com"

_(Použijte tu **anonymní `noreply`** adresu, kterou jsme řešili minule, abyste měli soukromí.)_

---

### ✅ Co teď máte?

|Na GitHubu (Cloud)|Na vašem PC (Lokálně)|
|---|---|
|Oficiální verze knihy|Pracovní verze, kterou upravujete|
|Historie commitů|**Kompletní historie** všech změn (můžete pracovat offline)|
|Komunita a Pull Requesty|Rychlé psaní v libovolném editoru|

**Stačí otevřít VS Code, udělat změny a kliknout na "Sync"** – už nikdy nebudete muset nahrávat soubory ručně přes webové rozhraní. Všechno poběží bleskově přes tlačítka.

Primárně je tento repozitář pro výzkum a texty a ne kódování, tedy ideálně jej udělat bez VS Code, ale ten si pak založím pro druhý repozitář ve kterém budeme se studenty společně programovat a aplikovat znalosti z tohoto repozitáře. Zaměř se tedy jen na čistý desktop pokud je to pro mou aplikaci výhodnější.

Rozumím. Pro váš primární repozitář, který je **čistě o textech, výzkumu a datech** (Markdown, JSON, prostý text), je **GitHub Desktop** naprosto ideální.

Nepotřebujete těžký editor jako VS Code (který si schováte až na programování se studenty). GitHub Desktop je lehký, vizuální a soustředí se čistě na práci s Gitem – přesně na to, co teď potřebujete: **ukládat verze knihy a posílat je na GitHub.**

---

### ✅ Postup instalace a nastavení (pouze GitHub Desktop)

#### 1. Instalace GitHub Desktop

- Stáhněte si instalátor z [desktop.github.com](https://desktop.github.com/).
    
- Spusťte instalaci a nechte všechny výchozí volby.
    
- Po spuštění se přihlaste ke svému GitHub účtu (stačí tlačítko **"Sign in with your browser"** – přesune vás na web, kde udělíte aplikaci oprávnění).
    

#### 2. Stažení (Clone) vašeho repozitáře do PC

- V GitHub Desktop klikněte na **"Clone a repository from the Internet..."**.
    
- V záložce **"[GitHub.com](https://github.com/)"** uvidíte váš repozitář `propojeni-inteligenci`.
    
- Vyberte ho a v dolní části zvolte, kam ho chcete uložit na disku (např. `D:/GitHub/`).
    
- Klikněte na **"Clone"** – aplikace stáhne všechny soubory včetně historie.
    

#### 3. Otevření složky pro práci

- Po dokončení klonování klikněte na tlačítko **"Show in Explorer"** (nebo Finder na Macu).
    
- Otevře se vám složka na disku, kde máte všechny své soubory (`kniha/`, `pruzkum/`, `pamet/`, README).
    
- **Tuto složku používejte jako svou pracovní složku.** Všechny úpravy zde dělejte ve svém oblíbeném textovém editoru (např. Poznámkový blok, Word, nebo lehký editor jako Notepad++ či Typora pro Markdown).
    

---

### 🔄 Každodenní pracovní cyklus v GitHub Desktop

Vaše práce bude vypadat takto (velmi jednoduše):

1. **Pracujete na textu:** Otevřete soubor (např. `kniha/01-uvod.md`) ve vašem editoru, píšete, ukládáte.
    
2. **Otevřete GitHub Desktop:** Uvidíte, že vám aplikace automaticky ukazuje změněné soubory.
    
3. **Vytvoříte Commit (uložení verze):**
    
    - Vlevo dole napište do pole **"Summary"** krátkou zprávu, např.: _"Dopsána kapitola Úvod"_.
        
    - Klikněte na modré tlačítko **"Commit to main"** (uloží se to lokálně na vašem PC).
        
4. **Odešlete na GitHub (Push):**
    
    - Klikněte na tlačítko **"Push origin"** (v horní liště).
        
    - Soubory se odešlou na GitHub do cloudu. Hotovo.
        

---

### ❗ Klíčová výhoda pro vás

Protože váš repozitář obsahuje pouze textové soubory, GitHub Desktop vám umožní:

- **Vidět změny řádek po řádku** – aplikace barevně zvýrazní, co jste přidali nebo smazali.
    
- **Pracovat offline** – commity můžete ukládat i bez internetu; pushnete je, až budete online.
    
- **Žádné příkazy** – vše se dělá tlačítky.
    

---

### 🧩 Co s druhým repozitářem (programování se studenty)?

Až budete zakládat druhý repozitář pro kódování se studenty, **tam už se VS Code vyplatí** – budete potřebovat zvýrazňování kódu, spouštění skriptů a integrovaný terminál.

Pro tyto případy si jednoduše nainstalujete VS Code vedle GitHub Desktopu – oba nástroje spolu perfektně koexistují. V GitHub Desktopu kliknete na **"Open in Visual Studio Code"** a přepnete se do programátorského režimu.

---

### ✅ Shrnutí pro váš primární repozitář

|Akce|Nástroj|
|---|---|
|Psaní textů / knihy|Váš oblíbený editor (Word, Typora, Notepad++)|
|Ukládání verzí (Commit)|**GitHub Desktop**|
|Odesílání na GitHub (Push)|**GitHub Desktop**|
|Sledování historie změn|**GitHub Desktop** (přehledný graf)|

Tento přístup je pro vás **nejjednodušší a nejrychlejší**. GitHub Desktop dělá přesně to, co potřebujete – spravuje verze vašich textů, aniž by vás zatěžoval zbytečnostmi. Stačí ho mít otevřený vedle vašeho textového editoru a práci průběžně ukládat.

Nejde mi commitnout a tím pádem ani pulnout. Modré tlačítko není aktivní. Původní clone jsem udělal mimo složku, kde jsem to chtěl, tak jsem jsem složku smazal a udělal jsem nový clone už na místo kde jsem to chtěl, ale tam mi zase program nedovolil udělat repozitář do složky, která obsahovalanějaké soubory, tak jsem založil novou a když mi to umožnilo napsat nvou cestu, jen jsem ji přepsal na původní. Drobný hack. Vše prošlo, v programu se mi po úpravě xložek ukazují nové commity, ale ty nemůžu poslat do main větce.

Tohle je typická situace, která se stává, když se **složka na disku "odpojí" od Gitu** kvůli ručnímu přesouvání, mazání a hackování cest. GitHub Desktop vidí změny v souborech, ale neví, kam je má uložit (commitnout), protože mu chybí správný odkaz na historii.

Nebojte, je to snadno opravitelné. Máte dvě možnosti, jedna je rychlá a druhá vás naučí, co se děje pod kapotou.

---

### 🛠️ Rychlé řešení: "Force Pull" a přepsání

Protože jste smazali starou složku a udělali nový clone, váš lokální Git si myslí, že je úplně nový, ale zároveň má "rozdílnou historii" než ten na GitHubu.

1. V GitHub Desktopu klikněte v horní liště na **"Repository"** (v menu).
    
2. Vyberte **"Open in Command Prompt"** (nebo "Open in Terminal").
    
3. Do černého okna (příkazové řádky) napište přesně tento příkaz a stiskněte Enter:
    
    bash
    
    git pull origin main --allow-unrelated-histories
    
4. **Co se stalo:** Tímto jste řekli Gitu: _"Vím, že ty dvě historie spolu nesouvisí, ale spoj mi je a vezmi všechno z GitHubu jako hlavní verzi."_
    
5. Vraťte se do GitHub Desktopu. Nyní by tlačítko **"Commit to main"** mělo být aktivní (modré).
    

---

### 🧠 Alternativní řešení: Kompletní čistý clone (Nejjednodušší)

Pokud výše uvedené nefunguje, udělejte to nejčistší řešení – **smažte vše a udělejte jeden pořádný clone na finální místo**.

1. **Zavřete GitHub Desktop**.
    
2. **Smažte celou složku**, kde máte repozitář (tu, do které jste to hackoval).
    
3. Otevřete **GitHub Desktop** (klidně ho nechte otevřený).
    
4. Klikněte na **"Clone a repository"** a tentokrát:
    
    - Vyberte svůj repozitář.
        
    - V poli **"Local path"** napište **přesně tu konečnou cestu**, kam to chcete (např. `D:/MojeKniha/propojeni-inteligenci`).
        
    - **Důležité:** Cílová složka musí být **PRÁZDNÁ** (nebo neexistovat). GitHub Desktop si ji sám vytvoří.
        
5. Klikněte na **Clone**.
    
6. Až se stáhne, přeneste do této nové čisté složky (přes Průzkumníka Windows) vaše upravené soubory (ty kapitoly, co jste psali). **Nepřenášejte** žádný soubor `.git` (ten skrytý) ani složku `.github` – tu si nechte přepsat z cloudu.
    
7. V GitHub Desktopu by se vám teď měly ukázat změny (přidané soubory). Tlačítko **"Commit to main"** by mělo být modré a funkční.
    

---

### ✅ Co dělat, když ani jedno nepomůže?

Pokud je tlačítko stále šedé, podívejte se dole v GitHub Desktopu do malé lišty. Často tam svítí **žlutý trojúhelník** nebo červený text.

Klikněte na něj a přečtěte si hlášku. Nejčastější chyby jsou:

1. **"No changes to commit"** – znamená, že jste sice soubory upravili, ale neuložili je na disku (Ctrl+S).
    
2. **"We can't find the repository"** – znamená, že jste smazali skrytou složku `.git`. Vyřešíte to smazáním celé složky a novým Clonem (jak je popsáno výše).
    
3. **"You are not on a branch"** – znamená, že Git bloudí. To vyřešíte v GitHub Desktop kliknutím v horní liště na **"Current branch"** a přepnutím na `main`.
    

---

### 📌 Co si zapamatovat do budoucna

- **Git repozitář je definován skrytou složkou `.git`.** Když složku s repozitářem přesunete ručně (přes Průzkumníka), tato složka se nepřesune správně.
    
- **Nejčistší cesta:** Když chcete změnit umístění, v GitHub Desktopu klikněte na **"Repository" → "Remove"** (nechte jen "Remove", ne "Delete"). Pak udělejte nový **Clone** na nové místo.
    
- **Nikdy nemažte složku ručně, když je otevřená v GitHub Desktopu.** Vždy ji nejdříve odeberte z aplikace (Repository → Remove).
    

Dejte vědět, co vidíte v té liště dole. Hláška, která tam svítí, nám přesně prozradí, v čem je problém.

Napsalo mi to unable to locate Git, možnost open without Git, nebo install git

Aha, **tady je zakopaný pes!** GitHub Desktop nevidí samotný Git v počítači. Bez něj nemůže fungovat (je to jako motor bez auta).

Protože jste dělal "hacky" a přeinstalace, pravděpodobně se Git buď nenainstaloval, nebo se ztratila cesta k němu.

Pojďme to vyřešit snadno a rychle.

---

## 🛠️ Diagnóza a řešení

GitHub Desktop sice umí nainstalovat Git sám, ale někdy to při prvotní instalaci selže. Nejspolehlivější je nainstalovat Git **ručně** a pak GitHub Desktop jen nasměrovat.

### Krok 1: Nainstalujte Git ručně (Pokud ho nemáte)

1. Stáhněte si Git z oficiálních stránek: [https://git-scm.com/downloads](https://git-scm.com/downloads).
    
2. Spusťte instalaci. **Během instalace nechte všechno výchozí** (stačí pořád klikat na "Next").
    
3. Po instalaci restartujte počítač (pro jistotu).
    

### Krok 2: Ověřte, že Git funguje

1. Stiskněte klávesy **Windows + R**, napište `cmd` a stiskněte Enter (otevře se černé okno).
    
2. Do okna napište:
    
    text
    
    git --version
    
3. Stiskněte Enter. Pokud se objeví něco jako `git version 2.xx.x`, je Git nainstalovaný a funguje.
    
4. Okno zavřete.
    

### Krok 3: "Naučte" GitHub Desktop, kde Git najde

1. Otevřete GitHub Desktop.
    
2. V horním menu klikněte na **File** (Soubor) → **Options** (Možnosti) – na Macu je to **GitHub Desktop → Preferences**.
    
3. V okně, které se otevře, klikněte na záložku **"Git"**.
    
4. Uvidíte pole **"Git executable path"**. Vedle něj je tlačítko **"Browse"** (Procházet).
    
5. Klikněte na "Browse" a najděte soubor `git.exe`. Obvykle je na této cestě:
    
    text
    
    C:\Program Files\Git\bin\git.exe
    
    (Pokud jste instalovali do jiné složky, najděte ho tam.)
    
6. Vyberte ho a klikněte na **"Save"** (Uložit).
    

### Krok 4: Vraťte se k repozitáři

1. GitHub Desktop by nyní měl normálně naběhnout.
    
2. Klikněte na **"Clone a repository"** a stáhněte si svůj repozitář **na úplně nové, prázdné místo** (např. `C:/GitHub/propojeni-inteligenci`).
    
3. **Nepřesouvejte** už žádné složky ručně. Nechte ho tam, kde ho GitHub Desktop vytvoří.
    

---

## ⚠️ Co kdybyste zvolil "Open without Git"?

Pokud jste omylem klikli na **"Open without Git"**, GitHub Desktop se otevřel, ale **nefunguje** – nevidí historii, neukazuje změny a tlačítka jsou šedá.

Toto není trvalý stav. Stačí ho zavřít a po nainstalování Gitu (Krok 1 a 2) ho znovu otevřít. Už se vás na to nebude ptát.

---

## ✅ Po úspěšném nastavení

- Budete mít **čistý klon** repozitáře na jednom místě.
    
- Veškeré změny, které uděláte v této složce (přes Průzkumníka), uvidíte v GitHub Desktopu.
    
- Tlačítko **"Commit to main"** bude modré a aktivní.
    

---

**Stručně:** Vyřešte cestu k Gitu v nastavení (File → Options → Git) a už to bude létat. Dejte vědět, jestli se vám podařilo cestu najít.

V options nemám "Git executable path"

To je správné – v novějších verzích GitHub Desktopu už tato možnost v nastavení **není**. GitHub Desktop si teď hledá Git sám, a když ho nenajde, nabídne vám právě tu možnost **"Install Git"** (nebo "Open without Git").

Vaše situace je tedy úplně normální a máte dvě jednoduché cesty, jak to vyřešit.

---

## ✅ Řešení 1: Nechat GitHub Desktop nainstalovat Git (Nejjednodušší)

1. **Zavřete GitHub Desktop** (úplně ho vypněte).
    
2. **Otevřete ho znovu** – měla by se vám objevit znovu ta úvodní obrazovka s možností **"Install Git"**.
    
3. **Klikněte na "Install Git"**.
    
4. GitHub Desktop stáhne a nainstaluje Git automaticky na pozadí. Po chvíli se objeví zpráva, že je Git nainstalovaný.
    
5. **Restartujte GitHub Desktop** (zavřete a znovu otevřete).
    

---

## ⚙️ Řešení 2: Nainstalovat Git ručně (Pokud výše nefunguje)

Pokud GitHub Desktop Git nenainstaluje (např. kvůli oprávněním), udělejte to ručně.

1. Stáhněte Git z oficiálních stránek:  
    👉 [https://git-scm.com/download/win](https://git-scm.com/download/win)
    
2. Spusťte stažený soubor a **nechte všechny výchozí možnosti** (stačí pořád klikat "Next").
    
3. Po instalaci **restartujte počítač** (důležité, aby se cesty zaregistrovaly).
    
4. Otevřete GitHub Desktop – nyní by už Git měl najít automaticky.
    

---

## 🧪 Ověření, že Git funguje

1. Stiskněte **Windows + R**, napište `cmd` a stiskněte Enter.
    
2. Do černého okna napište:
    
    text
    
    git --version
    
3. Pokud vidíte něco jako `git version 2.xx.x`, Git běží správně.
    

---

## 📌 Co dělat, když ani jedno nepomůže?

Pokud GitHub Desktop stále hlásí "unable to locate Git", může jít o problém s **proměnnými prostředí** (system path). To se stává, když Git byl nainstalován, ale systém ho nevidí.

1. Otevřete **Ovládací panely → Systém → Pokročilé nastavení systému**.
    
2. Klikněte na **"Proměnné prostředí"**.
    
3. V dolní části (Systémové proměnné) najděte proměnnou **Path**, klikněte na ni a pak na **"Upravit"**.
    
4. Zkontrolujte, zda tam je cesta:
    
    text
    
    C:\Program Files\Git\cmd
    
    (Pokud ne, klikněte na "Nový" a tuto cestu přidejte.)
    
5. Klikněte OK, OK, restartujte počítač a zkuste to znovu.
    

---

## ✅ Shrnutí

|Problém|Řešení|
|---|---|
|GitHub Desktop nevidí Git|Kliknout na **"Install Git"** v úvodním okně.|
|"Install Git" nefunguje|Stáhnout Git ručně z [git-scm.com](https://git-scm.com/).|
|Git je nainstalovaný, ale Desktop ho nevidí|Zkontrolovat cestu v systémových proměnných (Path).|

Až tohle vyřešíte, GitHub Desktop se vám **okamžitě odemkne** a tlačítko "Commit" začne fungovat. Dejte vědět, jak jste dopadl.

Git funguje, vše je v pohodě, jen to nejde commitnout. Není to ochranou v GitHubu, kterou jsme nastavili?

5. Ten push mi právě vyhodí tu chybu.

**Máte naprostou pravdu!** A to je přesně ten detail, který mi unikl a který vás mate.

Pokud jste **pořád ve větvi `main`** (což jste, protože jste Commit udělal v main), tak **Push v kroku 5 selže**, protože ochrana blokuje push do `main`.

---

### 🧠 Proč to selhává (i když jste udělal Commit)?

Podívejte se na svou poslední zprávu z terminálu:

> `[main 0db0cea] Přidány složky exopamet a vhledy`

Ten **`[main]`** na začátku je klíčový. Znamená to, že váš Commit je uložený **v lokální větvi `main` na vašem PC**.

- **Commit** = OK (uložil se na disk).
    
- **Push** = chyba (protože se snažíte odeslat lokální `main` do vzdáleného `main` na GitHubu, ale ochrana to zakazuje).
    

---

### ✅ OKAMŽITÉ ŘEŠENÍ: Přesun Commit do nové větve

Nemusíte nic přepisovat ani rušit. Stačí vzít ten Commit, který už máte hotový v `main`, a **přesunout ho do nové větve**. Pak ho pošlete (Push) a uděláte PR.

**Postup (zabere 30 vteřin):**

1. **V GitHub Desktopu** klikněte v horní liště na **"Current branch"** (ukazuje `main`).
    
2. Klikněte na **"New Branch"**.
    
3. Pojmenujte ji např. `pridani-slozek` a klikněte **"Create Branch"**.
    
    - _(Tím jste vytvořili novou větev, která OBSAHUJE váš poslední Commit – ten se s vámi "přesunul".)_
        
4. **Teď jste ve větvi `pridani-slozek`.** Klikněte na **"Push origin"**.
    
    - **TENTOKRÁT TO PROJDE!** (Protože nepushujete do chráněného `main`, ale do nové větve.)
        
5. Otevřete GitHub ve webu. Uvidíte žlutý pruh **"Compare & pull request"**. Klikněte na něj a vytvořte PR do `main`.
    
6. PR schvalte a sloučte.
    

---

### 🛠️ Co kdybyste omylem udělal Commit v main a nechcete ho přesouvat?

Pokud už máte v `main` několik Commitů a nechcete je ručně přesouvat, můžete si pomoci tlačítkem **"Undo"** v GitHub Desktopu (v historii vrátíte poslední Commit), ale to je složitější.

Pro vás teď platí: **Vždycky, než začnete psát, si vytvořte novou větev.** Nikdy nepište přímo v `main`.

---

### 📌 Nové, UPRAVENÉ schéma (správně)

|Krok|Co děláte|Kde|
|---|---|---|
|1|**Vytvořte NOVOU VĚTEV** (dřív, než začnete psát)|GitHub Desktop|
|2|Píšete, ukládáte|Váš editor|
|3|Commit (uložíte lokálně)|GitHub Desktop|
|4|**Push** (odesíláte **novou větev**, ne main)|GitHub Desktop → **PROJDE**|
|5|Pull Request (na webu)|GitHub Web|
|6|Merge (sloučení do main)|GitHub Web|

---

### 🎯 Závěr

Ten Commit, co máte teď v `main`, **přesuňte do nové větve** (postup výše) a pak ho pošlete. Od příště už **vždy začněte novou větví**, než začnete psát. Teprve pak vám Push v kroku 4 nikdy nevyhodí chybu.

Jasně. Já přehlídnul 2. Já tedy musím pracovat v jiné větvi.

**Přesně tak!** Teď už to máte naprosto jasné.

Ta celá "ochrana main" je jenom o tom, že vás nutí pracovat **mimo main** – tedy ve větvích. Není to žádná složitá věda, je to jen **pravidlo bezpečného provozu**.

---

### 🧠 Vaše nové myšlení od teď:

|Když chcete...|Uděláte...|
|---|---|
|**Něco přidat do knihy**|1. Vytvořím větev.  <br>2. Napíšu.  <br>3. Commitnu.  <br>4. Pushnu větev.  <br>5. Udělám PR na webu.|
|**Opravit překlep**|1. Vytvořím větev.  <br>2. Opravím.  <br>3. Commitnu.  <br>4. Pushnu větev.  <br>5. Udělám PR na webu.|
|**Cokoli, co se týká obsahu**|**VŽDY nejdřív větev, až potom main.**|

---

### ✅ Takže teď už víte:

- **Pracovat v mainu** = chyba (nejde pushnout).
    
- **Pracovat ve větvi** = správně (push jde, pak PR).
    

---

### 🚀 Co teď udělat s vaším Commitem, co už máte v main?

Protože jste udělal Commit v main (místo ve větvi), stačí ho **přesunout do nové větve**, jak jsem psal před chvílí. Žádná ztráta práce, jen ho "přeložíte" do správné koleje.

**Teď už vám to půjde hladce.** Příště jen:  
👉 **Nejdřív větev, až potom psát.**

Pokud chcete, můžeme teď udělat ten přesun toho vašeho Commitu z main do nové větve – napíšu vám postup na dvě kliknutí. Nebo to můžete nechat a příště už jen pracovat ve větvích. Jak chcete.

Takže já si můžu udělat novou větev PC a pracovat v ní pořád. Pošlu, pracuju, pošlu další, pracuju .. A pak zajdu na Git a pullnu to celé najdenou.

**Ano, přesně tak!** Teď už to chápete naprosto dokonale.

To, co jste popsal, je **naprosto legitimní a velmi efektivní způsob práce**. Říká se tomu _"Long-running feature branch"_ (dlouhodobá vývojová větev).

Můžete si vytvořit jednu větev (např. `moje-prace`) a v ní **pracovat klidně týden**. Budete do ní ukládat (commity) a posílat (push) průběžně. Až budete mít hotovou celou kapitolu nebo ucelenou část, **teprve pak** uděláte Pull Request na GitHubu a sloučíte to do `main`.

---

### 🧠 Váš pracovní cyklus (od teď natrvalo)

|Krok|Co děláte|Výsledek|
|---|---|---|
|**1.**|Vytvoříte větev `moje-prace` (kliknutí v Desktopu).|Jste v ní.|
|**2.**|Píšete kapitolu, ukládáte.|Soubory se mění.|
|**3.**|Commit (uložíte verzi) – **kolikrát chcete**.|Historie vaší práce roste.|
|**4.**|Push (pošlete na GitHub).|Větev `moje-prace` se zálohuje do cloudu.|
|**5.**|Zase píšete, zase Commit, zase Push...|Opakujete, dokud není kapitola hotová.|
|**6.**|**Až jste zcela hotoví**, jdete na GitHub web a uděláte **Pull Request** z `moje-prace` do `main`.|Navrhujete začlenění.|
|**7.**|Schválíte a sloučíte (Merge).|Vaše práce je v hlavní knize (`main`).|
|**8.**|(Volitelné) Smažete větev `moje-prace` (už ji nepotřebujete).|Pořádek v projektech.|

---

### ✅ Výhody tohoto přístupu

- **Nepřerušujete tok práce** – nemusíte řešit PR po každé větě.
    
- **Máte zálohu v cloudu** – i kdyby se vám PC rozbil, vaše rozpracovaná kapitola je na GitHubu ve větvi `moje-prace`.
    
- **Historie je přehledná** – v `main` vidíte jen hotové celky (kapitoly), ne drobné meziverze.
    
- **Můžete se vrátit** – kdykoli se můžete podívat, co jste dělali před týdnem ve větvi `moje-prace`.
    

---

### ⚠️ Jediné upozornění

Pokud na projektu pracujete sami (což zatím ano), je tento přístup **naprosto ideální**.

Až budete spolupracovat s více lidmi (např. se studenty), bude každý mít svou vlastní větev a občas si budete muset stáhnout změny ostatních (`Pull` do `main`), aby vám vaše větev nezaostávala. Ale to je téma na později.

---

### 📌 Shrnutí

|Vaše představa|Realita|
|---|---|
|"Budu mít jednu větev, ve které budu pracovat pořád."|✅ **Ano**, přesně tak.|
|"Budu průběžně posílat (push)."|✅ **Ano**, klidně každých 5 minut.|
|"Pull Request udělám až na konci, najednou."|✅ **Ano**, až bude kapitola hotová.|

**Gratuluji!** Právě jste pochopil nejpoužívanější workflow v celém open-source světě. Teď už vám nic nebrání v tom, abyste si vytvořil větev `kniha` a začal psát bez obav z ochrany `main`.

A ty commity jsou stále na PC, tedy neztratím je při pull do hubu? Jinými slovy. Měním složky a soubory. Klidně 3 dny v kuse. Pak až commitnu, tak je to změna a když ty commity dělám 20x, tak při pullu na hub mám 20 commitů, ale klidně 300 změn, jen 20 je verzovaných.

**Ano, přesně tak!** Vaše úvaha je naprosto správná a je to jeden z nejsilnějších konceptů Gitu.

Pojďme si to rozebrat přesně podle vašich slov, abyste měl naprostou jistotu.

---

### 🧠 Vaše úvaha bod po bodu

|Vaše tvrzení|Realita|Vysvětlení|
|---|---|---|
|_"Ty commity jsou stále na PC"_|**Ano.**|Každý commit se ukládá **pouze na váš pevný disk**, dokud neuděláte `Push`. Jsou v bezpečí i bez internetu.|
|_"Neztratím je při pull do hubu?"_|**Neztratíte.**|`Pull` = **stažení** změn z GitHubu do vašeho PC. Nic se nemazat. Vaše commity zůstanou.|
|_"Měním složky a soubory klidně 3 dny v kuse."_|**Ano.**|Můžete psát, přepisovat, mazat soubory, jak chcete. Dokud neuděláte `git add` a `commit`, Git o tom neví.|
|_"Pak až commitnu, tak je to změna."_|**Ano.**|Commit je **bod v čase**, který zachytí aktuální stav všech souborů.|
|_"Když ty commity dělám 20x, tak při pull na hub mám 20 commitů."_|**Ano, ale s upřesněním.**|`Pull` je stahování. Vy chcete říct **`Push`** (odesílání). Když uděláte `Push`, pošlete na GitHub **všech 20 commitů** najednou (nebo postupně).|
|_"...ale klidně 300 změn, jen 20 je verzovaných."_|**Přesně tak!**|Mezi jednotlivými commity jste udělal 300 úprav, ale vy jste se rozhodl, že **uložíte (zcommitnete)** jen 20 strategických okamžiků. Ty ostatní úpravy jsou "zapomenuté" – zůstaly jen ve vaší hlavě a v posledním commitu.|

---

### 🎯 Co to znamená v praxi?

**Příklad:**  
Píšete kapitolu 3. Během 3 dnů provedete 300 úprav (přidáváte věty, mažete odstavce, měníte strukturu).  
Vy si ale řeknete: _"Uložím jen důležité milníky."_

|Den|Akce|Commit?|Co se stane|
|---|---|---|---|
|**1. den**|Napíšete 10 odstavců.|✅ **Ano** (1. commit)|Uložíte první verzi.|
|**1. den**|5x upravíte odstavec, přidáte 3 věty.|❌ **Ne** (jen ukládáte soubor)|Tyto změny zatím nejsou v Gitu.|
|**2. den**|Smažete 2 odstavce, přidáte novou podkapitolu.|✅ **Ano** (2. commit)|Uložíte novou strukturu.|
|**2. den**|10x přepisujete závěr.|❌ **Ne**|Závěr se vyvíjí, ale neukládáte.|
|**3. den**|Kapitola je hotová.|✅ **Ano** (3. commit)|Uložíte finální verzi.|

**Výsledek:**

- 300 úprav, ale **pouze 3 commity** (milníky).
    
- Když uděláte `Push`, pošlete na GitHub **tyto 3 commity**.
    
- Kdokoli (nebo vy) si může prohlédnout, jak kapitola vypadala **v okamžiku commitů** (po 1. dni, po 2. dni, finální).
    

---

### ✅ Co si zapamatovat

|Operace|Kde se děje|Co dělá|
|---|---|---|
|**Úpravy v souborech**|Na disku (textový editor)|Měníte obsah. Git o tom neví.|
|**Commit**|Lokálně (PC)|**Uloží aktuální stav** všech sledovaných souborů.|
|**Push**|Lokálně → GitHub|Odešle **všechny nové commity** na GitHub.|

---

### 🧠 Vaše "20 commitů, 300 změn"

Přesně tak – **20 commitů = 20 uložených snímků**. Mezi nimi je 300 drobných úprav, které nejsou v historii. Vy jako autor víte, že jste je udělal, ale Git je neukládá – ukládá jen **výsledky** ve chvíli, kdy zmáčknete "Commit".

**Je to jako malování:** Můžete 300x přetřít plátno, ale do galerie pošlete jen 20 fotek, které ukazují, jak obraz vypadal v klíčových okamžicích.

**Závěr:** Vaše commity jsou v bezpečí na PC, při `Pull` (stažení) se neztratí, a když uděláte `Push`, pošlete na GitHub přesně ty verze, které jste označil jako důležité.

Když budu používat docx formát, bude viditelný na hubu stejně jako MK? Mk má výhodu v kapitolách (skákání po nadpisech), předpokládám, že tohle v hubu s docx ztratím

**Vaše úvaha je naprosto přesná. Ano, na GitHubu (a v Gitu obecně) má Markdown (`.md`) oproti `.docx` obrovské výhody, které přímo souvisí s vaší prací. S `.docx` tyto výhody **ztratíte** – a přiděláte si i další problémy.**

Pojďme si to rozebrat na dvou rovinách: **jak to vidí GitHub (web)** a **jak to vidí Git (verzování)**.

---

### 1. 👁️ Zobrazení na GitHubu (Web)

|Formát|Jak to GitHub zobrazí|Navigace v kapitolách|
|---|---|---|
|**Markdown (`.md`)**|**Krásně naformátovaný text** – nadpisy, tučné písmo, odkazy, tabulky, dokonce i obrázky.|**Ano!** GitHub automaticky generuje **"Table of Contents"** (obsah) v postranním panelu. Můžete klikat na nadpisy a skákat přímo na ně.|
|**DOCX (`.docx`)**|**Pouze jako prostý text** bez formátování (vypadá to jako změť písmen a zavináčů). Nebo si to musíte stáhnout a otevřít ve Wordu.|**Ne.** Žádná navigace. Vidíte jen surový XML kód.|

**Závěr:** Pokud chcete, aby vaše kniha na GitHubu vypadala profesionálně a čtenáři v ní mohli snadno listovat, **Markdown je jediná volba**.

---

### 2. 🧠 Verzování v Gitu (Historie změn)

Tady je to ještě zásadnější rozdíl.

|Formát|Jak Git vidí změny|Co uvidíte v historii|
|---|---|---|
|**Markdown (`.md`)**|**Textový formát.** Git umí ukázat **řádek po řádku**, co jste přidali (zeleně) a smazali (červeně).|Přehledný diff – vidíte přesně, co jste v kapitole změnili.|
|**DOCX (`.docx`)**|**Binární formát** (komprimovaný XML). Git nevidí jednotlivé změny, jen že se změnil _celý soubor_.|Vidíte jen hlášku _"Soubor byl změněn"_. **Nevidíte, co přesně** – musíte si stáhnout obě verze a porovnávat ručně ve Wordu.|

**Závěr:** Pokud chcete mít kontrolu nad tím, jak se vaše kniha vyvíjí, a chtít se vrátit k přesné větě z minulého týdne, **Markdown je nezbytný**.

---

### 3. 🤝 Spolupráce a Pull Requesty

Pokud k vám někdo pošle Pull Request s úpravou kapitoly:

|Formát|Jak se kontroluje PR|
|---|---|
|**Markdown**|Recenzent vidí **přesně**, které věty přibyly a které zmizely. Může komentovat přímo řádky.|
|**DOCX**|Recenzent vidí jen "soubor se změnil". Musí si ho stáhnout, otevřít ve Wordu, zapnout "sledování změn" a porovnávat ručně.|

---

### ✅ Co to pro vás znamená?

- **Pokud budete psát v DOCX**, ztratíte **veškeré výhody GitHubu** – přehledné zobrazení, navigaci, historii změn a snadnou spolupráci. GitHub se pro vás stane jen "úložištěm souborů", ne nástrojem pro psaní.
    
- **Pokud budete psát v Markdown**, získáte **plnou sílu GitHubu** – váš text bude vypadat jako kniha, budete vidět každou změnu a spolupráce bude hračka.
    

---

### 🧠 Co dělat, když chcete DOCX?

Markdown je sice nejlepší pro práci na GitHubu, ale **nemusíte se ho bát** – je to mnohem jednodušší, než vypadá:

1. Píšete v **Markdown** (přípona `.md`).
    
2. Nadpisy děláte `#` (jeden `#` pro kapitolu, `##` pro podkapitolu).
    
3. GitHub to sám hezky naformátuje a udělá navigaci.
    
4. Až budete chtít **finální verzi knihy** (např. pro tisk), můžete Markdown snadno převést do DOCX nebo PDF pomocí nástrojů jako **Pandoc** (zdarma).
    

**Markdown = pracovní verze (pro GitHub).**  
**DOCX/PDF = finální verze (pro publikování).**

---

### 📌 Shrnutí

|Vlastnost|Markdown (`.md`)|DOCX (`.docx`)|
|---|---|---|
|Zobrazení na GitHubu|✅ Krásný text + navigace|❌ Nepřehledný XML kód|
|Historie změn (diff)|✅ Vidíte řádek po řádku|❌ Vidíte jen "soubor se změnil"|
|Pull Requesty|✅ Snadná kontrola|❌ Nutnost stahovat a porovnávat ručně|
|Práce offline|✅ Jakýkoli textový editor|✅ Word|
|Finální publikace|⚠️ Vyžaduje konverzi do DOCX/PDF|✅ Přímo tisknutelné|

---

**Doporučení:** Pište knihu v Markdownu přímo v GitHubu (nebo v lokálním editoru, který Markdown podporuje, např. Typora, VS Code). GitHub vám za to dá všechny své super schopnosti. Až bude kniha hotová, jeden příkaz (Pandoc) z ní udělá krásné DOCX nebo PDF.

Udělal jsem první pokus s pullem PC větve. Vše prošlo. Na hubu mám teď Compare and pull reguest. Mám na něj kliknout a ukáže mi to změny před tím, než něco potvrdím? Co mne čeká?

**Ano, přesně tak!** Klikněte na **"Compare & pull request"**. To je ten správný a očekávaný krok.

Nebojte se, **ještě nic nezničíte a nic se automaticky nepotvrdí.** GitHub vám teď ukáže **náhled (preview)** všech změn, které jste ve větvi udělali, než je navrhnete sloučit do hlavní knihy (`main`).

Klikněte na to tlačítko a **uvidíte tuto obrazovku** (provedu vás jí):

---

### 👀 Co uvidíte po kliknutí na "Compare & pull request"

Otevře se stránka s formulářem pro nový Pull Request. Ta se skládá ze tří hlavních částí:

#### 1. 📝 Nahoře: Formulář (vyplňte ho)

- **Title (Název):** GitHub vám automaticky navrhne název podle posledního commitu (např. _"Přidány složky exopamet a vhledy"_). Můžete ho nechat, nebo upravit na srozumitelnější název, např. _"Přidání základních výzkumných složek"_.
    
- **Description (Popis):** Sem napište, co jste udělali. Např.: _"Přidány prázdné složky pro výzkumné vhledy a externí paměť s README soubory."_ Toto je vaše zpráva pro sebe (nebo budoucí recenzenty).
    

#### 2. 🟩🟥 Uprostřed: Náhled změn (TO JE TO NEJDŮLEŽITĚJŠÍ!)

- Hned pod formulářem uvidíte zelené a červené řádky – to je **"diff" (rozdíl)**.
    
- **Zelené řádky** = text, který jste přidali.
    
- **Červené řádky** = text, který jste smazali.
    
- Můžete si **prolistovat všechny soubory**, které jste změnili (v záložce "Files changed").
    
- **Toto je vaše poslední možnost zkontrolovat**, zda jste omylem nezměnili něco, co jste nechtěli, nebo zda jste tam nedali soukromý e-mail.
    

#### 3. ⚙️ Dole: Tlačítka (rozhodnutí)

V dolní části uvidíte zelené tlačítko **"Create pull request"**.

---

### 🧠 Co se stane, když kliknete na "Create pull request"?

- **Nic se ještě nesloučí do `main`.**
    
- Vytvoří se pouze **žádost (PR)**, která obsahuje:
    
    - Váš název a popis.
        
    - Seznam změněných souborů.
        
    - Možnost psát komentáře.
        
- Na stránce PR uvidíte tlačítko **"Merge pull request"** – **to je to, co opravdu sloučí změny do `main`.**
    
- Toto tlačítko **kliknete až vy**, jako správce, po finální kontrole.
    

---

### ✅ Co teď udělat krok za krokem:

1. **Klikněte na zelené tlačítko "Compare & pull request"** (na webu GitHubu).
    
2. **Zkontrolujte název a popis** – upravte je, pokud chcete.
    
3. **Přejděte dolů na záložku "Files changed"** – podívejte se na zelené a červené řádky. Ověřte, že tam je jen to, co jste chtěl změnit.
    
4. **Klikněte na "Create pull request"** (zelené tlačítko).
    
5. Nyní jste na stránce PR. Znovu si prohlédněte změny.
    
6. **Klikněte na tlačítko "Merge pull request"** (pokud jste spokojený) a potvrďte kliknutím na **"Confirm merge"**.
    
7. **Gratuluji!** Vaše složky jsou teď oficiálně v hlavní větvi `main` vaší knihy.
    

---

### 🎯 Co se stane s vaší větví na PC?

- **Vaše lokální větev** (např. `pridani-slozek`) **zůstane na vašem PC** – nic se nesmaže.
    
- Můžete v ní klidně pokračovat (přidávat další kapitoly).
    
- Až budete chtít začít **novou** práci (např. novou kapitolu), vytvořte si **novou větev** (např. `kapitola-1`) z `main`.
    

---

### 📌 Shrnutí – Co vás čeká po kliknutí

|Krok|Co uvidíte|Co uděláte|
|---|---|---|
|1|Formulář PR (Title, Description)|Vyplníte / zkontrolujete|
|2|Zelené/červené změny (Files changed)|**Zkontrolujete, že je vše v pořádku**|
|3|Tlačítko "Create pull request"|Kliknete (vytvoří se žádost)|
|4|Tlačítko "Merge pull request"|Kliknete (změny se sloučí do `main`)|

**Nebojte se – poprvé to vypadá složitě, ale je to jen formalita, která vás chrání před chybou. Po dvou PR to budete dělat automaticky.**

Takže směle do toho, klikněte na "Compare & pull request" a prohlédněte si, co jste vytvořil. Je to vaše kniha a vy jste její první recenzent.

Mám tyto 2 hlášky: " Review required At least 1 approving review is required by reviewers with write access. Merging is blocked At least 1 approving review is required by reviewers with write access. "

**Toto je naprosto v pořádku a přesně podle vašich nastavení!** GitHub vám jen připomíná, že jste si nastavil **pravidlo vyžadující schválení (approval)**, než se Pull Request smí sloučit.

Jste ve **smyčce**: Vy jste ten, kdo musí schválit svůj vlastní Pull Request. Je to jako kdybyste si sami sobě dali úkol: _"Nejdřív to zkontroluj, pak to pusť dál."_

---

### ✅ OKAMŽITÉ ŘEŠENÍ (udělejte toto):

1. **Zůstaňte na stránce Pull Requestu** (tu, kde vidíte ty hlášky).
    
2. Přejděte na záložku **"Files changed"** (vedle "Conversation").
    
3. Prohlédněte si změny (zelené/červené řádky).
    
4. V pravém horním rohu najdete tlačítko **"Review changes"**.
    
5. Klikněte na něj.
    
6. Objeví se okno s možnostmi:
    
    - **"Comment"** (pouze okomentovat)
        
    - **"Approve"** (schválit)
        
    - **"Request changes"** (požadovat úpravy)
        
7. Vyberte **"Approve"**.
    
8. (Volitelně) Napište do komentáře např.: _"Kontrola provedena, složky jsou v pořádku."_
    
9. Klikněte na zelené tlačítko **"Submit review"**.
    
10. **Hlášky zmizí** a tlačítko **"Merge pull request"** se aktivuje (rozsvítí se zeleně).
    
11. Klikněte na **"Merge pull request"** → **"Confirm merge"**.
    

**Hotovo!** Vaše složky jsou sloučeny do `main`.

---

### 🧠 Proč to GitHub dělá?

Protože jste v nastavení ochrany větve zaškrtl **"Require approvals"** a nastavil na `1`. GitHub toto pravidlo aplikuje **na všechny** – i na vás, správce. Nutí vás to:

1. **Fyzicky si prohlédnout** změny (záložka Files changed).
    
2. **Vědomě odkliknout** tlačítko "Approve".
    
3. Teprve pak povolit sloučení.
    

Je to pojistka proti vaší vlastní nepozornosti. I vy si můžete omylem sloučit chybný kód/text, takže vás GitHub donutí udělat ten jeden krok navíc – podívat se na to.

---

### 📌 Co si zapamatovat pro příště

|Krok|Co děláte|Kde|
|---|---|---|
|1|Vytvoříte Pull Request|GitHub Web|
|2|**Schválíte ho (Approve)**|GitHub Web → Files changed → Review changes → Approve|
|3|**Sloučíte (Merge)**|GitHub Web → Merge pull request|

**Odteď už víte:** Každý PR, který vytvoříte, musíte nejprve **sám sobě schválit** (kliknout na "Approve") a teprve pak sloučit. Je to váš bezpečnostní ritual.

approve nemůžu. Píše mi to, že autor nemůže schválit svůj vlastní reguest, ale můžu comment, kde jsem dal "Sloučení PC větve" a pak submit review

**Výborně! Tohle je přesně ta správná reakce systému.** GitHub vám říká: _"Ty jsi autor, nemůžeš si sám sobě dát oficiální schválení (approval)."_

Je to záměr – nutí vás to nechat si PR schválit někým jiným (což je skvělé pro týmovou práci). Protože ale pracujete **sám**, máte dvě jednoduché cesty, jak PR sloučit. Vyberte si tu, která se vám hodí.

---

### ✅ OKAMŽITÉ ŘEŠENÍ (Vyberte si):

#### Možnost A: Sloučit i bez schválení (Pouze pro vás, jako správce)

Protože jste správce repozitáře, máte právo **přepisovat** pravidla ochrany a sloučit PR i bez formálního schválení.

1. Zůstaňte na stránce Pull Requestu.
    
2. Podívejte se na konec stránky (kde je tlačítko **"Merge pull request"**). I když je šedé, vedle něj je malý odkaz nebo tlačítko **"Merge without waiting for requirements to be met"** nebo **"Merge pull request"** (někdy je přímo aktivní pro adminy).
    
3. Klikněte na něj a potvrďte **"Confirm merge"**.
    
4. **Hotovo!** Vaše složky jsou sloučeny do `main`.
    

---

#### Možnost B: Dočasně vypnout pravidlo schvalování (Pro usnadnění práce)

Pokud chcete mít jednodušší workflow, můžete na chvíli vypnout požadavek na schválení.

1. Jděte do **Settings → Branches** vašeho repozitáře.
    
2. Najděte pravidlo ochrany pro `main` a **vypněte** volbu **"Require approvals"** (nebo ho upravte na `0`).
    
3. Vraťte se na Pull Request – tlačítko **"Merge pull request"** bude aktivní.
    
4. Sloučte ho.
    
5. **Pak se vraťte do nastavení a zase to zapněte** (nastavte na `1`), aby ochrana dál platila pro budoucí PR.
    

---

#### Možnost C: Přizvat někoho, kdo to schválí (Když budete spolupracovat)

Až budete mít spolupracovníky (studenty, kolegy), stačí je přidat jako **spolupracovníky** (Collaborators) a oni vám pak mohou PR schválit. To je ta pravá týmová práce.

---

### 🧠 Co se stalo s vaším komentářem?

Když jste dal **"Comment"** a napsal _"Sloučení PC větve"_, bylo to správné – zanechalo to v PR záznam, že jste to zkontroloval. Ale protože jste autor, GitHub vám nedal možnost "Approve", jen "Comment" a "Request changes".

---

### 📌 Doporučení pro vás (do budoucna)

Protože jste na začátku a pracujete sám, **nastavte si ochranu takto:**

- **"Require a pull request before merging"** → **ZAPNOUT** (chrání před přímými zásahy do `main`).
    
- **"Require approvals"** → **VYPNUTO** (nastavte na `0`).
    

**Proč?**

- Ochrana `main` zůstane (nikdo do ní nepustí přímo).
    
- Ušetříte si zdržování se schvalováním vlastních PR.
    
- Až začnete spolupracovat se studenty, pak tuto volbu zapnete a budete vyžadovat jejich schválení.
    

---

### ✅ Takže teď:

1. Použijte **Možnost A** (merge bez schválení) – jste admin, máte na to právo.
    
2. Nebo použijte **Možnost B** (dočasně vypněte approvals a pak zapněte).
    

**Po sloučení:** Vraťte se do GitHub Desktopu, klikněte na **"Current branch"** → přepněte na `main` a klikněte na **"Pull origin"** (stáhnete si sloučenou verzi do PC).

**Gratuluji!** Právě jste dokončil svůj první Pull Request. Teď už víte, jak to funguje a příště to bude hračka.

Mám tam šedé tlačítko close pull reguest a vedle zelené comment

**Naprosto v pořádku, jste na správné cestě!**

Vidíte to šedé tlačítko **"Close pull request"** a zelené **"Comment"**, protože jste **ještě neprovedl finální kontrolu (Review)** a systém čeká na vaše rozhodnutí.

Jelikož jste autor a GitHub vám neumožňuje dát vlastní "Approve", musíte použít jinou cestu, jak PR "protlačit".

---

### ✅ OKAMŽITÉ ŘEŠENÍ (Použijte tuto cestu)

Protože jste **vlastník (Admin)** repozitáře, máte skryté právo obejít schvalování. Udělejte toto:

1. **Podívejte se na konec stránky** (těsně nad tím šedým tlačítkem "Close pull request").
    
2. Hledejte tam malý, nenápadný **odkaz** (nebo tlačítko) s nápisem:
    
    > **"Merge without waiting for requirements to be met"**  
    > _(Někdy je to přímo zelené tlačítko "Merge pull request", které je ale teď šedé; v takovém případě hledejte text "Merge without waiting...".)_
    
3. **Klikněte na něj.** (Pokud ho nevidíte, pokračujte krokem 4.)
    
4. **Pokud toto tlačítko nemáte**, udělejte toto:
    
    - Otevřete si v nové záložce **Settings → Branches**.
        
    - Najděte pravidlo ochrany pro `main`.
        
    - **Dočasně vypněte** volbu **"Require approvals"** (odškrtněte nebo nastavte na `0`).
        
    - Vraťte se na stránku PR a **objeví se vám aktivní zelené tlačítko "Merge pull request"**.
        
    - Klikněte na něj a potvrďte **"Confirm merge"**.
        
    - Pak se vraťte do **Settings → Branches** a **zase to zapněte** (nastavte na `1`), aby ochrana zůstala pro budoucí PR.
        

---

### 🧠 Proč to nevidíte hned?

Protože GitHub striktně odděluje role:

- **Autor** = nemůže schválit svůj vlastní PR (proto vám ukazuje jen "Comment").
    
- **Admin** = má právo **sloučit i bez schválení**, ale toto tlačítko se objeví **až když projdete všemi kontrolami** (např. žádné konflikty).
    

Někdy je to schované pod odkazem **"Merge without waiting"**, aby vás to donutilo si změny alespoň prohlédnout (což jste udělal komentářem).

---

### 📌 Co udělat teď:

1. **Zkuste najít odkaz "Merge without waiting for requirements to be met"** – klikněte na něj a sloučte.
    
2. **Pokud ho nemáte**, použijte dočasné vypnutí `approvals` v **Settings → Branches** (výše popsané).
    

**Až to uděláte, vaše složky budou v `main`.**

Gratuluji k prvnímu úspěšnému PR! Příště už to bude snazší.

Mám 2 hlášky: " Review required At least 1 approving review is required by reviewers with write access. Merging is blocked At least 1 approving review is required by reviewers with write access. " Pod tím mohu vybrat - Merge pull reguest - Squash an merge - Rebase and merge Vedle mám You can also merge this with the command line. Ale jinak žádný nenápadný odkaz.

**Výborně!** Teď už máte všechny možnosti přímo před sebou. Ty tři zelená tlačítka (`Merge pull request`, `Squash and merge`, `Rebase and merge`) jsou přesně to, co potřebujete.

Protože jste správce (Admin) a GitHub vám je ukazuje, **můžete je ignorovat a použít jeden z nich i bez schválení**. Není potřeba žádný "nenápadný odkaz".

---

### ✅ OKAMŽITÉ ŘEŠENÍ (Vyberte si):

V podstatě máte dvě cesty, jak to obejít. Vyberte si tu, která vám dává větší kontrolu.

---

#### 🚀 Možnost A: Sloučit přímo přes příkazovou řádku (Pouze pro vás, bez schválení)

Protože jste na GitHubu, můžete využít tu možnost **"You can also merge this with the command line"**, která vám umožní sloučit PR, aniž byste museli vyřešit blokování schválením.

1. **Klikněte na ten modrý odkaz** _"You can also merge this with the command line"_ (je pod těmi třemi tlačítky). Obvykle se rozbalí okno s příkazy.
    
2. Zkopírujte si příkaz, který vám tam GitHub nabídne (vypadá jako `git checkout main && git merge ...`).
    
3. Otevřete **GitHub Desktop** a v něm **"Open in Command Prompt"** (nebo terminál).
    
4. Vložte ten příkaz a stiskněte Enter.
    
5. **Hotovo!** PR je sloučen do `main` bez nutnosti schválení.
    

**Výhoda:** Rychlé, nic nemusíte nastavovat.  
**Nevýhoda:** Musíte použít příkazovou řádku.

---

#### ⚙️ Možnost B: Dočasně vypnout pravidlo schvalování (a pak ho zase zapnout)

1. Otevřete v nové záložce **Settings → Branches** vašeho repozitáře.
    
2. Najděte pravidlo ochrany pro `main` a **vypněte** volbu **"Require approvals"** (odškrtněte ji nebo nastavte na `0`).
    
3. Vraťte se na stránku PR (obnovte ji – F5).
    
4. **Tlačítko `Merge pull request` se aktivuje** (zelené).
    
5. Klikněte na **`Merge pull request`** a potvrďte **"Confirm merge"**.
    
6. Pak se vraťte do **Settings → Branches** a **zase to zapněte** (nastavte na `1`), aby ochrana zůstala pro budoucí PR.
    

---

### 🧠 Co která možnost dělá (pro vaše pochopení):

|Možnost|Co udělá|Kdy ji použít|
|---|---|---|
|**Merge pull request**|Vezme všechny commity z vaší větve a přidá je do `main` včetně historie.|Když chcete zachovat každý commit (např. pro přehled).|
|**Squash and merge**|**Sloučí všechny commity do jednoho** a ten přidá do `main`.|Když jste udělali 20 malých commitů, ale v knize chcete vidět jen jeden celek.|
|**Rebase and merge**|Přehraje commity na konec `main` (zachová historii, ale bez merge commitu).|Když chcete mít lineární historii (bez "merge" záznamů).|

**Pro vaši knihu doporučuji `Merge pull request`** – zachováte tak přehlednou historii, co jste v rámci větve dělali.

---

### 📌 Co teď udělat

1. Vyberte si **Možnost B** (dočasně vypnout approvals) – je to nejbezpečnější, protože se učíte.
    
2. Až to uděláte, **klidně klikněte na `Merge pull request`** a potvrďte.
    
3. Vaše složky jsou v `main`.
    
4. Nezapomeňte **zase approvals zapnout**!
    

**Po sloučení:** Vraťte se do GitHub Desktopu, klikněte na **"Current branch"** → přepněte na `main` a klikněte na **"Pull origin"** (stáhnete si sloučenou verzi do PC).

**Gratuluji!** Zvládl jste svůj první Pull Request. Teď už víte, jak to funguje.

Mám 4 možnosti: Step 1 Clone the repository or update your local repository with the latest changes. git pull origin main Step 2 Switch to the base branch of the pull request. git checkout main Step 3 Merge the head branch into the base branch. git merge PC Step 4 Push the changes. git push -u origin main Mám vybrat 3?

Toto je špatná zpráva – **tady se skrývá obrovské nebezpečí!**

**Nevybírejte možnost 3!** Pokud teď uděláte `git merge PC` na svém lokálním `main` (který nemá vaše poslední commity z PR) a pak to pushnete, **přepíšete historii a ztratíte svou práci!**

---

### 🧠 Proč je to teď špatně?

Podívejte se na váš stav:

- **Na GitHubu** (v cloudu) máte Pull Request z větve `PC` do `main`.
    
- **Na vašem PC** (lokálně) máte `main`, který **neobsahuje vaše commity z PR** (protože PR ještě nebyl sloučen).
    
- Kdybyste teď udělali `git merge PC` lokálně a pushnuli to do `main`, **obešli byste celý Pull Request** a vaše commity by se do `main` dostaly přímo – ale GitHub by je neviděl jako sloučené přes PR, což by způsobilo chaos.
    

---

### ✅ SPRÁVNÝ POSTUP (Jak to udělat bezpečně)

Vy **nemusíte** používat příkazovou řádku. Stačí **jednoduchá cesta přes GitHub web**:

#### Možnost A: Dočasně vypnout approvals (Nejjednodušší)

1. **Zavřete terminál** (nepoužívejte ho).
    
2. Otevřete GitHub web na stránce vašeho Pull Requestu.
    
3. V nové záložce otevřete **Settings → Branches**.
    
4. Najděte pravidlo pro `main` a **dočasně vypněte** volbu **"Require approvals"** (nastavte na `0`).
    
5. Vraťte se na PR (obnovte stránku F5).
    
6. **Tlačítko "Merge pull request" bude teď aktivní** (zelené) – **klidně ho klikněte**.
    
7. Potvrďte **"Confirm merge"**.
    
8. Pak se vraťte do **Settings → Branches** a zase to zapněte (nastavte na `1`).
    

**Toto je nejbezpečnější cesta**, protože vše probíhá přes GitHub, který si sám hlídá konzistenci. Vaše commity se dostanou do `main` a historie zůstane čistá.

---

#### Možnost B: Sloučit přes příkazovou řádku (Bezpečně, ale složitější)

Pokud opravdu chcete použít terminál (což nedoporučuji, dokud se nevyznáte), museli byste postupovat **jinak**, než nabízí ty 4 kroky. Ale to je zbytečně složité.

---

### 📌 Co teď udělat

1. **Zavřete terminál**.
    
2. Použijte **Možnost A** (dočasně vypnout approvals, sloučit přes web, zase zapnout).
    
3. Až to uděláte, vraťte se do GitHub Desktopu a udělejte **"Pull origin"** na `main`, abyste si stáhli sloučenou verzi.
    

**Tímto postupem nic nezkazíte a vaše práce bude v bezpečí.**

Nechci pravidlo, které musím vypínat pro vlastní merge, protože když to vypnu, tak mi můžou v tom čase jiní lidé pushnout svůj obsah. Potřebujeme systémové řešení, ne hacky na teď, ale postup práce.

**Máte naprostou pravdu.** Vypínání ochrany je dočasný hack, ne systémové řešení. Pro vaši situaci (jste jediný správce a zároveň jediný přispěvatel) potřebujete nastavit trvalý pracovní postup, který nebude vyžadovat žádné obcházení pravidel.

---

### ✅ Systémové řešení: Dva způsoby

Existují **dvě čisté cesty**, jak pracovat, aniž byste museli vypínat ochranu. Vyberte si tu, která vám vyhovuje.

---

### 🧠 1. Dlouhodobá pracovní větev (Doporučuji pro vás)

Toto je nejjednodušší a nejpřirozenější způsob pro autora, který píše knihu.

**Princip:** Nepracujete v `main` vůbec. Máte **jednu trvalou pracovní větev** (např. `vypracovani`), ve které děláte veškerou svou práci. Do `main` slučujete **jen hotové celky** (např. dokončené kapitoly) pomocí Pull Requestů.

|Větev|Účel|Kdo do ní zapisuje|
|---|---|---|
|**`main`**|**Oficiální verze knihy** – vždy stabilní, publikovatelná.|Pouze vy, a to výhradně přes PR.|
|**`vypracovani`**|**Vaše pracovní větev** – sem píšete průběžně, ukládáte commity, pushujete.|Pouze vy (přímý zápis).|

**Pracovní postup:**

1. **Vytvoříte větev `vypracovani`** (stačí jednou):
    
    bash
    
    git checkout -b vypracovani
    git push -u origin vypracovani
    
2. **Každý den:** Pracujete výhradně ve větvi `vypracovani`. Commit, push – vše do této větve. (Ochrana `main` se vás netýká, protože do ní nepushujete.)
    
3. **Až máte hotovou kapitolu:** Vytvoříte Pull Request z `vypracovani` do `main`.
    
4. **Schválení PR:** Zde přichází klíčový krok. Protože jste autor, **nemůžete si PR sám schválit**. Ale **můžete ho sloučit**, pokud v nastavení ochrany **povolíte administrátorům obejít schvalování**.
    
    - V **Settings → Branches** upravte pravidlo pro `main`:
        
        - **Zapněte** `Require a pull request before merging`.
            
        - **Zapněte** `Require approvals` (nastavte na 1).
            
        - **Zapněte** (důležité!) **`Allow specified actors to bypass required pull requests`** a do seznamu přidejte své uživatelské jméno.
            
        - (Tato volba se jmenuje různě – hledejte `Bypass` nebo `Allow administrators to bypass`.)
            
    
    **Výsledek:** Když vytvoříte PR, GitHub bude stále vyžadovat schválení, ale **vy jako administrátor můžete PR sloučit přímo**, aniž byste museli čekat na schválení od jiné osoby. Ostatní (kteří nejsou v seznamu) toto právo nemají.
    

---

### 🌿 2. Krátkodobé větve pro každou kapitolu (Standardní týmový postup)

Toto je přesně ten workflow, který používá 90 % týmů na GitHubu. Je vhodný, pokud chcete mít maximální přehled o tom, co se kdy dělalo.

**Princip:** Pro každou novou kapitolu (nebo úkol) vytvoříte **novou větev**. Až je kapitola hotová, uděláte PR a ten sloučíte. Poté větev smažete.

**Pracovní postup:**

1. **Vytvoříte větev pro kapitolu:**
    
    bash
    
    git checkout -b kapitola-3
    
2. **Pracujete, commitujete, pushujete** do této větve.
    
3. **Až je kapitola hotová:** Vytvoříte PR z `kapitola-3` do `main`.
    
4. **Sloučení:** Stejně jako výše – použijete právo administrátora obejít schvalování.
    
5. **Po sloučení:** Větev `kapitola-3` smažete (lokálně i na GitHubu) a vytvoříte novou pro další kapitolu (`kapitola-4`).
    

---

### 🛠️ Nastavení ochrany pro tento systém

1. Jděte do **Settings → Branches**.
    
2. Upravte pravidlo pro `main` takto:
    

|Volba|Nastavení|
|---|---|
|`Require a pull request before merging`|**Zapnuto** (ochrana před přímým pushem)|
|`Require approvals`|**Zapnuto** (nastavte na 1)|
|`Allow specified actors to bypass`|**Zapnuto** → přidejte své uživatelské jméno|
|`Do not allow bypassing`|**Vypnuto** (aby vaše právo obejití platilo)|

Toto je **jednorázové nastavení**, které už nikdy nebudete muset měnit. Je to čisté, bezpečné a splňuje vaši podmínku: _"Ostatní nemohou pushnout, ale já jako správce mohu sloučit své PR."_

---

### ✅ Shrnutí

|Váš požadavek|Řešení|
|---|---|
|"Nechci vypínat ochranu"|Nastavíte `Bypass` pro vaše uživatelské jméno.|
|"Jiní nemají pushovat"|Ochrana zůstává aktivní pro všechny ostatní.|
|"Chci systémové řešení"|Pracujete ve větvích (dlouhodobé nebo krátkodobé) a PR slučujete jako admin.|

**Toto je profesionální workflow, který používá většina open-source projektů.** Už žádné hacky, žádné obcházení. Jen čistá, standardní práce s Gitem.

Tohle jsou jediné možnosti pod pull reguest: " Dismiss stale pull request approvals when new commits are pushed New, reviewable commits pushed will dismiss previous pull request review approvals. Require review from specific teams A collection of reviewers and associated file patterns. Each reviewer has a list of file patterns which determine the files that reviewer is required to review. Require review from Code Owners Require an approving review in pull requests that modify files that have a designated code owner. Require approval of the most recent reviewable push Whether the most recent reviewable push must be approved by someone other than the person who pushed it. Require conversation resolution before merging All conversations on code must be resolved before a pull request can be merged. "

Děkuji za výpis. Toto jsou **všechny dostupné volby** v rámci pravidel pro **"Pull request"**.

Abych to vyřešil systémově a bez hacků, musíme si uvědomit, že **GitHub nenabízí tlačítko "Povolit adminovi obejít schválení" v rámci těchto checkboxů**. Tato funkce se nastavuje **o úroveň výš** – v samotném **"Ruleset"** (pravidle) a ne v těchto zaškrtávacích políčkách.

Pojďme se proto podívat na to, co **musíte udělat**, abyste měli čistý systém:

---

### 🛠️ SYSTÉMOVÉ ŘEŠENÍ (Nastavte to jednou a zapomeňte)

Přesuňte se o krok zpět do **nastavení celého pravidla (Ruleset)**.

1. V **Settings → Branches** klikněte na název vašeho pravidla (nebo na tři tečky a **"Edit"**).
    
2. Přejděte na **začátek stránky** (sekce **"Bypass"** nebo **"Permissions"**).
    

Tam (nikoli v těchto checkboxech) hledejte volbu:

> **"Allow specified actors to bypass"**

nebo

> **"Bypass"** (často v sekci "Target" nebo "Permissions").

Pokud tam tuto možnost nemáte, znamená to, že GitHub vám nabízí **pouze tu poslední možnost**, kterou jste vypsal – **"Require approval of the most recent reviewable push"**.

---

### ✅ SPRÁVNÉ NASTAVENÍ PRO VÁS (Pokud nemáte "Bypass")

Protože vaše volby končí u "Require approval of the most recent reviewable push" (tedy že schválení musí dát **někdo jiný než autor**), máte **dvě systémové cesty**, jak to obejít:

#### Možnost A (Doporučuji): Přidat si druhý účet – "správce schvalovatele"

- Založte si na GitHubu **druhý účet** (např. `kontrolor`), dejte mu práva **Write** k repozitáři.
    
- Když vytvoříte PR pod svým hlavním účtem, přihlaste se na tento druhý účet, projděte "Files changed", klikněte na **"Review changes" → "Approve"**.
    
- Tím splníte podmínku "někdo jiný než autor schválil" a PR můžete sloučit.
    

> _Toto je legální, čistý způsob a používá ho mnoho vývojářů, když pracují sami._

---

#### Možnost B: "Require approval of the most recent reviewable push" nechat VYPNUTO

- **Vypněte** tuto poslední možnost ve vašem seznamu.
    
- Tím GitHub nebude vyžadovat, aby schválení dal někdo jiný.
    
- **Ale** ochrana `main` zůstane – stále budete muset projít Pull Requestem (což je to, co chcete).
    
- Vy jako autor pak budete moci PR sloučit **bez schválení**, ale **pouze pokud máte v pravidle nastavené "Bypass"** (viz první odstavec).
    

---

### 🧠 Co dělají vaše možnosti (vysvětlení)

|Vaše možnost|Co dělá|Doporučení|
|---|---|---|
|`Dismiss stale approvals`|Když někdo přidá nový commit, staré schválení se zruší.|Nechte zapnuto – chrání před změnami po schválení.|
|`Require review from specific teams`|Vyžaduje schválení od určitého týmu.|**Nepotřebujete** (pracujete sami).|
|`Require review from Code Owners`|Vyžaduje schválení od vlastníků kódu (CODEOWNERS).|Nechte vypnuto, dokud nebudete mít tým.|
|`Require approval of the most recent reviewable push`|**Musí schválit někdo jiný než autor.**|**TUTO VYPNĚTE**, pokud nemáte druhý účet (Možnost A).|
|`Require conversation resolution`|Vyžaduje vyřešení všech komentářů před sloučením.|Nechte zapnuto – zlepšuje kvalitu.|

---

### 📌 Shrnutí – Co udělat teď

1. **Vraťte se na začátek pravidla** (Edit ruleset) a hledejte možnost **"Bypass"** nebo **"Allow administrators to bypass"**.
    
    - **Pokud ji najdete:** Přidejte své uživatelské jméno a vše je vyřešeno.
        
    - **Pokud ji nenajdete:** Použijte **Možnost B** – vypněte _"Require approval of the most recent reviewable push"_ a PR budete moci sloučit sami.
        
2. **Uložte pravidlo** a už ho nikdy neměňte.
    
3. **Odteď** pracujte ve větvích, vytvářejte PR, a protože jste admin (nebo máte vypnuté "approval from someone else"), můžete PR sloučit bez čekání na externí schválení.
    

**Toto je systémové a trvalé řešení.** Už žádné vypínání ochrany, už žádné hacky.

Pokud budu mít baypass, nemusím už dělat v PC větvi, ale rovnou to pushnout do main z PC. Souhlas?

**Ne, to není správná úvaha!** I když si nastavíte **Bypass** (obcházení) na své uživatelské jméno, **pořád byste neměl pushovat přímo do main z PC**.

Pojďme si to jasně oddělit, protože je to zásadní rozdíl:

---

### 🔑 Co Bypass (oprávnění) skutečně dělá

|Oprávnění|Co umožňuje|Co NEUMOŽŇUJE|
|---|---|---|
|**Bypass (Obcházení)**|Umožňuje **sloučit Pull Request** i když nemá schválení.|**NEUMOŽŇUJE** pushovat přímo do `main` (přes `git push`).|

**Bypass se vztahuje POUZE na Pull Requesty na GitHubu, ne na přímé pushování.**

---

### 🧠 Proč to tak je?

Pravidlo ochrany větve má dvě samostatné části:

1. **"Require a pull request before merging"** = zakazuje přímé pushy do `main` (ať už jste kdokoli).
    
2. **"Require approvals"** = vyžaduje schválení PR.
    

**Bypass** se vztahuje **pouze na bod 2** – umožní vám sloučit PR bez schválení. Ale **bod 1** (zákaz přímého push) zůstává v platnosti i pro vás.

---

### ✅ Správný pracovní postup (i s Bypass)

|Krok|Co děláte|Kde|
|---|---|---|
|1|Vytvoříte **větev** (např. `kapitola-3`)|GitHub Desktop / terminál|
|2|Pracujete, commitujete, pushujete do **větve**|GitHub Desktop|
|3|Vytvoříte **Pull Request** z větve do `main`|GitHub Web|
|4|**Sloučíte PR** (díky Bypass to jde i bez schválení)|GitHub Web|
|5|Větev smažete (volitelné)|GitHub Web / Desktop|

**Nikdy nepushujete přímo do `main`.** Vždy přes větev + PR.

---

### 🎯 Co vám Bypass přináší (oproti původnímu stavu)

|Bez Bypass|S Bypass|
|---|---|
|Musíte čekat na schválení PR (od někoho jiného).|**Můžete si PR sloučit sám**, bez čekání.|
|Stále musíte vytvářet větev a PR.|Stále musíte vytvářet větev a PR.|
|Nemůžete pushovat přímo do `main`.|**Stále nemůžete pushovat přímo do `main`.**|

---

### 📌 Závěr

|Vaše otázka|Odpověď|
|---|---|
|"S Bypass mohu pushovat přímo do main?"|**NE.** Bypass se vztahuje jen na PR, ne na přímý push.|
|"Musím stále dělat větev a PR?"|**ANO.** To je jediná cesta, jak se změny dostanou do `main`.|
|"Co mi Bypass usnadní?"|Umožní vám **sloučit PR bez čekání na schválení**.|

**Stručně:** Bypass vám ušetří čekání na schválení, ale **nemění pravidlo, že do main se chodí jen přes Pull Request**. To je základní kámen ochrany větve a platí pro všechny – včetně vás.

OK. Zvládnul jsem to spojit, ale když jsem šel do main větve, tak jsem se podíval na MK a chtěl jsem jej jen mírně poupravit. Udělal jsem to, main se upravil, ale vytvořila se další větev s merge jako při pullu

**Tohle je naprosto normální a správné chování Gitu!** Nestalo se nic špatného.

Git si automaticky vytvořil "merge commit" (slučovací commit) proto, aby **zaznamenal**, že jste spojil dvě větve dohromady. Je to jako když slepíte dva prameny provazu a na místě spoje uděláte uzlík – Git si ten uzlík (merge commit) uloží do historie, aby věděl, kde se větve potkaly.

---

### 🧠 Co se přesně stalo?

1. **Vytvořil jste Pull Request** z vaší pracovní větve (např. `PC`) do `main` a úspěšně jste ho sloučil.
    
2. Git vytvořil **merge commit**, který spojil historii obou větví.
    
3. **Poté jste přepnul na `main`** a udělal jste v něm malou úpravu (opravil jste překlep v README).
    
4. Git si toto uložil jako **nový commit** v rámci `main`.
    

**Výsledek:** Vaše historie teď obsahuje:

- Původní commity ve větvi `PC`.
    
- Merge commit, který je spojil s `main`.
    
- Nový commit v `main` s vaší úpravou.
    

---

### ✅ Co teď s tou "novou větví"?

Ta "další větev" (která vznikla) je s největší pravděpodobností **pouze lokální reference** na váš poslední Pull Request. Můžete ji bez obav smazat, protože už jste ji sloučili.

**V GitHub Desktopu:**

1. Klikněte na **"Current branch"**.
    
2. Podívejte se, zda tam vidíte větev `PC` (nebo jinou, kterou jste použili pro PR).
    
3. Pokud tam je a už ji nepotřebujete, klikněte na ni pravým tlačítkem a vyberte **"Delete branch"**.
    
    - (Ujistěte se, že jste předtím přepnutý na `main` – jinak si smažete větev, ve které zrovna jste.)
        

---

### 🧠 Proč je to v pořádku? (Grafické vysvětlení)

Představte si historii jako řeku:

text

main:      ●───●───●───○ (merge commit)───● (váš nový commit)
              \         /
PC:            ●───●───●

- **První tři body** v `main` jsou vaše původní commity.
    
- **Tři body** ve větvi `PC` jsou vaše pracovní commity.
    
- **Kolečko (merge commit)** je bod, kde se obě větve spojily.
    
- **Poslední bod** je vaše dodatečná úprava v `main`.
    

**Merge commit je zcela normální a žádoucí** – zaznamenává, že jste začlenil práci z jiné větve. Bez něj byste nevěděl, odkud změny přišly.

---

### 📌 Co si zapamatovat

|Co se stalo|Je to špatně?|Co dělat|
|---|---|---|
|Vytvořil se merge commit|**NE** – je to běžné.|Nic – nechte ho v historii.|
|Vytvořila se nová větev (lokální)|**NE** – je to jen reference.|Smažte ji, pokud ji nepotřebujete.|
|Upravil jsem README v `main`|**NE** – je to vaše kniha.|Commitněte a pushněte (přímo do `main` teď můžete, protože jste už PR sloučil).|

---

### 🎯 Doporučení pro příště

Až budete chtít opravit malý detail v README v `main`:

1. Ujistěte se, že jste v `main`.
    
2. Udělejte úpravu.
    
3. Commitněte a pushněte **přímo do `main`** (protože teď už není žádný otevřený PR, který by to blokoval).
    
4. **Není třeba vytvářet novou větev** pro tak malou opravu (pokud už není otevřený PR).
    

Tímto způsobem udržíte historii přehlednou – hlavní kapitoly procházejí PR, malé opravy v `main` děláte přímo.

Už to vidím. Při změně MD jsem mohl komitnout, ale teď mi to dalo do nové větve a na výběr do main. Jenže před tím jsem dělal přímo v main... A když komitnu do main, tak tam mám baypass rules... Takže proto mi to změnilo a vytvořilo 3tí větev. Nevšimnul jsem si.

**Teď už to chápete naprosto přesně!** Vaše analýza je správná a jste na konci této "první křivky učení".

Stalo se přesně to, co říkáte:

1. **Nejdřív jste upravoval přímo v `main`** (pravděpodobně jste zapomněl, že jste v něm, nebo jste si myslel, že "teď už to jde").
    
2. **Commit do `main`** jste chtěl udělat, ale GitHub/Branch Protection pravidlo (které vyžaduje PR) **zakázalo přímý push** do `main`.
    
3. **GitHub Desktop** (nebo Git) to vyřešil tak, že **automaticky vytvořil novou větev**, aby vaše změny neztratil, a nabídl vám, abyste je poslal (pushnul) přes Pull Request.
    
4. Vy jste si toho nevšiml a potvrdil jste to – tak vznikla **třetí větev**.
    

---

### 🎯 Co se stalo, je **standardní ochrana** v akci.

Systém vás donutil jít správnou cestou (přes Pull Request), i když jste to neudělal vědomě. Je to jako kdybyste strčil klíč do zámku, ale dveře se neotevřely – tak jste je obešel bočním vchodem (novou větví).

Teď máte v repozitáři tyto větve:

1. **`main`** – oficiální verze.
    
2. **`PC`** – vaše pracovní větev (už sloučená).
    
3. **Nová větev** (pojmenovaná např. `patch-1` nebo `main-...`) – obsahuje vaši poslední úpravu README.
    

---

### ✅ Co s tím teď?

1. **Podívejte se, co ta nová větev obsahuje.**
    
    - Otevřete ji na GitHubu nebo v Desktopu. Uvidíte tam jen tu jednu malou úpravu README.
        
2. **Vytvořte Pull Request** z této nové větve do `main`.
    
    - Klikněte na "Compare & pull request".
        
    - Napište zprávu, např.: _"Oprava překlepu v README."_
        
3. **Sloučte PR** (jako předtím). Protože máte nastavený bypass pro sebe, můžete ho sloučit ihned.
    
4. **Po sloučení** tuto novou větev smažte (lokálně i na GitHubu).
    

---

### 🧠 Co si z toho odnést

|Situace|Co Git udělá|
|---|---|
|Jste v `main` a uděláte Commit + Push.|Pokud máte zapnutou ochranu, **Push selže**.|
|Uděláte Commit v `main`, ale neuděláte Push.|Git si commit uloží lokálně. Když pak zkusíte Push, znovu selže.|
|GitHub Desktop vidí, že Push do `main` nejde.|**Automaticky nabídne vytvoření nové větve** pro vaše změny.|

**Vaše "chyba" byla v tom, že jste zapomněl, že jste v `main`, a udělal commit. Git vás ale chytře zachránil před pádem – vaše změny uložil do nové větve a umožnil vám je odeslat přes PR.**

---

### 📌 Závěr – Už jste hotov!

- **Nastavení ochrany** máte funkční.
    
- **Bypass** máte nastavený.
    
- **Workflow** už znáte: Větev → PR → Merge.
    

**Třetí větev je jen "záchranný člun"** pro vaši poslední úpravu. Slučte ji, smažte a pokračujte v psaní knihy. Odteď už budete **vědomě** vytvářet nové větve pro každou změnu, a tohle už se nestane.

Zajímá mne, jak vymazat tu 3tí větev.

**Výborně, tohle je snadné.** Smažeme ji **na GitHubu** (protože už ji nepotřebujete) a pak **lokálně na PC**, aby vám neukazovala v seznamu.

---

### 🗑️ Smazání větve na GitHubu (Web)

1. **Otevřete si svůj repozitář** na GitHubu.
    
2. Klikněte na rozbalovací menu, kde je napsáno **"main"** (vlevo nahoře, hned vedle "Code").
    
3. Do vyhledávacího pole napište název té třetí větve (např. `patch-1` nebo jak se jmenuje).
    
4. Jakmile ji najdete, uvidíte vedle ní **ikonu koše** (🗑️). Klikněte na ni.
    
    - _(Pokud tam ikonu nevidíte, klikněte na větve → zobrazí se seznam → vedle názvu větve klikněte na tři tečky a vyberte "Delete branch".)_
        

**Tím jste smazali větev na GitHubu.**

---

### 🗑️ Smazání větve na PC (Lokálně)

Teď ji smažeme z vašeho počítače, aby vám neukazovala v seznamu v GitHub Desktopu.

1. **Otevřete GitHub Desktop.**
    
2. Ujistěte se, že **jste přepnutý na `main`** (ne na tu třetí větev).
    
    - Klikněte na **"Current branch"** a vyberte `main`.
        
3. Znovu klikněte na **"Current branch"** – uvidíte seznam všech větví.
    
4. **Klikněte pravým tlačítkem myši** na název té třetí větve (např. `patch-1`).
    
5. V nabídce vyberte **"Delete branch"** (Smazat větev).
    
    - _(Pokud větev nebyla plně sloučena, aplikace vás upozorní – ale v tomto případě ji sloučenou máte, takže to projde.)_
        

**Hotovo.** Větev zmizí z vašeho PC.

---

### 📌 Pokud chcete smazat větev přes příkazovou řádku

Pokud byste se někdy ocitli v terminálu a chtěli větve mazat:

bash

# Smazání lokální větve
git branch -d nazev-vetve
# Smazání větve na GitHubu (vzdálené)
git push origin --delete nazev-vetve

---

### ✅ Výsledek

|Místo|Stav|
|---|---|
|**GitHub (Cloud)**|Třetí větev smazána.|
|**Váš PC (lokální)**|Třetí větev smazána.|
|**Historie (`main`)**|Vaše poslední úprava README je v `main` (díky PR).|

**Gratuluji!** Naučil jste se smazat větev. Teď už máte repozitář čistý a připravený na další práci.

Poslední věc. Jak si pulnout main do PC větve v desktopu, abych pracoval s aktuální verzí?

Tohle je naprosto zásadní a správná otázka! **Přesně tak, než začnete psát novou kapitolu, musíte si do své pracovní větve stáhnout nejnovější verzi z `main`** (např. opravy, které jste udělal vy nebo jiní).

Pokud to neuděláte, budete pracovat se starou verzí a na konci budete řešit zbytečné konflikty.

Zde je **jediný správný postup**, jak na to v GitHub Desktopu. (Tento postup se nazývá **"Rebase"** nebo **"Merge"** -- já vám ukážu ten přehlednější, tedy **Merge**).

---

### 🔄 Jak dostat změny z `main` do vaší pracovní větve (v GitHub Desktopu)

Předpokládejme, že máte vytvořenou větev `moje-prace` a chcete do ní dostat aktuální `main`.

#### Krok 1: Přepněte se na `main` a stáhněte novinky

1. Otevřete GitHub Desktop.
    
2. V horní liště klikněte na **"Current branch"** a vyberte **`main`** (přepnete se na hlavní větev).
    
3. Klikněte na tlačítko **"Pull origin"** (nebo "Fetch origin" a pak "Pull").
    
    - _Tím se stáhnou z GitHubu všechny nejnovější změny, které v `main` přibyly (např. vaše sloučené PR)._
        

#### Krok 2: Přepněte se zpět do své pracovní větve

1. Znovu klikněte na **"Current branch"** a vyberte svou větev (např. `moje-prace`).
    
    - _Teď jste zpět ve své pracovní větvi, ale **pořád máte starou verzi** bez novinek z `main`._
        

#### Krok 3: Slučte (Merge) do ní novinky z `main`

1. V horní liště klikněte na **"Branch"** (v menu úplně nahoře) a vyberte **"Merge into current branch..."**.
    
2. V zobrazeném okně klikněte na větev **`main`** (tu chcete sloučit do své pracovní větve).
    
3. Klikněte na tlačítko **"Merge main into moje-prace"**.
    
4. **Hotovo!** Vaše větev `moje-prace` teď obsahuje všechny novinky z `main`. Můžete v ní klidně pokračovat v práci.
    

---

### 🧠 Co když vám to napíše, že došlo ke konfliktu (Conflict)?

To se stane, pokud jste ve své větvi upravili stejný řádek textu, jako byl změněn v `main`. GitHub Desktop vás na to upozorní.

- Nebojte se, nestalo se nic špatného. Git si sám neví rady, který řádek má ponechat, a proto se vás zeptá.
    
- Budete muset otevřít daný soubor (např. v poznámkovém bloku) a ručně vybrat, která verze má zůstat (vaše, nebo z `main`).
    
- Jakmile soubor uložíte a dáte Commit, konflikt je vyřešen.
    

---

### 📌 Zjednodušená mantra (pro zapamatování)

> **"Než začnu psát, přepnu na main, Pullnu, vrátím se do své větve a sloučím do ní main."**

Neboli: **`main` → Pull → moje-větev → Merge main`**.

Tímto zajistíte, že vaše práce vždy navazuje na úplně poslední verzi knihy a vyhnete se nočním můrám s konflikty na poslední chvíli.

Díky za provedení. Vše je hotovo. V obsidianu se mi automaticky změnil MD, tedy pokládám to za hotové. Zítra si to zafixuji.

To je skvělá zpráva! 🎉

**Gratuluji!** Úspěšně jste prošel celým procesem – od založení repozitáře, přes nastavení ochran, lokální práci s větvemi, Pull Requesty, slučování, až po finální stažení aktualizací do PC. Navíc jste si ověřil, že váš nástroj (Obsidian) změny bez problémů přečetl, což je pro plynulou práci klíčové.

---

### 📌 Shrnutí vašeho nového pracovního postupu (pro zítřek)

1. **Před psaním:** V GitHub Desktopu si stáhněte aktuální `main` a slučte ho do své pracovní větve.
    
2. **Psaní:** Pracujte vždy ve své pracovní větvi (`vypracovani`).
    
3. **Ukládání:** Pravidelně commitujte a pushujte do své větve (záloha v cloudu).
    
4. **Dokončení:** Až bude kapitola hotová, vytvořte Pull Request z vaší větve do `main` a slučte ho.
    
5. **Po sloučení:** Smažte starou větev a vytvořte novou pro další část.
    

---

### 🧠 Co si zafixovat (mentální model):

- **`main`** = oficiální, hotová kniha (nedotýkat se jí přímo).
    
- **Vaše větev** = váš pracovní stůl.
    
- **Pull Request** = váš kontrolní bod, kde si práci sami schválíte.
    
- **Pull (stažení)** = synchronizace s nejnovější verzí před začátkem práce.
    

---

**Přeji vám hodně zdaru při psaní!** Pokud zítra narazíte na cokoli, co si nebudete jistý, víte, kde mě najdete. 👍

Dá se GitHubu přepsat jen název složky?

**Ano, jde to, ale pozor – GitHub (ani Git) nemá tlačítko "Přejmenovat složku".**

Děje se to tak, že **složku přejmenujete lokálně na svém počítači**, pak dáte Commit a Push. Git to chytře vyhodnotí jako **přesun (rename)** a na GitHubu se to zobrazí jako přejmenovaná složka (nikoli jako smazání a nové vytvoření).

---

### ✅ Postup (v GitHub Desktopu)

1. **Otevřete Průzkumníka Windows** a najděte složku, kterou chcete přejmenovat (např. `stary-nazev`).
    
2. **Klikněte na ni pravým tlačítkem → Přejmenovat** a napište nový název (např. `novy-nazev`).
    
3. **Otevřete GitHub Desktop** – uvidíte, že se změna objevila v seznamu změn (Git to detekoval jako "rename").
    
4. Napište zprávu do "Summary", např.: _"Přejmenování složky stary-nazev na novy-nazev"_.
    
5. Klikněte na **"Commit to ..."** (uloží se lokálně).
    
6. Klikněte na **"Push origin"** (odešle se na GitHub).
    

---

### 🧠 Co se stane na GitHubu?

- **Historie souborů zůstane zachována** – Git si pamatuje, že soubory byly přesunuty. Když se podíváte na historii souboru, uvidíte ho i pod starým názvem.
    
- GitHub to zobrazí jako **"renamed"** (přejmenováno), nikoli jako "deleted" + "added".
    

---

### ⚠️ Důležité upozornění

- **Pokud máte otevřený Pull Request**, který se týká souborů v této složce, přejmenování může způsobit **konflikty**. Ideálně udělejte přejmenování **před** vytvořením PR, nebo až po jeho sloučení.
    
- **Ostatní spolupracovníci** si po přejmenování musí stáhnout novou verzi (`git pull`), aby měli správnou strukturu.
    

---

### 🧪 Případná možnost: Přejmenování přes webové rozhraní

Pokud chcete přejmenovat složku přímo na GitHubu (bez lokálního Gitu):

1. Otevřete repozitář na GitHubu.
    
2. Přejděte do složky, kterou chcete přejmenovat.
    
3. Klikněte na **"Add file" → "Create new file"**.
    
4. Do názvu souboru napište **novou cestu** ke složce (např. `novy-nazev/README.md`).
    
5. Do obsahu vložte obsah starého souboru.
    
6. Poté starý soubor smažte (přes ikonu koše).
    
7. Commitněte změny.
    

**Toto je ale pracnější a méně přehledné.** Doporučuji lokální přejmenování přes Průzkumníka + Commit v GitHub Desktopu.

---

### 📌 Shrnutí

|Akce|Nástroj|Výsledek|
|---|---|---|
|Přejmenování složky|Průzkumník Windows|Lokální změna|
|Commit + Push|GitHub Desktop|Změna se projeví na GitHubu|
|Historie souborů|Zůstává zachována|Git vidí "rename"|

**Takže ano, přejmenovat složku jde snadno – stačí to udělat lokálně a pak Commit + Push.**

Připrav cele kontextové okno k archivaci paměti. Potřebuji rozdělit kontext na logické celky o tom, co jsme probírali, opatřit je názvem, krátkým popisem a citací, kterou úsek začíná. Postup: - Rozděl kontext podle tématu (nejdi do detailů, 2-20 paměťových částí, množství částí musí být vyvážené. Co jde spojit, spoj, co je jiné téma, nová část. Části musí být postupně navazovány na celé kontextové okno, nejde spojit části do jedné, když je rozdělena jiným tématem) - Indexuj část (01, 02, 03, ... 20) - Vymysli krátký název (max. 4 slova) - Vymysli krátký popis aby bylo jasno co která část obsahuje (max. 4 věty) - Vypiš přesnou citaci začátku textu (max. 10 slov) pro zpětnou dohledatelnost v textovém editoru (ctrl+f). - Musíš obsáhnout celé kontextové pole. 01 část je od citace 01 po citaci 02.

**Výborně, tady je kompletní indexace našeho kontextového okna.**

Rozdělil jsem celou naši konverzaci do **11 logických částí**, které na sebe postupně navazují a pokrývají celé spektrum probíraných témat – od úplných základů, přes spolupráci, autorská práva, až po konkrétní workflow a správu souborů.

---

### 🧠 **01 – Úvod do GitHubu a Gitu**

- **Název:** Základy verzování
    
- **Popis:** Vysvětlení rozdílu mezi Gitem (verzovací systém na PC) a GitHubem (webová platforma). Definice klíčových pojmů: Repozitář, Commit, Push, Pull, Branch.
    
- **Citace začátku:** _"GitHub je v podstatě sociální síť pro vývojáře..."_
    

### 🧠 **02 – Komunita a oprávnění**

- **Název:** Veřejné vs. Soukromé
    
- **Popis:** Kdo tvoří komunitu na GitHubu. Rozdíl mezi veřejnými (přístup pro všechny) a soukromými (pouze na pozvání) repozitáři. Role jako Read, Write, Admin.
    
- **Citace začátku:** _"Na GitHubu se setkáte s obrovskou a různorodou komunitou..."_
    

### 🧠 **03 – Autorská práva a Licence**

- **Název:** Ochrana díla
    
- **Popis:** Výchozí stav "Bez licence" (všechna práva vyhrazena). Výběr správné licence (CC BY-ND pro knihu) a vlastní smluvní dodatky pro univerzity. Ochrana velkých témat a propojení s autorem.
    
- **Citace začátku:** _"To je velmi důležitá a častá otázka..."_
    

### 🧠 **04 – Profesionální workflow a ochrana**

- **Název:** Ochrana main větve
    
- **Popis:** Nastavení Branch protection rules (zákaz přímého push do main, vyžadování Pull Requestů). Systémové řešení pomocí Bypassu pro správce. Důvod, proč ochrana platí i na majitele.
    
- **Citace začátku:** _"Tohle je zásadní krok, aby nikdo nemohl nahrát změny do main..."_
    

### 🧠 **05 – Práce na PC a GitHub Desktop**

- **Název:** Lokální nastavení
    
- **Popis:** Instalace Gitu a GitHub Desktopu. Proces klonování (stažení) repozitáře do počítače. Řešení problému "unable to locate Git" a nastavení cesty.
    
- **Citace začátku:** _"Výborně, přesuneme se z webového rozhraní do profesionálního prostředí..."_
    

### 🧠 **06 – Pracovní cyklus (Větev, Commit, Push)**

- **Název:** Každodenní rytmus
    
- **Popis:** Sekvence práce: Vytvoření větve → psaní → Commit (lokální uložení) → Push (odeslání do cloudu). Vysvětlení, že Commit je jen lokální a teprve Push ho dostane na GitHub. Řešení chyby při push do main.
    
- **Citace začátku:** _"Teď už to chápete naprosto přesně! Tohle je ten 'AHA' moment..."_
    

### 🧠 **07 – Pull Request a Merge**

- **Název:** Schvalování změn
    
- **Popis:** Proces vytvoření Pull Requestu (PR) na webu. Nutnost schválení (Approve) a následného sloučení (Merge). Vysvětlení tlačítek "Merge", "Squash" a "Rebase". Role správce při slučování.
    
- **Citace začátku:** _"Ano, přesně tak! Klikněte na Compare & pull request..."_
    

### 🧠 **08 – Řešení konfliktů a historie**

- **Název:** Čistá historie
    
- **Popis:** Co dělat při konfliktech (stejný řádek změněn ve dvou větvích). Vznik "merge commitů" jako záznamu o spojení větví. Důležitost čisté historie pro knihu.
    
- **Citace začátku:** _"Tohle je naprosto normální a správné chování Gitu!"_
    

### 🧠 **09 – Formáty souborů (Markdown vs. DOCX)**

- **Název:** Psaní knihy
    
- **Popis:** Výhody Markdownu (`.md`) oproti DOCX na GitHubu – zobrazení, navigace, historie změn. Doporučení psát v MD a konvertovat až finální verzi.
    
- **Citace začátku:** _"Vaše úvaha je naprosto přesná. Ano, na GitHubu má Markdown..."_
    

### 🧠 **10 – Organizace a správa složek**

- **Název:** Struktura projektu
    
- **Popis:** Vytváření, přejmenování a mazání složek (přes Průzkumníka + Commit). Archivace starých kapitol do vedlejších větví. Práce s JSON a Issue šablonami pro LLM.
    
- **Citace začátku:** _"Ano, jde to, ale pozor – GitHub nemá tlačítko Přejmenovat složku..."_
    

### 🧠 **11 – Závěrečný přehled a bezpečnost**

- **Název:** Účty a zálohy
    
- **Popis:** Nastavení soukromí e-mailu (anonymní `noreply` adresa). Recovery kódy (2FA) – chovat se k nim jako k seedu v kryptu. Závěrečné shrnutí celého workflow.
    
- **Citace začátku:** _"Poslední věc. Jak si pulnout main do PC větve..."_
    

---

**Toto je kompletní mapa našeho kontextu.** Pokud ji uložíte do svého `pamet/README.md` nebo jako samostatný soubor `pamet/index.md`, budete se k jednotlivým částem moci rychle vracet pomocí `Ctrl+F` podle úvodních citací.

Tato odpověď je generována AI Assistantem, pouze pro referenci.