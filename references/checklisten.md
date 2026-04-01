# Checklisten — Dokumente & Compliance (Deutschland)

> Lade diese Datei bei: Dokumentenprüfung (Impressum, AGB, Datenschutzerklärung, AVV, NDA), Compliance-Audits, Erstellung neuer rechtlicher Dokumente, Einstieg in ein neues Projekt.

---

## Checkliste 1: Impressum (§ 5 DDG)

### Anbieter-Typ: Einzelperson / Freiberufler
- [ ] Vorname und Nachname (vollständig)
- [ ] Straße, Hausnummer, PLZ, Ort
- [ ] E-Mail-Adresse (direkt erreichbar, kein Formular allein)
- [ ] ggf. Telefonnummer (empfohlen, nicht mehr zwingend)
- [ ] ggf. Berufliche Kammer / Berufsbezeichnung + Aufsichtsbehörde
- [ ] ggf. Berufsrecht und Zugangsland (z.B. "zugelassen in Deutschland")
- [ ] USt-ID oder Steuernummer (wenn USt-pflichtig)
- [ ] Inhaltlich Verantwortlicher (bei redaktionellen Inhalten, § 18 Abs. 2 MStV)

### Anbieter-Typ: GmbH / UG
- [ ] Firma (vollständig mit Rechtsformzusatz)
- [ ] Sitz der Gesellschaft (eingetragener Sitz!)
- [ ] Geschäftsführer (alle vertretungsberechtigten Personen)
- [ ] Handelsregisternummer + zuständiges Amtsgericht
- [ ] USt-ID (§ 27a UStG)
- [ ] E-Mail-Adresse
- [ ] ggf. Aufsichtsbehörde (bei regulierten Tätigkeiten)
- [ ] Inhaltlich Verantwortlicher (bei redaktionellen Inhalten)

### Anbieter-Typ: AG
- Wie GmbH, zusätzlich:
- [ ] Vorstand (alle Mitglieder)
- [ ] Vorsitzender des Aufsichtsrats

### Anbieter-Typ: GbR / OHG / KG
- [ ] Alle Gesellschafter mit vollständigem Namen und Adresse
- [ ] Bei KG: Komplementär(e) benennen

### Prüfung Erreichbarkeit
- [ ] Impressum über max. 2 Klicks von der Startseite erreichbar
- [ ] Impressum in der Fußzeile verlinkt
- [ ] Mobil erreichbar (nicht hinter Hamburger-Menü versteckt)
- [ ] Impressum auf Social-Media-Profil angegeben (Bio, "Über uns")
- [ ] Impressum-Link auch in E-Mail-Signatur (bei geschäftlichen E-Mails empfohlen)

---

## Checkliste 2: Datenschutzerklärung

### Grundstruktur
- [ ] Verantwortlicher vollständig benannt (= Impressum-Angaben)
- [ ] Datenschutzbeauftragter genannt (Name + Kontakt), falls vorhanden/pflichtgemäß
- [ ] Erstellungsdatum / "Stand: [Monat Jahr]"

### Je Verarbeitungsvorgang (Art. 13 DSGVO)
Für jede Verarbeitung (Website-Besuch, Kontaktformular, Newsletter, Shop-Bestellung, etc.):
- [ ] Welche Daten werden erhoben?
- [ ] Zweck der Verarbeitung
- [ ] Rechtsgrundlage (Art. 6 DSGVO: Einwilligung / Vertrag / rechtliche Verpflichtung / berechtigtes Interesse)
- [ ] Bei berechtigtem Interesse: Welches Interesse? Interessenabwägung erwähnen
- [ ] Empfänger der Daten (konkrete Namen oder Kategorien)
- [ ] Drittlandtransfer? (Wenn ja: Garantie = SCC / Angemessenheitsbeschluss)
- [ ] Speicherdauer (oder Kriterien für Festlegung)

### Betroffenenrechte (Art. 15-22 DSGVO)
- [ ] Auskunftsrecht (Art. 15)
- [ ] Berichtigungsrecht (Art. 16)
- [ ] Löschungsrecht (Art. 17)
- [ ] Einschränkungsrecht (Art. 18)
- [ ] Datenübertragbarkeit (Art. 20)
- [ ] Widerspruchsrecht (Art. 21) — besonders bei Direktwerbung und berechtigtem Interesse
- [ ] Recht auf menschliche Überprüfung bei automatisierten Entscheidungen (Art. 22)
- [ ] Widerrufsrecht für Einwilligungen

