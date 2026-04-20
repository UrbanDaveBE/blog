---
title: "Everything Claude Code (ECC) mit Gemini & Antigravity"
date: 2026-04-20T17:58:00+02:00
draft: false
tags: ["ECC", "Gemini", "Antigravity", "AI-Agents"]
categories: ["Tools", "Guides"]
author: "UrbanDaveBE"
---

# Guide: ECC für Gemini & Antigravity (Fork Version)

Dieser Guide beschreibt, wie du meine Version von **Everything Claude Code (ECC)** für den Einsatz mit **Gemini** und der **Antigravity IDE** installierst und konfigurierst.

## Warum dieser Fork?
Mein Fork unter [github.com/UrbanDaveBE/everything-claude-code](https://github.com/UrbanDaveBE/everything-claude-code) ist speziell darauf optimiert, die mächtigen ECC-Agenten und Skills in den Gemini-Harness zu bringen.

## Installation

### 1. Repository klonen
Zuerst klonst du das Repository lokal in dein gewünschtes Verzeichnis:

```bash
git clone https://github.com/UrbanDaveBE/everything-claude-code.git
cd everything-claude-code
```

### 2. Installations-Skript ausführen
Der Fork enthält ein spezialisiertes Skript für verschiedene Targets. Für Gemini nutzt du den `--target gemini` Flag:

**Für macOS/Linux:**
```bash
./install.sh --target gemini --profile full
```

**Für Windows (PowerShell):**
```powershell
.\install.ps1 --target gemini --profile full
```

Dieser Befehl installiert:
- **AGENTS**: Die spezialisierten Sub-Agenten (Planner, Architect, Reviewer etc.).
- **Rules**: Die Verhaltensregeln für den Claude/Gemini Bot.
- **Skills**: Die vordefinierten Workflows (TDD, Refactoring, Security Scan).

## Konfiguration in Antigravity / Gemini

Sobald die Installation durchgelaufen ist, erkennt Antigravity (oder jeder andere Gemini-basierte Harness) die neuen Regeln und Agents automatisch, sofern die Pfade in deiner Umgebung korrekt gesetzt sind.

### Wichtige Befehle
In der Konversation mit der KI kannst du nun die ECC-Logik nutzen:
- `Delegiere die Architektur-Planung an den Architect-Agenten.`
- `Führe einen Security-Review nach ECC-Standard durch.`

## Zusammenfassung
Mit dieser Kombination hast du das Beste aus zwei Welten: Die Intelligenz von Google Geminis Modellen und das strukturierte Framework von Everything Claude Code für effizientes, agentenbasiertes Coding.
