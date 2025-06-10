<!--
author:   Hannes Tegelbeckers
email:    hannes.tegelbeckers@ovgu.de
version:  2.0.0
language: de
narrator: Deutsch Female

comment:  Dieses interaktive Lernmodul vermittelt fundamentale Konzepte und praktische Techniken für die Datenanalyse mit Pandas in Python.

script:   https://cdn.jsdelivr.net/pyodide/v0.24.1/full/pyodide.js
import:   https://raw.githubusercontent.com/LiaScript/CodeRunner/master/README.md


-->

# 🐼 Pandas Selbstlerntool für Fachinformatiker

> **Ziel:** Interaktives Erlernen der Pandas-Bibliothek für Datenanalyse in Python
> 
> **Zielgruppe:** Auszubildende Fachinformatiker im Versicherungswesen
> 
> **Dauer:** Ca. 4-6 Stunden (je nach Vorkenntnissen)

## 📋 Kursübersicht

Diese interaktiven Lernmodule führen Sie systematisch in die **Pandas**-Bibliothek ein – das zentrale Werkzeug für Datenanalyse in Python. Jede Lektion kombiniert Theorie mit praktischen Übungen und verwendet realitätsnahe Beispiele aus dem Versicherungswesen.

### 🎯 Lernziele

Nach Abschluss dieses Moduls können Sie:

- [x] **Grundlagen:** Pandas importieren und grundlegende Datenstrukturen verstehen
- [x] **Datenmanipulation:** DataFrames erstellen, laden und transformieren
- [x] **Analyse:** Deskriptive Statistiken berechnen und Daten explorieren
- [x] **Praxis:** Realitätsnahe Versicherungsdaten analysieren

### 📚 Voraussetzungen

**Erforderlich:**
- Grundlegende Python-Kenntnisse (Variablen, Schleifen, Funktionen)
- Verständnis für Datenstrukturen (Listen, Dictionaries)

**Empfohlen:**
- Jupyter Notebook oder PyCharm IDE
- Grundkenntnisse über Tabellenkalkulation (Excel)

### 🛠️ Setup & Installation

Bevor wir beginnen, stellen Sie sicher, dass Pandas installiert ist:

```bash
pip install pandas numpy matplotlib
```

**Tipp:** In Anaconda-Umgebungen ist Pandas meist bereits vorinstalliert.

---

## 📖 Lektion 1: Grundlagen der Pandas-Bibliothek

> **Lernzeit:** ~45 Minuten
> 
> **Inhalte:** Pandas kennenlernen, Series und DataFrame verstehen

### 1.1 🚀 Was ist Pandas?

**Pandas** (**Pan**el **Da**ta **S**tructures) ist eine mächtige Open-Source-Bibliothek für:

- **Datenmanipulation** und -analyse
- **Datenimport/-export** (CSV, Excel, JSON, SQL-Datenbanken)
- **Datentransformation** und -bereinigung
- **Zeitreihenanalyse**

