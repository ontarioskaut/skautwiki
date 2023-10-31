---
title: Scout QR game
description: 
published: true
date: 2023-10-31T18:08:41.983Z
tags: 
editor: markdown
dateCreated: 2023-10-31T18:08:41.983Z
---

# Scout QR game
Nějaký ten rok dozadu vznikla během noci den před schůzkou webová aplikace, která má funkci skenování QR kódů a zobrazení předdefinované otázky, po jejímž vyplnění se členům ukáže další místo na mapě. Tenkrát to bylo použito na hru ve dvou skupinkách po Centrálním parku na Jižních Svazích. Pokud by se někomu něco takového hodilo, přikládám zdrojové kódy a jak to vlastně fungovalo. 

Pokud se na to díváš a říkáš si, že na to nemáš dostatečné informatické znalosti, klidně kontaktuj [Hrušku](/owiki/tym#hru%C5%A1ka-pavel-perni%C4%8Dka), který se zprovozněním rád pomůže.

## Jak to funguje
- členi se rozdělí do rozumně velkých skupinek
- ve skupince stačí jeden telefon
- v telefonu si člověk načte webovou stránku, kde hra běží (ideálně self-hostovaná). Tuto stránku stačí načíst jen jednou - vše je zabudované v jedné stránce, takže o data nemusíte mít strach.
- tak je na hlavní stránce tlačítko Skenovat
- scannerem si každá družinka naskenuje svůj aktivační kód a dozví se místo svého prvního stanoviště
- na každém dalším stanoviti je nějaký úkol nebo otázka, na kterou se dá odpoědět textovou odpovědí. Pokud je odpověď správná, tk se dozví místo dalšího stanoviště.


