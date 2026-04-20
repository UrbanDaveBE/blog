---
title: "Everything Claude Code (ECC) mit Gemini & Antigravity"
date: 2026-04-20T17:58:00+02:00
draft: false
tags: ["ECC", "Gemini", "Antigravity", "AI-Agents"]
categories: ["Tools", "Guides"]
author: "UrbanDaveBE"
toc: true
---

# 🤖 Guide: ECC für Gemini & Antigravity

In diesem Guide erfährst du, wie du meinen spezialisierten Fork von **Everything Claude Code (ECC)** installierst und für die Nutzung mit **Google Gemini** und der **Antigravity IDE** optimierst.

> [!NOTE]
> Mein Fork unter [github.com/UrbanDaveBE/everything-claude-code](https://github.com/UrbanDaveBE/everything-claude-code) ist speziell darauf optimiert, die mächtigen ECC-Agenten in den Gemini-Harness zu integrieren.

---

## 🛠️ Installation

Folge diesen Schritten, um ECC auf deinem System einzurichten.

### 1. Repository klonen
Zuerst klonst du das Repository lokal in dein Arbeitsverzeichnis:

```bash
git clone https://github.com/UrbanDaveBE/everything-claude-code.git
cd everything-claude-code
```

### 2. Das Installations-Skript ausführen
Der Fork enthält ein Skript für verschiedene Zielplattformen. Für Gemini verwenden wir den `--target gemini` Flag.

> [!IMPORTANT]
> Nutze den `--profile full` Parameter, um alle Agenten (Architect, Planner, Reviewer) und Skills (TDD, Security Scan) zu installieren.

#### **Für macOS / Linux:**
```bash
chmod +x install.sh
./install.sh --target gemini --profile full
```

#### **Für Windows (PowerShell):**
```powershell
.\install.ps1 --target gemini --profile full
```

---

## 🏗️ Funktionsumfang

Nach der Installation stehen dir folgende Komponenten zur Verfügung:

| Komponente | Beschreibung |
| :--- | :--- |
| **AGENTS** | Spezialisierte Sub-Agenten wie Planner, Architect und Reviewer. |
| **RULES** | Verhaltensregeln, die das Modell für ECC-Workflows optimieren. |
| **SKILLS** | Vordefinierte Workflows wie TDD (Test Driven Development) oder Refactoring. |

---

## 🚀 Nutzung in Antigravity / Gemini

Sobald die Installation abgeschlossen ist, erkennt Antigravity (oder jeder andere Gemini-Harness) die neuen Regeln und Agenten automatisch.

### **Wichtige Befehle & Prompts**
Du kannst die ECC-Logik jetzt direkt in deinen Prompts anfordern:

- `[ ]` "Delegiere die Architektur-Planung für dieses Feature an den Architect-Agenten."
- `[ ]` "Führe einen Security-Review Code-Scan nach ECC-Standard durch."
- `[ ]` "Erstelle einen TDD-Workflow für die neue Login-Funktion."

---

## 📝 Zusammenfassung
Durch die Kombination von **Google Geminis** Rechenpower und dem strukturierten Framework von **Everything Claude Code** erhältst du ein mächtiges Werkzeug für effizientes, agentenbasiertes Coding.

**Links:**
- [Mein Fork auf GitHub](https://github.com/UrbanDaveBE/everything-claude-code)
- [Antigravity IDE (Gemini-basiert)](https://github.com/google-deepmind/antigravity)
- [ECC Original Repository](https://github.com/statelyai/everything-claude-code)
