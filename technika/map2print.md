---
title: Tisknutí vlastní mapy
description: 
published: true
date: 2023-08-27T18:39:41.426Z
tags: 
editor: markdown
dateCreated: 2022-08-16T22:34:35.149Z
---

# Tisknutí vlastní mapy
> Tady přidat životní storku
{.is-info}

Na to píšu jednoduchý skript v Pythonu:
[map2print – Github repozitář](https://github.com/pavelpernicka/map2print)
- můžeš si to upravit jak chceš 
- časem by to chtělo dodělat webový frontend, aby to zvládl kdokoliv
## Jak to funguje
- vezme si to souřadnicové ohraničení pomyslného boxu v mapě (maximální a minimální zeměpisná šířka a délka vybrané oblasti)
![nacrt_map_box.png](/obrazky/nacrt_map_box.png)
- vypočítá si to čísla mapových dlaždic v pravém horním rohu a levém dolním rohu podle pozic a přiblížení (měřítka mapy)
**Výpočet:**
  - TODO
- Vytvoří se seznam dlaždic mezi těmito čisly
- Vytvoří se prázdný obrázek s velikostí podle počtu dlaždic (1 dlaždice = 256 px)
- Postupně se stahují obrázky a doplňují do obrázku
- vznikne dost velký obrázek
- ten rozřežeme na menší obrázky ve velikosti tisknutelné na A4 papír
- Vytvoří se PDF s těmito obrázky na stránkách
## co se musí dodělat
- webserver
- ochrana před přetížením z požadavků na webserver
- cahcování dlaždic, protože nechceme přetěžovat tileservery [openstreetmap](https://openstreetmap.org) nebo jinší
- **Teď se nevytvoří obrázky pro přesně vybranou oblast, vše je totiž zaokrouhlené na kachličky**, takže se musí přidat ořezávání krajových kachliček (vypočítá se, na kterém bodě v ose X nebo Y se kachlička šmikne)
![nacrt_map_box-tiles.png](/obrazky/nacrt_map_box-tiles.png)
## Co má normální smrtelník udělat, aby dostal mapu
- jít na http://bboxfinder.com/
- vytvořit obdélník v místě, co tě zajímá
- zkopírovat hodnoty `box` (viz obrázek)
![bbox.png](/obrazky/bbox.png)
- poslat je Hruškovi
## Využití
- už se to jednou hodilo, když medvědice plánovaly dvoudenku. Ovšem nakonec zřejmě změnily trasu atak naše mapa byla nejspíše nevyužita