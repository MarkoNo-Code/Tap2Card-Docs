# Tap2Card — Dokumentation

Öffentliche Rechts- und Datenschutzseiten für die Tap2Card-App, ausgeliefert über
GitHub Pages: **https://markono-code.github.io/Tap2Card-Docs/**

Diese Seiten sind aus den Store-Einträgen verlinkt. Die Seite zur Kontolöschung
ist Pflichtbestandteil für Google Play und den App Store — sie muss ohne Login
und ohne installierte App erreichbar bleiben.

## Seiten

| Datei | URL | Inhalt |
|---|---|---|
| `index.html` | `/` | Übersicht, verlinkt die drei Dokumente |
| `privacy-policy.html` | `/privacy-policy.html` | Privacy Policy (Englisch) |
| `datenschutzerklaerung.html` | `/datenschutzerklaerung.html` | Datenschutzerklärung (Deutsch) |
| `delete-account/index.html` | `/delete-account/` | Kontolöschung, zweisprachig |

Die beiden Sprachfassungen der Datenschutzerklärung sind **getrennte Seiten**,
kein JavaScript-Umschalter. Rechtstexte sollen unter einer eigenen, zitierbaren
URL stehen und ohne JS vollständig lesbar sein; die Kopfzeile verlinkt jeweils
die andere Sprache und `hreflang` verbindet die beiden für Suchmaschinen.

## Aufbau

```
Tap2Card-Docs/
├── assets/
│   ├── css/docs.css     # das gesamte Design, ein File
│   ├── js/docs.js       # nur Theme-Umschalter und Jahreszahl
│   └── img/             # App-Icon und Favicon
├── index.html
├── privacy-policy.html
├── datenschutzerklaerung.html
├── delete-account/index.html
└── _deploy/             # lokale Kopie, gitignored
```

Kein Build, keine Abhängigkeiten. Eine Datei im Browser öffnen ist die komplette
Entwicklungsschleife. Jede Seite trägt im `<head>` ein winziges Inline-Skript,
das das gespeicherte Farbschema vor dem ersten Paint setzt — ohne das blitzt beim
Laden das falsche Theme auf.

`_deploy/` ist eine lokale Kopie zum Hochladen und steht in `.gitignore`. Wenn du
Seiten änderst, spiegle sie dorthin, sonst laufen die beiden auseinander.

## Design-Familie

Diese Seiten gehören zu einer Familie aus drei Sites — markono.dev, Tap2Card-Docs
und Ausgetrunken-Docs. Sie teilen Struktur, Komponentennamen, Token-Vokabular und
die Theme-Mechanik; unterschiedlich sind nur Akzentfarbe, Grund und Schriftton.

**Kanonische Beschreibung: `MarkoNoDev/docs/DESIGN_FAMILY.md`** in `Claude-Projects`.
Dort steht auch, warum es bewusst *keine* gemeinsame CSS-Datei gibt und was beim
Ändern in allen drei Sites nachgezogen werden muss.

Die Akzentfarben stammen aus `Tap2Card/Android/.../ui/theme/Color.kt`:
Teal `#05556F` für hell, Türkis `#56C1D9` für dunkel. Keine Farbe wird für die
Website erfunden.

## Kontakt

tap2card@markono.dev

---

© 2026 Marko Nonninger. Alle Rechte vorbehalten.
