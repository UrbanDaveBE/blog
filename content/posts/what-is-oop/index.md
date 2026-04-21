---
title: "Was ist OOP? Objektorientierte Programmierung erklärt"
date: 2026-04-21T14:20:00+02:00
draft: false
toc: true
tags:
  - OOP
  - Basics
  - Clean Code
categories:
  - Development
  - Basics
---

# 📦 Was ist Objektorientierte Programmierung (OOP)?

Objektorientierte Programmierung (kurz **OOP**) ist ein Programmierparadigma, das auf dem Konzept von **"Objekten"** basiert. Im Gegensatz zur prozeduralen Programmierung, wo Code in Funktionen und Abläufen organisiert wird, gruppiert OOP zusammengehörige Daten und Verhaltensweisen in bausteinartigen Entitäten.

Stelle dir ein Auto vor. Anstatt eine Funktion `fahre_auto(farbe, marke)` zu schreiben, erstellst du ein Objekt `Auto`, das Eigenschaften (Farbe, Marke) und Methoden (fahren, bremsen) in sich vereint.

---

## 1. Klassen und Objekte

### **Klassen (Der Bauplan)**
Eine Klasse ist wie ein Bauplan oder eine Blaupause. Sie definiert, welche Eigenschaften und Methoden die Objekte später haben werden, enthält aber selbst noch keine konkreten Daten.

### **Objekte (Die Realität)**
Ein Objekt ist eine Instanz einer Klasse. Wenn die Klasse der Bauplan für ein Auto ist, ist das Objekt das tatsächliche, physische Auto (z.B. ein roter Ferrari), das in deiner Einfahrt steht.

```python
# Die Klasse (Bauplan)
class Auto:
    def __init__(self, marke, farbe):
        self.marke = marke # Eigenschaft
        self.farbe = farbe # Eigenschaft

    def fahren(self):      # Methode
        print(f"Das {self.farbe}e Auto der Marke {self.marke} fährt los!")

# Das Objekt (Instanz)
mein_auto = Auto("Ferrari", "rot")
mein_auto.fahren()
```

---

## 2. Die 4 Säulen der OOP

Damit eine Sprache wirklich als objektorientiert gilt, sollte sie die folgenden vier Kernkonzepte unterstützen:

### 1. Kapselung (Encapsulation)
Daten und die Methoden, die darauf operieren, werden in einer einzigen Einheit (Klasse) gebündelt. Der interne Zustand eines Objekts wird nach außen hin versteckt (`private`) und kann nur über definierte Schnittstellen (Methoden wie Getter/Setter) verändert werden. Das schützt vor ungewollten Änderungen.

### 2. Abstraktion (Abstraction)
Komplexe Implementierungsdetails werden verborgen. Ein Auto hat ein Lenkrad und Pedale – das reicht dem Fahrer. Er muss nicht wissen, wie exakt der Motor intern die Einspritzung regelt. Abstraktion bedeutet, nur das Nötigste nach außen hin preiszugeben.

### 3. Vererbung (Inheritance)
Klassen können Eigenschaften und Verhalten von anderen Klassen erben. Das fördert Code-Wiederverwendung.
- *Beispiel*: Eine Klasse `Hund` erbt von der allgemeinen Klasse `Tier`. Beide können `atmen()`, aber nur der Hund kann `bellen()`.

### 4. Polymorphismus (Polymorphism)
"Vielgestaltigkeit". Verschiedene Klassen können dieselbe Methode definieren, aber unterschiedlich implementieren.
- *Beispiel*: Ein `Hund` und eine `Katze` haben beide eine Methode `sprich()`. Wenn man `Tier.sprich()` aufruft, bellt der Hund, aber die Katze miaut – je nachdem, welches Objekt gerade dahintersteckt.
