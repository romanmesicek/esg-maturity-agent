# ESG Maturity Agent

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

AI-Agent zur Nachhaltigkeitsanalyse von Unternehmen basierend auf dem Ainsbury-Grayson 5-Stages-of-Maturity-Modell.

Der Agent führt automatisierte Web-Recherche durch, bewertet Unternehmen anhand von 11 Kategorien und generiert umfassende HTML-Berichte mit interaktiven Radar-Diagrammen. Eine wissenschaftlich fundierte **Communication Bias Adjustierung** korrigiert systematische positive Verzerrungen in der Unternehmenskommunikation.

## Funktionsweise

**Was der Agent macht:**

1. Recherchiert automatisch Nachhaltigkeitsinformationen aus Web-Quellen, Berichten und Pressemeldungen
2. Überprüft die Rechercheergebnisse auf einen positiven Kommunikations-Bias und anhand von Greenwashing-Kriterien und gewichtet diese entsprechend
3. Bewertet Unternehmen systematisch in 11 Embedding-Kategorien auf einer ordinalen Skala von 1 (Denier) bis 5 (Champion)
4. Weist jeder Bewertung ein Konfidenz-Level zu, das angibt, wie verlässlich die Einschätzung ist
5. Generiert interaktive HTML-Berichte mit Radar-Diagrammen

### Die 5 Reifegradstufen

| Stage | Name | Beschreibung |
|-------|------|--------------|
| 1 | Denier | Keine Anerkennung von Nachhaltigkeitsverantwortung |
| 2 | Complier | Einhaltung gesetzlicher Mindestanforderungen |
| 3 | Risk Mitigator | Aktives Risikomanagement für Nachhaltigkeitsthemen |
| 4 | Opportunity Maximiser | Systematische Nutzung von Nachhaltigkeitschancen |
| 5 | Champion | Vorreiter mit integrierter Nachhaltigkeitsstrategie |

### Die 11 Embedding-Kategorien

1. Purpose, Vision, Values & Strategy
2. Tone from the Top: Leadership
3. Tone from the Top: Board Oversight and Governance
4. Key Targets, Incentives and Measurement
5. Embedded in Strategic Business Units and Functions
6. Everybody's Business: Engaging Employees
7. Everybody's Business: Energising the Value Chain
8. Skills, Knowledge Management and Training
9. Stakeholder Engagement, Communications
10. Collaborations, Partnerships and Sustainability Networks
11. Specialist CR Function

### Konfidenz-System

Jede Bewertung enthält eine Konfidenz-Markierung, die angibt, wie verlässlich die Einschätzung ist:

- **Hoch** = mehrere klare Evidenzquellen
- **Mittel** = einige Evidenz vorhanden
- **Niedrig** = Bewertung basiert auf Inferenz

## Communication Bias Adjustierung

Forschung zeigt systematische positive Verzerrung in Unternehmenskommunikation:
- 94% der Investoren glauben, dass Nachhaltigkeitsberichte unbelegte Behauptungen enthalten (PwC, 2023)
- 42-53% der Umweltaussagen sind vage, irreführend oder unbegründet (EU-Kommission, 2020)
- Selbstberichtete Emissionen sind typischerweise 10-14% niedriger als extern verifizierte Werte (MIT Sloan, 2024)

Der Agent wendet daher eine transparente Bias-Adjustierung an:

| Faktor | Adjustment |
|--------|------------|
| Keine externe Prüfung | -0.5 Punkte |
| Limited Assurance | -0.25 Punkte |
| Je identifiziertem Red Flag | -0.25 Punkte |

**Red Flags:** Vage Ziele, Disclosure-Performance Gap, übermäßig positive Sprache, fehlende Scope 3 Daten, Net-Zero ohne Pfad, inkonsistente Aussagen, fehlende Negativberichterstattung, überwiegend Absichtserklärungen.

## Projektstruktur

```
esg-maturity-agent/
├── .claude/
│   └── agents/
│       └── esg-maturity-agent.md   # Agent-Definition
├── skills/
│   └── esg-maturity/               # Skill für Claude Code
│       ├── SKILL.md
│       └── references/
├── source/                         # Referenzmaterial (lokal)
├── templates/                      # HTML-Report-Templates
├── input/                          # Kundenmaterial (lokal)
├── output/                         # Generierte Berichte (lokal)
├── CLAUDE.md                       # Detaillierte Dokumentation
├── LICENSE                         # MIT License
└── README.md
```

## Verwendung

### Option 1: Eigenständige Session (Terminal)

```bash
claude --agent esg-maturity-agent
```

Dann den Prompt eingeben:
```
Führe eine Nachhaltigkeitsanalyse für [Firmenname] durch.
Branche: [Branche]
```

### Option 2: Innerhalb einer Claude Code Session

Einfach den gewünschten Task beschreiben - Claude Code delegiert automatisch an den Agent:

```
Führe eine Nachhaltigkeitsanalyse für [Firmenname] durch.
```

> **Hinweis:** Der `/agent` Befehl funktioniert nur zum Starten neuer Sessions im Terminal, nicht innerhalb einer laufenden Session.

## Output

Der Agent generiert in `output/[firmenname]_[datum]/`:

- `[firmenname]_analyse_roh.md` - Rohdaten, Rechercheergebnisse und quantitative Bias-Analyse
- `[firmenname]_greenwashing_screening.md` - Separates Greenwashing-Screening mit Red Flag-Analyse
- `[firmenname]_analyse_bericht.html` - Formatierter Bericht mit interaktivem Radar-Diagramm

### Demo-Beispiel

Ein Beispiel-Bericht für ein anonymes Musterunternehmen ist verfügbar:

**[Live-Demo ansehen](https://romanmesicek.github.io/esg-maturity-agent/templates/bericht_demo.html)**

Dieses Demo zeigt alle Funktionen des generierten Berichts:
- Interaktives Radar-Diagramm mit allen 11 Kategorien
- Executive Summary und Unternehmensprofil
- Detailbewertung mit Konfidenz-Indikatoren
- Top 3 Stärken und Entwicklungspotenziale
- Branchenvergleich mit Wettbewerbern

## Akademische Grundlage

- Ainsbury, R. & Grayson, D. (2014). *Business Critical: Understanding a Company's Current and Desired Stages of Corporate Responsibility Maturity*. Doughty Centre for Corporate Responsibility, Cranfield University.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

You are free to use, modify, and distribute this software for any purpose, including commercial applications.

---

**Entwicklung:** Roman Mesicek | [www.mesicek.com](https://www.mesicek.com)
