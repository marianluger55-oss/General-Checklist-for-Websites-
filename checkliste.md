# Website-Checkliste – [Projektname]

> Typ: [Website-Typ] · Technik: [CMS / Framework] · Hosting: [Anbieter] · Stand: [Datum]
> Security und Legal sind nicht enthalten – dafür eigene Checklisten verwenden.
> Platzhalter in [Klammern] = offene Entscheidung. ⓣ = abhängig vom Website-Typ (Abschnitt 10).

---

## 1. Briefing & Projektstart

- [ ] Auftrag schriftlich bestätigt
- [ ] Website-Typ festgelegt
- [ ] Ziel der Website in einem Satz + messbares Erfolgskriterium (z. B. Anfragen pro Monat)
- [ ] Zielgruppe und wichtigste Handlung (Haupt-CTA) festgelegt
- [ ] Kurze Wettbewerbsanalyse (mind. 3 vergleichbare Websites)
- [ ] Sitemap / Seitenliste schriftlich abgestimmt
- [ ] Leistungsumfang fixiert – inkl. was ausdrücklich **nicht** enthalten ist
- [ ] Inhalte geklärt: Wer liefert Texte, Bilder, Logo, Videos – bis wann?
- [ ] Markenelemente erhalten (Logo als Vektor, Farben, Schriften, Styleguide)
- [ ] Referenz-Websites gesammelt (gefällt / gefällt nicht)
- [ ] Sprachen festgelegt
- [ ] Domain: Registrar bekannt, läuft auf den Auftraggeber, Zugang vorhanden
- [ ] Bestehende E-Mail-Adressen auf der Domain erfasst (MX-Einträge nicht zerstören)
- [ ] Relaunch? → Liste aller alten URLs exportiert ⓣ
- [ ] Ansprechpartner und Freigabeberechtigte benannt
- [ ] Zeitplan mit Meilensteinen schriftlich bestätigt

## 2. Setup

- [ ] Projektablage / Projektstatus-Dokument angelegt
- [ ] Versionsverwaltung eingerichtet (z. B. Git-Repository) ⓣ
- [ ] CMS / Framework installiert, Admin-Zugang angelegt
- [ ] Konfiguration getrennt von Code, Zugangsdaten nicht im Repository
- [ ] Code-Qualität: Linter / Formatter aktiv ⓣ
- [ ] Automatischer Build bzw. Deployment-Pipeline [Tool] ⓣ
- [ ] Staging-Umgebung eingerichtet (passwortgeschützt oder `noindex`)

## 3. Design

- [ ] Designrichtung (Moodboard / Mockups) vom Auftraggeber freigegeben
- [ ] Farben, Typografie, Abstände als einheitliches System definiert
- [ ] Kontraste geprüft (Fließtext mind. 4,5:1)
- [ ] Mobile Ansicht zuerst gestaltet, dann Desktop
- [ ] Zustände bedacht: Hover, Fokus, Fehler, Leer, Laden
- [ ] Favicon, App-Icons, Social-Share-Bild (Open Graph, 1200×630)
- [ ] Korrekturrunden mitgezählt [Anzahl laut Vereinbarung]
- [ ] Design-Freigabe schriftlich

## 4. Build

### Struktur & Komponenten
- [ ] Wiederverwendbare Bausteine statt Einzellösungen
- [ ] Redaktionelle Inhalte vom Auftraggeber selbst pflegbar
- [ ] CMS-Felder verständlich benannt, Hilfetexte wo nötig
- [ ] Ein `<h1>` pro Seite, logische Überschriften-Hierarchie
- [ ] Navigation per Tastatur bedienbar, Fokus sichtbar
- [ ] Seitentitel / Website-Name ist nicht mehr der Vorlagen-Standard

### Bilder & Medien
- [ ] Bilder komprimiert, moderne Formate (WebP / AVIF), passende Größen
- [ ] Alt-Texte für inhaltliche Bilder, dekorative Bilder mit leerem Alt
- [ ] Videos komprimiert, kein Autoplay mit Ton

### Formulare
- [ ] Versand zuverlässig eingerichtet [Mail-Dienst]
- [ ] Bestätigung an Absender + Benachrichtigung an Empfänger
- [ ] Labels an allen Feldern, verständliche Fehler- und Erfolgsmeldungen
- [ ] Spam-Schutz aktiv [Honeypot / Captcha]

### Fehlerseiten & Logging
- [ ] Hilfreiche 404-Seite (Links zur Startseite / Suche)
- [ ] Eigene Seite für Serverfehler (500)
- [ ] Fehler werden geloggt bzw. gemeldet [Tool]

### Inhalte
- [ ] Keine Platzhaltertexte (Lorem ipsum) oder Testbilder mehr
- [ ] Kontaktdaten überall identisch
- [ ] Social-Media-Links korrekt
- [ ] Alle Sprachversionen vollständig, Sprachumschalter funktioniert ⓣ
- [ ] Content-Freeze vor Go-Live vereinbart

## 5. SEO & Analytics

