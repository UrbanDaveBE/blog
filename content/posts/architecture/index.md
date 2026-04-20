---
title: "The Architecture Compendium: Principles & Patterns"
date: 2025-02-07T19:23:25+01:00
draft: false
toc: true
tags:
  - Architecture
  - Best Practices
  - Patterns
categories:
  - Architecture
  - CheatSheets
---

# 🏛️ The Architecture Compendium

This is a curated collection of fundamental software development principles, architectural patterns, and industry standards. It serves as a quick reference for designing robust and scalable systems.

---

## 1. Software Development Principles 🛠️

Fundamental rules for writing clean and maintainable code.

*   **SOLID (Object-Oriented Design)**: The bedrock of OOP. [Read my detailed post on SOLID]({{< ref "solid" >}}).
*   **DRY (Don’t Repeat Yourself)**: Every piece of knowledge must have a single, unambiguous, authoritative representation within a system.
*   **KISS (Keep It Simple, Stupid)**: Most systems work best if they are kept simple rather than made complicated.
*   **YAGNI (You Ain’t Gonna Need It)**: A principle of extreme programming (XP) that states a programmer should not add functionality until deemed necessary.
*   **GRASP (General Responsibility Assignment Software Patterns)**: Nine basic principles in object-oriented design and responsibility assignment (e.g., Creator, Controller, Low Coupling, High Cohesion).

---

## 2. Software Architecture Patterns 🏗️

High-level structures used to organize software systems.

*   **CQRS (Command Query Responsibility Segregation)**: Segregating the operations that read data from the operations that update data. [Martin Fowler on CQRS](https://martinfowler.com/bliki/CQRS.html).
*   **Event Sourcing**: Ensuring every change to the state of an application is captured in an event object.
*   **Hexagonal Architecture (Ports & Adapters)**: Creating loosely coupled application components that can be easily connected to their software environment via ports and adapters. [Alistair Cockburn's original post](https://alistair.cockburn.us/hexagonal-architecture/).
*   **Twelve-Factor App**: A methodology for building software-as-a-service apps that are scalable, maintainable, and portable. [12factor.net](https://12factor.net/).
*   **RESTful Principles**: An architectural style for providing standards between computer systems on the web, making it easier for systems to communicate with each other.

---

## 3. Enterprise Architecture Frameworks 🏢

Broad frameworks for organizing IT infrastructure across large organizations.

*   **TOGAF (The Open Group Architecture Framework)**: A high-level approach to design, which is typically modeled at four levels: Business, Application, Data, and Technology. [Official Site](https://www.opengroup.org/togaf).
*   **Zachman Framework**: A schema for organizing architectural artifacts (in other words, design documents, target specifications, and models) that takes into account both what the artifact targets and what particular issue is being addressed.
*   **FEAF (Federal Enterprise Architecture Framework)**: A framework for organizational change through the design and implementation of an enterprise architecture.
*   **SOA Principles (Service-Oriented Architecture)**: A style of software design where services are provided to the other components by application components, through a communication protocol over a network.
*   **Microservices Principles**: An approach to developing a single application as a suite of small services, each running in its own process and communicating with lightweight mechanisms.

---

## 4. Database Principles 💾

Ensuring data integrity, availability, and consistency.

*   **ACID (Transactions)**:
    - **Atomicity**: All changes are made or none are.
    - **Consistency**: Data is in a valid state after a transaction.
    - **Isolation**: Concurrent transactions don't interfere.
    - **Durability**: Changes persist even after a crash.
*   **CAP Theorem**: States that a distributed data store can only provide two of the following three guarantees: **Consistency**, **Availability**, and **Partition tolerance**.
*   **BASE (NoSQL)**: Basically Available, Soft state, Eventual consistency (An alternative to ACID).

---

## 5. DevOps & Infrastructure 🚀

*   **CI/CD (Continuous Integration/Deployment)**: The automated practice of merging code changes and deploying them to production.
*   **Infrastructure as Code (IaC)**: Managing and provisioning infrastructure through machine-readable definition files (e.g., Terraform, Ansible).
*   **Immutable Infrastructure**: An approach where servers are never modified after deployment. If something needs to change, a new server is built from a common image.

---

## 6. Security Principles 🔒

*   **Least Privilege**: A subject should be given only those privileges needed for it to complete its task.
*   **Defense in Depth**: Utilizing multiple layers of security for protecting assets.
*   **Zero Trust**: A security framework requiring all users, whether in or outside the organization's network, to be authenticated, authorized, and continuously validated.

---

## 7. Distributed Systems & Cloud ☁️

*   **Fallacies of Distributed Computing**: A set of assertions made by L Peter Deutsch and others at Sun Microsystems describing false assumptions that programmers new to distributed applications invariably make.
*   **Design for Failure**: A design strategy that assumes things will go wrong and ensures the system can recover gracefully.

---

## 8. Agile & Process Principles 🏃

*   **Agile Manifesto**: A formal proclamation of four key values and 12 principles to guide an iterative and people-centric approach to software development. [AgileManifesto.org](https://agilemanifesto.org/).
*   **Iterative Development**: A way of breaking down the software development of a large application into smaller chunks.

---

## 📚 Further reading & Resources
- [Martin Fowler - Architecture Patterns](https://martinfowler.com/architecture/)
- [Architecture Notes - A collection of diagrams and notes](https://architecturenotes.co/)
- [Clean Architecture by Robert C. Martin](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)