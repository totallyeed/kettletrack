# 🚀 Schnellstart-Anleitung für KettleTrack PWA

## In 5 Minuten zur eigenen App!

### Schritt 1: Icons erstellen (2 Minuten)
1. Öffne `create-icons.html` in deinem Browser
2. Klicke auf beide Download-Buttons
3. Du hast jetzt `icon-192.png` und `icon-512.png`

### Schritt 2: Bei Netlify deployen (2 Minuten)
1. Gehe zu [netlify.com](https://netlify.com) und erstelle einen Account
2. Klicke auf "Add new site" → "Deploy manually"
3. Ziehe diese Dateien in den Upload-Bereich:
   - kettletrack-pwa.html
   - manifest.json
   - service-worker.js
   - icon-192.png
   - icon-512.png
4. Warte 10 Sekunden → Deine App ist live! 🎉

Du bekommst eine URL wie: `https://deine-app.netlify.app/kettletrack-pwa.html`

### Schritt 3: Auf dem Handy installieren (1 Minute)

#### iPhone:
1. Öffne die URL in Safari
2. Tippe auf Teilen-Symbol
3. "Zum Home-Bildschirm"
4. Fertig!

#### Android:
1. Öffne die URL in Chrome
2. Tippe auf "Installieren" Banner
3. Fertig!

---

## Alternative: GitHub Pages (etwas mehr Setup)

### Schritt 1: GitHub Repository erstellen
1. Gehe zu [github.com](https://github.com) und logge dich ein
2. Klicke auf "New repository"
3. Name: `kettletrack` (oder was du willst)
4. Mache es "Public"
5. Klicke "Create repository"

### Schritt 2: Dateien hochladen
1. Klicke auf "uploading an existing file"
2. Ziehe alle Dateien rein (HTML, manifest, service-worker, icons)
3. Klicke "Commit changes"

### Schritt 3: GitHub Pages aktivieren
1. Gehe zu "Settings" → "Pages"
2. Source: "Deploy from a branch"
3. Branch: "main" → Folder: "/ (root)"
4. Klicke "Save"

Nach 1-2 Minuten ist deine App live unter:
`https://[dein-username].github.io/kettletrack/kettletrack-pwa.html`

---

## Testen

1. Öffne die URL auf deinem Handy
2. Die App sollte laden
3. Füge einen Test-Eintrag hinzu
4. Schließe den Browser
5. Öffne wieder → Dein Eintrag ist noch da! ✅

---

## Häufige Fehler

**"manifest.json nicht gefunden"**
→ Stelle sicher, dass alle Dateien im gleichen Ordner sind

**Icons werden nicht angezeigt**
→ Dateinamen müssen GENAU `icon-192.png` und `icon-512.png` sein

**"Installieren" Button fehlt (iPhone)**
→ Nutze Safari, nicht Chrome

**App funktioniert nicht offline**
→ Öffne sie einmal online, dann wird sie gecacht

---

## Das war's! 🎉

Du hast jetzt eine voll funktionsfähige App:
- ✅ Installierbar auf jedem Gerät
- ✅ Funktioniert offline
- ✅ Speichert deine Daten lokal
- ✅ Sieht aus wie eine native App

**Viel Spaß beim Training!** 💪🏋️
