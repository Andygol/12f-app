---
title: Główna
description: W jaki sposób zapewnić najwyższą elastyczność pod względem elastyczności, mobilności i skalowalności w procesie tworzenia aplikacji SaaS.
hide:
 - toc
 - navigation
---

## Wprowadzenie

We współczesnym świecie oprogramowanie jest powszechnie wytwarzane w formie usługi, nazywane  _software-as-service (SaaS)_ lub aplikacjami internetowymi. Dwanaście aspektów aplikacji jest metodologią budowania aplikacji SaaS, które:

* Używają **deklaratywnego** formatu by zautomatyzować konfigurację aplikacji w celu zmniejszenia czasu i kosztów dołączenia nowych programistów do projektu;
* Mają **czysty kontrakt** z systemem operacyjnym, umożliwiając **jak największą możliwość przenoszenia** pomiędzy środowiskami, w których działają;
* Są dopasowane do **wdrożenia** na nowoczesne **chmury obliczeniowe**, zapobiegając potrzebie użycia serwerów i administracji systemu;
* **Minimalizują rozbieżności** pomiędzy środowiskami developerskimi i produkcyjnymi, umożliwiając **nieustanne wdrażanie aplikacji** by zmaksymalizować prędkość zmian;
* I mogą **skalować się** bez większej zmiany narzędzi, architektury, czy sposobu pracy zespołu.

Metodologia dwunastu aspektów może być stosowana do aplikacji napisanych w każdym języku programowania i wykorzystujących dowolną kombinację usług wspierających (bazy danych, kolejki, cache pamięci etc).

## Background

Kontrybutorzy tego dokumentu byli bezpośrednio zaangażowani w tworzenie i wdrażanie setek aplikacji i pośrednio byli świadkami produkcji, działania i skalowania setek tysięcy aplikacji dzięki naszej pracy na platformie [Heroku](http://www.heroku.com/).

Ten dokument jest podsumowaniem całego naszego doświadczenia i obserwacji szerokiej gamy aplikacji SaaS. Jest on połączeniem idealnych praktyk developmentu, zwracania szczególnej uwagi na naturalny rozrost aplikacji w czasie, dynamiki współpracy developerów pracujących nad jednym codebase'm, oraz [unikania kosztów gnijącego oprogramowania](http://blog.heroku.com/archives/2011/6/28/the_new_heroku_4_erosion_resistance_explicit_contracts/).

Naszym celem jest podniesienie poziomu świadomości o podstawowych problemach, które dostrzegliśmy przy tworzeniu nowoczesnych aplikacji, zapewnienie wspólnego słownictwa do rozmowy o tych problemach oraz zaoferowanie ogólnych rozwiązań dla tych problemów wraz z towarzyszącą terminologią. Format dokumentu jest inspirowany książkami Martina Fowlera
 *[Patterns of Enterprise Application Architecture](http://books.google.com/books/about/Patterns_of_enterprise_application_archi.html?id=FyWZt5DdvFkC)* oraz *[Refactoring](http://books.google.com/books/about/Refactoring.html?id=1MsETFPD3I0C)*.

## Dla kogo przeznaczony jest ten dokument?

Dla każdego developera tworzącego aplikacje, które działają jako usługa. Dla każdego Dev-opsa, który wdraża i zarządza takimi aplikacjami.

## The Twelve Factors

### [I. Codebase](./codebase.md)

Jedno źródło kodu śledzone systemem kontroli wersji, wiele wdrożeń

### [II. Zależności](./dependencies.md)

Jawnie zadeklaruj i wydziel zależności

### [III. Konfiguracja](./config.md)

Przechowuj konfigurację w środowisku

### [IV. Usługi wspierające](./backing-services.md)

Traktuj usługi wspierające jako przydzielone zasoby

### [V. Buduj, publikuj, uruchamiaj](./build-release-run.md)

Oddzielaj etap budowania od uruchamiania

### [VI. Procesy](./processes.md)

Uruchamiaj aplikację jako jeden lub więcej bezstanowych procesów

### [VII. Przydzielanie portów](./port-binding.md)

Udostępniaj usługi przez przydzielanie portów

### [VIII. Współbieżność](./concurrency.md)

Skaluj przez odpowiednio dobrane procesy

### [IX. Zbywalność](./disposability.md)

Zwiększ elastyczność pozwalając na szybkie uruchamianie i zatrzymywanie aplikacji

### [X. Jednolitość środowisk](./dev-prod-parity.md)

Utrzymuj konfigurację środowisk jak najbardziej zbliżoną do siebie

### [XI. Logi](./logs.md)

Traktuj logi jako strumień zdarzeń

### [XII. Zarządzanie aplikacją](./admin-processes.md)

Uruchamiaj zadania administracyjne jako jednorazowe procesy
