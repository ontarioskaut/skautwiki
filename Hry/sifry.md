---
title: Šifry
description: 
published: true
date: 2023-08-31T19:30:21.671Z
tags: 
editor: markdown
dateCreated: 2023-04-03T06:42:39.515Z
---

# Šifry

Stejně jako je užitečné mít někde sepsané otázky, které lze znovu použít, tak je užitečné, nemuset vždy znovu vymýšlet šifry. 

> Pokud budou mít autoři dostatek času, tak se možná pokusí udělat k tomuto souboru taktéž programový dodatek na šifrování a dešifrování
{.is-info}

## Základní teorie


## Morseovka
Morseovka patří mezi mezi skauty velmi rozšířenou šifru. Samotná morseovka je ale poměrně často poněkud fádní a je velmi jednoduché čárky a tečky nahradit libovolnou jinou dvojicí symoblů. (Nejčastěji tedy trojicí se započtením oddělovacího znaku). Morseovka navíc dobře slouží jako nástavba na jinou šifru. (už zapsání řešení morseovky pozpátku může výrazně prodloužit čas luštění, jelikož nebude možné tak snadno hádat další znaky.)

|--|-----|----------------|--|-----|----------------|
|A|. _ | Akát|N| _ . | Nástup|
|B|_ . . .|Blýskavice|O| _ _ _ | Ó náš pán|
|C|_ . _ .| Cílovníci|P|. _ _ . |Papírnící|
|D|_ . . |Dálava|Q| _ _ . _ |Kvílí orkán|
|E|.|Erb|R| . _ . |Rarášek|
|F|. . _ .| Filipíny|S| . . . |Sekera, sobota, svačina|
|G|_ _ .| Grónská zem|T| _ |Trám, tón|
|H|. . . .|Hrachovina|U| . . _ |Učený|
|CH|_ _ _ _ |Chvátá k nám sám|V| . . . _ |Vyučený|
|I|. .|Ibis|W|. _ _ |Vagón klád, Wolframův drát|
|J|. _ _ _ |Junácká hůl / Jasmín bílý|X| _ . . _ |Xénokratés|
|K| _ . _ |Krákorá|Y| _ . _ _ |Ý se ztrácí|
|L| . _ . .| Lupíneček|Z|_ _ . .| Známá žena|
|M| _ _ |Mává|


Méně známá tabulka zobrazuje postupné rozložení podle množství čárek a teček. I tato může být někdy využita k šifrám.
![morse-tabulka.png](/obrazky/morse-tabulka.png)

řešení: Gondor
- základní: _ _ . / _ _ _ / _ . / _ . . / _ _ _ / . _ . //
- převrácená: . . _ / . . . / . _ / . _ _ / . . . / _ . _ //
- záměna za obrázky: :frowning_face: :frowning_face: :smiley: :neutral_face:  :frowning_face: :frowning_face: :frowning_face: :neutral_face: :frowning_face: :smiley: :neutral_face: :frowning_face: :smiley: :smiley: :neutral_face: :frowning_face: :frowning_face: :frowning_face: :neutral_face: :smiley:  :neutral_face: :smiley: 
pzn. záměna může být také například 1 a 0, častá je šipka otočená na jednu či druhou stranu
- speciální:
	 - vlny
	 - les
