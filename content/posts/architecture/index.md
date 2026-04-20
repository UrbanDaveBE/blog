---
title: "Arch_compendium"
date: 2025-02-07T19:23:25+01:00
draft: false
toc: false
images:
tags:
  - untagged
---

# 1. Software Development Principles

## SOLID (Object-Oriented Design)

- **Single Responsibility**: A class should have one reason to change.
- **Open/Closed**: Open for extension, closed for modification.
- **Liskov Substitution**: Subtypes must be replaceable with their base types.
- **Interface Segregation**: Avoid bloated interfaces; split them into smaller ones.
- **Dependency Inversion**: Depend on abstractions, not concretions.

## DRY (Don’t Repeat Yourself)
- Avoid code duplication.

## KISS (Keep It Simple, Stupid)
- Simplicity over complexity.

## YAGNI (You Ain’t Gonna Need It)
- Don’t add functionality until necessary.

## GRASP (General Responsibility Assignment)
- Patterns like Creator, Controller, Low Coupling, etc.

---

# 2. Software Architecture Principles

## CQRS (Command Query Responsibility Segregation)
- Separate read and write operations.

## Event Sourcing
- Store state changes as events.

## Hexagonal/Ports & Adapters
- Decouple core logic from external systems.

## Twelve-Factor App
- Principles for cloud-native apps (e.g., config in environment, stateless processes).

## RESTful Principles
- Statelessness, uniform interface, cacheability.

---

# 3. Enterprise Architecture Frameworks

## TOGAF
- A methodology for enterprise architecture design.

## Zachman Framework
- A matrix for organizing architectural artifacts.

## FEAF
- U.S. Federal Enterprise Architecture Framework.

## SOA Principles (Service-Oriented Architecture)
- Loose coupling, service contracts, reusability, composability.

## Microservices Principles
- Decentralized data, bounded contexts, infrastructure automation.

---

# 4. Database Principles

## ACID (Transactions)
- **Atomicity**: All-or-nothing execution.
- **Consistency**: Valid state transitions.
- **Isolation**: Concurrent transactions don’t interfere.
- **Durability**: Committed data survives failures.

## CAP Theorem
- Trade-offs between **Consistency**, **Availability**, and **Partition tolerance**.

## BASE (NoSQL)
- **Basically Available**, **Soft state**, **Eventual consistency**.

---

# 5. DevOps & Infrastructure

## CI/CD (Continuous Integration/Deployment)
- Automate testing and delivery.

## Infrastructure as Code (IaC)
- Manage infrastructure via code (e.g., Terraform).

## Immutable Infrastructure
- Replace servers instead of modifying them.

---

# 6. Security Principles

## Least Privilege
- Minimal access rights for users/systems.

## Defense in Depth
- Multiple layers of security.

## Zero Trust
- Verify explicitly, assume breach.

---

# 7. Distributed Systems & Cloud

## Fallacies of Distributed Computing
- Assumptions to avoid (e.g., "The network is reliable").

## Design for Failure
- Assume components will fail (e.g., Netflix Chaos Monkey).

---

# 8. Agile & Process Principles

## Agile Manifesto
- Individuals over processes, working software over documentation.

## Iterative Development
- Deliver incrementally.