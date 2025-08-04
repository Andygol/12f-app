---
title: Home
description: Como garantir a máxima flexibilidade em termos de elasticidade, mobilidade e escalabilidade no processo de criação de aplicações SaaS.
hide:
 - toc
 - navigation
---

## Introdução

Na era moderna, software é comumente entregue como um serviço: denominados *web apps*, ou *software-como-serviço*. A aplicação doze-fatores é uma metodologia para construir softwares-como-serviço que:

* Usam formatos **declarativos** para automatizar a configuração inicial, minimizar tempo e custo para novos desenvolvedores participarem do projeto;
* Tem um **contrato claro** com o sistema operacional que o suporta, oferecendo **portabilidade máxima** entre ambientes que o executem;
* São adequados para **implantação** em modernas **plataformas em nuvem**, evitando a necessidade por servidores e administração do sistema;
* **Minimizam a divergência** entre desenvolvimento e produção, permitindo a **implantação contínua** para máxima agilidade;
* E podem **escalar** sem significativas mudanças em ferramentas, arquiteturas, ou práticas de desenvolvimento.

A metodologia doze-fatores pode ser aplicada a aplicações escritas em qualquer linguagem de programação, e que utilizem qualquer combinação de serviços de suportes (banco de dados, filas, cache de memória, etc).

## Experiência

Os contribuidores deste documento estão diretamente envolvidos no desenvolvimento e implantação de centenas de aplicações, e indiretamente testemunhando o desenvolvimento, operação e escalada de centenas de milhares de aplicações através de seu trabalho na plataforma [Heroku](http://www.heroku.com/).

Este documento sintetiza toda nossa experiência e observação em uma variedade de aplicações que operam como software-como-serviço. Isto é a triangulação de práticas ideais ao desenvolvimento de software, com uma atenção particular a respeito das dinâmicas de crescimento orgânico de uma aplicação ao longo do tempo, a dinâmica de colaboração entre desenvolvedores trabalhando em uma base de código, e evitando os [custos de erosão de software](http://blog.heroku.com/archives/2011/6/28/the_new_heroku_4_erosion_resistance_explicit_contracts/)

Nossa motivação é aumentar a consciência de alguns problemas sistêmicos que temos visto no desenvolvimento de aplicações modernas, prover um vocabulário comum para discussão destes, e oferecer um amplo conjunto de soluções conceituais para esses problemas com a terminologia que os acompanha. O formato é inspirado nos livros de Martin Fowler *[Padrões de Arquitetura de Aplicações Enterprise](http://books.google.com/books/about/Patterns_of_enterprise_application_archi.html?id=FyWZt5DdvFkC)* e *[Refatorando](http://books.google.com/books/about/Refactoring.html?id=1MsETFPD3I0C)*.

## Quem deve ler este documento?

Qualquer desenvolvedor que esta construindo aplicações que rodam como serviço. Engenheiros de Operações que implantam ou administram tais aplicações.

## Os Doze Fatores

### [I. Base de Código](./codebase.md)

Uma base de código com rastreamento utilizando controle de revisão, muitos deploys

### [II. Dependências](./dependencies.md)

Declare e isole as dependências

### [III. Configurações](./config.md)

Armazene as configurações no ambiente

### [IV. Serviços de Apoio](./backing-services.md)

Trate os serviços de apoio, como recursos ligados

### [V. Construa, lance, execute](./build-release-run.md)

Separe estritamente os builds e execute em estágios

### [VI. Processos](./processes.md)

Execute a aplicação como um ou mais processos que não armazenam estado

### [VII. Vínculo de porta](./port-binding.md)

Exporte serviços por ligação de porta

### [VIII. Concorrência](./concurrency.md)

Dimensione por um modelo de processo

### [IX. Descartabilidade](./disposability.md)

Maximizar a robustez com inicialização e desligamento rápido

### [X. Dev/prod semelhantes](./dev-prod-parity.md)

Mantenha o desenvolvimento, teste, produção o mais semelhante possível

### [XI. Logs](./logs.md)

Trate logs como fluxo de eventos

### [XII. Processos de Admin](./admin-processes.md)

Executar tarefas de administração/gerenciamento como processos pontuais