- rozšířené (morseovku lze schovat do čehokoli, co má dvě varianty. Zde je ukázaných pár, možností je ale celá řada. Kromě velkých a malých písmen, nebo licých a sudých čísel, se může jednat o 
	- velká malá písmena: AFd BMW Gq Tli XCV rTg
  - lichá sudá čísla: 241 682 83 479 862 741
  - morseovku lze schovat do čehokoli, co má dvě varianty. Zde je ukázaných pár, možností je ale celá řada. Kromě velkých a malých písmen, nebo licých a sudých čísel, se může jednat například o souhlásky a samohlásky. Stejný princip lze použít u obrázků. Nemusí jít o dva/tři obrázky, ale o dvě/tři kategorie obrázků.
  
## Transpoziční
Mnoho šifer je založeno jen na přeskládání písmen podle určitého klíče. A i jednoduché zapsání slova pozpátku může, v kombinaci třeba s morseovkou, vše ztížit.


řešení: Eriador
- text zapsán pozpátku: Rodaire
- každé druhé: Ewroiaapdlomr
- přední - zadní: Eidroar
- dopředu ob jedno a návrat zpět: Erroida
- čtverce
|-|-|-|
|E|E|R|
|R|W|O|
|I|A|D|
Lze pracovat s vícero směry a možnostmi projití tabulky (šnek, had, sloupce) a výchozí pozice též nemusí být vždy nahoře. 


## Definice nové abecedy
Celá škála šifer je založených na definici nové abecedy. Nejjednoduším příkladem je Caesarova šifra (posun písmen v abecedě). Už tam ale může dojít k posunu o jedno až 27 písmen. Při vyšších číslech je ale nutné někdy bokem definovat právě toto posunové číslo. Někdy jde posun definovat také písmenem. Například posun o 4 znamená že A=E. A samozřejmě existuje těžší verze posouvání každého písmene o jiný počet. To je podobné šifrování pomocí velké tabulky.



Mnohé šifry ale definují "novou" abecedu složitějším způsobem. Typickým je soupis nějakých 26 položek, ze kterých vždy první písmeno vezmeme a to pak zastupuje A, první písmeno z druhé položky zastupuje B, atd. 

Používaný je též systém otočené abecedy, kdy A=Z, Y=B

|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|A|B|C|D|E|F|G|H|I|J|K|L|M|N|O|P|Q|R|S|T|U|V|W|X|Y|Z|
|Z|Y|X|W|V|U|T|S|R|Q|P|O|N|M|L|K|J|I|H|G|F|E|D|C|B|A|


Stará vojenská šifra je pak založena na znalosti nějakého úryvku (často používána kniha, kterou měli všichni u sebe, například Bible). 

například úryvek z Euklidových základů:
"Bod jest, co nemá dílu. Čára pak délka bez šířky. Hranicemi čáry jsou body. Přímá jest čára, která svými body táhne se rovně. Plocha jest, co jen délku a šířku má. Hranicemi plochy jsou čáry."

By vytvořil abecedu kdy první písmeno úryvku odpovídá písmenu A atd. Ale pak je nutné přeskočit opakující se symboly (pokud tedy potřebujeme používat poslední písmena abecedy, je nutné použít úryvek se všemi znaky)

|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|A|B|C|D|E|F|G|H|I|J|K|L|M|N|O|P|Q|R|S|T|U|V|W|X|Y|Z|
|B|O|D|J|E|S|T|C|N|M|A|I|L|U|R|P|K|Z|Y|H|V|

Další možností je postunutí abecedy podle klíčového slova. Zbytek je doplněn podle abecedy.
S klíčovým slovem Tolkien, bychom tak dostali abecedu
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|A|B|C|D|E|F|G|H|I|J|K|L|M|N|O|P|Q|R|S|T|U|V|W|X|Y|Z|
|T|O|L|K|I|E|N|A|B|C|D|F|G|H|J|M|P|Q|R|S|U|V|W|X|Y|Z|


řešení: ROHAN
- caesarova šifra: spibo
- otočená abeceda: ilszm
- abeceda z úryvku: zrcbu
- posunutá abeceda: qjath

další kategorií je záměna písmen abecedy za zpravidla první písmeno názvu. Asi nejrozšířenější je vlajková šifra. Použít můžeme ale teoreticky i značky aut, nebo jakýchkoli libovolných předmětů.
řešení: SIRMARILION
- vlajková: :sweden: :ireland: :romania: :macedonia: :australia: :ru: :it: :latvia: :israel: :oman: :norway:
*Může nastat mírný konflikt mezi anglickými a českými názvy. Zajímavostí je, že na písmeno O začíná pouze Omán. Který ale bohužel není příliš známý.*

## Definované šifr (se šifrovacím pravítkem)

Existuje mnoho zaužívaných šifer, které si ale obvykle člověk nepamatuje z hlavy. Mezi nejznámější patří (hned po morseovce, což je výjimka u skautů) Brailovo písmo, praporková nebo praporová abeceda. Pro podobné šifry existují takzvaná šifrovací pravítka. Na soutěžích se používá například [napalm](/obrazky/sifr_prav_napalm.pdf)

Nejpoužívanější je tento sloupec. Obsahuje obrácenou abecedu, čísla v pořadí, normální abecedu, morseovu abecedu, brailovo písmo, pořadí v římských číslech, pořadí ve dvojkové, trojkové, osmičkové i šesnáctkové soustavě, praporkovou abecedu tzv. semafor a námořní vlajky pro abecedu.
![sifr_prav.png](/obrazky/sifr_prav.png)

Tato velká tabulka je používána pro sčítací šifru (též Tritheimovu). Je dáno dopředu známé heslo. Napřéklad ARNOR. A slovo které chceme zašifrovat, například GONDOR. Postupujeme tak, že si v horní liště najdeme písmeno G (7. sloupec) a sjíždíme v daném sloupci dolů, dokud nenarazíme na písmeno A (20. řádek), první písmeno v šifře pak tedy bude T. Dále postoupíme k písmenu O a najdeme pod ním písmeno R, dostaneme C. Po "vyplýtvání" hesla ho bereme odznovu. V našem případě tak celkový klíč bude ARNORA
Celková šifra bude TCZKCI
![sifr_prav2.png](/obrazky/sifr_prav2.png)

## Zbylé

řešení: Sirmarilion
- dvojice znaků > AC znamená B: RT HJ QS LN ZB QS HJ KM HJ NP MO
- čísla znamenají pořadí v abecedě: 19 9 18 13 1 18 9 12 9 15 14
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|1|2|3|4|5|6|7|8|9|10|11|12|13|14|15|16|17|18|19|20|21|22|23|24|25|26|
|A|B|C|D|E|F|G|H|I|J|K|L|M|N|O|P|Q|R|S|T|U|V|W|X|Y|Z|
*na to, jak jednoduše šifra vypadá, má celou řadu použití a může se objevit v celé řadě obmněn, nebo jako jeden z kroků*
- telefoní šífra: 7 333 666 5 1 666 333 444 333 555 55 
|---|---|---|-------|---|---|---|-----------|---|---|---|
|číselník|||        |přizpůsobená verze||||nokia|||
|1|2|3|             |ABC|DEF|GHI|        ||ABC|DEF|
|4|5|6|             |JKL|MNO|PQR|        |GHI|JKL|MNO|
|7|8|9|             |STU|VWX|YZ|         |PQRS|TUV|WXYZ|
- za písmenem: DAHJQSJHSQIDFAKNQRDBYCQMDGJQAJIFYQIDFPOQRNUABQIDBAQLDCBIQICDDACBKQOCQN
*písmeno šifry je vždy za nějakým písmenem, typicky něco méně obvyklého, jako Q nebo X*






  