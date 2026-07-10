jak pozvat někoho do GitHubu? Kde najdu link?

Pozvání někoho do GitHubu záleží na tom, **kam** je chcete pozvat.

GitHub má několik úrovní a každá má své vlastní tlačítko a odkaz. Zde je přehled podle toho, co potřebujete:

---

### 1. Chcete pozvat spolupracovníka do svého **REPOZITÁŘE** (kód)

Pokud chcete, aby mohl upravovat váš kód ve vašem projektu:

1. Jděte na hlavní stránku vašeho repozitáře na GitHubu.
    
2. Klikněte na záložku **Settings** (Nastavení) – úplně vpravo nahoře.
    
3. V levém menu klikněte na **Collaborators** (Spolupracovníci).
    
4. Klikněte na zelené tlačítko **Add people** (Přidat lidi).
    
5. Zadejte jeho **uživatelské jméno**, **celé jméno** nebo **e-mail** na GitHubu.
    
6. Klikněte na jeho jméno a potvrďte.
    

> **Odkaz, který pošlete vy:** Žádný speciální odkaz neexistuje. GitHub mu po přidání pošle **e-mailové pozvání**. Vy mu můžete jen poslat přímý odkaz na váš repozitář (např. `github.com/tvujucet/nazev-repozitare`) a on si ho tam najde, až přijme pozvánku v e-mailu.

---

### 2. Chcete pozvat člena do **ORGANIZACE** (firma, tým)

Pokud máte firemní nebo týmový účet (GitHub Organization):

1. Jděte na hlavní stránku vaší organizace (např. `github.com/nazev-organizace`).
    
2. Klikněte na záložku **People** (Lidé).
    
3. Klikněte na zelené tlačítko **Invite member** (Pozvat člena).
    
4. Zadejte jeho uživatelské jméno nebo e-mail.
    
5. Nastavte mu roli (např. _Member_ nebo _Owner_) a případně ho přiřaďte do týmů.
    
6. Klikněte na **Send invitation**.
    

> **Odkaz:** GitHub opět primárně posílá pozvánku e-mailem. Pozvaná osoba ji uvidí také po přihlášení na své GitHub notifikaci (zvoneček nahoře vpravo).

---

### 3. Chcete někomu poslat **PŘÍMÝ ODKAZ** na repozitář (jen pro čtení)

Pokud mu chcete poslat jen odkaz, aby si váš kód **prohlédl** nebo ho naklonoval (ale neupravoval), stačí mu poslat URL v prohlížeči:

- Příklad: `https://github.com/tvuj-ucet/nazev-repozitare`
    

---

### 4. Kde najdu odkaz na pozvání pro "Čtenáře" (pokud je repozitář soukromý)?

Pokud je repozitář **soukromý** a vy chcete, aby ho někdo jen viděl (bez možnosti editace), musíte ho přidat jako **spolupracovníka** (viz bod 1) a při přidávání mu vedle jména nastavit roli na **Read** (Čtenář) místo Write (Zapisovatel).

---

### Shrnutí – Kde hledat tlačítko:

|Kam chcete pozvat?|Cesta na GitHubu|
|---|---|
|Do svého repozitáře|`Repozitář` → `Settings` → `Collaborators` → `Add people`|
|Do organizace|`Vaše organizace` → `People` → `Invite member`|
|Do svého osobního účtu (sdílení účtu)|**To nejde a nedoporučuje se** (prosdílení přihlašovacích údajů je proti pravidlům).|

**Důležité:** Pozvaná osoba musí mít **vlastní účet na GitHubu**. Bez něj pozvánku nepřijme. Pokud ji nemá, pošlete jí nejdříve odkaz na registraci: `https://github.com/join`.

Jaký je rozdíl mezi 1. a 3.? Jako že chápu, ale myslel jsem když je repozitář veřejný, že 1. může dělat každý.

Máte naprostou pravdu, že jste to podchytil. Omlouvám se, že to v předchozí odpovědi nebylo dost jasné.

Rozdíl mezi **1. (přidání jako Collaborator)** a **3. (poslání URL odkazu)** je zásadní a opravdu závisí na tom, jestli je repozitář **veřejný**, nebo **soukromý**. Pojďme si to přesně rozčlenit:

---

**1. Když je repozitář VEŘEJNÝ (Public)**

- **Odkaz (3.)**: Stačí poslat komukoliv odkaz `github.com/uzivatel/repozitar`. Ten člověk si váš kód může **prohlížet**, stáhnout si ho (klonovat) a používat ho. **Nesmí** však do něj nahrávat změny (pushovat) ani vytvářet nové větve, pokud nemá vaše výslovné oprávnění.
    
