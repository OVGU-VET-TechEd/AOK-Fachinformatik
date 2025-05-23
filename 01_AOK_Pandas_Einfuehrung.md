<!--
author:   Fachinformatiker Ausbildungsmodul
email:    ausbildung@versicherung.de
date:     22/05/2025
version:  1.0
language: de
narrator: Deutsch Female

repository: https://github.com/liascript/
logo:     https://upload.wikimedia.org/wikipedia/commons/2/22/Pandas_mark.svg
comment:  Diese Selbstlerneinheit führt Auszubildende in die Pandas-Bibliothek ein.
-->

# 🐼 Einführung in Pandas

                --{{0}}--
Diese Einheit vermittelt dir die Grundlagen zur Installation und ersten Nutzung der Pandas-Bibliothek in Python. Pandas ist eines der wichtigsten Werkzeuge für die Arbeit mit strukturierten Daten – besonders im Gesundheitswesen.


    --{{0}}--
!?[](https://github.com/OVGU-VET-TechEd/AOK-Fachinformatik/blob/main/media/Pandas%20Development.mp4)

** The AI will explain, please listen carefully ** 

!?[Was ist Pandas?](https://www.youtube.com/watch?v=vmEHCJofslg)


## 🎯 Lernziele

* Du verstehst, was Pandas ist und wann man es verwendet.
* Du installierst Pandas korrekt in deiner Entwicklungsumgebung.
* Du importierst die Bibliothek in Python und erzeugst erste DataFrames.

---

## 📦 1. Was ist Pandas?

Pandas ist eine Open-Source-Python-Bibliothek zur Datenanalyse und -bearbeitung.
Sie stellt zwei zentrale Datentypen bereit:

* **Series**: eindimensionale Daten (wie eine Liste)
* **DataFrame**: tabellarische Daten mit Zeilen und Spalten (wie eine Excel-Tabelle)

### 🧠 Beispiel:

```python
import pandas as pd

# Series erzeugen
serie = pd.Series([10, 20, 30])
print(serie)

# DataFrame erzeugen
daten = {
    "Name": ["Max", "Lisa", "Ali"],
    "Alter": [28, 24, 30]
}
df = pd.DataFrame(daten)
print(df)
```

<script>@input</script>

---

## ⚙️ 2. Installation von Pandas

Die Installation erfolgt meist über pip:

```bash
pip install pandas
```

Oder innerhalb von Jupyter Notebooks:

```python
!pip install pandas
```

<script>@input</script>

---

## 🔍 3. Pandas importieren

```python
import pandas as pd
```

Dieser Befehl importiert Pandas unter dem Alias `pd`, was in der Praxis Standard ist.

---

## ✅ Mini-Quiz: Pandas-Grundlagen

Welche Aussage ist korrekt?

\[( )] Pandas ist eine Datenbank.
\[( )] Pandas ist eine Visualisierungsbibliothek wie matplotlib.
\[(X)] Pandas dient der Datenanalyse und -verarbeitung.
\[( )] Pandas kann nur mit CSV-Dateien arbeiten.

\-- Bei Fehlern: Hinweis --

> Denk daran: Pandas arbeitet mit tabellarischen Daten und ist für Datenmanipulation entwickelt worden.

---

## 🛠 Praxisaufgabe: Dein erster DataFrame

### ✏️ Aufgabe:

Erstelle einen DataFrame mit drei Spalten:

* "Kunde"
* "Alter"
* "Tarif"

und mindestens drei Zeilen mit Daten deiner Wahl.

```python
# Deine Lösung hier:
import pandas as pd

# Beispieldaten
kunden = {
    "Kunde": ["Anna", "Bernd", "Clara"],
    "Alter": [31, 45, 29],
    "Tarif": ["A1", "B2", "A2"]
}

# DataFrame erstellen
df = pd.DataFrame(kunden)
print(df)
```

<script>@input</script>

---

## 🔁 Wiederholung

| Begriff     | Bedeutung                     |
| ----------- | ----------------------------- |
| `Series`    | Eindimensionale Datenstruktur |
| `DataFrame` | Tabellarische Datenstruktur   |
| `pd`        | Alias für pandas beim Import  |

### 🧠 Reflexion:

Wozu könnte Pandas in einer Krankenkasse eingesetzt werden? Notiere 2 Anwendungsideen:

1. \[\[\_\_\_]]
2. \[\[\_\_\_]]

---

## 🎉 Abschluss

Herzlichen Glückwunsch! Du hast die Grundlagen zur Verwendung von Pandas gelernt.

**Möchtest du mit "Series und DataFrames im Detail" weitermachen?**

<script input="select" value="Ja" options="Ja|Nein|Später">
"Du hast '" + @input + "' gewählt."
</script>

<!-- Ende der Selbstlerneinheit -->
