# Předmluva
Tento dokument je výcuc z prezentací pana M, které jsou vlastně výcucem ze skript. Ostatní pomocné dokumenty byly moc špatné, tak jsem se rozhodl udělat vlastní.

# Značení
číslo) Kapitola <br />
písmenko) Podkapitola <br />
🔴 Nejasnosti a hnusy (hlavně u otázek)<br />
🔵 Přímo věci ze zkoušek <br />
🟣 Jazyk logiky <br />
💚 Správná odpověď (otázky) <br />
💥 Špatná odpověď (otázky) <br />

[Link / skok rovnou k otázkám](#otázky-vysvětlení-k-individuálním-odpovědím-v-závorce-špatné-odpovědi-mohou-chybět-ale-nejdůležitější-jsou-stejně-odpovědi-správné-)
<br />

Spolu související části z kapitol budou zlinkovány. :) <br /><br />

## 1) Základy
### a) Co je vlastně logika?
Logika je věda o správném usuzování. Je to nástroj, který ověřuje platnost argumentů.

**Úsudek / argument / výrok:** na základě předpokladů / premis můžeme usoudit, zda je závěr pravdivý. Závěr je nutně pravdivý, když jsou všechny premisy pravdivé.

Zabýváme se deduktivně platnými úsudky. Logické vyplývání závěru:
$P_1...P_n\models Z$ <br /><br /><br />


### b) Logické vyplyvání, tedy, pravda / nepravda
Závěr bude logicky vyplývat, pokud v úsudku nikdy nebudou pravdivé všechny předpoklady a zároveň nepravdivý závěr = správná logická forma. Pro správnou logickou formu taktéž potřebujeme, aby všechny nutné předpoklady byly uvedené:

🔵
Předpoklad: Číslo 7 je prvočíslo <br />
◻️◻️◻️ <br />
Závěr: Číslo 7 je dělitelné 1 a samo sebou <br /><br />
(mimochodem, takto budou dál zobrazovány úsudky, jen bez označení předpokladů a závěrů) <br /><br />
*Logika je jako AI, odvozuje si skutečnosti jen z toho, co ví. Logika nebere v úvahu souvislost, mezi "být prvočíslem" a "být dělitelný 1 a sám sebou". Musí se ji vše strčit "pod nos".* <br />

$P_1...P_n\models Z$ <br />
(pokud toto má pravdivé premisy a nepravidvý závěr, tak jde o spor) <br /><br />

🔵 **Reflexivita:** Pokud je jeden z předpokladů závěrem, tak závěr logicky vyplývá. <br /><br />

Ve výrokové logice (VL), formule (složený výrok, např. "A") výrokově logicky vyplývá z množiny formulí "M" (značíme: $M\models A$), jestliže A je pravdivá v každém modelu množiny M (jednička na konci řádku v pravdivostní tabulce, tedy pravda). <br />
Při všech ohodnoceních, kdy jsou pravdivé předpoklady, je pravdivý i závěr. Tedy, závěr je pravdivý ve všech modelech předpokladů. <br />

Logické vyplývání dokazujeme nepřímo sporem: předpokládáme, že úsudek není platný (premisy pravdivé a závěr nepravdivý) a pak se k tomu zkoušíme dostat. Pokud nalezneme spor, úsudek je platný. <br />
V přímém způsobu nepředpokládáme opak (tedy, že úsudek je neplatný). Můžeme např. přes pravdivostní tabulku (i pokud dokazujeme tautologičnost). <br />

Všechny úsudky se stejnou logickou formou jako nějaký platný úsudek jsou platné. Tedy, za proměnné (např. p, q, r) můžeme dosadit jiné proměnné a nic to nezmění. <br /> $(p \cap q) \supset r$ <br /><br /><br />


### c) Platnost / správnost
🔵 Úsudek může být platný a zároveň jeho závěr nepravdivý - avšak jedna premisa úsudku bude nutně nepravdivá. Úsudek je logicky platný pokud ve všech interpretacích, kde máme pravdivé premisy, máme pravdivý i závěr. <br />

🔵 Správnost úsudku je dána logickou strukturou. <br /><br />

🔵 **Monotónnost:** Je-li úsudek platný, pak rozšíření množiny předpokladů o další předpoklad nevede ke změně platnosti úsudku. <br />
&nbsp;&nbsp; A <br />
&nbsp;&nbsp; B <br />
&nbsp;&nbsp; C <br />
◻️◻️◻️ <br />
&nbsp;&nbsp; E <br /><br />

Je to samé co: <br /><br />

