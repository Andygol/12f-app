---
title: Hlavná
description: Ako zabezpečiť maximálnu flexibilitu z hľadiska pružnosti, mobility a škálovateľnosti pri vytváraní aplikácií SaaS.
hide:
 - toc
 - navigation
---

## Úvod

V modernej dobe sa zvyčajne softvér dodáva ako služba: nazýva sa *webová aplikácia*, alebo *software-as-a-service*. Dvanásť faktorová aplikácia je metodológia na budovanie software-as-a-service aplikácií, ktoré:

* Používajú **deklaratívne** formáty na automatizáciu nastavení, a minimalizáciu času a nákladov pre nových developerov, ktorí sa začlenia do projektu;
* Obsahuje **jasnú zmluvu** s operačným systémom, nad ktorým bežia, čím umožňujú  **maximálnu portabilitu** medzi rôznymi prostrediami;
* Sú vhodné na **nasadenie** na moderné **cloudové platformy**, čím vylučujú potrebu serverov a systémových administrátorov;
* **Minimalizujú rozdiely** medzi vývojom a produkciou, čím umôžňujú **continuous deployment** s maximálnou agilnosťou;
* A sú **škálovateľné** bez významných zmien v nástrojoch, architektúre alebo vývojárskych postupoch.

Dvanásť faktorová metodológia sa dá použiť na aplikácie písané v akomkoľvek programovacom jazyku, ktoré používajú akúkoľvek kombináciu podporných služieb (databáza, fronta, pamäťová cache, atď).

## Background

The contributors to this document have been directly involved in the development and deployment of hundreds of apps, and indirectly witnessed the development, operation, and scaling of hundreds of thousands of apps via our work on the <a href="http://www.heroku.com/" target="_blank">Heroku</a> platform.

This document synthesizes all of our experience and observations on a wide variety of software-as-a-service apps in the wild.  It is a triangulation on ideal practices for app development, paying particular attention to the dynamics of the organic growth of an app over time, the dynamics of collaboration between developers working on the app's codebase, and <a href="http://blog.heroku.com/archives/2011/6/28/the_new_heroku_4_erosion_resistance_explicit_contracts/" target="_blank">avoiding the cost of software erosion</a>.

Our motivation is to raise awareness of some systemic problems we've seen in modern application development, to provide a shared vocabulary for discussing those problems, and to offer a set of broad conceptual solutions to those problems with accompanying terminology.  The format is inspired by Martin Fowler's books *<a href="https://books.google.com/books/about/Patterns_of_enterprise_application_archi.html?id=FyWZt5DdvFkC" target="_blank">Patterns of Enterprise Application Architecture</a>* and *<a href="https://books.google.com/books/about/Refactoring.html?id=1MsETFPD3I0C" target="_blank">Refactoring</a>*.

## Kto by si mal prečítať tento dokument?

Každý vývojár pracujúci na aplikácii, ktorá beží ako služba. Systémoví administrátori, ktorý také aplikácie nasadzujú.

## The Twelve Factors

### [I. Zdrojový kód](./codebase.md)

Jeden zdrojový kód vo verzionovacom systéme, veľa nasadení

### [II. Závislosti](./dependencies.md)

Explicitne deklarované a izolované závislosti

### [III. Konfigurácia](./config.md)

Konfigurácia uložená v prostredí

### [IV. Podporné služby](./backing-services.md)

Podporné služby sú pripojené zdroje

### [V. Build, release, run](./build-release-run.md)

Jasne oddelené fázy budovania, vydani a behu

### [VI. Procesy](./processes.md)

Aplikácia sa vykonáva ako jeden alebo viac bezstavových procesov

### [VII. Port binding](./port-binding.md)

Export služieb cez porty

### [VIII. Concurrency](./concurrency.md)

Škálovanie pomocou modelu procesov

### [IX. Disposability](./disposability.md)

Maximalizácia robustnosti rýchlym štartom a vhodným vypnutím

### [X. Dev/prod parity](./dev-prod-parity.md)

Vývojové, testovacie a produkčné prostredie sú čo najpodobnejšie ako sa dá

### [XI. Logy](./logs.md)

Logy sú prúdy udalostí

### [XII. Admin procesy](./admin-processes.md)

Spúštanie administrátorských/správcovských úloh ako jednorazových procesov