### Beschwerderecht
- [ ] Hinweis auf Beschwerderecht bei Aufsichtsbehörde (Art. 77)
- [ ] Zuständige Behörde nennen (nach Bundesland des Firmensitzes)

### Besondere Themen
- [ ] Cookies und Tracking → Verweis auf Cookie-Richtlinie oder Integration
- [ ] Google Analytics / Matomo / etc. → Separate Erläuterung mit Opt-Out
- [ ] YouTube / Google Maps / Social Media Einbindungen → Datenweitergabe erklären
- [ ] Newsletter → Einwilligung, Double-Opt-In, Empfänger, Abmeldemöglichkeit
- [ ] Bewerbungen → Aufbewahrungsdauer, Löschung nach Ablehnung
- [ ] Zahlungsdienstleister (PayPal, Stripe, etc.) → Datenweitergabe

---

## Checkliste 3: Cookie-Consent (§ 25 TTDSG + Art. 6 DSGVO)

### Consent-Banner / CMP (Consent Management Platform)
- [ ] Banner erscheint vor Setzen nicht-notwendiger Cookies
- [ ] "Ablehnen" ist genauso prominent wie "Akzeptieren" (nicht versteckt)
- [ ] Keine vorausgewählten Haken bei optionalen Kategorien
- [ ] Kein "Weitersurfen = Einwilligung"-Konstrukt
- [ ] Kategorien klar beschrieben (Notwendig, Statistik, Marketing, etc.)
- [ ] Granulare Ablehnung möglich (einzelne Tools ablehnen)
- [ ] Einwilligung wird dokumentiert (Zeitstempel, Version, Auswahl)
- [ ] Widerruf der Einwilligung jederzeit möglich (z.B. über Datenschutz-Einstellungen in Footer)
- [ ] Einwilligungsnachweis vorhanden (Protokollierung)

### Technisch notwendige Cookies (keine Einwilligung)
- [ ] Nur wirklich notwendige Cookies ohne Consent gesetzt
- [ ] Session-IDs, Login-Tokens, Warenkorb = OK
- [ ] CSRF-Token, Load-Balancing = OK
- [ ] Komfort-Cookies (Sprache): Grauzone — Einwilligung sicherheitshalber einholen

### Drittanbieter-Prüfung
- [ ] Alle eingebundenen Tools gelistet (Google Fonts, Analytics, Maps, Ads...)
- [ ] US-Tools: SCC geprüft? Angemessenheitsbeschluss vorhanden?
- [ ] Google Analytics 4: IP-Anonymisierung aktiviert, keine User-ID ohne Einwilligung
- [ ] Meta Pixel: Nur mit aktiver Einwilligung laden

---

## Checkliste 4: Auftragsverarbeitungsvertrag (AVV, Art. 28 DSGVO)

### Muss ein AVV abgeschlossen werden?
AVV erforderlich wenn:
- Dritter verarbeitet personenbezogene Daten **im Auftrag** des Verantwortlichen
- Der Dritte hat **keinen eigenen Zweck** — er handelt nur nach Weisung
- Typische Fälle: Cloud-Hosting, E-Mail-Dienste, Newsletter-Tools, CRM, Analytics, Support-Tools

Kein AVV nötig (Joint-Controller stattdessen):
- Beide Parteien bestimmen Zwecke und Mittel gemeinsam (→ Art. 26 DSGVO)

### Mindestinhalt des AVV (Art. 28 Abs. 3 DSGVO)
- [ ] Gegenstand der Verarbeitung
- [ ] Dauer der Verarbeitung
- [ ] Art und Zweck der Verarbeitung
- [ ] Art der personenbezogenen Daten
- [ ] Kategorien betroffener Personen
- [ ] Pflichten und Rechte des Verantwortlichen

