---
title: "Mein neuer Titel"
date: 2026-04-21T14:36:00+02:00
draft: true
toc: true
tags:
  - Tag1
  - Tag2
categories:
  - Category1
---

# Hauptüberschrift (H1)

Dies ist dein Text. Kurze Info vorab: Mache dir angewöhnt, dass die Hauptdatei in deinen Ordnern immer **`index.md`** heißen muss (damit Hugo die Bilder zuordnen kann). 

**Wenn du einen Beitrag schreiben willst:**
1. Kopiere diesen kompletten `_vorlage` Ordner.
2. Benenne die Kopie auf deinen Titel um (z.B. in `mein-thema`). Das `_` fällt dabei weg, sodass Hugo den neuen Ordner nicht mehr ignoriert!
3. Ändere hier oben im "Header" `draft: true` auf `draft: false`.

---

## 🖼️ Bilder einfügen

Packe das Bild (z.B. `architektur.png`) einfach in exakt diesen Ordner, neben diese `index.md` Datei.

**So referenzierst du es dann:**
```markdown
![Hier steht die Bildbeschreibung (für blinde Nutzer usw.)](architektur.png)
```

**Bilder mit einem zusätzlichen Hover-Titel:**
```markdown
![Beschreibung](architektur.png "Dieser Titel erscheint, wenn man mit der Maus über das Bild fährt")
```

---

## ✍️ Die wichtigsten Markdown-Befehle

### 1. Textformatierung
* **Fett:** `**Dieser Text ist fett**` 
* *Kursiv:* `*Dieser Text ist kursiv*` 
* ~~Durchgestrichen:~~ `~~Dieser Text ist durchgestrichen~~`
* `Inline-Code`: Wenn du Befehle wie `git push` im Text nutzt, umschließe sie mit einfachen Backticks (\`).

### 2. Überschriften
```markdown
# H1 Überschrift (Meist nur 1x pro Seite für den Titel)
## H2 Überschrift (Für wichtige Unterkapitel)
### H3 Überschrift (Zum tiefer gliedern)
```

### 3. Listen
**Ungeordnet (Aufzählung):**
```markdown
- Erster Punkt
- Zweiter Punkt
  - Eingerückter Punkt
```

**Geordnet (Nummeriert):**
```markdown
1. Mehl abwiegen
2. Wasser zugeben
3. Kneten
```

### 4. Links
```markdown
[Hier klicken für Google](https://www.google.ch)
```

### 5. Blockzitate (Quotes)
```markdown
> "Das ist ein schönes Zitat, um etwas hervorzuheben."
> - Jemand Wichtiges
```

### 6. Mehrzeilige Code-Blöcke
Verwende 3 Backticks am Anfang und Ende. Du kannst auch die Sprache (z.B. `python`, `java`, `bash`) angeben, damit Hugo die Syntax farblich schön markiert:

````markdown
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
````

---
*Viel Spaß beim Bloggen! Vergiss nicht am Ende dein Repo zu pushen.*
