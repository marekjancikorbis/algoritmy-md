Algoritmizace – maturitní otázka


1. Algoritmus a jeho vlastnosti

Algoritmus je přesný návod, jak krok za krokem vyřešit nějakou úlohu. Má konečný počet kroků a vede od vstupních údajů k výsledku. Návod musí být tak jasný, aby ho zvládl provést člověk i počítač.

Algoritmizace je hledání a sepsání takového návodu pro konkrétní problém.

Slovo algoritmus pochází ze jména perského matematika Al-Chvárizmího (9. století), jehož jméno se latinsky psalo „Algoritmi“. Známý starý příklad je Eukleidův algoritmus na výpočet největšího společného dělitele.

Vlastnosti algoritmu:

Konečnost – algoritmus jednou skončí, neběží donekonečna. Porušení: nekonečný cyklus.

Jednoznačnost (determinovanost) – každý krok je přesně daný a ve stejné situaci se vždy pokračuje stejně. Porušení: pokyn „přidej trochu soli“.

Obecnost (hromadnost) – řeší celý typ úloh, ne jen jeden konkrétní případ. Porušení: postup, který umí sečíst jen 3 + 5.

Má výsledek (rezultativnost) – vždy dojde k nějakému výstupu. Porušení: postup, který nic nevrátí ani nevypíše.

Srozumitelné kroky (elementárnost) – každý krok je tak jednoduchý, že ho ten, kdo algoritmus provádí, umí udělat. Porušení: pokyn „vyřeš rovnici“ pro někoho, kdo to neumí.

Opakovatelnost – pro stejné vstupy dá vždy stejný výsledek.

Efektivita – dojde k výsledku v rozumném čase a nespotřebuje zbytečně moc paměti.

K maturitě stačí hlavně prvních pět: konečnost, jednoznačnost, obecnost, výsledek a srozumitelné kroky.

Příklad – největší společný dělitel (Eukleides):

1. Načti dvě kladná celá čísla a, b.
2. Dokud b není 0: spočítej zbytek po dělení a / b, pak do a dej b a do b dej zbytek.
3. Vypiš a – to je největší společný dělitel.

Algoritmus skončí, protože zbytek je pořád menší. Je jednoznačný, funguje pro jakákoli čísla a má výsledek.

Doplněk – jak je algoritmus rychlý (složitost):
Časová složitost říká, jak rychle roste počet kroků, když roste velikost vstupu. Paměťová složitost říká, kolik paměti algoritmus potřebuje. Například hledání prvku procházením celého seznamu trvá úměrně jeho délce, kdežto půlení seřazeného seznamu (binární vyhledávání) je mnohem rychlejší.


2. Fáze vzniku programu

Program nevzniká jen psaním kódu – to je jen jedna část. Celému postupu od nápadu po údržbu se říká životní cyklus programu.

