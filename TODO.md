# Tap2Card-Docs — offene Punkte

Stand: 09.09.2026, nach dem Redesign auf die Design-Familie
(`MarkoNoDev/docs/DESIGN_FAMILY.md`).

Am 11.09.2026 im Browser abgenommen, committet und gepusht. `README.md` und
diese Datei werden per `_config.yml` nicht mit ausgeliefert.

---

## 1. Beim nächsten App-Release

- [ ] **Datenschutz-Link in der App fehlt** — weder Android noch iOS verlinken die
      Datenschutzerklärung. Apple 5.1.1(i) und Google Play verlangen ihn auch
      *in* der App, nicht nur im Store-Eintrag. Das Review hat es bisher nicht
      bemängelt, das kann sich bei jedem Update ändern.

## 2. Store-Material

- [ ] `app-icon.html`, `feature-graphic.html`, `feature-graphic-screenshot.jpeg`,
      `presentation-graphic*.png` liegen **ungetrackt** im Wurzelverzeichnis und
      wurden bewusst nicht mit committet — sie sind keine Website und würden
      sonst öffentlich ausgeliefert. Besser nach
      `Claude-Projects/PlayStore-AppStore-Files/` verschieben.

## 3. Inhaltlich noch offen

- [ ] **Ein Jurist hat da nicht draufgeschaut.** Die Datenschutztexte wurden am
      09.09.2026 inhaltlich geändert (Verantwortlicher jetzt Winterthur statt
      Deutschland, iOS und App Store ergänzt, Anmeldewege benannt, Apple-Widerruf
      bei Löschung, NFC-Verhalten unter iOS). Das Datum steht jetzt konsistent auf
      dem 09.09.2026. Die Änderungen bilden ab, was der Code tut — sie sind keine
      Rechtsberatung.
- [ ] **Nicht geprüft: was Tap2Card sonst noch verarbeitet.** Für Ausgetrunken
      wurde das systematisch durchgegangen (Firebase, Maps, Billing, Auth-Provider).
      Für Tap2Card steht nur fest: Supabase, Google Play Billing, Anmeldung per
      E-Mail / Apple / Google. **Kein** Firebase, **kein** Analytics, **kein**
      Crashlytics. Ob die Policy damit vollständig ist, ist nicht abschliessend
      geprüft — die sechs In-App-Käufe (Kartendesigns) tauchen im Text
      beispielsweise nirgends auf.

## 4. Aufräumen, wenn Zeit ist

- [ ] `_deploy/` ist eine gitignorierte Kopie zum Hochladen und aktuell synchron.
      Da GitHub Pages ohnehin aus dem Repo baut: prüfen, ob der Ordner überhaupt
      noch einen Zweck hat.

---

## Was fertig ist

Vier Seiten im Design der Familie: Übersicht, Privacy Policy (EN),
Datenschutzerklärung (DE), Kontolöschung (zweisprachig). Sprachumschalter als
echte Links statt JS, Inhaltsverzeichnis als sticky Spalte, Berechtigungen als
Karten mit Stroke-Icons statt Emoji, Theme-Umschalter mit dem Speicherschlüssel
`markono.theme`, Print-Stylesheet.
