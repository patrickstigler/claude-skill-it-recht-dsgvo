# Anwalt DE — Deutsches IT-Recht & DSGVO Skill für Claude

Ein Claude Skill für rechtliche Ersteinschätzungen im deutschen IT-Recht und Datenschutzrecht (DSGVO/BDSG). Der Skill unterstützt Entwickler, Unternehmer und Einzelpersonen dabei, rechtliche Sachverhalte zu verstehen und sich auf das Gespräch mit einem Rechtsanwalt vorzubereiten.

[![Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/W7W51C9X4H)

> **Wichtig:** Dieser Skill ersetzt keine anwaltliche Beratung. Er dient ausschließlich der allgemeinen Information und Orientierung.

---

## Fachgebiete

- **DSGVO & Datenschutzrecht** — Datenpannen, Betroffenenrechte, AVV, Einwilligung, Drittlandtransfer, Bußgelder
- **IT-Sicherheitsrecht** — NIS2, BSIG, Meldepflichten, KRITIS
- **Telemedienrecht** — Impressumspflicht (DDG/TMG), DSA, Plattformhaftung
- **IT-Vertragsrecht** — SaaS, Software-Kauf/-Miete, Werkverträge, AGB-Prüfung
- **Urheberrecht** — Software-Schutz, Open Source Lizenzen, Arbeitnehmerurheberrecht
- **Wettbewerbsrecht** — Abmahnungen, UWG, Cookie-Consent
- **KI-Recht** — EU AI Act, Risikoklassen, Zeitplan

---

## Struktur

```
anwalt-de/
├── Skill.md                    # Hauptskill (YAML-Frontmatter, siehe unten)
├── README.md                   # Diese Datei
└── references/
    ├── dsgvo.md                # DSGVO-Artikel, Bußgelder, Aufsichtsbehörden, SCC
    ├── it-recht.md             # IT-Gesetze, NIS2, Urheberrecht, AI Act, Impressum
    ├── vertragsrecht.md        # BGB, AGB-Recht, Vertragstypen, Gewährleistung
    └── checklisten.md          # Prüflisten: Impressum, DSE, Cookie, AVV, Datenpanne
```

### Referenz-System

Der Skill nutzt Progressive Disclosure — referenzierte Dateien werden nur bei Bedarf geladen:

| Referenz | Wann geladen |
|----------|-------------|
| `references/dsgvo.md` | DSGVO-Fragen, Datenpannen, Betroffenenrechte, AVV, Cookies |
| `references/it-recht.md` | IT-Verträge, Impressum, NIS2, Urheberrecht, KI-Recht |
| `references/vertragsrecht.md` | AGB, Softwareverträge, BGB, Kündigung, Gewährleistung |
| `references/checklisten.md` | Dokumentenprüfung, Compliance-Checks, Datenpannen |

---

## Installation

Voraussetzungen für **Custom Skills** in Claude (Web/App): Siehe [How to create custom Skills](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills) — u. a. **Codeausführung aktiviert**, Datei **`Skill.md`** (nicht `SKILL.md`), Ordnername entspricht dem Feld **`name`** im Frontmatter (`anwalt-de`).

### Als Claude Code Skill

```bash
# Repository klonen — Zielordner muss anwalt-de heißen (wie name im Skill)
git clone https://github.com/DEIN-USER/anwalt-de.git ~/.claude/skills/anwalt-de

# Oder: Repo unter anderem Namen geklont → umbenennen
mv claude-skill-it-recht-dsgvo ~/.claude/skills/anwalt-de
```

### In `.claude/settings.json` eintragen (optional)

Claude erkennt Skills automatisch aus dem Skills-Verzeichnis.

### Als ZIP für Claude (Desktop / „Skill installieren“)

Die ZIP muss **einen Ordner** als Wurzel haben — nicht lose Dateien ([Packaging](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills)):

```bash
# Aus dem Elternverzeichnis (Ordner heißt anwalt-de und enthält Skill.md)
zip -r anwalt-de.skill anwalt-de/
```

Wenn das Repo lokal noch `claude-skill-it-recht-dsgvo` heißt: zuerst nach `anwalt-de` kopieren oder umbenennen, dann wie oben packen.

Anschließend in Claude **Customize → Skills** die Datei hochladen bzw. den Skill aktivieren und mit Testprompts prüfen, ob er geladen wird.

### Frontmatter-Hinweis

| Feld | Grenze | Hinweis |
|------|--------|--------|
| `description` | max. 200 Zeichen | Wird von Claude zum automatischen Aktivieren genutzt; längere Texte können die Installation blockieren |
| `name` | max. 64 Zeichen | Sollte zum Ordnernamen passen |

---

## Verwendung

### Automatische Aktivierung

Der Skill aktiviert sich automatisch bei Anfragen wie:

- *"Brauche ich eine Einwilligung für diese Verarbeitung?"*
- *"Wir hatten eine Datenpanne — was müssen wir jetzt tun?"*
- *"Ist unser Impressum vollständig?"*
- *"Prüf mal unsere AGB auf unwirksame Klauseln"*
- *"Muss ich einen AVV mit meinem Cloud-Anbieter abschließen?"*
- *"Was bedeutet NIS2 für unser Unternehmen?"*
- *"Kann ich Google Analytics ohne Consent nutzen?"*
- *"Wir bekommen eine Abmahnung — was tun?"*
- *"Welche Rechte haben DSGVO-Auskunftsanfragen?"*

### Manuelle Aktivierung

```
/anwalt-de [deine Frage]
```

### Dokumente hochladen

Lade Verträge, AGB, Datenschutzerklärungen oder Behördenbescheide hoch — der Skill analysiert sie direkt.

---

## Beispiel-Ausgabe

```
# Rechtliche Ersteinschätzung: Cookie-Tracking ohne Einwilligung

> ⚠️ Keine Rechtsberatung — nur allgemeine Erstorientierung

## Sachverhalt
Das Unternehmen setzt Google Analytics 4 ein, ohne eine Einwilligung der Websitebesucher
einzuholen. Betroffene Verarbeitung umfasst pseudonyme Nutzungsprofile auf US-Servern.

## Rechtliche Einordnung
- § 25 Abs. 1 TTDSG: Zugriff auf Endgerätedaten (Cookies/JS-Tags) erfordert Einwilligung
- Art. 6 Abs. 1 lit. a DSGVO: Einwilligung als Rechtsgrundlage für Profiling
- Art. 44-46 DSGVO: Drittlandtransfer in USA erfordert Garantien (SCC + TIA)

## Risikoanalyse
| Risiko | Schwere | Wahrscheinlichkeit | Rechtsgrundlage |
|--------|---------|--------------------|-----------------|
| Bußgeld Aufsichtsbehörde | 🟡 Mittel | Mittel | Art. 83 DSGVO |
| UWG-Abmahnung durch Mitbewerber | 🟡 Mittel | Hoch | § 3a UWG |
| Abmahnung durch Verbraucherschutzverband | 🟡 Mittel | Mittel | UKlaG |

## Handlungsempfehlungen
1. **Sofort**: Google Analytics bis zur Implementierung eines gültigen Consents deaktivieren
2. **Kurzfristig**: CMP (Consent Management Platform) implementieren
3. **Mittelfristig**: SCC mit Google prüfen, TIA durchführen

## Empfohlene nächste Schritte
→ Fachanwalt für IT-Recht / Datenschutzrecht konsultieren für rechtssichere CMP-Konfiguration
```

---

## Rechtlicher Hinweis

Dieser Skill und alle darin enthaltenen Informationen sind **keine Rechtsberatung** im Sinne des Rechtsdienstleistungsgesetzes (RDG). Die Nutzung dieses Skills begründet kein Mandatsverhältnis.

Die Inhalte dienen ausschließlich der allgemeinen Information und ersetzen keine auf den Einzelfall bezogene rechtliche Beratung durch einen zugelassenen Rechtsanwalt. Für verbindliche Rechtsauskünfte wenden Sie sich an einen Fachanwalt für IT-Recht oder Datenschutzrecht.

Rechtsstand der Referenzinformationen: **April 2026** (DSGVO, BDSG, TTDSG, DDG, NIS2, EU AI Act)

---

## Inspiration & Quellen

- Strukturell inspiriert von [claude-legal-skill](https://github.com/evolsb/claude-legal-skill) (US-Recht)
- Prompt-Struktur angelehnt an [Fabric Patterns](https://github.com/danielmiessler/Fabric)
- Rechtliche Quellen: [gesetze-im-internet.de](https://www.gesetze-im-internet.de), [EUR-Lex](https://eur-lex.europa.eu), [BfDI](https://www.bfdi.bund.de), [BSI](https://www.bsi.bund.de)

---

## Mitwirken

Pull Requests für folgende Bereiche willkommen:
- Neue Rechtsgebiete (Arbeitsrecht, Markenrecht, Verbraucherrecht...)
- Aktuelle Gesetzesänderungen und EuGH-Urteile
- Weitere Checklisten
- Verbesserungen am Analyse-Workflow

---

## Lizenz

**MIT + Commons Clause**

Der Skill steht unter der MIT-Lizenz mit einem Commons Clause Zusatz. Das bedeutet:

| Was | Erlaubt? |
|-----|---------|
| Eigenes Unternehmen / eigenes Projekt | ✅ Ja |
| Anpassen und erweitern | ✅ Ja |
| Community-Beiträge (Forks, PRs) | ✅ Ja |
| Weitergabe mit Attribution | ✅ Ja |
| Als kostenpflichtiger Dienst verkaufen | ❌ Nein |
| Als "AI-Rechtsberatungs-Service" vermarkten | ❌ Nein |

Der vollständige Lizenztext ist in [LICENSE](./LICENSE) zu finden.
