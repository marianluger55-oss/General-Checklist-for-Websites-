---
name: website-checkliste
description: Grundlagen-Checkliste für Website-Projekte von Briefing bis laufendem Betrieb. Verwenden, wenn ein Website-Projekt startet, der Projektstand geprüft oder die Go-Live-Bereitschaft bewertet werden soll. Security und Legal sind nicht enthalten.
---

# Website-Checkliste (Grundlagen)

Dieser Skill liefert eine Basis-Checkliste für Website-Projekte (Freelancer, Agenturen, interne Teams) und erklärt, wie sie eingesetzt wird. Die Vorlage liegt in `references/checkliste.md`.

**Nicht enthalten:** Security und Legal (Impressum, Datenschutz, Cookies, Verträge, Barrierefreiheitsrecht). Diese Themen brauchen eigene, auf das jeweilige Land abgestimmte Checklisten. Wenn ein Punkt dorthin gehört, nur darauf hinweisen – keine Rechtsberatung geben.

## Wann verwenden

- **Projektstart** → projektspezifische Checkliste erstellen
- **Statusprüfung** („Wo stehen wir?") → offene Punkte je Phase zusammenfassen
- **Vor Abnahme oder Go-Live** → GO / NO-GO je Phase bewerten

## Vorgehen

### 1. Rahmen klären

Fehlende Angaben kurz erfragen, maximal ein bis zwei Fragen auf einmal:

- **Website-Typ:** One-Pager, Landingpage, Unternehmenswebsite, Onlineshop, Web-App
- **Technik:** CMS / Framework / Baukasten (z. B. WordPress, Next.js, Webflow, Shopify) und Hosting
- **Relaunch oder Neubau?**
- **Ein- oder mehrsprachig?**
- **Eigene Prozessregeln** des Nutzers, z. B. Anzahlung vor Start, Anzahl Korrekturrunden, Zahlung vor Go-Live

Ist etwas nicht zu klären, mit der naheliegendsten Annahme weitermachen und sie oben in der Datei notieren.

### 2. Checkliste anpassen

- Vorlage aus `references/checkliste.md` laden.
- Punkte mit ⓣ laut Abschnitt 10 der Vorlage für den Website-Typ übernehmen, ersetzen oder streichen.
- Tool-Beispiele in Klammern (z. B. „[Plausible / Matomo / GA4]") durch das tatsächlich genutzte Tool ersetzen. Unbekannt → als Platzhalter stehen lassen.
- Technik-spezifische Punkte ergänzen, z. B. bei WordPress: Plugins aktualisiert, ungenutzte Plugins/Themes entfernt; bei Next.js: `next build` lokal getestet; bei Shopify: Zahlungs- und Versandtests.
- Eigene Prozessregeln des Nutzers als Punkte und – wo sinnvoll – als Gates einfügen.

### 3. Datei erstellen

- Markdown-Datei, Name z. B. `checkliste-<projektname>.md` (kleingeschrieben, Bindestriche).
- Kopfzeile: Projekt, Website-Typ, Technik, Datum.
- Offene Entscheidungen als Platzhalter in [eckigen Klammern].
- Keine Punkte erfinden, die nicht zum Projekt passen – lieber streichen als aufblähen.

### 4. Statusprüfung

Wenn der Nutzer Fortschritt meldet oder den Stand wissen will:

- Je Phase zählen: erledigt / offen / blockiert.
- **Blocker zuerst** nennen, dann offene Punkte der aktuellen Phase.
- Am Ende ein klares **GO** oder **NO-GO** für den nächsten Meilenstein.

## Gates (NO-GO, solange offen)

Standard-Gates – nur gültig, wenn sie zum Projekt passen:

- Kein Go-Live ohne **schriftliche Abnahme** durch den Auftraggeber
- Kein Go-Live ohne **Rollback-Plan** und **getestetes Backup** (ein nie zurückgespieltes Backup zählt nicht)
- Kein Go-Live mit Staging-Einstellungen (`noindex`, blockierende `robots.txt`)
- Kein DNS-Umzug ohne Prüfung bestehender **E-Mail-Einträge (MX)**

Eigene Gates des Nutzers (z. B. „kein Start ohne Anzahlung") zusätzlich übernehmen.

## Grundsätze

- Die Website gehört dem Auftraggeber: Domain und wichtige Zugänge laufen auf ihn.
- Freigaben immer schriftlich festhalten.
- Lieber eine kurze, vollständig abgehakte Liste als eine lange, halb ignorierte.
