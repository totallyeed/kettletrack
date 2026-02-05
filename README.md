# KettleTrack PWA 🏋️ v2.0

Dein persönlicher Kettlebell Trainingslog als Progressive Web App - installierbar auf iOS, Android und Desktop!

## 🆕 Was ist neu in v2.0?

### 🎯 Hauptfeatures
- ✨ **Accordion-UI**: Übersichtliche, klappbare Bereiche
- 🔄 **7-Tage-Sync**: Automatisches Laden der letzten Trainings aus Google Drive
- 📊 **Vergleichswerte**: Sieh deine letzten 3 Sessions bei jeder Übung
- 💾 **Exercise History**: Speichert automatisch deine Fortschritte
- 🗑️ **Alle löschen**: Button zum Zurücksetzen aller Einträge

[Siehe CHANGELOG.md für Details](CHANGELOG.md)

## 📱 Installation auf dem Handy

### iOS (iPhone/iPad)

1. Öffne die App-URL in Safari
2. Tippe auf das **Teilen-Symbol** (Quadrat mit Pfeil nach oben)
3. Scrolle runter und wähle **"Zum Home-Bildschirm"**
4. Benenne die App (z.B. "KettleTrack")
5. Tippe auf **"Hinzufügen"**

**Fertig!** Die App erscheint als Icon auf deinem Home-Bildschirm

### Android

1. Öffne die App-URL in Chrome
2. Chrome zeigt automatisch einen **"Zur Startseite hinzufügen"**-Banner
3. Oder: Menü (⋮) → **"App installieren"** oder **"Zum Startbildschirm hinzufügen"**
4. Bestätige die Installation

### Desktop (Chrome, Edge, etc.)

1. Öffne die App-URL
2. Klicke auf das **Install-Symbol** in der Adressleiste (⊕ oder ⬇)
3. Oder: Menü → **"KettleTrack installieren"**

---

## ✨ Features

### 🎯 Kern-Features
- ✅ **Trainingseinträge erfassen**: Datum, Tag, Runde, Übung, Reps, Notizen
- ✅ **Accordion-UI**: Klappbare Bereiche für bessere Übersicht
- ✅ **Vergleichswerte**: Sieh deine letzten 3 Sessions bei jeder Übung
- ✅ **Exercise History**: Automatische Fortschrittsspeicherung (letzte 10 Sessions pro Übung)
- ✅ **7-Tage-Sync**: Lade deine letzten Trainings aus Google Drive
- ✅ **Google Drive Integration**: Speichere Logs als Google Docs
- ✅ **Lokale Datenspeicherung**: Deine Daten bleiben auf deinem Gerät
- ✅ **Export als Markdown**: Download oder teilen als .md Datei
- ✅ **Zwischenablage-Funktion**: Schnell kopieren & einfügen
- ✅ **Trainingsplan hochladen**: .md Dateien hochladen
- ✅ **Offline-Funktionalität**: Funktioniert ohne Internet
- ✅ **Installierbar als App**: Wie eine native App nutzen
- ✅ **Auto-Save**: Daten gehen nie verloren

### 🆕 NEU in v2.0
- 🔄 **Sync-Funktion**: Lädt letzte 7 Tage aus Google Drive
- 📊 **Vergleichswerte-Anzeige**: Info-Box mit letzten Sessions
- 💾 **Exercise History**: localStorage für Fortschritt
- 🗑️ **Alle löschen**: Einträge zurücksetzen
- 🎨 **Besseres UI**: Accordion-basiert, moderne Cards
- ⚙️ **Einstellungen-Bereich**: Google Account + Plan Upload

### 📱 PWA-Features
- 📱 Läuft wie eine native App
- 🔌 Funktioniert offline
- 💾 Automatische Updates im Hintergrund
- 🚀 Schneller Start
- 🔒 Sicher (nur du hast Zugriff auf deine Daten)

---

## 🛠️ Technische Details

### Gespeicherte Daten (localStorage)
- `kettletrack-entries` - Deine Trainingseinträge
- `kettletrack-plan` - Dein hochgeladener Trainingsplan
- `kettletrack-exercise-history` - 🆕 Letzte 10 Sessions pro Übung
- `kettletrack-accordion-states` - 🆕 UI-Zustand der Accordions
- `kettletrack-last-sync` - 🆕 Zeitstempel des letzten Syncs
- `google_access_token` - Google Drive OAuth Token

### Cache-Strategie
Der Service Worker cached:
- Die HTML-Datei
- React-Bibliotheken
- Das Manifest

**Cache-First mit Network-Fallback** für optimale Performance

### Browser-Kompatibilität
- ✅ iOS Safari 11.3+
- ✅ Android Chrome 40+
- ✅ Desktop Chrome/Edge/Firefox
- ⚠️ iOS erfordert Safari (nicht Chrome iOS)

---

## 📝 Trainingsplan Format

Wenn du einen eigenen Trainingsplan hochladen möchtest, nutze dieses Format:

```markdown
| Tag | Fokus | Übungen |
| --- | --- | --- |
| Montag | Upper Body Push | 1. Kettlebell Overhead Press 2. Kettlebell Floor Press |
| Dienstag | Lower Body + Core | 1. Kettlebell Goblet Squat 2. Kettlebell Swing |
```

---

## 🐛 Troubleshooting

### "Installieren" Button erscheint nicht
- Stelle sicher, dass die App über HTTPS läuft
- Prüfe ob alle Dateien korrekt hochgeladen sind
- Bei iOS: Nutze Safari (nicht Chrome)

### Daten gehen verloren
- Prüfe Browser-Einstellungen (Cookies/localStorage erlaubt?)
- Nutze nicht den Inkognito-Modus
- Mache regelmäßig Markdown-Exports als Backup

### App lädt nicht offline
- Öffne die App einmal online, damit der Cache gefüllt wird
- Prüfe ob der Service Worker registriert ist (Browser DevTools → Application → Service Workers)

### Sync funktioniert nicht
- Stelle sicher, dass du mit Google angemeldet bist (⚙️ Einstellungen)
- Prüfe ob Dateien im Format `KettleTrack_Log_YYYY-MM-DD` vorliegen
- Dateien müssen im Ordner `KettleTrack/Logs/` liegen
- Prüfe Browser-Konsole (F12) für Fehlermeldungen

### Vergleichswerte erscheinen nicht
- Führe einmal einen Sync durch (🔄 Synchronisierung)
- Oder: Füge Einträge hinzu und speichere in Drive
- Exercise History wird automatisch aufgebaut

---

## 🔐 Datenschutz

- **Alle Daten bleiben auf deinem Gerät** (localStorage)
- Google Drive Zugriff nur für von der App erstellte Dateien
- Keine Server-Kommunikation (außer Google Drive API)
- Keine Tracking-Cookies
- Keine Analytics
- Open Source - du kannst den Code einsehen

---

## 📄 Lizenz

MIT License - Frei verwendbar für private und kommerzielle Zwecke



**Viel Erfolg beim Training! 🏋️💪**

*Version 2.0.0 - Februar 2026*
