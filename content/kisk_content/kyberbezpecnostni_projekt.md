+++ 
title = "Kyberbezpečnost, design a lidé: Miniprojekt" 
date = "2025-07-24" 
author = "Anežka Müller" 
+++

### Zarámování

Kurzu Kyberbezpečnost, design a lidé, který jsem v tomto semestru absolvovala, je v roce 2025 navázán na [Czech Cybersecurity Seminars](https://css.muni.cz/), a proto byl součástí i návrh a realizace vlastního miniprojektu pro zvýšení kybernetické bezpečnosti v konkrétní organizaci.

Cílem miniprojektu bylo navázat spolupráci s malou lokální oficiální komunitní organizací a pomoci v ní implementovat nějaké opatření v oblasti kybernetické bezpečnosti. 
Během celé doby realizace jsme mohli využít konzultací s vyučujícími, kteří nám pomohli co nejlépe nastavit realistické cíle a připravit finální intervenci tak, aby měla v organizaci reálný dopad.

### Průběh

Miniprojekt měl celkem 5 fází:
* Výběr organizace
* Nastavení mindsetu    
* Rámování problému, definování designové výzvy
* Návrh kyberbezpečnostního opatření
* Realizace opatření

Každou fázi jsme podrobně dokumentovali v terénním deníku a průběžně jsme dostávali zpětnou vazbu, abychom věděli, zda postupujeme správným směrem. 

Výběr organizace byl čistě na nás. 
Měli jsme dané parametry, které musela organizace splňovat, ale také svobodu v tom, jakou organizaci pro spolupráci oslovíme. 
Šlo především o to, aby naše práce měla reálný dopad a přínos pro organizaci, která by jinak na pomoc v rámci kyberbezpečnostních opatření dosahovala s obtížemi. 

V mém případě šlo o malou neziskovou organizaci zaměřenou na environmentální tématiku. 
Funguje dva roky, má malý pětičlenný tým a vznikla oddělením od jiné, větší organizace. 
To se nakonec ukázalo jako klíčové pro zaměření finálního návrhu opatření. 

Během základního průzkumu jsem zjistila, že téma kyberbezpečnosti není v organizaci nijak akcentováno a chybí i základní bezpečnostní návyky, například při sdílení hesel, práci s nástroji nebo přístupu k datům. 
Proto jsem identifikovala tři oblasti, na které jsem se chtěla primárně zaměřit. 
Bezpečnostní kulturu obecně, správu hesel a bezpečnou práci s daty.

Z prvního hlubšího rozhovoru v rámci rámování problému vyplynulo, že organizace aktuálně využívá SW infrastrukturu původní mateřské organizace, což považují za dlouhodobě neudržitelné a plánují přechod na vlastní nástroje, které aktuálně vybírají. 
Potvrdilo se, že v organizaci není nastavená žádná bezpečnostní politika ani pro práci s daty, v rámci používaných nástrojů, ani pro sdílení hesel. 
Přechod k vlastním nástrojům se tedy jevil jako vhodná příležitost zavést v organizaci nějaké bezpečnostní minimum.   

Původním cílem spolupráce tedy měla být pomoc s nastavením bezpečnostní politiky v organizaci a týmu. 
Zahrnovat měla návrh základních bezpečnostních pravidel pro celý tým, návrh bezpečného využívání nově zaváděných nástrojů a návrh bezpečné práce s daty. 
To se však rychle ukázalo jako příliš ambiciózní a rozsáhlé, jak z hlediska časové náročnosti, tak mých znalostí a schopností. 
Proto jsme se po poradě a podrobném rozboru možností s vyučující a posléze se zástupci organizace dohodli na zúžení záměru pouze na část bezpečné práce s daty a to konkrétně na provedení datového auditu jako podklad pro další práci.

### Výstupy

Aktuálně organizace používá řadu nástrojů společných s původní zakládající organizací. 
Není jasná struktura vlastnictví dat, jakými daty organizace disponuje, kdo k nim má přístup, kdo by k nim měl mít přístup, a jak s nimi bezpečně zacházet. 
Cílem datového auditu tedy bylo zmapovat, jaká data organizace vlastní, kde jsou uložena, kdo k nim má přístup, jak se používají a jak jsou spravována, a navržení doporučení do budoucna.

V rámci realizace jsem uskutečnila rozhovory s týmem, ve kterých jsem se zaměřila na práci s daty, datovými úložišti a dalšími používanými nástroji. 
Na základě zjištěných informací jsem vytvořila datový inventář, který popisuje jednotlivé nástroje, ve kterých se nacházejí nějaká organizační data. 
Obsahuje název a popis nástroje, jeho účel v rámci práce s daty, informace, zda obsahuje citlivá nebo osobní data, zda obsahuje data klíčová pro organizaci, kdo je vlastníkem nástroje (vyplývá z historie organizace, část nástrojů je stále spravována původní mateřskou organizací), kdo má administrátorská práva a kdo má v současnou chvíli do nástroje přístup, zda jsou data pravidelně aktualizována a někde zálohována. 

Pro lepší pochopení problematických míst jsem zpracovala v Miro vizuální mapu datových toků, která zobrazuje nástroje a procesy na cestě dat od zisku po archivaci. 
Krom faktického popisu aktuálního stavu jsem se snažila zapracovat i to, jak jednotliví členové týmu popisovali chtěný stav, který ale třeba není v současné chvíli naplňován.

Finálním výstupem, který jsem předala spolu se dvěma výše zmíněnými organizaci, je dokument se shrnutím zjištění, popisem problémů a doporučeními do budoucna. 
Obsahuje popis procesu, odkazy na jednotlivé výstupy, stručné shrnutí a podrobné popisy tří oblastí, které se v rozhovorech opakovaly a ke kterým se mi podařilo získat dostatek informací. 
Jedná se o datová úložiště, osobní a citlivá data a používané nástroje. Každá sekce obsahuje popis situace, rozpis problematických bodů a návrh doporučení na jejich řešení. 
Tento dokument by měl organizaci sloužit jako podpora při přechodu na nové nástroje a nastavování vnitřních pravidel pro podporu bezpečného chování v kyberprostoru.

Už během rozhovorů se ukazovalo, že tým není spokojený se současnou situací, uvědomuje si problémy a je ochoten se podílet na jejich řešení. 

Organizace už začala dělat první kroky ke sjednocení datových úložišť a plánuje revizi nástrojů a přístupů. 
Spolu s tím je v plánu navrhnout a zavést jednotný proces, jak pracovat s daty. 

