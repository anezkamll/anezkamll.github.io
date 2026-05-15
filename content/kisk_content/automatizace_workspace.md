+++ 
title = "Zpracování příchozích dokumentů v rámci Google Workspace" 
date = "2026-05-15" 
author = "Anežka Müller" 
+++

### Zarámování 

V rámci předmětu Budoucnost práce, technologie, komunikace jsme dostali za úkol vybrat si nějaký pain point v našem pracovním nebo soukromém životě a pokusit se jej vyřešit za pomoci dostupných nástrojů nebo změnou procesu.

Rozhodla jsem se zaměřit na proces zpracování příchozích faktur v jedné z neziskových organizací, se kterými spolupracuji. 
Princip je ale možné zobecnit na jakékoliv typy příchozí pošty, kterou je potřeba zpracovávat jednotným způsobem, kde se dokola opakují stejné postupy a je tedy možné velkou část kroků automatizovat.

Mým cílem bylo popsat cestu, kterou prochází jednotlivé příchozí faktury, od vstupu přes úhradu po předání externí účetní firmě, a s pomocí nástrojů, které už má organizace k dispozici, celý proces zefektivnit. 
Největší problém, který organizace řešila, je, že neexistuje celkový přehled, jaké faktury do organizace přichází a v jakém jsou aktuálně stavu. 
Chodí různými cestami a různým lidem. 
Zároveň je potřeba faktury ukládat na specifické místo na Google Drive, kde se k nim přidává prefix dle projektu, ke kterému mají být v účetnictví přiřazeny. 
Vše se navíc řeší manuálně a zvyšuje se tak možnost lidské chyby.

### Proces a nástroje

Navržený proces byl tedy celkem přímočarý:
- Sjednotit místo, kterým do organizace faktury přicházejí.
- Příchozí faktury automaticky ukládat na dedikované místo na disku.
- Vytvořit záznam o příchozí faktuře do dedikované tabulky.
- V tabulce pracovat se stavy, ve kterých se faktura nachází.
- Po zaplacení faktury ji v rámci disku přesunout do složky pro účetní s předem daným prefixem.

Řešení jsem poté konzultovala s Claudem, který jej kompletně navrhl s pomocí nástrojů dostupných v Google Workspace:

- **Gmail**: příjem obsahu, vyhledávání, štítkování
- **Google Drive**: ukládání souborů do struktury složek
- **Google Sheets**: evidence faktur a přehled stavů
- **Apps Script**: řízení a spouštění jednotlivých kroků

Celá automatizace je napojená na Google účet a po prvotním nastavení funguje sama na pozadí.

### Na čem to stojí

**Dedikovaná e-mailová adresa**: Jedna adresa jen pro příchozí obsah daného typu, v mém případě faktur. 
Skript pak ví přesně, co sledovat, a nemusí procházet celý inbox. 
Já jsem zvolila formu Google Group, aby nebyly faktury vázané na e-mail jednoho člověka, ale v případě potřeby se mohlo měnit složení osob, které mají k obsahu Google Group přístup. 

**Jedna tabulka se stavy**: V našem případě Google Spreadsheet, který se tak stal hlavním zdrojem pravdy. 
Každá položka prochází předem definovanými stavy a automatizace na ně různými způsoby reaguje. 

**Lidský zásah**: Automatizace rozpozná, že něco přišlo, ale není úplně všemocná. 
V našem procesu je potřeba určit, pod jaký projekt faktura patří, a vytáhnout z faktury některé konkrétní informace, což pak ovlivňuje další kroky v automatizaci.

**Reakce na změny stavů**: Když se změní v tabulce u dokumentu stav, automaticky se spustí s ním související akce, například odchozí notifikace, přesun nebo přejmenování souboru, vytvoření úkolu. 
Apps Script _onEdit_ trigger spouští akci v okamžiku, kdy je políčko upraveno.

**Záchranná síť**: Denní souhrnný e-mail se seznamem všeho, co je aktuálně otevřené. 
Posílá se jen tehdy, když je co hlásit. 
Pojistka, abychom na nic nezapomněli. 

### Jak to funguje

Základní funkce se spouští v pravidelných intervalech (u nás 15 minut). 
Prohledá Gmail, zpracuje přílohy nebo jiný relevantní obsah, vytvoří řádek v tabulce a e-mail zarchivuje s předem definovaným štítkem.

Druhá funkce sleduje tabulku. 
Spustí se v okamžiku, kdy dojde ke změně políčka se stavem. 
Ovládá například rozesílání notifikací nebo přesun a přejmenování dokumentů.

Třetí funkce posílá ranní přehled. 
Projde tabulku a pošle seznam všech položek v “aktivních” stavech (v mém případě vše krom “uhrazeno”). 

Všechny tři funkce jsou na sobě nezávislé, ale všechny jsou navázané na daný Google Spreadsheet, na který je navázán celý skript v Apps Scriptu.

### Kde automatizace pomáhá a kde ne

Tak, jak je automatizace nastavená teď, nám hodně pomohla sjednotit a zefektivnit celý proces, který nebyl předtím vůbec definovaný a ve zpracování příchozích faktur byl chaos.

Mechanické věci zvládne spolehlivě. 
Uložit soubor, vytvořit řádek v tabulce, odeslat notifikaci, přesunout obsah do správné složky, přejmenovat soubor podle potřeby. Repetitivní a pro člověka trochu otravné věci, naopak ideální pro automatizaci pomocí jednoducháho skriptu. 

Kde jsem narazila byla extrakce informací přímo z dokumentů, v mém případě dodavatel nebo částka k úhradě. 
Pak věci, ke kterým je potřeba znát nějaký kontext, u mě zatřízení do projektu a kontrola správnosti faktury. 
A také ověření, zda je faktura uhrazena. 

Část těchto operací by nejspíš šla řešit, typicky kontrola úhrady skrze napojení na banku přes API.
V této fází ale nebylo cílem úplně eliminovat lidskou práci, šlo o sjednocení a zefektivnění procesu v rámci stávajících možností.
To se nám v tuto chvíli podařilo dosáhnout, ale určitě budeme proces dál vylepšovat. 
