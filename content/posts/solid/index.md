---
title: "Solid"
date: 2025-02-08T12:35:44+01:00
draft: false
toc: false
images:
tags:
  - untagged
---

# SOLID Principles (Object-Oriented Design)

SOLID ist ein Akronym für fünf Prinzipien, die dabei helfen, sauberen, wartbaren und erweiterbaren Code zu schreiben. Diese Prinzipien sind besonders nützlich in der objektorientierten Programmierung (OOP).

---

## 1. Single Responsibility Principle (SRP)

### **Was?**
- Eine Klasse sollte **nur eine Aufgabe** haben.
- Es sollte **nur einen Grund geben**, die Klasse zu ändern.

### **Warum?**
- **Wartbarkeit**: Änderungen an einer Aufgabe beeinflussen nicht andere Teile des Systems.
- **Testbarkeit**: Klassen mit einer einzigen Verantwortung sind einfacher zu testen.

### **Beispiel:**

#### Falsch:
```python
class Report:
    def generate_report(self):
        print("Generating report...")

    def save_report(self):
        print("Saving report...")

```

#### Richtig: 
```python
class ReportGenerator:
    def generate_report(self):
        print("Generating report...")

class ReportSaver:
    def save_report(self):
        print("Saving report...")
```

## 2. Open/Closed Principle (OCP)

### Was?
- Klassen sollten **offen für Erweiterungen**, aber **geschlossen für Modifikationen** sein.
- Neue Funktionalität sollte durch **Hinzufügen von neuem Code** (z. B. neue Klassen) erreicht werden, nicht durch Ändern von bestehendem Code.

### Warum?
- **Stabilität:** Bestehender Code bleibt unverändert und funktioniert weiterhin.
- **Erweiterbarkeit:** Neue Anforderungen können leicht umgesetzt werden.

### **Beispiel:**
#### Falsch:
```python
class AreaCalculator:
    def calculate_area(self, shape):
        if shape == "circle":
            return 3.14 * radius * radius
        elif shape == "square":
            return side * side
```
- Bei jeder neuen Form muss die Methode calculate_area geändert werden.

```python
class Shape:
    def area(self):
        pass

class Circle(Shape):
    def area(self):
        return 3.14 * self.radius * self.radius

class Square(Shape):
    def area(self):
        return self.side * self.side
```
- Neue Formen können durch Erben von Shape hinzugefügt werden, ohne AreaCalculator zu ändern.

## 3. Liskov Substitution Principle (LSP)

### Was?
- **Kindklassen** sollten **ohne Probleme** anstelle ihrer **Elternklassen** verwendet werden können.
Das Verhalten der Kindklasse sollte das der Elternklasse **nicht verletzen.**

### Warum?
- **Polymorphismus:** Ermöglicht die Verwendung von Subklassen, ohne das System zu brechen.
- **Vorhersagbarkeit:** Das Verhalten bleibt konsistent.

### **Beispiel:**
#### Falsch:
```python
class Bird:
    def fly(self):
        print("Flying...")

class Ostrich(Bird):  # Strauß kann nicht fliegen!
    def fly(self):
        raise NotImplementedError("Ostriches can't fly!")
```
- Die Klasse **Ostrich** verletzt das Verhalten der Elternklasse **Bird**, da sie nicht fliegen kann.

```python
class Bird:
    pass

class FlyingBird(Bird):
    def fly(self):
        print("Flying...")

class Ostrich(Bird):
    pass
```
- Hier wird die Hierarchie verbessert: FlyingBird erbt von Bird und implementiert fly, während Ostrich einfach nur ein Bird ist, der nicht fliegen kann.


## 3. Interface Segregation Principle (ISP)

### Was?
- **Interfaces** sollten **klein und spezialisiert** sein, nicht groß und allgemein.
- Klassen sollten nicht gezwungen werden, Methoden zu implementieren, die sie nicht brauchen.

### Warum?
- **Flexibilität:** Klassen implementieren nur das, was sie wirklich benötigen.
- **Wartbarkeit:** Änderungen an einem Interface betreffen nur die Klassen, die es tatsächlich verwenden.

### **Beispiel:**
#### Falsch:
```python
class Printer:
    def print(self):
        pass
    def scan(self):
        pass
    def fax(self):
        pass

class SimplePrinter(Printer):
    def print(self):
        print("Printing...")
    def scan(self):  # Wird nicht benötigt!
        raise NotImplementedError("SimplePrinter can't scan!")
    def fax(self):  # Wird nicht benötigt!
        raise NotImplementedError("SimplePrinter can't fax!")
```
- SimplePrinter muss unnötige Methoden implementieren.

```python
class Printer:
    def print(self):
        pass

class Scanner:
    def scan(self):
        pass

class FaxMachine:
    def fax(self):
        pass

class SimplePrinter(Printer):
    def print(self):
        print("Printing...")
```
- Die Interfaces sind aufgeteilt: SimplePrinter implementiert nur Printer.

## Dependency Inversion Principle (DIP)

### Was?
- **Abhängigkeiten** sollten auf **Abstraktionen** basieren, nicht auf konkreten Implementierungen.
- High-Level-Module sollten nicht von Low-Level-Modulen abhängen, sondern beide sollten von Abstraktionen abhängen.


### Warum?
- **Flexibilität:** Einfacherer Austausch von Komponenten.
- **Testbarkeit:** Abhängigkeiten können leicht gemockt werden.

### **Beispiel:**
#### Falsch:
```python
class LightBulb:
    def turn_on(self):
        print("LightBulb: On")

class Switch:
    def __init__(self):
        self.bulb = LightBulb()
    def operate(self):
        self.bulb.turn_on()
```
- Switch hängt direkt von der konkreten Klasse LightBulb ab.

```python
class SwitchableDevice:
    def turn_on(self):
        pass

class LightBulb(SwitchableDevice):
    def turn_on(self):
        print("LightBulb: On")

class Switch:
    def __init__(self, device: SwitchableDevice):
        self.device = device
    def operate(self):
        self.device.turn_on()
```
- Switch hängt von der Abstraktion SwitchableDevice ab, nicht von LightBulb.