- **Přidání jako Collaborator (1.)**: Toto děláte ve chvíli, kdy chcete, aby **mohl do vašeho veřejného repozitáře zapisovat** (tedy nahrávat kód, mazat větve, zakládat pull requesty přímo). Bez tohoto přidání to dělat nemůže.
    

> **Zkráceně pro veřejný repozitář:**  
> Stačí poslat odkaz (3.) = dívá se.  
> Musí ho přidat (1.) = může upravovat.

---

**2. Když je repozitář SOUKROMÝ (Private)**

- **Odkaz (3.)**: Když pošlete pouhý odkaz (např. `github.com/uzivatel/soukromy-repo`), ten člověk uvidí **chybovou stránku 404 (Not Found)**. Soukromý repozitář totiž nevidí nikdo kromě vás a lidí, které tam ručně přidáte.
    
- **Přidání jako Collaborator (1.)**: Toto je **jediná možnost**, jak mu umožnit repozitář **vůbec vidět**. Když ho přidáte přes `Settings > Collaborators`, můžete mu při přidávání vedle jména nastavit roli:
    
    - **Read (Čtenář)**: Bude ho vidět, může si ho stáhnout, ale **nesmí** do něj nahrávat.
        
    - **Write (Zapisovatel)**: Bude ho vidět **a** bude do něj moct nahrávat.
        

> **Zkráceně pro soukromý repozitář:**  
> Posílání samotného odkazu (3.) je k ničemu (nepůjde otevřít).  
> Musí ho vždy přidat (1.) – a podle toho, jakou roli mu dáte, určíte, zda se jen dívá, nebo i upravuje.

---

### Takže reálně, jak to uděláte vy?

- Pokud máte **veřejný projekt** a chcete, aby se na něj někdo jen podíval nebo ho použil → pošlete mu **odkaz (3.)**.
    
- Pokud chcete, aby **do vašeho kódu přímo zasahoval** (ať už je repozitář veřejný, nebo soukromý) → musíte ho **přidat jako Collaborator (1.)**.
    

Snad je to teď srozumitelnější! Dejte vědět, pokud řešíte konkrétní situaci (např. jestli chcete, aby jen nahlásil chyby, nebo s vámi opravdu kódoval).

Připrav cele kontextové okno k archivaci paměti. Potřebuji rozdělit kontext na logické celky o tom, co jsme probírali, opatřit je názvem, krátkým popisem a citací, kterou úsek začíná. Postup: - Rozděl kontext podle tématu (nejdi do detailů, 2-20 paměťových částí, množství částí musí být vyvážené. Co jde spojit, spoj, co je jiné téma, nová část. Části musí být postupně navazovány na celé kontextové okno, nejde spojit části do jedné, když je rozdělena jiným tématem) - Indexuj část (01, 02, 03, ... 20) - Vymysli krátký název (max. 4 slova) - Vymysli krátký popis aby bylo jasno co která část obsahuje (max. 4 věty) - Vypiš přesnou citaci začátku textu (max. 10 slov) pro zpětnou dohledatelnost v textovém editoru (ctrl+f). - Musíš obsáhnout celé kontextové pole. 01 část je od citace 01 po citaci 02.

Během našeho rozhovoru jsme probrali tato témata. Zde je přehled pro archivaci paměti, rozdělený do logických celků tak, jak na sebe v kontextu navazovaly:

---

**01 – Základní pozvání do GitHubu**  
_Popis:_ Úvodní vysvětlení, jak pozvat někoho do GitHubu. Rozdělení podle místa (repozitář, organizace, účet) a popis tlačítek.  
_Citace začátku:_ "Pozvání někoho do GitHubu záleží na tom, kam je chcete pozvat."

---

**02 – Pozvání do repozitáře vs. odkaz pro čtení**  
_Popis:_ Vysvětlení zásadního rozdílu mezi přidáním jako Collaborator (s oprávněním zapisovat) a pouhým posláním URL odkazu.  
_Citace začátku:_ "Máte naprostou pravdu, že jste to podchytil."

---

**03 – Veřejný vs. soukromý repozitář a práva**  
_Popis:_ Detailní rozlišení, jak funguje odkaz a přidání spolupracovníka u veřejného (Public) a soukromého (Private) repozitáře. Role Read a Write.  
_Citace začátku:_ "Rozdíl mezi 1. (přidání jako Collaborator) a 3. (poslání URL odkazu) je zásadní..."

---

**04 – Praktické doporučení a závěr**  
_Popis:_ Shrnutí, jak postupovat v praxi podle typu projektu (veřejný x soukromý) a co dělat, když chcete, aby někdo pouze nahlásil chybu, nebo s vámi aktivně kódoval.  
_Citace začátku:_ "Takže reálně, jak to uděláte vy?"