### Inhaltliche Pflichten des Auftragsverarbeiters (vertraglich festlegen)
- [ ] Verarbeitung nur auf dokumentierte Weisung
- [ ] Vertraulichkeit (alle verarbeitenden Personen verpflichtet)
- [ ] Technische und organisatorische Maßnahmen (TOMs) nach Art. 32
- [ ] Regelung zu Sub-Auftragsverarbeitern (generelle oder spezifische Genehmigung)
- [ ] Unterstützung des Verantwortlichen bei Betroffenenrechten
- [ ] Unterstützung bei Art. 32-36 Pflichten (TOMs, DSFA, Meldepflichten)
- [ ] Löschung oder Rückgabe aller Daten nach Auftragsende
- [ ] Bereitstellung aller notwendigen Informationen zur Nachweisführung
- [ ] Auditrechte des Verantwortlichen

### Gängige Sub-Auftragsverarbeiter (häufig im SaaS-Bereich)
- Prüfe ob Cloud-Anbieter (AWS, Azure, GCP) Sub-AVV hat
- Zahlungsdienstleister mit Datenzugriff → ebenfalls AVV prüfen
- Support-Tools (Zendesk, Intercom) → Datenzugriff auf Kundendaten = AVV nötig

---

## Checkliste 5: NIS2-Compliance (ab Oktober 2024)

### Schritt 1: Betroffenheitsprüfung
- [ ] In welchem Sektor ist das Unternehmen tätig?
- [ ] Unternehmensgröße: Mitarbeiterzahl, Jahresumsatz, Jahresbilanzsumme
- [ ] Einordnung: Wesentliche Einrichtung / Wichtige Einrichtung / Nicht betroffen

### Schritt 2: Registrierung
- [ ] Beim BSI registriert (NIS2-Meldepflicht)
- [ ] Kontaktstelle benannt (24/7 erreichbar für BSI)

### Schritt 3: Risikomanagement
- [ ] Risikoanalyse für Netz- und Informationssysteme durchgeführt
- [ ] Sicherheitskonzept dokumentiert
- [ ] Mindestmaßnahmen umgesetzt:
  - [ ] Risikoanalyse und Informationssicherheitskonzept
  - [ ] Bewältigung von Sicherheitsvorfällen (Incident Response Plan)
  - [ ] Business Continuity (BCM, Backup, Notfallpläne)
  - [ ] Supply-Chain-Sicherheit (Lieferantenbewertung)
  - [ ] Sicherheit bei Erwerb, Entwicklung und Wartung
  - [ ] Policies zu Cyberhygiene und Schulungen
  - [ ] Kryptographie und Verschlüsselung
  - [ ] Personalsicherheit, Zugangskontrolle, Asset Management
  - [ ] Multi-Faktor-Authentifizierung
  - [ ] Sichere Kommunikation (verschlüsselt)

### Schritt 4: Meldeprozess
- [ ] Prozess für Erkennung erheblicher Sicherheitsvorfälle vorhanden
- [ ] 24h-Erstmeldung an BSI sichergestellt
- [ ] 72h-Folgebericht-Prozess dokumentiert
- [ ] 1-Monat-Abschlussbericht-Pflicht bekannt

### Schritt 5: Governance
- [ ] Geschäftsführung über NIS2-Pflichten informiert und geschult
- [ ] Verantwortlichkeit für IT-Sicherheit klar geregelt
- [ ] Geschäftsführung billigt Sicherheitsmaßnahmen

---

## Checkliste 6: Datenpanne — Sofortmaßnahmen

**Diese Checkliste ist zeitkritisch! Frist: 72 Stunden für Behördenmeldung (Art. 33 DSGVO)**

### Sofort (erste Stunden)
- [ ] Datenpanne identifiziert und dokumentiert (Zeitpunkt, Art, Umfang)
- [ ] Interne Meldekette aktiviert (IT-Sicherheit, Geschäftsführung, DSB)
- [ ] Zugang für Angreifer beenden / Vorfall eindämmen
- [ ] Beweise sichern (Logs, Screenshots) — ohne Manipulation!
- [ ] Erste Risikoeinschätzung: Welche Daten? Wie viele Betroffene? Welche Risiken?

### Innerhalb 24 Stunden (NIS2 für betroffene Unternehmen)
- [ ] NIS2-Erstmeldung ans BSI (falls NIS2-pflichtig)

