# website-checkliste

Ein Claude-Skill mit einer Grundlagen-Checkliste für Website-Projekte – vom Briefing über Design, Build, SEO, QA und Go-Live bis zur Übergabe und Wartung.

Gedacht für Freelancer, Agenturen und interne Teams. Unabhängig von CMS, Framework oder Hosting.

## Was der Skill macht

- **Projektstart:** fragt Website-Typ, Technik, Relaunch/Neubau und Sprachen ab und erstellt eine angepasste `checkliste-<projekt>.md`
- **Statusprüfung:** zählt je Phase erledigt / offen / blockiert und nennt Blocker zuerst
- **Go-Live-Bewertung:** gibt ein klares GO oder NO-GO anhand fester Gates (Abnahme, Rollback, getestetes Backup, keine Staging-Einstellungen, MX geprüft)

**Nicht enthalten:** Security und Legal (Impressum, Datenschutz, Cookies, Verträge). Dafür sind eigene, länderspezifische Checklisten nötig.

## Aufbau

```
website-checkliste/
├── SKILL.md                  # Anweisungen für Claude
├── README.md
└── references/
    └── checkliste.md         # Vorlage mit 10 Abschnitten
```

## Installation

**Claude.ai / Claude Desktop:** Ordner als ZIP hochladen unter *Einstellungen → Fähigkeiten / Skills*.

**Claude Code:** Ordner kopieren nach
- `~/.claude/skills/website-checkliste/` (für alle Projekte) oder
- `.claude/skills/website-checkliste/` (nur im aktuellen Projekt)

## Verwendung

Beispiele:

- „Erstelle mir eine Website-Checkliste für einen Onlineshop mit Shopify."
- „Wo stehen wir bei der Checkliste für Projekt X?"
- „Sind wir bereit für den Go-Live?"

## Anpassen

Die Vorlage in `references/checkliste.md` ist bewusst neutral. Eigene Regeln (z. B. Anzahlung vor Projektstart, Anzahl Korrekturrunden, bevorzugte Tools) können direkt dort ergänzt oder dem Skill im Gespräch mitgeteilt werden.

## Hinweis

Die Checkliste ist eine Arbeitshilfe, keine Garantie für Vollständigkeit und keine Rechtsberatung.
