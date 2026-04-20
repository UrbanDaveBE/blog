---
title: "SOLID Principles: Clean Code & Design"
date: 2025-02-08T12:35:44+01:00
draft: false
toc: true
tags:
  - Architecture
  - Clean Code
  - OOP
categories:
  - Development
  - Guides
---

# 🏗️ SOLID Principles (Object-Oriented Design)

SOLID ist ein Akronym für fünf grundlegende Prinzipien des objektorientierten Designs. Sie wurden von **Robert C. Martin (Uncle Bob)** geprägt und helfen dabei, Software zu entwickeln, die **wartbar**, **erweiterbar** und **testbar** ist.

---

## 1. Single Responsibility Principle (SRP)
> "A class should have one, and only one, reason to change."

### **Was?**
Eine Klasse sollte **nur eine einzige Aufgabe** haben. Wenn eine Klasse mehrere Verantwortlichkeiten übernimmt, führt dies zu einer starken Kopplung und erhöht die Fehleranfälligkeit bei Änderungen.

### **Warum?**
- **Wartbarkeit**: Änderungen an einer Funktion beeinflussen keine anderen, unabhängigen Funktionen.
- **Klarheit**: Der Code ist leichter zu verstehen, da jede Klasse genau das tut, was ihr Name verspricht.

### **Beispiel**
#### ❌ Falsch (Zwei Aufgaben: Datenverarbeitung und Speicherung)
```python
class Report:
    def generate_report(self):
        # Logik zur Berichterstellung
        pass

    def save_to_file(self):
        # Logik zum Speichern in eine Datei
        pass
```

#### ✅ Richtig (Verantwortlichkeiten getrennt)
```python
class ReportGenerator:
    def generate(self):
        pass

class ReportSaver:
    def save(self, data):
        pass
```

---

## 2. Open/Closed Principle (OCP)
> "Software entities should be open for extension, but closed for modification."

### **Was?**
Man sollte in der Lage sein, das Verhalten einer Klasse zu erweitern, ohne ihren bestehenden Quellcode zu verändern. Dies wird meist durch **Abstraktion** und **Intererfaces** erreicht.

### **Warum?**
- **Stabilität**: Bestehender, getesteter Code bleibt unverührt.
- **Erweiterbarkeit**: Neue Features (z.B. eine neue Bezahlmethode) können einfach hinzugefügt werden.

### **Beispiel**
#### ❌ Falsch (Muss bei jeder neuen Form geändert werden)
```python
class AreaCalculator:
    def calculate(self, shape):
        if shape.type == "circle":
            return 3.14 * shape.radius ** 2
        elif shape.type == "square":
            return shape.side ** 2
```

#### ✅ Richtig (Abstraktion nutzt Polymorphismus)
```python
class Shape:
    def area(self):
        pass

class Circle(Shape):
    def area(self):
        return 3.14 * self.radius ** 2

class Square(Shape):
    def area(self):
        return self.side ** 2
```

---

## 3. Liskov Substitution Principle (LSP)
> "Subtypes must be substitutable for their base types."

### **Was?**
Objekte einer Basisklasse sollten durch Objekte ihrer Unterklassen ersetzt werden können, ohne dass das Programm fehlerhaft reagiert. Unterklassen dürfen das erwartete Verhalten der Basisklasse nicht einschränken oder verletzen.

---

## 4. Interface Segregation Principle (ISP)
> "Clients should not be forced to depend upon interfaces that they do not use."

### **Was?**
Interfases sollten klein und spezialisiert sein. Es ist besser, viele spezifische Interfaces zu haben als ein einziges "fettes" Interface, das Methoden enthält, die viele Implementierungen gar nicht benötigen.

---

## 5. Dependency Inversion Principle (DIP)
> "Depend upon abstractions, not concretions."

### **Was?**
Module auf hoher Ebene sollten nicht von Modulen auf niedriger Ebene abhängen. Beide sollten von Abstraktionen abhängen. Abstraktionen sollten nicht von Details abhängen, sondern Details von Abstraktionen.

---

## 🚀 Zusammenfassung

| Prinzip | Kurzbeschreibung | Ziel |
| :--- | :--- | :--- |
| **S**RP | Single Responsibility | Hohe Kohäsion, eine Aufgabe pro Klasse. |
| **O**CP | Open/Closed | Erweiterbarkeit ohne Code-Änderung. |
| **L**SP | Liskov Substitution | Korrekte Vererbungshierarchien. |
| **I**SP | Interface Segregation | Schlanke, spezifische Schnittstellen. |
| **D**IP | Dependency Inversion | Entkopplung durch Abstraktionen. |

---

## 📚 Weiterführende Links & Quellen
- [Wikipedia: SOLID (deutsch)](https://de.wikipedia.org/wiki/Prinzipien_objektorientierten_Designs)
- [Martin Fowler: Principles of Software Architecture](https://martinfowler.com/articles/principles-architecture.html)
- [Robert C. Martin: The SOLID Principles](https://blog.cleancoder.com/)