&nbsp;&nbsp; A <br />
&nbsp;&nbsp; B <br />
&nbsp;&nbsp; C <br />
&nbsp;&nbsp; D <br />
◻️◻️◻️ <br />
&nbsp;&nbsp; E <br /> [Platnost / správnost ve výrokové logice](#g-správnost-vl-v-rezolučce) <br /><br /><br />


### d) Spojitost mezi log. vyplýváním a platností
Logické vyplývání (pravda, nepravda) můžeme dokazovat přes platnost úsudku. Úsudek je platný, pokud je formule pravdivá, ale může být také platný, pokud závěr a jedna premisa je nepravdivá. Neplatný úsudek se skládá z nepravdivého závěru, jen když žádná z premis není nepravdivá. <br /><br /><br />



## 2) VL - výroková logika
### a) Základ
Analyzuje způsoby skládání jednoduchých výroků do výroků složených pomocí logických spojek. Výrok je tvrzení, o němž má smysl prohlásit, zda je pravdivé či nepravdivé. Výrok nemůže být otázka ani rozkaz. Avšak ne všechny oznamovací věty jsou výroky (Francouzský král je holohlavý - nemá smysl se nad tímto zamýšlet, když fracouzský král ani neexistuje).<br /><br />
Výroky dělíme na: <br />
*	Jednoduché - žádná vlastní část jednoduchého výroku již není výrokem.
*	Složené - výrok má vlastní část(i), která je/jsou výrokem. Logické spojky a závorky. <br /><br />
Význam jednoduchých výroků redukuje VL na pravdu (1) a nepravdu (0). Výroková logika je tedy algebrou pravdivostních hodnot. Příklady složených výroků: <br /><br />

*	V Praze prší a v Brně je hezky.
*	Není pravda, že v Praze prší. (negace) <br /><br />

🟣 **Dobře utvořena formule:** Formální jazyk je zadán abecedou (množina výchozích symbolů) a gramatikou (množina pravidel, která udávají, jak vytvářet "Dobře Utvořené Formule" - DUF. Můžeme chápat, jako správný "syntax": <br /><br />

*	Výrokové symboly: p, q, r (také příklady atomických formulí)
*	Logické spojky (funktory)
*	Pomocné symboly jako např. závorky
* Neatomická formule: $(p \cap q) \supset r$
* Složená formule: $(A \cap B)$ (A, B jsou neatomické formule) <br /><br />

!! Špatně nezneužíváme priorit a závorek! Negace má větší prioritu než např. konjunkce nebo disjunkce. !! <br /><br />

🟣 **Spojky:**
* Negace: "není pravda, že", ne-sloveso
* Konjunkce: "a" (plachetnice a parníky jsou lodě - NENÍ konjunkce!), "ale", "a zároveň", v predikátové logice (PL) pak spojka pro formalizování existenční kvantif.
* Disjunkce: "nebo"
* Implikace: "jestliže, pak", "když, tak", "je-li, pak", "pokud, pak". První člen je antecedent a druhý konsekvent (nepředpokládá se žádná obsahová souvislost). POZOR: "pouze když, pak" je přehozená implikace! ("Pokud se zlepší stav mého účtu, půjdu na pivo." - $z \supset p$, "Pouze když se zlepší stav mého účtu, půjdu na pivo." - $p \supset z$). POMŮCKA: BEZ PENĚZ DO HOSPODY NELEZ! "Protože" není spojka pro implikaci. V predikátovce je implikace spojka pro formalizovaný všeobecný kvantifikátor.
* Ekvivalence: "Právě tehdy když", "tehdy a jen tehdy" ALE NE "tehdy, když" (to je implikace).
*	Negovaná ekvivalence neboli XOR: "Buď a nebo", "... a nebo...". $\neg(p \equiv q)$ <br /><br /><br />


### b) Sémantika (význam) formulí
* Pravdivostní ohodnocení (valuace) výrokových symbolů - 1 nebo 0, tedy pravda nebo nepravda.
* Pravdivostní funkce - pro každé ohodnocení výrokových symbolů přiřazuje formuli jeji pravdivostní hodnotu. <br />
(popisujeme zde pravdivostní tabulku, respektive, její proměnné a konečnou pravdivostní hodnotu formule na koncci řádku)
[Sémantika v PL](#c-sémantika-pl1) <br /><br /><br />


### c) Splnitelnost formulí (tautologie, kontradikce, model)
**Model:** Ohodnocení proměnných, kde formule "A" je pravdivá - 1 na konci řádku v pravdivostní tabulce (u cvičení: kroužkujeme proměnné) <br />
**Splnitelná formule:** Má aspoň jeden model. Tautologie je zvláštní případ splnitelné formule. <br />
**Tautologie:** Každé ohodnocení je modelem. <br />
**Nesplnitelná formule / kontradikce:** Nemá ani jeden model. <br />
**Splnitelná množina formulí:** Existuje-li ohodnocení, které je modelem každé formule.
[Splnitelnost v PL](#d-splnitelnost--model-PL1) <br />
[Splnitelnost ve výrokové logice](#f-splnitelnost-vl-v-rezolučce) <br /><br /><br />


### d) Normální formy
Každé formuli přísluší právě jedna pravdivostní funkce (pravdivostní tabulka). Každé jedné takové funkci pak přísluší nekonečně mnoho formulí, které jsou navzájem ekvivalentní (A <=> B, A <=> C, B <=> D, C <=> D, atd.). 🔵 DŮLEŽITÉ!! Nesmíme plést tyto ekvivalence: <=> (značí úpravu) s $\equiv$ (značí stejné modely / splnitelnost - u otázek na to opět upozorním)!! Platí však A <=> B, právě když formule $A \equiv B$ je tautologie. <br />
**Element:** = literál. Literál je výrokový symbol nebo jeho negace (p, $\neg p$). <br />
**Elementární konjunkce (EK) / disjunkce (ED):** konjunkce / disjunkce literálů (celkem useless). <br />
**Úplná elementární konjunkce (UEK) / disjunkce (UED):** EK nebo ED, kde se každý symbol z množiny vyskytuje jen jednou. Useful jen pro hledání UDNF / UKNF. <br />
**Konjunktivvní (KNF) / disjunktivní normální forma (DNF):** konjunkce elementárních disjunkcí a disjunkce elementárních konjunkcí respectively. <br />
**ÚPLNÁ KONJ. NORMÁLNÍ FORMA (UKNF) / ÚPLNÁ DISJUN. NORMÁLNÍ FORMA (UDNF):** jsou ekvivalentní s původní formulí, ze které je odvozujeme. Tvar disjunkce úplných elementárních konjunkcí a konjunkce úplných element. disjunkcí. Jsou to tzv. kanonické tvary v řádcích pravd. tabulky (1 - UEK, 0 - UED). Každá formule, která není kontradikce má UDNF. Každá formule, která není tautologie má UKNF. <br /><br /><br /> 

### e) Rezoluční metoda ve VL - basics
Nechť I je literál (i), z formule $(A \cup I) \cap (B \cup \neg I)$ odvoď $(A \cup B)$. <br />
Pokud je $(A \cup I) \cap (B \cup \neg I)$ pravdivá, tak oba disjunkty (také klausule) musí být taky pravdivé (kvůli té konjunkci) $(A \cup I) = 1$  $(B \cup \neg(I)) = 1$ <br />
$(A \cup B)$ je pravdivá v modelu původní formule (díky disjunkcím je funkce pravdivá v jakémkoliv ohodnocení pro I (0, 1). Zachovala se pravdivost, ale není to přechod k ekvivalentní formuli. Důkaz byl proveden pro jakýkoliv model. Platí, že konjunktivní rozšiření formule o náš rezolvent (A U B) nemění pravdivostní funkci formule: $(A \cup I) \cap (B \cup \neg I) \cap (A \cup B)$ <br />

Jinými slovy: Pokud je původní formule pravdivá při nějaké valuaci a pokud je formule vycházející z původní formule pravdivá ve všech možných případech, tak vycházející formule je pravdivá v modelu původní formule. Pravdivostní funkce původní formule se nezmění, pokud vycházející formuli konjunktivně přidáme k té původní formuli. <br />

Konjunktivní normální forma (KNF) se v rezoluční metodě nazývá klauzulární forma. Jednotlivé konjunkty se nazývají klauzule. K prázdné klauzuli na konce rezoluční metody se dostaneme přes přidávání rezolventů (blíže ve 4. prezentaci od pana M). <br />

*	R(f) - konjunktivní rozšíření formule F o všechny rezolventy. Tedy, všechny možné kombinace rezoluce.
*	R0(F) = Ri(F) = R(Ri-1(F)) - rezoluční uzávěr formule F.
*	Platí, že: Ri(F) <=> F <br /><br /><br />


### f) Splnitelnost VL v rezolučce
* Důkaz, že A je kontradikce (nesplnitelná): existuje n takové, že Rn(A) obsahuje prázdnou klauzuli. Tedy, existuje rezoluční proces, který nás dostane k prázdné klauzuli.
* Nepřímý důkaz (naše "normální" rezoluční metoda), že A je tautologie: $\neg A$ je kontradikce.
* Důkaz, že množina formulí je nesplnitelná: musíme u všech dokázat, že to jsou kontradikce. <br />

Odvodit, co vyplývá z {A1,...,An} znamená odvodit všechny rezolventy. Používané pro AI. Máme formuli, na kterou používáme rezoluční metodu. Každé jeji upravené části odvozují další skutečnosti (cv. 4, příklad 2. v RES).
[Splnitelnost v PL](#d-splnitelnost--model-PL1) <br />
[Splnitelnost v logice - základy](#c-splnitelnost-formulí-tautologie-kontradikce-model) <br /><br /><br />


### g) Správnost VL v rezolučce
* Důkaz správnosti úsudku $A_1...A_n\models Z$ (rezolučkama)
*	🔵 Přímý - postupným vytvářením rezolvent odvodíme, že vyplývá.
* 🔵 Nepřímý - dokážeme že $A_1...A_n \supset Z$ je tautologie, neboli $A_1 \cap ... \cap A_n \supset \neg Z$ je kontradikce - nesplnitelná. <br />
(příklady ve 4. prezentaci od pana M) <br />

* V rezolučce můžeme v každém kroku vypustit jen jednu dvojici literálů.
* 🔴 Můžeme na konci z formule odvodit dvě tautologie, což je v pořádku, protože tautologie vyplývá z jakékoli formule(???).
* Můžeme uvíznout na nekonečné větvi nebo nic neodvodíme. [Platnost / správnost v logice - základy](#c-platnost--správnost) <br /><br /><br />

## Důležité pojmy (so far, nalinkované mezi sebou výše)
* Vyplývání [Logické vyplývání - základy](#b-logické-vyplyvání-tedy-pravda--nepravda)
* Platnost / správnost [Platnost / správnost v logice - základy](#c-platnost--správnost)
* Splnitelnost [Splnitelnost v logice - základy](#c-splnitelnost-formulí-tautologie-kontradikce-model)
* Sémantika [Sémantika ve VL](#b-sémantika-význam-formulí) <br /><br /><br />



## 3) 🔵 Množiny
### a) Co je množina?
Množina je soubor prvků a je svými prvky plně určena; množinu s prvky a, b, c značíme: {a, b, c}. <br />
Prvkem množiny může být opět množina. Množina také nemusí mít žádné prvky: $\varnothing$. <br />
Příklady množin: $\varnothing$, {a,b}, {b,a},{a,b,a}, {{a,b}}, {a,{b,a}}, { $\varnothing$ , { $\varnothing$ },{{ $\varnothing$ }}} <br />
Množiny jsou identické, právě tehdy a jen tehdy, když mají stejné prvky (princip extenzionality). <br /><br /><br />


### b) Důležité vztahy a operace (a můžeme nahradit čímkoliv, jen nechat závorky a symboly)
*	$a \in$ {a, b}
*	$a \notin$ {{a, b}} ALE {a,b} $\in$ {{a,b}}
*	$\varnothing \in$ { $\varnothing$ , { $\varnothing$ },{{ $\varnothing$ }}}, ale neleží pro žádné a,b,c..
*	{a, b} = {b, a} = {a,b,a} ALE {a,b} $\ne$ {{a, b}} $\ne$ {a, {b, a}}
*	$\varnothing \notin \varnothing$ ALE $\varnothing \subseteq \varnothing$
*	{a} $\subseteq$ {a}
*	$\varnothing \subseteq$ {a} ALE $\varnothing \notin$ {a}
*	{a} $\nsubseteq$ {{a}}

* Podmnožina: $\subseteq$ - A je podmnožinou B, právě když A $\cup$ B = B A ZÁROVEŇ právě když A $\cap$ B = B. V A jsou prvky z B.
* Vlastní podmnožina: $\subset$ - A je vlastní podmnožinou B, právě když A je podmnožinou B, ale A se nerovná B (B má vlastní prvky, které nejsou v A).
* Průnik: $\cap$
* Sjednocení: $\cup$
* Rozdíl: \
* Doplněk (komplement): Doplněk A k M. Nechť A je podmnožinou M, výsledek = M \ A
* Kartézský součin: NOTE! <a,b> se nerovná <b,a>. U n-tic záleží na pořadí a prvky se mohou opakovat (narozdíl od množin)
* Zobecnění: A x ... x A - množina n-tic. Také můžeme značit $A^{n}$.
* Potenční množina: P(A) = {B | B $\subseteq$ A}, značíme také $2^{A}$. Krátce, do potenční množiny libovolné množiny patří: Ø, všechny prvky množiny individuálně a všemožné kombinace prvků mezi sebou v množině. <br />

🔵 **Kardinalita / mohutnost:** Mohutnost množiny (také kardinalita množiny) je pojmem teorie množin vyjadřující velikost, počet prvků u konečných, ale i nekonečných množin. Značíme |M|. <br />
|A| = |B| právě když existuje bijekce f (níže): A $\to$ B <br />
|A| menší nebo rovno |B| právě když existuje injekce f (níže): A $\to$ B <br /><br /><br />


### c) Relace a funkce
* Relace mezi množinami A, B je podmnožina Kartézského součinu A x B. Používa n-tice.
* Notace: <a,b> $\in$ R značíme také R(a,b) nebo a R b.
* Můžeme si představit jako tabulku (i v prezentaci), kde řádky jsou jednotlivé n-tice.

Funkce (zobrazení):
* Ve funkci musí být v prním argumentu furt „stejný“ prvek ($a_1$, $a_2$, $a_3$ – $a_1$, $a_2$ nebo $a_3$ se nesmí opakovat) a ke každému takovému prvku existuje nanejvýš prvek druhý (výsledek funkce).
* Množinu M x...x M nazýváme def. obor (doména) funkce f, množinu M pak obor hodnot (range).
* Jako interpretace funkčních symbolů symbolů formulí predikátové logiky 1 (níže v dokumentu) používáme pouze totální funkce.

* Surjekce: Všechny prvky z "pravé" množiny musí být použité a více prvků z "levé množiny" může vést k jednomu prvku zprava.
* Injekce: Všechny prvky z levé množiny musí být použité a více prvků z pravé množiny nemůže vést k jednomu zprava.
* Bijekce: Párování každého prvku s každým z obou množin.

* 🔵 Parciální funkce - nemá žádný obraz
* Totální funkce - celá doména, např. f(x) <br /><br /><br />



## 4) Predikátová logika 1. řádu (PL1)
### a) Co je PL1?
Jednoduché výroky, kde VL nestačí. "existuje ..", "všechna ..", "žádná .." apod. <br />
*	x - je individuová proměnná. Člen nějakého predikátu ("skupiny").
* Velké písmena (např. P v P(x)) jsou predikátové symboly.
*	Funkční symbol - konstanta (např. "a", O(a)).
*	Každý symbol proměnné (x,y,...) je term.
*	Jsou-li prvky ve funkci termy a f je funkční symbol, tak f($t_1$, $t_2$) je term.
* Atomické formule se skládá z predikátového symbolu, který má v závorce termy (P(x), P(t)).
* Formule - každá atomická formule je formule.


### b) 🟣 Jazyk PL1
* Všeobecný kvantifikátor: "všichni", "žádní", "nikdo".
* Existenční kv.: "někdo", "něco", "někteří", "existuje".
* POZOR NA DVOJÍ ZÁPOR! Je lepší si větu přeložit do AJ, příklady: 1) "Žádná ryba není inteligentní." $\to$ "No fish is inteligent". Negace bude u vlastnosti inteligence!!, 2) "Všichni vodníci nejsou mokří." $\to$ "All mermen are not wet." Negace bude na začátku formule!! (lehce clunky angličtina nutná pro tuto pomůcku) <br /><br /><br />


### c) Sémantika PL1
Pokud nevíme, co znamenají symboly v PL (P, Q, R,...), tak nemá smysl zjišťovat pravdivost formule. Avšak např. P(x) $\supset$ P(x) je vždy pravdivá (za všech okolností), je tautologie.

* P(x, f(x)) - binární (2 argumenty). Označuje tedy binární relaci. R $\subseteq$ U x U
* f(x) - unární. Označuje tedy nějakou funkci. f $\subseteq$ U x U, f: U $\to$ U
[Sémantika ve VL](#b-sémantika-význam-formulí) <br /><br /><br />


### d) Splnitelnost / model PL1
Spojené se sémantikou. Model je interpretace (skládá se z univerza, relací a funkcí), ve které vše dává smysl.
Např.: U - všichni lidi
R(x) - x jsou členi univerza, třeba: jsou savci. PLATÍ!
U - přirozená čísla bez nuly a jedničky
R(x, y) - y je druhý prvek pro člen univerza, na y je aplikovaná funkce:
f(y) - $x^{2}$
PLATÍ! Pro každý člen univerza existuje nějaký prvek, který není stejný jako x a je to jeho druhá mocnina.
(další příklady sémantiky a modelů jsou v 6. prezentaci, 20. slide a dál nebo ve CV.)
[Splnitelnost v logice - základy](#c-splnitelnost-formulí-tautologie-kontradikce-model) <br />
[Splnitelnost ve výrokové logice](#f-splnitelnost-vl-v-rezolučce) <br /><br /><br />


### e) Rezolučka PL1
Formule $\models$ F je pravdivá ve všech interpretacích. <br />
Formule $P_1...P_n \models Q$ je pravdivá ve všech modelech množiny předpokladů. POUZE PRO UZAVŘENÉ FORMULE!! <br />
* Pokud máme mezi jednotliv. P konjunkce, tak Q je pravdivá ve všech modelech. \neg Q pak není pravdivá v žádném modelu.
* Znak vyplývání můžeme brát jako implikaci.
* PRO UZAVŘENÉ FORMULE PLATÍ EKVIVALENCE!!
* Pokud je negovaná formule kontradikcí (prázdna klauzule), tak původní formule je logicky pravdivá.
* Formule je nesplnitelná, když je nepravdivá v každé interpretaci nad všemi možnými univerzy. <br /><br />

Skolemova klauzulární forma je speciální konjunktivní normální forma pro PL rezolučku. - 🔵 důkaz sporem (přímý důkaz můžeme použít jen když formule neobsahují existenční kvantifikátory). <br />
**Skolemizace:** ZACHOVÁVÁ SPLNITELNOST!! Avšak skolemizovaná formule nemusí být ekvivalentní k původní formuli, ani z ní vyplývat. <br /><br />

**Klauzule:** <br />
Klauzule je konečná disjunkce literálů. <br />
Vzhledem k asociativitě a komutativitě disjunkce nezáleží na pořadí literálů v klauzuli a klauzuli můžeme také pojímat jako disjunktivní množinu literálů. <br />
Klauzulární formu můžeme také pojímat jako konjunktivní množinu klauzulí. <br /><br /><br />



## 5) Aristetolova logika
* 🔵 Fragmenty predikátové logiky.
* SUBJEKT, a úsudky z nich vytvořené.

*	Všechna S jsou P, SaP
*	Žádné S není P, SeP
*	Některá S jsou P, SiP
*	Některá S nejsou P, SoP <br />

Všechny pojmy S, P jsou zde neprázdné. <br />
Aristetolova logika - logický čtverec might be helpful. <br />
Součástí Aristetol. logiky jsou sylogismy a Vennovy diagramy. <br /><br /><br />


🔵 ## SLOVA PANOVA (potvrzeno panem M)
*Jestliže jsou premisy i závěr pravdivý, pak je usudek platný.* NEPLATÍ!! 💥 <br /><br /><br />



## OTÁZKY!! (vysvětlení k individuálním odpovědím v závorce, špatné odpovědi mohou chybět, ale nejdůležitější jsou stejně odpovědi správné) <br />
- formule nejsou přepsané do Latexu protože není moc čas
[Link / skok úplně nahoru](#předmluva) <br />

### 1) Pro formuli $p \supset (q \lor \neg q)$
💚 Je splnitelná (v pravdivostní tabulce má aspoň jeden řádek na konci jedničku, tato formule je dokonce tautologie) <br />
💚 Je ekvivalentní s formulí $(p \land q) \supset q$ (obě formule mají stejné výsledky pravdivostní tabulky – jsou tautologiemi) <br />
💚 Je ekvivalentní s formulí $q \supset (\neg p \lor p)$ (obě formule mají stejné výsledky pravdivostní tabulky – jsou tautologiemi) <br />
💚 Je logicky pravdivá, neboť konsekvent implikace je v každé valuaci výrokové proměnné q pravdivý. <br />
💥 Její negace je splnitelná formule (její negace je kontradikce, přotože původní je tautologie)

### 2) Pomocí rezoluční metody v PL1
💚 Lze syntaticky ověřovat platnost Aris. sylogismů. ((jsou to pozůstatky / fragment PL) <br />
💚 Lze ověřit platnost libovol. Aris. sylogismu. ((jsou to pozůstatky / fragment PL) <br />
💚 Lze nepřímo dokazovat platnost daného úsudku. (rezolučka umí dokazovat přímo i nepřímo) <br />
💚 Lze parciálně ověřit tautologičnost formule. <br />
💚 Lze nepřímo dokázat tautologičnost formule. <br />
💥 Ověřujeme, zda závěr vyplývá z nespočetné množiny předpokladů (toto je case diagramů nebo VL, ale určitě ne PL)

### 3) Sémantická metoda ve VL
💚 Aplikovaná na daný úsudek ověřuje, zda závěr pravdivý ve všech modelech předpokladů (ano, sémantika je přece jenom o pravdivostních hodnotách výroků) <br />
💚 Není metoda sémantických tabel (sémantické tabla, také tree proof, je grafická metoda) <br />
💚 Je tabulková metoda a metoda sémantickým sporem (rozumíme pravdivostní tabulku nebo důkaz sporem) <br />
💚 Ověřuje platnost pomocí valuací výrokových proměnných.

### 4) Mějme množiny A = {1,2,3}, B = {b} a relaci R. Která z následujících tvrzení jsou platná?
💚 Pokud relace R je definována jako podmnožina A x B: {[1,b], [2,b], [3, b]}, pak se jedná o surjektivní zobrazení <br />
💚 Pokud relace R je definována jako podmnožina B x A $\cup$ A x B a jedná se o symetrickou relaci. Pokud je v relaci R dvojice [1,b], pak se v relaci R nachází rovněž dvojice [b,1] <br />
💚 Pokud relace R je definována jako podmnožina A x B: {[1,b], [2,b], [3, b]}, pak se nejedná o injektivní zobrazení
💚 Pokud relace R je def jako podmnožina BxA sjednoceno s AxB a jedná se o symetrickou relaci, potom je v relaci R dvojice [1,b], pak se v relaci R nachází rovněž dvojice [b,1].

### 5) Které z tvrzení platí pro formuli $\forall x \forall y$ [P(x,y) $\supset$ Q(f(x),y)]
💚 V jejím modelu je binární relace P podmnožinou relace Q (binární relace má dva argumenty - zde "y", které je u obou stejné a "x", které se v Q aplikuje do funkce) <br />
(TO DÁLE ZNAMENÁ:) <br />
💚 Je splnitelná, neboť existuje její model. <br />
💚 Má jako svůj model například tuto interpretační strukturu: <br />
U = N (množina přir. čísel), <br />
P={[x,y]|x=y}, Q={[x,y]|x>=y}, <br />
f' ... druhá mocnina.

### 6) Metoda Vennových diagramů
💚 Je sémantická metoda, která ověřuje, zda závěr je platný ve všech modelech předpokladů <br />
💚 Je sémantická metoda, kterou lze ověřit platnost Aristotelových sylogismů (sémantické metody pro PL a Aristetolovu logiku obsahují Venn. Diagramy) <br />
💚 Používá se pro ověření platnosti úsudků v PL1 s maximálně třemi jednomístnými predikáty (ve cvičeních min. 2 množiny a max 3) <br />
💚 Je založena na naivní teorii množin (predikáty jsou podobné množinám)

### 7) Která z následujících tvrzení platí pro tuto situaci: množina A je podmnožinou množiny B.
💚 Rozdíl množiny A a B je prázdná množina (V množině A by nic nezbylo - dle definice podmnožiny) <br />
💚 Doplněk množiny B leží v doplňku množiny A (doplněk je odečítání druhý od prvního) <br />
💚 Všechny prvky množiny A leží v množině B i v případě, že A je prázdná množina. <br />
💚 Prvek leží v množině A pouze když leží v množině B.

### 8) Následující úsudek:
Číslo 2 je nezáporné. <br />
Číslo 2 je prvočíslo. <br />
◻️◻️◻️ <br />
Číslo 2 je dělitelné samo sebou beze zbytku. <br />
💚 Je neplatný, protože závěr z premis nevyplývá (logika je jako AI, nechápe souvislost mezi tím, že 2 je „členem prvočísel“ a tím, že prvočísla, tedy i 2, jsou dělitelné samo sebou beze zbytku) <br />
(TO ZNAMENÁ ŽE:) <br />
💚 Je neplatný, protože formalizujeme-li jej, pak závěr není platný v libovolném modelu předpokladů

### 9) Které z tvrzení platí pro formuli ∀x[P(x) ⊃ Q(a,b)]
💚 Formule [∃xP(x) ⊃ Q(a,b)] z ní vyplývá. <br />
💚 Je ekvivalentní s formulí [¬∃xP(x) ⋁ Q(a,b)] (mají stejné modely) <br />
💥 Je ekvivalentní s formulí [∀xP(x) ⊃ Q(a,b)] <br />
💥 Je ekvivalentní s formulí [¬∃xP(x) ⊃ Q(a,b)] <br />
💥 Její negací je formule ∀x[P(x) ⋀ ¬Q(a,b)] (není ani změněný kvantifikátor)

### 10) Pomocí rezoluční metody ve VL
💚 Lze ověřit, zda negovaná formule je kontradikce. <br />
💚 Lze nepřímo dokázat tautologičnost formule. <br />
💚 Lze ověřit tautologičnost formule a platnost úsudku VL. <br />
💚 Lze nepřímo dokázat platnost úsudku. <br />
💥 Lze ověřit, že tento úsudek je platný: <br />
Všechny opice jsou krásné, <br />
Judy je opice <br />
◻️◻️◻️ <br />
Judy je krásná. (platí pro PL a ne VL)

### 11)	Která z následujících tvrzení jsou pravdivá?
💚 Relace je podmnožina kartézského součinu <br />
💚 Následující relace nad celými čísly jsou totální funkce: sčítání, násobení, rozdíl (dělení je parciální) <br />
💚 Všechny podmnožiny relace A = {<1, 2>, <2, 4>, <3, 6>} jsou relacemi <br />
💚 Funkce dělení na celých číslech je parciální <br />
💚 Pokud v metodě přirozené dedukce zavedeme hypotézu H a odvodíme z ní formuli A, pak jako řádný krok důkazu musíme zavést formuli H ⊃ A <br />
💚 Princip unifikace v obecné (…), kdy je |- ∀x Px⊃P(X/term) <br />
💚 Metodou sémantických tabel využívá disjunktivních zákonu <br />
💚 Správnost úsudku ověřujeme bez empirického zkoumání stavu světa <br />
💚 Pro automatizované ověření platnosti úsudku je důležitá jeho správná formalizace <br />
💚 Hilbertův kalkul je úplný kalkul stejně jako metoda přirozené dedukce. <br />
💥 Funkce sčítání reálných čísel je pouze parciální <br />
💥 Zobrazení není relace (relace je zobrazení)

### 12)	Které z následujících systémů spojek ve VL jsou úplné:
💚 negace, disjunkce <br />
💚 negace, implikace <br />
💥 disjunkce, implikace <br />
💥 konjunkce, disjunkce <br />
💥 konjunkce, implikace <br />
💥 konjunkce, disjunkce, implikace, ekvivalence <br />
(víme, že {¬, ∧, ∨, ⇒} tvoří úplný systém logických spojek.. nyní si stačí uvědomit, že platí: (a ⇒ b) |=| (¬a ∨ b) a (a ∧ b) |=| ¬(¬a ∨ ¬b).. 3. množina ∆ = {¬, ∧} tvoří úplný systém logických spojek - jediné správné kombinace jsou: {¬,→}, {¬,∧}, {¬,∨}, SOURCE: MUNI)

### 13) Označte, které z následujících formulí jsou logicky pravdivé.
💚 [∀xP(x) ∨ ∀xQ(x)] ⊃ ∀x[P(x) ∨ Q(x)] (přesouvání kvantifikátoru jako krok 6 skolemizace - zákon distribuce kvantifikátorů!!) <br />
💚 ¬∃x[A ⊃ B(x)] ≡ ∀x[¬A ∨ B(x)] (modely) <br />
💚 ∃x[P(x) ∧ Q(x)] ⊃ [∃xP(x) ∧ ∃xQ(x)] <br /> (přesouvání kvantifikátoru jako krok 6 skolemizace - zákon distribuce kvantifikátorů!!) <br />
💚 ¬∃x[P(x) ∧ Q(x)] ⊃ [∀xP(x) ∨ ∀xQ(x)] (negace, přesouvání kvantifikátoru jako krok 6 skolemizace - zákon distribuce kvantifikátorů!!) <br />
💚 A(x/y) ⊃ ∃xA(x) (term t je substituovatelný za proměnnou x) <br />
💥 ¬∀x[P(x) ∧ Q(x)] ≡ [∃xP(x) ∧ ∃xQ(x)] <br />
💥 ¬[∀xP(x) ⊃ (Q(y) ⊃ ∀xP(x))] ≡ [∃x¬P(x) ∨ (Q(y) ∧ ∃xP(x))] <br />
💥 ∀xA(x) ≡ ∃xA(x) (není to samé) <br />
💥 ∀x∀yA(x,y) ⊃ ∀x∀y¬A(x,y) <br />
💥 ∃x∀yA(x,y) ≡ ∃y∀xA(x,y) (nemůžeme vyměnit proměnné v kvantifikátorech)

### 14) Určete, které z následujících úsudků jsou logicky platné:
💚 Venku prší. Karel je veselý. Venku prší. (pokud je závěr v předpokladu, tak vyplývá) <br />
💥 Každý filozof je líný. Petr není filozof. Petr není líny. (Petr může být líný, není nijak dáno, že jenom filozofové jsou líní) <br />
💥 Každý pes je zelený. Alík není pes. Alík není zelený. (stejné vysvětlení jako u filozofů) <br />
💥 Venku sněží. Svítí slunce. Venku nesněží. (spor)

### 15) Složené výroky ve VL jsou:
💚 Dnes sněží a mrzne. <br />
💚 Jestliže bude sněžit, tak si postavíme sněhuláka.
💥 Sněhová královna vládne v říši sněhu a ledu. (neexistuje sněhová královna, nemá smysl se nad tímto vůbec zamýšlet) <br />
💥 Mrzne až praští. (subjektivní) <br />
💥 Z čerstvě napadaného sněhu se velmi dobře budují velké hromady. (nemá ani spojku) <br />
💥 Lední hokej je velmi zajímavý sport pro všechny věkové kategorie. (subjektivní a není tam ani spojka) <br />

### 16) 🔴 Nechť PU a QU jsou obory pravdivosti predikátů P, Q. Pak:
💚 Je-li formule ∀xPx⊃Qx v dané interpretaci pravdivá, pak platí, že PU ⊆ QU <br />
💚 Formule ∀x[P(x) ⊃ Q(x)] ≡ [∃xP(x) ⊃ ∀xQ(x)] je logicky pravdivá, neboť je-li PU ⊆ QU, pak je-li PU neprázdné, tak QU = U. <br /> <br />
💚 Formule [∃xP(x) ∧ ∃xQ(x)] ⊃ ∃x[P(x) ∧ Q(x)] je logicky pravdivá, neboť je-li (PU ∩ QU) neprázdný, pak musí být jak PU, tak QU neprázdné. <br />
💚 Formule [∀xP(x) ∨ ∀xQ(x)] ≡ ∀x[P(x) ∨ Q(x)] je logicky pravdivá, neboť je-li PU = U nebo QU = U, pak je také sjednocení (PU ∪ QU) = U. <br />
💚 Formule ∃x[P(x) ∧ Q(x)] ⊃ [∃xP(x) ∧ ∃xQ(x)] je logicky pravdivá, neboť je-li (PU ∩ QU) neprázdné, pak musí být jak PU, tak QU neprázdné. <br />
💥 Formule ∃x[P(x) ∨ Q(x)] ≡ [∃xP(x) ∨ ∃xQ(x)] je logicky pravdivá, protože je-li (PU ∪ QU) neprázdné, pak musí být PU nebo QU neprázdné množiny a naopak.

### 17) Určete, které z následujících tvrzení jsou pravdivé:
💚 Relace použité pro interpretaci v PL1 musí být homogenní. <br />
💚 Libovolnou n-argumentovou funkci lze vyjádřit pomocí n+1 argumentové relace. <br />
💚 Správnost úsudku je dána pouze logickou strukturou premis a závěru. <br />
💚 PL1 pracuje pouze s totálními funkcemi, tj. takovými, kdy každý vzor má právě jeden obraz. <br />
💚 Metodou přirozené dedukce v PL 1 lze dokazovat jak přímo, tak i nepřímo. <br />
💚 Pokud je množina A vlastní podmnožinou B, pak B má alespoň jeden prvek, který neleží v A. <br />
💚 Při použití obecné rezoluční metody obecně vedeme důkaz nepřímo. <br />
💚 Sound argument je takový, jehož premisy jsou pravdivé, tedy i závěr je pravdivý. <br />
💥 Jestliže jsou premisy i závěr pravdivé, pak je úsudek platný. (neplatí, potvrzeno Menšíkem) <br />
💥 Predikátová logika druhého řádu je méně expresivní než PL1. (druhý řád je víc expresivní - logicky) <br />
💥 Každý platný úsudek, který jsem schopni adekvátně formalizovat v PL1, jsme schopni adekvátně formalizovat i ve VL tak, že zůstane platným. <br />
💥 Ze sporné množiny předpokladů nemůže vyplývat pravdivý závěr. <br />
💥 Funkce je libovolná podmnožina kartézského součinu. <br />
💥 Relace je pouze zprava jednoznačné zobrazení. <br />
💥 Funkce použité pro interpretaci v PL1 mohou být parciální, tj. takové, kdy každý vzor má minimálně jeden obraz. (parciální = nemá žádný obraz)

### 18) Nechť F je formule VL obsahující literály a, b, c, pak F:
💚 Má celkem 8 ohodnocení. (2 na počet literálů) <br />
💥 Je tautologií, pokud existuje alespoň jeden model. (musí být všechny model) <br />
💥 Je sporná, pokud aspoň jedno ohodnocení není modelem. <br />
💥 Je kontradikcí, pokud nemá alespoň jeden literál pravdivé ohodnocení. (neřešíme literály, ale modely a nesmí být žádný model)

### 19) Pomocí Vennových diagramů provádíme v PL1:
💚 Ověřování platnosti úsudků, které jsou složeny ze tří subjekt-predikátových (S-P) výroků (kde S i P jsou nějaké vlastnosti). <br />
💚 Ověřování platnosti libovolných úsudků v PL1. <br />
💚 Kontrolu správnosti kategorických sylogismů. (Aristetol. sylogismy) <br />
💚 Ověřování platnosti úsudků v PL1, pokud obsažené predikáty jsou unární. (P(x) řešíme s těmito predikáty) <br />
💥 Ověřování platnosti úsudků v logikách vyšších řádů než PL1. <br />
💥 Kontrolu správnosti úsudků, které jsou složeny z elementárních výroků VL. <br />
💥 Ověřování platnosti úsudků v PL1, pokud obsažené predikáty jsou aspoň binární.

### 20) Nechť A, B ⊨ C a A, C ⊨ D, pak:
💚 Formule A je pravdivá ve všech modelech množiny formulí {B, C}. <br />
💚 Formule D je pravdivá v každém modelu množiny formulí {A, C}. <br />
💚 A,C ⊨ C <br />
💥 Pokud jsou formule A, B nepravdivé, pak je i C nepravdivé. <br />
💥 Když není pravdivá formule D, tak není pravdivá ani A ani B.

### 21) Nechť platí: A, B, C ⊨ D, pak:
💚 D je formule pravdivá v každém modelu množiny formulí {A, B, C}. <br />
💚 A, B ⊨ D <br />
💚 A, B, C, E ⊨ D <br />
💚 Nemůže nastat případ, kdy formule A, B, C jsou v určené interpretaci pravdivé a formule D není <br />
💚 Pokud je D nepravdivá formule, pak je alespoň jedna formule z A, B, C nepravdivá <br />
💥 Formule D nemusí být pravdivá v každém modelu množiny formulí {A, B, C}, avšak musí být pravdivá v aspoň jednom. <br />
💥 Množina formulí {A, B, C, ¬D} má model. <br />
💥 A, B, C, D jsou nutně pravdivé

### 22) Která z následujících tvrzení jsou správné?
💚 Formule ∀x[P(x) ⊃ Q(x)] definuje v dané interpretaci vztah „být podmnožinou“ mezi obory pravdivosti P a Q. (pokud je členem P tak je členem Q) <br />
💚 Formule ∃x[P(x) ⊃ Q(x)] definuje v dané interpretaci vztah „být podmnožinou“ mezi obory pravdivosti P a Q. (pokud je členem P tak je členem Q) <br />
💚 Formule ∀xPx⊃¬Qx definuje v dané interpretaci vazbu „být disjunktem“ … P a Q <br />
💚 Každá formule tvaru ∃xP(x) definuje v dané interpretaci určitou podmnožinu universa. <br />
💚 Každá formule tvaru P(x) s volnou proměnnou x definuje v dané interpretaci určitou podmnožinu universa. <br />
💚 když chceme rezoluční metodu použit v PL tak je nutno formuli dát to Skolemovy klauzulární formy. <br />
💥 Formule ∀x[P(x) ⊃ ¬Q(x)] definuje v dané interpretaci vztah „být podmnožinou“ mezi obory pravdivosti P a Q.

### 23) Určete, co platí pro klausuli:
💚 Je to konečná disjunkce literálů. <br />
💚 Je to elementární disjunkce. <br />
💚 Neobsahuje konjunkci. <br />
💚 Neobsahuje implikaci. <br />
💥 Je to elementární konjunkce. <br />
💥 Obsahuje pouze konjunkci literálů. <br />
💥 Je to konečná konjunkce výrokových symbolů. <br />
💥 Obsahuje pouze výrokové proměnné.

### 24) Která z následujících tvrzení jsou platná pro vztahy mezi množinami:
💚 Množina A je identická množině B, právě když mají stejné prvky, to jest, když všechny prvky náležící množině A náleží také množině B a naopak. <br />
💚 Množina A je vlastní podmnožinou množiny B, značíme A ⊂ B, právě tehdy, když každý prvek z A je také prvkem B a ne naopak. <br />
💥 Z definice podmnožiny plyne, že ne každá množina je svou podmnožinou. <br />
💥 Množina A se rovná množině B, právě když každý prvek A je také prvkem B a ne naopak. <br />
💥 Prázdná množina není podmnožinou žádné množiny. <br />
💥 Množina A je podmnožinou množiny B, značíme A ⊆ B, právě tehdy a jen tehdy, když mají identické prvky. <br />
💥 Množina A je vlastní podmnožinou množiny B, značíme A ⊂ B, právě když každý prvek A je také prvkem B. <br />
💥 Množina A se rovná množině B, právě když každý prvek A je také prvkem B a ne naopak.

### 25) Která z následujících tvrzení platí pro rezoluční metodu ve VL?
💚 Rezoluční metoda umožňuje prokázat platnost úsudku jak sporem, tak přímou metodou. <br />
💚 Platnost úsudku nezávisí na interpretaci. <br />
💚 Pro důkaz pomocí rezoluční metody je nutné převést formuli do KNF. <br />
💥 Pro důkaz pomocí rezoluční metody je nutné převést formuli do UKNF. <br />
💥 Pro důkaz pomocí rezoluční metody je nutné převést formuli do UDNF. <br />
💥 Pro důkaz pomocí rezoluční metody je nutné převést formuli do DNF. <br />
💥 V případě nepřímého důkazu tautologičnosti formule ((a ⊃ b) ∧ (b ⊃ c) ⊃ (a ⊃ c) pomocí rezoluční metody nedojde k odvození prázdné klausule. (DOJDE!)

### 26) Určete, které z následujících tvrzení je pravdivé:
💚 Pokud je množina A vlastní podmnožina množiny B, pak B má aspoň jeden prvek, který neleží v A. <br />
💚 Operaci rozdíl libovolných dvou množin lze vyjádřit pomocí operace doplňku na těchto dvou množinách. <br />
💚 Potenční množina množiny M je množina všech podmnožin množiny M, tedy mezi její prvky patří i množina M. <br />
💥 Množiny jsou identické, právě když mají stejný počet prvků. <br />
💥 Pokud existuje nějaký prvek, který je v množině A a není v množině B, potom je B nutně podmnožinou množiny A. <br />
💥 Pokud mají dvě množiny stejnou mohutnost, pak jsou identické. <br />
💥 Průnik dvou libovolných množin je vždycky neprázdný.

### 27) Která tvrzení platí:
💚 Pokud mě zajímá podoba výsledné pravdivostní funkce dané formule, použiji tabulkovou metodu nikoli rezoluční. <br />
💚 Formule VL má 2 na "n" možných valuací, kde "n" je počet výrokových proměnných v dané formuli. <br />
💚 Pokud výrokově logický úsudek zapíšeme ve tvaru formule (P1 ∧ P2 ∧ … ∧ Pn) ⊃ Z, kde P1 až Pn jsou premisy a Z je závěr, pak je úsudek platný tehdy a jen tehdy, když je tato formule pravdivá v každé valuaci. <br />
💚 Metoda sémantických tabel je grafická metoda aplikace distributivního zákona. <br />
💚 Metoda ověřování tautologičnosti formule sémantickým sporem ověřuje, zda existuje 
 valuace, která splňuje negovanou formuli. <br />
💥 Důkaz pomocí rezoluční metody lze vést ve VL pouze přímo. <br />
💥 Rezoluční pravidlo lze na formuli F uplatňovat, pouze když je formule převedena do úplné normální konjunktivní formy. <br />
💥 Rezoluční pravidlo ve VL zachovává splnitelnost, ale nikoliv pravdivost. <br />
💥 Každá tautologie tvoří úplnou konjunktivní i disjunktivní normální formu.

### 28) Mějme množiny A, B, C. Pak množina (A ∩ (B ∪ C):
💚 Je prázdná, pokud A neobsahuje alespoň jeden prvek z B nebo z C. <br />
💚 Je prázdná vždy, když (B ∪ C) je prázdná. <br />
💚 Je prázdná vždy když A je prázdná. <br />
💚 Obsahuje maximálně |A| prvků. <br />
💥 Obsahuje minimálně |B|+|C| prvků. <br />
💥 Je prázdná, pokud alespoň jedna z množin A, B, C je prázdná. <br />
💥 Je vždy prázdná. <br />
💥 Je neprázdná, pokud každá z množin A, B, C je neprázdná.

### 29) Co následujícího platí? (je fajn si tu udělat pravdivostní tabulku)
💚 Jedním z modelů formule (p ⊃ q) ∧ (q ∨ r) je valuace p=0, q=0, r=1. <br />
💚 Každá valuace, pro kterou je q=1, je modelem formule (p ⊃ q) ∧ (q ∨ r). <br />
💥 Žádná valuace, pro kterou p=0 a q=0, není modelem formule (p ⊃ q) ∧ (q ∨ r). <br />
💥 Valuace p=1, q=0, r=1 je modelem formule (p ⊃ q) ∧ (q ∨ r). <br />
💥 Formule (p ⊃ q) ∧ (q ∨ r) má právě 2 modely. 
💥 Žádná valuace, pro kterou q=0, není modelem formule (p ⊃ q) ∧ (q ∨ r). <br />

### 30) Která z následujících formulí patří mezi zákony komutace kvantifikátorů?
💚 ∀x∀y A(x,y) ≡ ∀y∀x A(x,y)

### 30) Formule F je splnitelná v interpretaci
💚 Právě tehdy když existuje ohodnocení e proměnných takové, že platí |= F[e] v interpretaci I <br />
💚 Právě když existuje ohodnocení e proměnných takových, že F[e] je pravdivá v dané interpretační struktuře <br />
💚 Právě když existuje ohodnocení e promenných takový, že formule F je v tomto ohodnocení v dané interpretaci pravdivá

### 31) Algebraickou strukturu (R \ {0}, *) s operací násobení Nad množinou reálných čísel.
💚 Operace * je uzavřená na nosiči Struktura (Z\{0}, *) je podgrupou této struktury <br />
💚 Operace * je komutativní

### 32) Která z následujících tvrzení o formálních teoriích jsou správné:
💚 Axiomy konzistentní teorie musí být vzájemně bezesporné <br />
💚 Axiomy teorie jsou nezávislé, když žádný axiom není dokazatelný z jiných axiomu

[Link / skok úplně nahoru](#předmluva)
<br />
[Link / skok na začátek otázek](#otázky-vysvětlení-k-individuálním-odpovědím-v-závorce-špatné-odpovědi-mohou-chybět-ale-nejdůležitější-jsou-stejně-odpovědi-správné-)