![Pandas Logo](https://pandas.pydata.org/static/img/pandas_white.svg)

**Warum Pandas im Versicherungswesen?**

- Analyse von Schadensfällen und Leistungsabrechnungen
- Kundendatenauswertung und Segmentierung
- Prämienkalkulation und Risikobewertung
- Compliance-Reporting und Datenqualitätsprüfung

### 1.2 📦 Import und erste Schritte

**Konvention:** Pandas wird standardmäßig als `pd` importiert:

```python
import pandas as pd
import numpy as np

# Version prüfen
print(f"Pandas Version: {pd.__version__}")
print(f"NumPy Version: {np.__version__}")
```
@Pyodide.eval

**💡 Quiz: Pandas Import**

Vervollständigen Sie den korrekten Import:

```python
import pandas as [[pd]]
```

[[pd]]
***
<script>
  let input = "@input".trim();
  input === "pd" ? true : false;
</script>
***

### 1.3 🧮 Pandas Datenstrukturen

Pandas basiert auf zwei Hauptdatenstrukturen:

#### 📊 Series (1D-Datenstruktur)

Eine **Series** ist wie eine Spalte in einer Tabelle:

```python
import pandas as pd

# Series mit Versicherungsbeiträgen erstellen
beitraege = pd.Series([285.50, 298.75, 275.00, 320.25, 290.00], 
                     index=['Jan', 'Feb', 'Mar', 'Apr', 'Mai'],
                     name='Monatsbeitrag_EUR')

print("Beiträge Series:")
print(beitraege)
print(f"\nDatentyp: {beitraege.dtype}")
print(f"Anzahl Werte: {len(beitraege)}")
```
@Pyodide.eval

**Wichtige Series-Eigenschaften:**

- **Index:** Eindeutige Kennzeichnung jedes Wertes
- **Values:** Die eigentlichen Daten
- **Name:** Optionaler Name der Series
- **Dtype:** Datentyp der Werte

#### 📋 DataFrame (2D-Tabellenstruktur)

Ein **DataFrame** ist wie eine Excel-Tabelle:

```python
import pandas as pd

# Beispiel: Kundendaten einer Krankenversicherung
kunden_data = {
    'KundenID': [1001, 1002, 1003, 1004, 1005],
    'Name': ['Anna Müller', 'Bob Schmidt', 'Clara Yilmaz', 'David Weber', 'Eva Fischer'],
    'Alter': [29, 41, 35, 52, 28],
    'Versicherungstyp': ['Privat', 'Gesetzlich', 'Privat', 'Gesetzlich', 'Privat'],
    'Monatsbeitrag': [285.50, 198.75, 345.00, 215.25, 290.00],
    'Eintrittsdatum': ['2020-01-15', '2019-06-23', '2021-03-10', '2018-11-05', '2022-02-28']
}

df = pd.DataFrame(kunden_data)
print("Kundendaten DataFrame:")
print(df)
```
@Pyodide.eval

**DataFrame-Übersicht erhalten:**

```python
# Grundlegende Informationen
print("Shape (Zeilen x Spalten):", df.shape)
print("\nSpaltennamen:", df.columns.tolist())
print("\nDatentypen:")
print(df.dtypes)
print("\nErste 3 Zeilen:")
print(df.head(3))
```
@Pyodide.eval

### 1.4 🔍 Praktische Übung: DataFrame erkunden

**Aufgabe:** Analysieren Sie das Kundendaten-DataFrame:

```python
# Ihr Code hier - erkunden Sie das DataFrame
import pandas as pd

# Kundendaten neu laden
kunden_data = {
    'KundenID': [1001, 1002, 1003, 1004, 1005],
    'Name': ['Anna Müller', 'Bob Schmidt', 'Clara Yilmaz', 'David Weber', 'Eva Fischer'],
    'Alter': [29, 41, 35, 52, 28],
    'Versicherungstyp': ['Privat', 'Gesetzlich', 'privat', 'Gesetzlich', 'Privat'],
    'Monatsbeitrag': [285.50, 198.75, 345.00, 215.25, 290.00],
    'Eintrittsdatum': ['2020-01-15', '2019-06-23', '2021-03-10', '2018-11-05', '2022-02-28']
}
df = pd.DataFrame(kunden_data)

# Versuchen Sie folgende Operationen:
# 1. Durchschnittsalter berechnen
print("Durchschnittsalter:", df['Alter'].mean())

# 2. Anzahl Privat- vs. Gesetzlich Versicherte
print("\nVerteilung Versicherungstyp:")
print(df['Versicherungstyp'].value_counts())

# 3. Höchster und niedrigster Beitrag
print(f"\nHöchster Beitrag: {df['Monatsbeitrag'].max():.2f} EUR")
print(f"Niedrigster Beitrag: {df['Monatsbeitrag'].min():.2f} EUR")
```
@Pyodide.eval

### 1.5 ❓ Wissenstest: Series vs. DataFrame

**Multiple Choice:** Welche Aussagen sind korrekt?

- [x] Eine Series hat einen Index und kann verschiedene Datentypen enthalten
- [x] Ein DataFrame besteht aus mehreren Series mit gemeinsamen Index
- [ ] Series können nur numerische Werte enthalten
- [x] DataFrames ähneln Excel-Tabellen mit Zeilen und Spalten
- [ ] Der Index eines DataFrames muss immer numerisch sein

### 1.6 🏃‍♂️ Hands-On Challenge

**Erstellen Sie Ihr eigenes DataFrame:**

Stellen Sie sich vor, Sie arbeiten in der Schadensabteilung. Erstellen Sie ein DataFrame mit folgenden Schadensfällen:

```python
# Ihre Aufgabe: Erstellen Sie ein DataFrame 'schaeden' mit:
# - SchadenID: [2001, 2002, 2003, 2004]
# - Schadensart: ['Unfall', 'Sturm', 'Diebstahl', 'Unfall'] 
# - Schadenhoehe: [1250.00, 3800.50, 750.25, 2100.75]
# - Status: ['Offen', 'Bearbeitet', 'Abgeschlossen', 'Offen']

# Ihr Code hier:
import pandas as pd

schaeden_data = {
    'SchadenID': [2001, 2002, 2003, 2004],
    'Schadensart': ['Unfall', 'Sturm', 'Diebstahl', 'Unfall'],
    'Schadenhoehe': [1250.00, 3800.50, 750.25, 2100.75],
    'Status': ['Offen', 'Bearbeitet', 'Abgeschlossen', 'Offen']
}

schaeden = pd.DataFrame(schaeden_data)
print("Schadensfälle DataFrame:")
print(schaeden)

# Zusatzaufgaben:
print(f"\nGesamtschadenhöhe: {schaeden['Schadenhoehe'].sum():.2f} EUR")
print(f"Durchschnittlicher Schaden: {schaeden['Schadenhoehe'].mean():.2f} EUR")
print(f"Anzahl offene Fälle: {(schaeden['Status'] == 'Offen').sum()}")
```
@Pyodide.eval

### 1.7 ✅ Lernkontrolle

**Drag & Drop:** Ordnen Sie die Begriffe richtig zu:

| Begriff | Definition |
|---------|------------|
| Series | [[1D-Datenstruktur mit Index]] |
| DataFrame | [[2D-Tabellenstruktur]] |
| Index | [[Eindeutige Kennzeichnung der Zeilen]] |
| Columns | [[Spaltennamen des DataFrames]] |

**Kurze Reflexion:**

Beantworten Sie für sich:

1. Wann würden Sie eine Series vs. ein DataFrame verwenden?
2. Welche Vorteile bietet Pandas gegenüber regulären Python-Listen?
3. Wie könnte Pandas in Ihrem Arbeitsbereich eingesetzt werden?

---

## 🎯 Zusammenfassung Lektion 1

**Was Sie gelernt haben:**

✅ **Pandas Grundlagen:** Import, Zweck und Anwendungsbereiche
✅ **Series:** 1D-Datenstruktur mit Index verstehen und erstellen  
✅ **DataFrame:** 2D-Tabellenstrukturen aufbauen und erkunden
✅ **Grundoperationen:** `.head()`, `.shape`, `.dtypes`, `.mean()` etc.
✅ **Praxisbezug:** Anwendung auf Versicherungsdaten

**Nächste Schritte:**

In **Lektion 2** lernen Sie:
- Daten aus verschiedenen Quellen importieren (CSV, Excel)
- Datenbereinigung und -transformation
- Erweiterte Indexierung und Filterung

---

## 📝 Zusatzaufgaben (Optional)

**Level 1 - Einsteiger:**
Erstellen Sie eine Series mit den Wochentagen als Index und Ihren täglichen Arbeitszeiten als Werte.

**Level 2 - Fortgeschritten:**
Erstellen Sie ein DataFrame mit fiktiven Mitarbeiterdaten (Name, Abteilung, Gehalt, Einstellungsdatum) und berechnen Sie Grundstatistiken.

**Level 3 - Profi:**
Kombinieren Sie mehrere Series zu einem DataFrame und führen Sie eine einfache Analyse durch (z.B. Korrelation zwischen Alter und Beitragshöhe).

---

## 🔗 Weiterführende Ressourcen

- [Offizielle Pandas Dokumentation](https://pandas.pydata.org/docs/)
- [Pandas Cheat Sheet](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf)
- [10 Minutes to Pandas](https://pandas.pydata.org/docs/user_guide/10min.html)

---

*© 2025 | Hannes Tegelbeckers | Version 2.0.0*