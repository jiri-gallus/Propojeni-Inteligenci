# Úkol  

Je potřeba rozložit kontextové okno na informační celky. Jednotlivé věty, které se doplňují. nejít na nižší celky. Celý kontext budeš tvořit ve 3 vlnách.
### 1. generace tokenů
- Definovat téma
Zvolí se metrika posuzování.
### 2. generace tokenů
- vypsat celé citace celků a obhájit, které jsou mimo téma.
Odfiltrují se celky, které nemusíme analyzovat.
### 3. generace tokenů
- vypsat celé citace celků a obhájit, které téma neprohlubují.
Analýzu procházet a vypisovat celky zpětně. Na konci kontextového okna se očekává nejvíce neprohlubujících témat.
## Zlaté pravidlo
Bojujeme proti patern recognition bias.
- Nevypisuješ do kontextu nic jiného, než 1. 2. 3. vlnu a text zlatého pravidla.
- 1. vlna nesmí vést k označení prvního výskytu myšlenky za neprohlubující.
- 2. a 3. vlna má opakující se vzor pro každý jednotlivý celek. Celá citace>Obhajoba>Text zlatého pravidla
- Hledáme všechny informační celky, které téma neprohlubují.
### Text zlatého pravidla:
"Vzor v kontextu je principiální. Nejde o hranice možného. LLM se musí dívat při každém tokenu nezaujatě vůči vzoru. Braň zlaté pravidlo!"
# Text k analýze