# Changelog

Alle wichtigen Änderungen an KettleTrack werden hier dokumentiert.

## [2.0.0] - 2026-02-05

### 🎉 Major Update - Accordion UI & Sync-Funktion

#### ✨ Neue Features
- **Accordion-basiertes UI**: Alle Bereiche sind jetzt klappbar
  - ➕ Neuer Eintrag
  - 📊 Meine Einträge
  - 🔄 Synchronisierung (NEU!)
  - ⚙️ Einstellungen
  - Zustand wird im localStorage gespeichert

- **7-Tage-Sync aus Google Drive**:
  - Lädt automatisch KettleTrack-Logs der letzten 7 Tage
  - Parst Google Docs und extrahiert Trainingseinträge
  - Aktualisiert Exercise History
  - Zeigt Sync-Status mit Zeitstempel

- **Exercise History & Vergleichswerte**:
  - Speichert letzte 10 Sessions pro Übung
  - Info-Box zeigt letzte 3 Ausführungen
  - Erscheint automatisch bei Übungsauswahl
  - Format: "🔥 Letztes Mal: 60 gesamt"

- **Google Doc Parser**:
  - Liest strukturiertes Format aus Google Docs
  - Extrahiert: Datum, Tag, Runde, Übung, Reps, Notizen
  - Robust gegen Formatvariationen

- **"Alle löschen" Funktion**:
  - Button zum Löschen aller Einträge
  - Mit Sicherheitsabfrage

#### 🎨 UI/UX Verbesserungen
- Moderne Card-basierte UI mit Schatten
- Smooth Animationen für Accordions
- Bessere Icons und Badges
- Install Banner in Einstellungen verschoben
- Loading Spinner bei Sync/Save Operationen
- Responsive Design optimiert

#### 🔧 Technische Verbesserungen
- localStorage für Exercise History (`kettletrack-exercise-history`)
- localStorage für Accordion-States (`kettletrack-accordion-states`)
- localStorage für letzten Sync-Zeitstempel (`kettletrack-last-sync`)
- Automatischer Cache-Update beim Speichern in Drive
- Verbesserte Error-Handling für Google Drive API

#### 🐛 Bug Fixes
- Keine bekannten Bugs

---

## [1.0.0] - 2026-01-XX

### 🎉 Erste Version

#### Features
- Trainingseinträge erfassen (Datum, Tag, Runde, Übung, Reps, Notizen)
- Lokale Datenspeicherung (localStorage)
- Export als Markdown-Datei
- Zwischenablage-Funktion
- Trainingsplan hochladen (.md Dateien)
- Google Drive Integration (Speichern)
- Offline-Funktionalität (PWA)
- Installierbar als App
- Auto-Save

---

## Upgrade-Anleitung v1 → v2

### Was bleibt erhalten:
✅ Alle deine Trainingseinträge (in localStorage)
✅ Dein hochgeladener Trainingsplan
✅ Google Account Verbindung

### Was ist neu:
🆕 Exercise History (wird automatisch aufgebaut beim nächsten Sync)
🆕 Accordion-States (Standard: Neuer Eintrag + Meine Einträge offen)

### Empfohlene Schritte nach Update:
1. App öffnen - alles funktioniert wie vorher
2. Mit Google anmelden (falls noch nicht verbunden)
3. "Synchronisierung" öffnen → "Jetzt synchronisieren"
4. Exercise History wird aufgebaut mit Daten der letzten 7 Tage
5. Ab jetzt siehst du Vergleichswerte bei jeder Übung! 🎉

### Bei Problemen:
- Cache leeren (Browser-Einstellungen)
- App neu installieren
- Vorher Markdown-Export als Backup!

---

## Geplante Features (v2.1+)

- 📈 Statistik-Dashboard mit Grafiken
- 🎯 Persönliche Rekorde (PRs) highlighten
- 📅 Kalenderansicht
- 🔔 Erinnerungen für Trainingstage
- 📊 Fortschritts-Charts
- 🏆 Achievements/Badges
- 🌙 Dark Mode
- 🌍 Multi-Language Support

---

**Viel Spaß mit v2.0! 💪🏋️**
