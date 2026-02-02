# KettleTrack PWA 🏋️

Dein persönlicher Kettlebell Trainingslog als Progressive Web App - installierbar auf iOS, Android und Desktop!

## 📦 Was ist enthalten?

- **kettletrack-pwa.html** - Die Haupt-App (alles in einer Datei)
- **manifest.json** - PWA Manifest für Installation
- **service-worker.js** - Offline-Funktionalität und Caching
- **create-icons.html** - Tool zum Generieren der App-Icons

## 🚀 Installation & Deployment

### Option 1: GitHub Pages (Kostenlos & Einfach)

1. Erstelle ein neues GitHub Repository
2. Lade folgende Dateien hoch:
   - `kettletrack-pwa.html`
   - `manifest.json`
   - `service-worker.js`
   - `icon-192.png` (siehe Icon-Erstellung unten)
   - `icon-512.png` (siehe Icon-Erstellung unten)

3. Gehe zu Repository Settings → Pages
4. Wähle Branch "main" und "/" als Root
5. Deine App ist dann unter: `https://[dein-username].github.io/[repo-name]/kettletrack-pwa.html`

### Option 2: Netlify/Vercel (Noch einfacher)

1. Erstelle Account bei [Netlify](https://netlify.com) oder [Vercel](https://vercel.com)
2. Ziehe alle Dateien in den Upload-Bereich
3. App ist sofort live!

### Option 3: Eigener Server

Lade alle Dateien auf deinen Webspace hoch. Die App benötigt HTTPS für PWA-Features!

## 🎨 Icons erstellen

Es gibt zwei Wege, die Icons zu erstellen:

### Weg 1: Mit dem Generator (Empfohlen)
1. Öffne `create-icons.html` in deinem Browser
2. Klicke auf "Download 192x192" und "Download 512x512"
3. Speichere die Dateien als `icon-192.png` und `icon-512.png`

### Weg 2: Eigene Icons (Professionell)
Erstelle eigene Icons mit einem Tool wie:
- [Figma](https://figma.com)
- [Canva](https://canva.com)
- Photoshop/Illustrator

**Wichtig:**
- icon-192.png: 192 × 192 Pixel
- icon-512.png: 512 × 512 Pixel
- Format: PNG mit transparentem Hintergrund (optional)

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

## ✨ Features

### Bereits implementiert:
- ✅ Trainingseinträge erfassen (Datum, Tag, Runde, Übung, Reps, Notizen)
- ✅ Lokale Datenspeicherung (deine Daten bleiben auf deinem Gerät)
- ✅ Export als Markdown-Datei
- ✅ Zwischenablage-Funktion
- ✅ Trainingsplan hochladen (.md Dateien)
- ✅ Offline-Funktionalität
- ✅ Installierbar als App
- ✅ Auto-Save (Daten gehen nie verloren)

### PWA-Features:
- 📱 Läuft wie eine native App
- 🔌 Funktioniert offline
- 💾 Automatische Updates im Hintergrund
- 🚀 Schneller Start
- 🔒 Sicher (nur du hast Zugriff auf deine Daten)

## 🛠️ Technische Details

### Gespeicherte Daten
Alle Daten werden im **localStorage** deines Browsers gespeichert:
- `kettletrack-entries` - Deine Trainingseinträge
- `kettletrack-plan` - Dein hochgeladener Trainingsplan

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

## 🔧 Anpassungen

### Farben ändern
In `kettletrack-pwa.html` kannst du die Farben anpassen:

```html
<meta name="theme-color" content="#111827"> <!-- App-Farbe -->
```

```json
// In manifest.json
"background_color": "#f9fafb",
"theme_color": "#111827"
```

### Trainingsplan anpassen
Der Standard-Trainingsplan ist im Code enthalten. Du kannst:
1. Den Code direkt anpassen (im `defaultTrainingPlan` Objekt)
2. Oder: Eine `.md` Datei hochladen über die App

### Service Worker Update
Ändere die Version in `service-worker.js`:
```javascript
const CACHE_NAME = 'kettletrack-v2'; // Version hochzählen
```

## 📝 Trainingsplan Format

Wenn du einen eigenen Trainingsplan hochladen möchtest, nutze dieses Format:

```markdown
| Tag | Fokus | Übungen |
| --- | --- | --- |
| Montag | Upper Body Push | 1. Kettlebell Overhead Press 2. Kettlebell Floor Press |
| Dienstag | Lower Body + Core | 1. Kettlebell Goblet Squat 2. Kettlebell Swing |
```

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

### Icons werden nicht angezeigt
- Prüfe Dateinamen: genau `icon-192.png` und `icon-512.png`
- Prüfe ob Dateien im gleichen Ordner wie die HTML-Datei liegen
- Icons müssen PNG-Format haben

## 🔐 Datenschutz

- **Alle Daten bleiben auf deinem Gerät** (localStorage)
- Keine Server-Kommunikation
- Keine Tracking-Cookies
- Keine Analytics
- Open Source - du kannst den Code einsehen

## 📄 Lizenz

MIT License - Frei verwendbar für private und kommerzielle Zwecke

## 🎯 Nächste Schritte

1. Icons erstellen
2. App auf GitHub Pages/Netlify deployen
3. Auf deinem Handy installieren
4. Training tracken! 💪

## 💡 Tipps

- **Backup erstellen:** Exportiere regelmäßig deine Einträge als Markdown
- **Schneller Zugriff:** Platziere die App im Dock/auf dem Home-Bildschirm
- **Offline nutzen:** Einmal geladen, funktioniert die App auch ohne Internet
- **Updates:** Bei Änderungen einfach die Dateien auf dem Server aktualisieren

## 🆘 Support

Probleme oder Fragen? 
- Prüfe das Troubleshooting oben
- Öffne ein Issue auf GitHub
- Schau in die Browser-Konsole (F12) für Fehlermeldungen

---

**Viel Erfolg beim Training! 🏋️💪**