1. Zadání – co má program dělat, pro koho a jaké má splnit požadavky.
2. Rozbor úlohy (analýza) – jaké jsou vstupy, výstupy, omezení a zvláštní případy. Velký problém se rozdělí na menší části.
3. Návrh algoritmu – vymyslí se postup a způsob uložení dat, postup se zapíše (slovně, pseudokódem nebo diagramem).
4. Psaní kódu (implementace) – algoritmus se přepíše do programovacího jazyka. Vznikne zdrojový kód.
5. Překlad – zdrojový kód se převede do podoby, které rozumí počítač:
   kompilátor přeloží celý program předem (C, C++, Pascal),
   interpret překládá a rovnou provádí program za běhu, řádek po řádku (Python, JavaScript),
   kombinace: program se přeloží do mezikódu, který pak spouští virtuální stroj (Java, C#).
6. Ladění – hledání a opravování chyb.
7. Testování – ověření, že program funguje správně pro různé vstupy.
8. Dokumentace – návod pro uživatele a popis kódu pro programátory (komentáře).
9. Nasazení – předání programu uživatelům, instalace.
10. Údržba – opravy chyb nalezených při používání, vylepšení a nové verze.

Fáze se v praxi opakují. Chyba nalezená při testování vrací práci zpět k ladění, někdy až k návrhu. Když jdou fáze přísně jedna za druhou, říká se tomu vodopádový model. Dnes se častěji pracuje v krátkých opakovaných kolech, kdy se program postupně vylepšuje (agilní vývoj).


3. Způsoby zápisu algoritmu a programu

Algoritmus jde zapsat několika způsoby, od obyčejného textu až po kód, kterému rozumí počítač.

Slovně – postup popsaný běžnými větami, jako recept. Výhoda: pochopí to každý. Nevýhoda: nepřesné, dá se to pochopit různě, bývá to dlouhé.

Pseudokód – text podobný programovacímu jazyku, ale bez přísných pravidel zápisu. Výhoda: přesný, blízký kódu, nezávislý na konkrétním jazyce. Nevýhoda: počítač ho nespustí.

Vývojový diagram – kreslený zápis pomocí domluvených značek spojených šipkami. Výhoda: přehledný a názorný. Nevýhoda: u velkých programů se v něm člověk ztratí a špatně se upravuje.

Strukturogram – do sebe vnořené obdélníky bez šipek. Výhoda: nutí psát přehledně a uspořádaně. Nevýhoda: špatně se kreslí a mění.

Programovací jazyk – skutečný kód (Python, C#, Java…). Výhoda: dá se rovnou spustit. Nevýhoda: musíš znát jazyk a jeho pravidla.

Matematický zápis – vzorce. Výhoda: krátký a přesný. Nevýhoda: hodí se jen pro matematické úlohy.

Značky vývojového diagramu:

ovál – začátek a konec
obdélník – příkaz nebo výpočet
rovnoběžník (kosý obdélník) – načtení nebo vypsání dat
kosočtverec – podmínka, rozhodnutí ano / ne
šestiúhelník – cyklus s pevným počtem opakování
obdélník se zdvojenými bočními stranami – volání podprogramu (funkce)
kroužek – spojka mezi částmi diagramu
šipka – kudy se pokračuje

Tři základní stavební kameny:
Každý algoritmus jde poskládat jen ze tří věcí:

Posloupnost – příkazy jdou jeden po druhém.
Větvení – podle podmínky se jde jednou nebo druhou cestou (if / else).
Cyklus – opakování: s podmínkou na začátku (while), s podmínkou na konci (do…while) nebo s pevným počtem opakování (for).

Příklad – stejný algoritmus třemi způsoby:

Slovně: Načti dvě čísla. Když je první větší, vypiš první, jinak vypiš druhé.

Pseudokód:

    načti a, b
    jestliže a > b pak
        vypiš a
    jinak
        vypiš b
    konec jestliže

Python:

    a = int(input())
    b = int(input())
    if a > b:
        print(a)
    else:
        print(b)

Vývojový diagram slovy: Začátek (ovál) → načti a, b (rovnoběžník) → podmínka a > b ? (kosočtverec). Při „ano“ jde šipka na vypiš a, při „ne“ na vypiš b (obojí rovnoběžník). Obě cesty se pak spojí a vedou na Konec (ovál).


4. Syntaxe a sémantika

Syntaxe říká, jak se program správně píše. Sémantika říká, co napsaný program znamená a co udělá.

Syntaxe jsou pravidla zápisu jazyka – jako gramatika: klíčová slova, čárky, závorky, odsazení, pořadí. Kontroluje ji překladač ještě před spuštěním.

Sémantika je význam – co se skutečně stane, když se příkaz provede.

Přirovnání k češtině: věta „Zelené myšlenky zuřivě spí.“ je gramaticky správně, ale nedává smysl. Je tedy správná syntakticky, ale ne významově.

Druhy chyb:

Syntaktická chyba – chyba v zápisu. Program se vůbec nespustí. Příklad: chybějící závorka print("Ahoj" nebo chybějící dvojtečka za if. Najde ji překladač.

Chyba za běhu – program se spustí, ale během práce spadne. Příklad: dělení nulou, sáhnutí mimo seznam, neexistující soubor. Ohlásí ji systém při běhu.

Logická (významová) chyba – program běží, ale dává špatný výsledek. Příklad: průměr spočítaný jako a + b / 2 místo (a + b) / 2. Najde ji jen programátor laděním a testováním.

Logické chyby jsou nejzrádnější, protože je překladač neodhalí. Proto je potřeba program ladit a testovat.

Souvisí s tím ještě pragmatika – jak se jazyk používá v praxi, tedy styl, zvyklosti a čitelnost kódu.


5. Ladění a testování

Testování chyby hledá – zjistí, že program nefunguje. Ladění zjistí, proč nefunguje, a chybu opraví. Testování umí ukázat, že chyby v programu jsou, ale nikdy nedokáže, že tam žádné nejsou.

Ladění (debugging)

Ladění je hledání příčiny chyby v kódu a její oprava. Anglické slovo bug (brouk) se tradičně spojuje s můrou, kterou v roce 1947 našli v počítači Harvard Mark II.

Nástroje a postupy:

Debugger – nástroj ve vývojovém prostředí, který umí spouštět program pomalu a pod kontrolou.
Bod přerušení (breakpoint) – místo, kde se program zastaví.
Krokování – program se provádí po jednom příkazu:
   step over – zavolanou funkci provede celou najednou, nejde do ní,
   step into – vleze dovnitř funkce,
   step out – dokončí funkci a vrátí se ven.
Sledování proměnných – průběžně ukazuje, jaké hodnoty proměnné mají.
Seznam rozpracovaných funkcí (call stack) – ukazuje, které funkce se právě provádějí.
Kontrolní výpisy – vypsání hodnot pomocí print() na důležitých místech, případně zapisování do souboru (logování).
Procházení na papíře – ruční tabulka hodnot proměnných krok po kroku.
Vysvětlování nahlas (gumová kachnička) – když kód někomu (nebo něčemu) vysvětluješ, často si chybu sám všimneš.

Testování

Testování je ověřování, že program dělá to, co má podle zadání.

Podle toho, jestli tester vidí do kódu:
Černá skříňka (black box) – tester kód nezná, zkouší jen vstupy a kontroluje výstupy podle zadání.
Bílá skříňka (white box) – tester kód zná a zkouší všechny jeho cesty: větve, cykly, podmínky.
Šedá skříňka (grey box) – něco mezi, tester zná kód jen částečně.

Podle toho, jak velkou část programu test zkouší:
1. Jednotkové testy – zkouší jednotlivé funkce zvlášť, často automaticky.
2. Integrační testy – zkouší, jestli spolu jednotlivé části dobře spolupracují.
3. Systémové testy – zkouší celý program jako celek.
4. Přejímací testy – zákazník ověřuje, že program dělá, co chtěl. Alfa test probíhá u vývojáře, beta test u vybraných uživatelů.

Další pojmy:
Opakované testování (regresní) – po každé úpravě znovu pustit staré testy, aby oprava nerozbila něco jiného.
Testování bez spuštění (statické) – čtení a kontrola kódu, třeba když ho projde kolega. Testování za běhu se říká dynamické.
Zátěžové testy – jak se program chová při velkém množství dat nebo uživatelů.
Testovací případ – konkrétní vstup a výsledek, který očekáváme.
TDD – nejdřív se napíše test, až potom kód.

Jak vybrat testovací data:
běžné hodnoty – obvyklý vstup,
krajní hodnoty – 0, 1, největší možné číslo, prázdný seznam, první a poslední prvek,
neplatné vstupy – záporné číslo, text místo čísla, prázdný vstup,
zvláštní případy – stejná čísla, záporná čísla, hodně velká čísla.

Příklad pro program „větší ze dvou čísel“: (5, 3), (3, 5), (4, 4), (−2, −7), (0, 0), („abc“, 3).


6. Rekurze

Rekurze znamená, že funkce zavolá sama sebe, aby vyřešila menší verzi stejného problému. Musí mít podmínku, kdy přestane, jinak by se volala donekonečna.

Každá rekurzivní funkce má dvě části:
1. Základní případ (ukončovací podmínka) – tak jednoduchý případ, že se vyřeší rovnou, bez dalšího volání.
2. Rekurzivní krok – problém se zmenší a funkce zavolá sama sebe s menším vstupem.

Druhy rekurze:
Přímá – funkce A volá sama sebe.
Nepřímá – funkce A volá funkci B a ta zase volá A.
Koncová – volání sebe sama je úplně poslední věc, kterou funkce udělá. Překladač ji pak umí převést na obyčejný cyklus.

Příklad 1 – faktoriál

Matematicky: 0! = 1 a n! = n × (n − 1)! pro n větší než 0.

    def faktorial(n):
        if n == 0:                    # kdy přestat
            return 1
        return n * faktorial(n - 1)   # funkce volá sama sebe

Jak to proběhne pro faktorial(3):
faktorial(3) potřebuje 3 × faktorial(2), takže ho zavolá.
faktorial(2) potřebuje 2 × faktorial(1), takže ho zavolá.
faktorial(1) potřebuje 1 × faktorial(0), takže ho zavolá.
faktorial(0) vrátí rovnou 1 – tady se zanořování zastaví.
Pak se výsledky vracejí zpátky nahoru: 1 → 1 × 1 = 1 → 2 × 1 = 2 → 3 × 2 = 6.

Příklad 2 – Fibonacciho posloupnost

F(0) = 0, F(1) = 1, F(n) = F(n − 1) + F(n − 2).

    def fib(n):
        if n < 2:
            return n
        return fib(n - 1) + fib(n - 2)

Tahle verze je hodně pomalá, protože stejné hodnoty počítá pořád dokola. Pomůže cyklus nebo zapamatování už spočítaných výsledků.

Další typické příklady:
Hanojské věže – přesunout n disků znamená přesunout n − 1 disků na pomocnou tyč, přesunout největší disk a pak přesunout n − 1 disků na cílovou tyč. Potřeba je 2 na n minus 1 tahů.
Procházení složek v počítači (složka obsahuje další složky) nebo stromových struktur.
Řadicí algoritmy QuickSort a MergeSort – úlohu rozdělí na menší, vyřeší je a spojí („rozděl a panuj“).
Binární vyhledávání, výpočet největšího společného dělitele, mocnina.
Fraktály v grafice – Kochova vločka, Sierpińského trojúhelník.

Zásobník a přetečení

Každé volání funkce si počítač odloží do takzvaného zásobníku (stack) – s parametry, proměnnými a místem, kam se má vrátit. Když je rekurze moc hluboká nebo chybí podmínka konce, zásobník se zaplní a program spadne. Tomu se říká přetečení zásobníku (stack overflow). Python dovolí zhruba 1000 zanoření.

Rekurze vs. cyklus

Rekurze: krátký a elegantní zápis, podobný matematické definici. Každé volání ale zabírá paměť, je pomalejší a hrozí přetečení zásobníku. Hodí se na stromy, úlohy typu „rozděl a panuj“ a věci, které jsou rekurzivně definované.

Cyklus: zápis bývá delší, ale paměti potřebuje stále stejně a je rychlejší. Hrozí nekonečný cyklus. Hodí se na jednoduché opakování.

Každá rekurze se dá přepsat na cyklus a naopak.


7. Shrnutí a možné doplňující otázky

Osnova odpovědi na 10–15 minut:
1. Co je algoritmus, odkud pochází slovo, příklad (Eukleides).
2. Vlastnosti – vyjmenovat a ke každé říct jednu větu.
3. Fáze vzniku programu – od zadání po údržbu; rozdíl kompilátor vs. interpret.
4. Způsoby zápisu – slovně, pseudokód, vývojový diagram (nakreslit značky), strukturogram, kód; tři stavební kameny.
5. Syntaxe vs. sémantika a tři druhy chyb s příkladem.
6. Ladění (debugger, bod přerušení, krokování) a testování (černá/bílá skříňka, druhy testů, testovací data).
7. Rekurze – co to je, podmínka konce, faktoriál na tabuli, rekurze vs. cyklus.

Otázky, které může zkoušející položit:
Co se stane, když rekurzivní funkce nemá podmínku konce?
Jaký je rozdíl mezi kompilátorem a interpretem? Uveďte jazyky.
Proč překladač neodhalí logickou chybu?
Jaký je rozdíl mezi testováním a laděním?
Nakreslete vývojový diagram cyklu, který sečte čísla 1 až n.
Přepište rekurzivní faktoriál na cyklus.
Kterou vlastnost algoritmu porušuje nekonečný cyklus? (konečnost)
Jaká testovací data zvolíte pro program, který zjistí, jestli je číslo prvočíslo?

Faktoriál cyklem (pro porovnání s rekurzí):

    def faktorial(n):
        vysledek = 1
        for i in range(2, n + 1):
            vysledek *= i
        return vysledek
