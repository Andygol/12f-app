---
title: Hlavní
description: Metodika pro vytváření aplikací SaaS, která poskytuje maximální flexibilitu vývoje, přenositelnost a škálovatelnost.
hide:
 - toc
 - navigation
---

## Úvod

V moderní době je software často dodáván jako služba, což označujeme pojmem *webová aplikace* nebo *software-as-a-service (SaaS)*. Twelve-factor metodika slouží pro vytváření (SaaS) aplikací, které:

* Používají **deklarativní** formáty pro nastavení automatizace, což vede k minimalizaci času a nákladů potřebných pro začlenění nových vývojářů do projektu;
* Mají **jasný kontrakt** s operačním systémem ve kterém běží, čímž je umožněna **maximální přenositelnost** mezi různými běhovými prostředími;
* Jsou vhodné pro **nasazení** na moderních **cloudových platformách**, což eliminuje potřebu správy serverů a podpůrných systémů;
* **Minimalizují rozdíly** mezi vývojovým a produkčním prostředím, čímž umožňují **průběžné nasazovaní** a maximální flexibilitu;
* Umožňují **vyškálování** bez výrazných změn v nástrojích, architektuře nebo vývojových postupech.

Twelve-factor metodiku lze použít na aplikace napsané v jakémkoliv programovacím jazyce a používající libovolnou kombinaci podpůrných služeb (databáze, fronty, vyrovnávací paměť atd.).

## Pozadí

Přispěvatelé tohoto dokumentu se přímo podíleli na vývoji a nasazení stovek aplikací a byli svědky vývoje, provozu a škálování stovek tisíc aplikací prostřednictvím své práce na platformě <a href="http://www.heroku.com/" target="_blank">Heroku</a>.

Tento dokument shromažďuje všechny naše zkušenosti a postřehy týkající se široké škály aplikací typu software-as-a-service v divočině. Jedná se o sadu ideálních postupů pro vývoj aplikací se zvláštní pozorností věnovanou dynamice organického růstu aplikace v průběhu času, dynamice spolupráce mezi vývojáři pracujícími na kódu aplikace a <a href="http://blog.heroku.com/archives/2011/6/28/the_new_heroku_4_erosion_resistance_explicit_contracts/" target="_blank">vyhýbání se nákladům na erozi softwaru</a>.

Naší motivací je zvyšovat povědomí o některých systémových problémech, které jsme zaznamenali v moderním vývoji aplikací, poskytnout společnou slovní zásobu pro diskusi o těchto problémech a nabídnout rozsáhlou sadu koncepčních řešení těchto problémů s doprovodnou terminologií. Formát je inspirován knihami Martina Fowlera *<a href="https://books.google.com/books/about/Patterns_of_enterprise_application_archi.html?id=FyWZt5DdvFkC" target="_blank">Patterns of Enterprise Application Architecture</a>* a *<a href="https://books.google.com/books/about/Refactoring.html?id=1MsETFPD3I0C" target="_blank">Refactoring</a>*.

## Kdo by měl číst tento dokument?

Každý vývojář pracující na aplikaci, která běží jako služba. Systémoví inženýři, kteří takové aplikace nasazují nebo spravují.

## The Twelve Factors

### [I. Zdrojový kód](./codebase.md)

Mějte jeden zdrojový kód ve verzovacím systému a mnoho nasazení.

### [II. Závislosti](./dependencies.md)

Explicitně deklarujte a izololujte závislosti.

### [III. Konfigurace](./config.md)

Konfigurace ukládejte do prostředí.

### [IV. Podpůrné služby](./backing-services.md)

Nakládejte s podpůrnými službami jako s připojenými zdroji.

### [V. Sestavení, vydání, spuštění](./build-release-run.md)

Striktně oddělte fáze sestavení, vydání a spuštění.

### [VI. Procesy](./processes.md)

Spouštějte aplikaci jako jeden nebo více bezestavových procesů.

### [VII. Vazba s portem](./port-binding.md)

Exportujte služby pomocí vazby na port.

### [VIII. Souběh](./concurrency.md)

Škálujte do šířky použitím proces modelu.

### [IX. Zahoditelnost](./disposability.md)

Maximalizujte robustnost pomocí rychlého spouštění a korektního vypnutí.

### [X. Podobnost Vývoj/Produkce](./dev-prod-parity.md)

Udržujte si co nejmenší rozdíly mezi vývojovým, testovacím a produkčním prostředím.

### [XI. Logy](./logs.md)

S logy zacházejte jako s proudy událostí.

### [XII. Admin procesy](./admin-processes.md)

Spouštějte administrativní úlohy jako jednorázové procesy.