### Innerhalb 72 Stunden (Art. 33 DSGVO)
- [ ] Risikoeinschätzung abgeschlossen
- [ ] Entscheidung: Meldung an Aufsichtsbehörde erforderlich?
  - Meldung NICHT nötig, wenn: Kein Risiko für Betroffene (z.B. verschlüsselte Daten, Verlust nicht sensitiver Infos)
  - Meldung NÖTIG, wenn: Risiko für Rechte und Freiheiten betroffener Personen
- [ ] Meldung an zuständige Datenschutzbehörde (Kontaktdaten → dsgvo.md)
- [ ] Inhalt der Meldung (Art. 33 Abs. 3):
  - [ ] Art der Verletzung
  - [ ] Kategorien und ungefähre Anzahl der Betroffenen
  - [ ] Kategorien und ungefähre Anzahl der betroffenen Datensätze
  - [ ] Name und Kontaktdaten des DSB oder sonstiger Anlaufstelle
  - [ ] Wahrscheinliche Folgen der Verletzung
  - [ ] Ergriffene oder geplante Maßnahmen

### Bei hohem Risiko: Betroffene informieren (Art. 34 DSGVO)
- [ ] Einschätzung: Voraussichtlich hohes Risiko für Betroffene?
  - Ja → Unverzügliche Benachrichtigung der Betroffenen
  - Nein → Keine Pflicht (aber dokumentieren warum)
- [ ] Inhalt der Benachrichtigung:
  - [ ] Art der Datenpanne (verständlich)
  - [ ] Kontaktdaten des DSB
  - [ ] Wahrscheinliche Folgen
  - [ ] Getroffene Maßnahmen (auch Tipps für Betroffene)

### Nacharbeitung
- [ ] Datenpannen-Register aktualisiert (Art. 33 Abs. 5 DSGVO — immer!)
- [ ] Interne Untersuchung: Wie konnte es passieren?
- [ ] Maßnahmen zur Verhinderung ähnlicher Vorfälle umgesetzt
- [ ] Kommunikation mit Anwalt über mögliche Haftungsrisiken

---

## Checkliste 7: Betroffenenanfragen bearbeiten (Art. 12-22 DSGVO)

**Frist: 1 Monat ab Eingang (verlängerbar um 2 Monate bei Komplexität)**

### Eingangsbearbeitung
- [ ] Anfrage identifiziert und als Betroffenenantrag eingestuft
- [ ] Datum des Eingangs dokumentiert
- [ ] Fristdatum berechnet (1 Monat = gleicher Tag des Folgemonats)
- [ ] Identität der anfragenden Person verifiziert (nicht übertrieben, aber angemessen)

### Art der Anfrage bestimmen
- [ ] Auskunft (Art. 15): Welche Daten? Woher? Wofür? Wie lange? Wer bekommt sie?
- [ ] Berichtigung (Art. 16): Welche Daten sollen korrigiert werden?
- [ ] Löschung (Art. 17): Gilt Ausnahme (Archivierung, Rechtsanspruch, öffentl. Interesse)?
- [ ] Einschränkung (Art. 18): Gilt bis zur Klärung eines Streits
- [ ] Datenübertragbarkeit (Art. 20): Nur bei Einwilligung oder Vertrag als Rechtsgrundlage
- [ ] Widerspruch (Art. 21): Bei berechtigtem Interesse oder Direktwerbung

### Antwort
- [ ] Innerhalb der Frist geantwortet
- [ ] Antwort unentgeltlich (Ausnahme: offensichtlich unbegründet/exzessiv)
- [ ] Kopie der Daten in strukturiertem, maschinenlesbarem Format (bei Art. 15/20)
- [ ] Ggf. Ablehnung begründet + Hinweis auf Beschwerderecht

---

## Schnell-Referenz: Zuständige Aufsichtsbehörden nach Bundesland

(Vollständige Liste mit Links → dsgvo.md)

| Firmensitz | Zuständige Behörde |
|-----------|-------------------|
| Bayern | BayLDA (private Stellen): lda.bayern.de |
| Berlin | BlnBDI: datenschutz-berlin.de |
| NRW | LDI NRW: ldi.nrw.de |
| BW | LfDI BW: datenschutz.bwl.de |
| Hamburg | HmbBfDI: datenschutz.hamburg.de |
| Hessen | HBDI: datenschutz.hessen.de |
| Sachsen | SDTB: datenschutz.sachsen.de |
| Alle anderen | → dsgvo.md für vollständige Liste |
