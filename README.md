# Partition-Wizard

![Status](https://img.shields.io/badge/status-active-success)
![Platform](https://img.shields.io/badge/platform-Windows-blue)
![Language](https://img.shields.io/badge/language-VB.NET-purple)
![Framework](https://img.shields.io/badge/framework-Windows%20Forms-informational)
![License](https://img.shields.io/badge/license-Proprietary-red)

**Partition-Wizard** ist eine moderne Windows-Anwendung zur Analyse, Verwaltung, Diagnose und Wiederherstellung von Datenträgern, Partitionen und Laufwerken.

Die Anwendung wurde mit **VB.NET / Windows Forms** entwickelt und bietet eine übersichtliche Oberfläche für Speichergeräte, Dateisysteme, Diagnosefunktionen, Recovery-Funktionen, Lizenzprüfung und Updates.

---

## Übersicht

Partition-Wizard richtet sich an Nutzer und Entwickler, die eine grafische Anwendung zur Anzeige und Prüfung von Laufwerken benötigen.

Die Anwendung kann Speichergeräte erkennen, Informationen anzeigen, Dateisysteme unterscheiden und verschiedene Wartungs- und Diagnosefunktionen bereitstellen.

```text
Partition-Wizard
├── Laufwerke erkennen
├── Partitionen anzeigen
├── Dateisysteme analysieren
├── Windows-, Linux- und macOS-Strukturen unterscheiden
├── Diagnosefunktionen ausführen
├── Wiederherstellungsfunktionen nutzen
├── Lizenzstatus prüfen
└── Updates über OTA-System installieren
```

---

## Funktionen

- Erkennung verbundener Laufwerke und Datenträger
- Anzeige von Speicherinformationen
- Analyse von Partitionen und Dateisystemen
- Unterstützung für verschiedene Speicherarten
- Erkennung von Windows-, Linux- und macOS-Strukturen
- Diagnose- und Prüfwerkzeuge
- Wiederherstellungsfunktionen
- Moderne Benutzeroberfläche mit eigenen Controls
- Eigene Diagramm-, Button-, Spinner-, Progressbar- und Menü-Komponenten
- OTA-Updater mit Manifest-Prüfung
- Lizenzsystem mit lokaler und Online-Prüfung
- Lokaler Lizenz-Cache
- Log-System für Diagnose und Fehleranalyse
- Saubere Fehlerbehandlung mit Logging
- Erweiterbare Projektstruktur

---

## Eigene UI-Komponenten

Partition-Wizard verwendet mehrere selbst entwickelte Controls für eine einheitliche und moderne Oberfläche:

- `ClassButton`
- `ClassSpinner`
- `ClassMenuStrip`
- `ClassProgressbar`
- `ClassDiagramControl`
- `ClassCircleDiagramControl`

Diese Komponenten sorgen für eine professionelle Darstellung und verbessern die Bedienbarkeit der Anwendung.

---

## Systemanforderungen

| Komponente | Voraussetzung |
|---|---|
| Betriebssystem | Windows 10 / Windows 11 |
| Sprache | VB.NET |
| Oberfläche | Windows Forms |
| Entwicklungsumgebung | Visual Studio 2022 empfohlen |
| Architektur | x86 / x64 |
| Rechte | Administratorrechte für bestimmte Laufwerksfunktionen empfohlen |

---

## Installation

### Repository klonen

```bash
git clone https://github.com/DEIN-BENUTZERNAME/Partition-Wizard.git
```

### Projekt öffnen

Öffne die Projektdatei mit Visual Studio.

Empfohlen:

```text
Visual Studio 2022
```

### Projekt kompilieren

In Visual Studio:

```text
Build > Build Solution
```

Oder per Tastenkombination:

```text
Strg + Umschalt + B
```

---

## Projektstruktur

```text
Partition-Wizard/
├── Forms/
│   ├── HomeFormV2.vb
│   ├── UpdateForm.vb
│   └── weitere Fenster
│
├── Classes/
│   ├── Licence.vb
│   ├── Diagnostic.vb
│   ├── LinuxFunktionen.vb
│   ├── ClassButton.vb
│   ├── ClassSpinner.vb
│   ├── ClassMenuStrip.vb
│   ├── ClassProgressbar.vb
│   ├── ClassDiagramControl.vb
│   └── ClassCircleDiagramControl.vb
│
├── data/
│   ├── licence.dat
│   ├── trial.dat
│   ├── licence.block
│   └── online_license_cache.json
│
├── log/
│   ├── updater.log
│   ├── licence.log
│   └── diagnostic.log
│
├── README.md
└── LICENSE
```

---

## Updater

Partition-Wizard besitzt einen integrierten OTA-Updater.

Der Updater kann:

- Verbindung zum Update-Server prüfen
- Service-Status prüfen
- Manifest-Datei lesen
- Versionen vergleichen
- Update-Paket herunterladen
- SHA256-Prüfung durchführen
- Fehler separat protokollieren
- Fallback-Server verwenden
- Update-Informationen anzeigen

Beispiel für eine `update.txt`:

```ini
version=3.1.0.0
package=https://example.com/partitionwizard/update.zip
sha256=
channel=stable
info=Partition-Wizard Version 3.1
```

---

## Lizenzsystem

Das Lizenzsystem unterstützt:

- Lokale Lizenzdatei
- Testphase
- Online-Lizenzprüfung
- Lizenz-Cache
- Sperrdatei bei ungültiger Lizenz
- Manipulationsschutz
- Diagnose-Logs

Wichtige Dateien:

```text
data/licence.dat
data/trial.dat
data/licence.block
data/online_license_cache.json
log/licence.log
```

---

## Logging

Partition-Wizard kann verschiedene Logs erzeugen:

```text
log/updater.log
log/licence.log
log/diagnostic.log
```

Diese Dateien helfen bei:

- Fehleranalyse
- Update-Problemen
- Lizenzproblemen
- Laufwerksdiagnose
- unerwarteten Programmfehlern

---

## Sicherheitshinweis

Partition-Wizard arbeitet teilweise mit Laufwerks- und Partitionsinformationen.

Funktionen wie Formatieren, Wiederherstellen oder Änderungen an Datenträgern sollten nur mit Vorsicht verwendet werden.

Vor Änderungen an Datenträgern wird empfohlen:

- wichtige Daten zu sichern
- das richtige Laufwerk auszuwählen
- Administratorrechte zu verwenden
- Diagnose-Logs zu prüfen
- keine Aktionen auf unbekannten Datenträgern auszuführen

---

## Entwicklung

Das Projekt verwendet bewusst strikte VB.NET-Einstellungen:

```vb
Option Strict On
Option Explicit On
```

Dadurch wird der Code stabiler, sauberer und besser wartbar.

Empfohlene Entwicklungsumgebung:

- Visual Studio 2022
- VB.NET
- Windows Forms
- .NET Framework oder passende .NET-Version des Projekts
- Windows 10 oder Windows 11

---

## Code-Richtlinien

Für die Weiterentwicklung werden folgende Regeln empfohlen:

- bestehende Funktionen nicht unnötig löschen
- neue Funktionen möglichst modular aufbauen
- wichtige Aktionen mit Logging versehen
- Fehler sauber mit `Try...Catch` behandeln
- UI nicht blockieren
- längere Aktionen mit `Async/Await` ausführen
- Dateizugriffe vorher prüfen
- sicherheitskritische Funktionen extra absichern
- keine sensiblen Daten hart im Code speichern

---

## Roadmap

Geplante oder mögliche Erweiterungen:

- Erweiterte Linux-Dateisystemanalyse
- Verbesserte macOS-Datenträgererkennung
- SMART-Werte anzeigen
- Theme-System für die Oberfläche
- Erweiterte Recovery-Funktionen
- Mehrsprachigkeit
- Export von Diagnoseberichten
- Verbesserter Update-Installer
- Signierte Update-Pakete
- Erweiterter Manipulationsschutz
- Verbesserte Darstellung für kleine Displays

---

## Screenshots

Screenshots können später im Ordner `screenshots` abgelegt werden.

Beispiel:

```markdown
![Startseite](screenshots/home.png)
![Laufwerksanalyse](screenshots/analyse.png)
![Updater](screenshots/updater.png)
```

---

## Build-Hinweise

Bei Problemen mit dem Build bitte prüfen:

- Sind alle `.vb` Dateien im Projekt eingebunden?
- Sind alle Namespaces korrekt?
- Sind benötigte Ressourcen vorhanden?
- Wird die richtige .NET-Version verwendet?
- Sind alle Verweise korrekt gesetzt?
- Hat Visual Studio alle Pakete wiederhergestellt?

---

## Bekannte Hinweise

Einige Funktionen benötigen je nach System Administratorrechte.

Dazu können gehören:

- Laufwerksinformationen auslesen
- Datenträger prüfen
- bestimmte Diagnosefunktionen ausführen
- Wiederherstellungsfunktionen nutzen
- Systemnahe Informationen abfragen

---

## Haftungsausschluss

Diese Software befindet sich in aktiver Entwicklung.

Die Nutzung erfolgt auf eigene Verantwortung.

Der Entwickler übernimmt keine Haftung für:

- Datenverlust
- beschädigte Partitionen
- fehlerhafte Bedienung
- falsche Laufwerksauswahl
- Schäden durch unsachgemäße Verwendung
- fehlgeschlagene Wiederherstellung
- Fehler durch experimentelle Funktionen

Vor jeder Änderung an Datenträgern sollte ein vollständiges Backup erstellt werden.

---

## Autor

Entwickelt von:

```text
Kevin
```

Projekt:

```text
Partition-Wizard
```

---

## Lizenz

Dieses Projekt ist nicht automatisch Open Source.

Alle Rechte liegen beim Entwickler, sofern keine separate Lizenzdatei vorhanden ist.

```text
Copyright © Kevin 2026
Alle Rechte vorbehalten.
```

---

## Support

Bei Fehlern oder Verbesserungsvorschlägen kann ein GitHub-Issue erstellt werden.

Bitte dabei angeben:

- Windows-Version
- Programmversion
- genaue Fehlermeldung
- Schritte zum Reproduzieren
- relevante Log-Dateien
- Screenshot, falls möglich

---

## Hinweis für Entwickler

Dieses Projekt ist modular aufgebaut.

Neue Funktionen sollten möglichst als eigene Klasse oder eigenes Control umgesetzt werden, damit der Code übersichtlich und wartbar bleibt.

Empfohlen:

```text
Eine Klasse = eine klare Aufgabe
```

Dadurch bleibt Partition-Wizard langfristig stabil, wartbar und erweiterbar.