- [ ] Title (≤ 60 Zeichen) und Meta-Description (≤ 155 Zeichen) je Seite
- [ ] Sprechende URLs, keine doppelten Inhalte
- [ ] `sitemap.xml` vorhanden, nur Live-Domain enthalten
- [ ] `robots.txt` korrekt (Staging blockiert, Live erlaubt + Sitemap verlinkt)
- [ ] Canonical-Tags gesetzt
- [ ] Open-Graph- und Twitter-Card-Tags
- [ ] Strukturierte Daten (z. B. Organization / LocalBusiness / Product / FAQ)
- [ ] `hreflang` bei mehreren Sprachen ⓣ
- [ ] 301-Weiterleitungen von alten URLs ⓣ
- [ ] Analytics eingebunden, Ziele/Events definiert [Plausible / Matomo / GA4]
- [ ] Google Search Console (ggf. Bing Webmaster Tools) eingerichtet, Sitemap eingereicht
- [ ] Google Unternehmensprofil verknüpft (lokale Unternehmen) ⓣ

## 6. QA

### Geräte & Browser
- [ ] Chrome, Safari, Firefox, Edge (aktuelle Versionen)
- [ ] iOS und Android auf echten Geräten getestet
- [ ] Breiten 360 / 768 / 1024 / 1440 px ohne Bruch, kein horizontales Scrollen

### Performance
- [ ] Produktions-Build lokal ohne Fehler und Warnungen ⓣ
- [ ] Lighthouse Mobile und Desktop: Performance ≥ [90], Accessibility ≥ [95], Best Practices ≥ [95], SEO ≥ [95]
- [ ] Core Web Vitals grün (LCP < 2,5 s, CLS < 0,1, INP < 200 ms)
- [ ] Schriften optimiert geladen, Caching sinnvoll eingestellt

### Barrierefreiheit (Grundcheck)
- [ ] Komplette Seite nur mit Tastatur bedienbar
- [ ] Automatischer Test ohne kritische Fehler [axe / WAVE]
- [ ] Zoom auf 200 % ohne Layoutbruch

### Funktion
- [ ] Alle Links geprüft – keine 404 oder Weiterleitungsketten [Linkchecker]
- [ ] Alle Formulare getestet, E-Mails kommen an (nicht im Spam)
- [ ] Telefon- und E-Mail-Links am Handy getestet
- [ ] CMS-Test: Textänderung erscheint korrekt auf der Seite
- [ ] Rechtschreibung und Grammatik geprüft

### Abnahme
- [ ] Auftraggeber hat Staging geprüft
- [ ] Schriftliche Abnahme liegt vor

## 7. Deployment

### Vorbereitung
- [ ] Go-Live-Termin abgestimmt (nicht Freitag / vor Feiertagen)
- [ ] Rollback-Plan: alte Seite bzw. alter DNS-Stand dokumentiert
- [ ] DNS-TTL rechtzeitig vorher gesenkt

### Go-Live
- [ ] Produktionsumgebung bereit [Hosting]
- [ ] Konfiguration / Umgebungsvariablen für Produktion gesetzt
- [ ] Datenbank und Inhalte von Staging übernommen
- [ ] DNS umgestellt, MX-Einträge unverändert
- [ ] HTTPS aktiv, http → https und www ↔ ohne www sauber weitergeleitet
- [ ] E-Mail-Versand von der Live-Domain geprüft (SPF / DKIM / DMARC)
- [ ] `noindex` / Staging-`robots.txt` entfernt
- [ ] Uptime-Monitoring aktiv [Tool]
- [ ] Erstes Backup erstellt und Wiederherstellung einmal getestet
- [ ] Formulare und wichtigste Seiten live getestet

### Nachbeobachtung (erste 2–4 Wochen)
- [ ] Search Console: Indexierung und Fehler beobachten
- [ ] 404-Aufrufe prüfen, fehlende Weiterleitungen nachziehen
- [ ] Uptime, Fehlerlogs und Formulareingänge kontrollieren

## 8. Übergabe

- [ ] Kurzanleitung für das CMS (Dokument oder Video)
- [ ] Zugänge übergeben – der Auftraggeber ist Eigentümer
- [ ] Übersicht: Domain, Hosting, Dienste, Laufzeiten, wer hat welchen Zugang
- [ ] Support-Weg und Reaktionszeiten erklärt
- [ ] Schlussrechnung gestellt
- [ ] Feedback / Bewertung / Referenz-Freigabe angefragt
- [ ] Projekt fürs Portfolio dokumentiert
- [ ] Nachbetrachtung: Was lief gut, was wird am Prozess geändert?

## 9. Laufender Betrieb (bei Wartung)

- [ ] Regelmäßige Updates (CMS, Plugins, Abhängigkeiten) [Intervall]
- [ ] Regelmäßiger Check von Uptime, Logs und Analytics
- [ ] Backups automatisch, Wiederherstellung stichprobenartig testen
- [ ] Domain- und Zertifikatsablauf im Blick
- [ ] Zugänge prüfen, wenn sich Personen beim Auftraggeber ändern
- [ ] Reporting an den Auftraggeber [Intervall]
- [ ] Aufwand pro Projekt erfassen

## 10. Hinweise je Website-Typ ⓣ

- **One-Pager / Landingpage:** minimale Sitemap, meist eine Sprache; Fokus auf einen CTA und Ladezeit.
- **Unternehmenswebsite:** voller Ablauf, besonderes Augenmerk auf CMS-Pflege und SEO.
- **Onlineshop:** zusätzlich Produktdaten, Steuern, Zahlungs- und Versandtests, Bestell-E-Mails, Testbestellung mit Storno.
- **Web-App:** zusätzlich Login-Flows, Rollen und Rechte, Datenmigration, Lasttest.
- **Baukasten (Webflow, Wix, Squarespace …):** Setup-, Build- und Deployment-Punkte entfallen größtenteils; Domain-, SEO-, QA- und Übergabepunkte bleiben.
