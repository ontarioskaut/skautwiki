---
title: Poznámky ke skautským Wordpress šablonám
description: 
published: true
date: 2024-01-07T01:11:01.634Z
tags: 
editor: markdown
dateCreated: 2024-01-06T22:55:23.153Z
---

# Poznámky ke skautským wordpress šablonám
- de facto jde o overwritování a přidání několika pravidel v CSS stylech již existujících šablon.
- pro nasazení mimo [Lebeda hosting](https://lebedahosting.cz/): https://github.com/skaut/dsw-sablony (třeba nainstlovat čistý wordpress + šablony popsané v README)
  - ~~nejsou ovšem dostupné defaultní texty~~ Defaultní texty lze importovat z [XML souborů](https://github.com/skaut/dsw-sablony/commit/2f4e5a422c3e50324886b0a3b6c9c690998885ab) v adresáři [exporty-obsahu](https://github.com/skaut/dsw-sablony/tree/master/exporty-obsahu)
  - v administraci v sekci Nástroje > Import doinstaluj importovací metodu Wordpress. Klikni na Spustit import a vyber .xml soubor stažený z git repozitáře. Spusť import a modli se
  ![wp_skaut_import_1.png](/obrazky/wordpress/wp_skaut_import_1.png)
  ![wp_skaut_import.png](/obrazky/wordpress/wp_skaut_import.png)
- v Lebeda hostingu by měla být naklikatelná automatická instlace wordpressu včetně potřebných šablon, stylů a defaultního obsahu
  - nikdy jsem to nepoužíval - TODO: kdo ví, může napsat
## Poznámky
- když se odstraní defaultní obarvení, defaultní obrázek v šabloně pro střediska není ve vrchní části dostatečně kontrastní vůči textu hlavního menu (ano, defaultní obarvení do zelené barvy působí divně)
- otázka vkusu: mezi sekcemi (resp. z technického hlediska divy :upside_down_face:) jiného barevného stylu se díky marginům tvoří nevzhledně a rušivě vypadající bílé mezery:
  ![wp_skaut_whitespaces.png](/obrazky/wordpress/wp_skaut_whitespaces.png)
  - na ošetření zkusím vymyslet CSS overwrite, který by ale nenarušil zbytek stránek
  - takto si myslím, že by to mohlo být lepší:
  ![wp_skaut_whitespaces_corrected.png](/obrazky/wordpress/wp_skaut_whitespaces_corrected.png)
- na poslední sekci se sponzory je použit šablonový widget. Šablona je však designovaná na 2 obsazené widgety, takže pokud zobrazujeme pouze první widget, bude vždy smrsknutý na půlku obrazovky. Na velkých počítači to tedy bude působit divně. 
  - takto by se to dalo ošetřit (Šablona > Přizpůsobit > CSS):
```css
.footer-widgets {
		width: 100%;
}
.sponzori {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex-wrap: wrap;
    gap: 2rem;
}

.footer-widgets-outer-wrapper {
    padding: 0;
}
```
  - obsah widgetu: 
```html
Nějaký text nad tím
<div class="sponzori">
  <a href="https://www.zlin.eu">
    <img src="https://wp-test.pernicka.cz/wp-content/uploads/2023/10/zlin-logo.png" alt="" width="300" /></a>
  <a href="https://lesycr.cz">
    <img src="https://wp-test.pernicka.cz/wp-content/uploads/2023/10/lcr-logo.png" alt="" width="150" /></a>
  <a href="https://ipsos.cz">
    <img src="https://wp-test.pernicka.cz/wp-content/uploads/2023/10/ipsos-logo.png" alt="" width="110" /></a>
  <a href="https://google.cz">
    <img src="https://wp-test.pernicka.cz/wp-content/uploads/2023/10/google-logo.png" alt="" width="250" /></a>
  <a href="https://ceskatelevize.cz">
    <img src="https://wp-test.pernicka.cz/wp-content/uploads/2023/10/ct-logo.png" alt="" width="160" /></a>
  <a href="https://msmt.cz">
    <img src="https://wp-test.pernicka.cz/wp-content/uploads/2023/10/msmt-logo.png" alt="" width="150" /></a>
</div>
```
  - takový je výsledek: https://wp-test.pernicka.cz/
- tabulky s popiskem dělají nepořádek s overflow - scrollovací lišta se zobrazí vždy, pokud je přítomen popisek (figcaption). Zároveň tabulky nejsou připravené na zobrazení na mobilech.
  ![wp_skaut_tables_wrong.png](/obrazky/wordpress/wp_skaut_tables_wrong.png)
  - řešení by mohlo vypadat takto:
  ![wp_skaut_tables_1.png](/obrazky/wordpress/wp_skaut_tables_1.png)
  a na mobilech takto: 
  ![wp_skaut_tables.png](/obrazky/wordpress/wp_skaut_tables.png)
  - řešení: 
```css
.wp-block-table figcaption{
    display: inline;
}

.wp-block-table table {
    white-space: nowrap;
}
```