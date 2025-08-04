---
title: Home
description: A methodology for creating SaaS applications that provides maximum development flexibility, portability, and scalability.
hide:
 - toc
 - navigation
---

## Introduction

In the modern era, software is commonly delivered as a service: called *web apps*, or *software-as-a-service*.  The twelve-factor app is a methodology for building software-as-a-service apps that:

* Use **declarative** formats for setup automation, to minimize time and cost for new developers joining the project;
* Have a **clean contract** with the underlying operating system, offering **maximum portability** between execution environments;
* Are suitable for **deployment** on modern **cloud platforms**, obviating the need for servers and systems administration;
* **Minimize divergence** between development and production, enabling **continuous deployment** for maximum agility;
* And can **scale up** without significant changes to tooling, architecture, or development practices.

The twelve-factor methodology can be applied to apps written in any programming language, and which use any combination of backing services (database, queue, memory cache, etc).

## Background

The contributors to this document have been directly involved in the development and deployment of hundreds of apps, and indirectly witnessed the development, operation, and scaling of hundreds of thousands of apps via our work on the <a href="http://www.heroku.com/" target="_blank">Heroku</a> platform.

This document synthesizes all of our experience and observations on a wide variety of software-as-a-service apps in the wild.  It is a triangulation on ideal practices for app development, paying particular attention to the dynamics of the organic growth of an app over time, the dynamics of collaboration between developers working on the app's codebase, and <a href="http://blog.heroku.com/archives/2011/6/28/the_new_heroku_4_erosion_resistance_explicit_contracts/" target="_blank">avoiding the cost of software erosion</a>.

Our motivation is to raise awareness of some systemic problems we've seen in modern application development, to provide a shared vocabulary for discussing those problems, and to offer a set of broad conceptual solutions to those problems with accompanying terminology.  The format is inspired by Martin Fowler's books *<a href="https://books.google.com/books/about/Patterns_of_enterprise_application_archi.html?id=FyWZt5DdvFkC" target="_blank">Patterns of Enterprise Application Architecture</a>* and *<a href="https://books.google.com/books/about/Refactoring.html?id=1MsETFPD3I0C" target="_blank">Refactoring</a>*.

## Who should read this document?

Any developer building applications which run as a service.  Ops engineers who deploy or manage such applications.

## The Twelve Factors

### [I. Codebase](./codebase.md)

One codebase tracked in revision control, many deploys

### [II. Dependencies](./dependencies.md)

Explicitly declare and isolate dependencies

### [III. Config](./config.md)

Store config in the environment

### [IV. Backing services](./backing-services.md)

Treat backing services as attached resources

### [V. Build, release, run](./build-release-run.md)

Strictly separate build and run stages

### [VI. Processes](./processes.md)

Execute the app as one or more stateless processes

### [VII. Port binding](./port-binding.md)

Export services via port binding

### [VIII. Concurrency](./concurrency.md)

Scale out via the process model

### [IX. Disposability](./disposability.md)

Maximize robustness with fast startup and graceful shutdown

### [X. Dev/prod parity](./dev-prod-parity.md)

Keep development, staging, and production as similar as possible

### [XI. Logs](./logs.md)

Treat logs as event streams

### [XII. Admin processes](./admin-processes.md)

Run admin/management tasks as one-off processes
