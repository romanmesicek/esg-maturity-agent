# ESG Maturity Agent

## Project Overview

This project contains resources for building an AI agent focused on corporate sustainability assessment and analysis, combining the Ainsbury-Grayson Corporate Responsibility Maturity Model with the EU's ESRS (European Sustainability Reporting Standards) framework.

**Version:** v3
**Programmierung und Optimierung:** Roman Mesicek | [www.mesicek.com](https://www.mesicek.com)

## Source Materials

### 1. Ainsbury-Grayson Komplettreferenz

**File:** `source/ainsbury_grayson_referenz.md`

Umfassende deutschsprachige Referenzdokumentation des Frameworks mit:
- Theoretischer Hintergrund und akademische Einordnung
- Die 5 Reifegradstufen im Detail
- Die 11 Embedding-Kategorien
- **APPENDIX 1:** Detaillierte Stufenmatrix für alle 11 Kategorien (A1.1-A1.11)
- **APPENDIX 2:** Funktionale Bereiche - Operations, Marketing, Finance, HR, R&D, External Affairs (A2.1-A2.6)
- **APPENDIX 3:** Dunphy's Höchste Reifegradstufen (Vergleichsmodell)

### 2. The Embedding Sustainability Model (11 Categories)

**File:** `source/ainsbury_grayson_top-level_categories.md`

The "Bulls-eye" or "Target" model with interconnected elements:

**Core Vision:**
1. Purpose, Vision, Values & Strategy

**Strategic Layer:**
2. Tone from the Top: Leadership
3. Tone from the Top: Board Oversight and Governance
4. Key Targets, Incentives and Measurement
5. Embedded in Strategic Business Units and Functions
6. Everybody's Business: Engaging Employees
7. Everybody's Business: Energise the Value Chain

**Operational Enablers:**
8. Skills, Knowledge Management and Training
9. Stakeholder Engagement, Communications (including investors)
10. Collaborations, Partnerships and Sustainability Networks
11. Specialist Corporate Responsibility/Sustainability Function

## The 5 Stages of Maturity

| Stage | Name | Description |
|-------|------|-------------|
| 1 | **Denier** | No recognition of responsibility for Social, Environmental, Economic (SEE) impacts |
| 2 | **Complier** | Following laws and common business practices |
| 3 | **Risk Mitigator** | Identifying material SEE impacts, reducing negative impacts to mitigate risks |
| 4 | **Opportunity Maximiser** | Systematically seeking business opportunities from positive impacts |
| 5 | **Champion** | Embracing sustainability in value-chain, collaborating with others, advocating policy changes |

## Key Concepts for Agent Development

### Assessment Dimensions

For each of the 11 categories, companies can be evaluated across:
- **Mindset**: Time-horizon, focus, outlook, transparency, collaboration approach
- **Purpose, Strategy, Organization, Policies & Practices**: Formal structures and processes
- **Performance**: Actual results and outcomes

### Maturity Indicators

The model provides specific indicators for what each stage looks like across:
- Strategy integration
- Leadership behavior
- Board governance
- Target-setting and measurement
- Business unit embedding
- Employee engagement
- Value chain activation
- Knowledge management
- Stakeholder communications
- External collaborations
- Specialist function role

## Project Structure

```
esg-maturity-agent/
├── .claude/
│   ├── agents/
│   │   └── esg-maturity-agent.md            # Hauptagent für Nachhaltigkeitsanalyse
│   └── settings.json                        # Auto-Approval Konfiguration
├── source/                                  # Referenzmaterial
│   ├── ainsbury_grayson_referenz.md         # Komplettreferenz mit Appendices
│   └── ainsbury_grayson_top-level_categories.md
├── templates/                               # HTML-Report-Templates
│   ├── bericht_template.html                # HTML-Template mit Radar-Diagramm
│   └── bericht_demo.html                    # Demo-Bericht (Muster GmbH)
├── input/                                   # Kundenmaterial für Analysen
│   └── README.md                            # Anleitung für Input-Materialien
├── output/                                  # Generierte Analyseberichte
│   └── README.md
└── CLAUDE.md                                # Diese Dokumentation
```

## Sustainability Analysis Agent

### Aufruf

**Option 1: Eigenständige Session (Terminal)**
```bash
claude --agent esg-maturity-agent
```

**Option 2: Innerhalb einer Claude Code Session**
Einfach den gewünschten Task beschreiben - Claude Code delegiert automatisch an den Agent:
```
Führe eine Nachhaltigkeitsanalyse für [Firmenname] durch.
Branche: [Branche]
Fokus: [optional: spezifische Schwerpunkte]
```

> **Hinweis:** Der `/agent` Befehl funktioniert nur zum Starten neuer Sessions, nicht innerhalb einer laufenden Session. Innerhalb einer Session wird der Agent automatisch basierend auf seiner Beschreibung verwendet.

### Workflow (5 Phasen)

1. **Input & Kontext**: Firmenname, Branche erfassen; Input-Ordner prüfen
2. **Web-Recherche**: Website, Nachhaltigkeitsberichte, ESG-Ratings, Pressemeldungen
3. **Ainsbury-Grayson Bewertung**: 11 Kategorien mit 1-5 Skala, Konfidenz-Markierung
4. **Qualitative Analyse**: Stärken/Schwächen für Strategie, Prozesse, Kommunikation
5. **Output-Generierung**: Markdown + HTML-Bericht mit Radar-Diagramm

### Output

Der Agent generiert in `output/[firmenname]_[datum]/`:
- `analyse_roh.md` - Rohdaten und Volltext
- `analyse_bericht.html` - Formatierter Bericht mit interaktivem Radar-Diagramm

### Konfidenz-System

Jede Kategoriebewertung enthält eine Konfidenz-Markierung:
- **[Hoch]**: Mehrere klare Evidenzquellen
- **[Mittel]**: Einige Evidenz, nicht vollständig verifizierbar
- **[Niedrig]**: Wenig direkte Evidenz, Bewertung basiert auf Inferenz

## Input-Ordner

Für jede Analyse können Kundenmaterialien in `input/[firmenname]/` bereitgestellt werden:
- Nachhaltigkeitsberichte (PDF)
- Geschäftsberichte (PDF)
- Pressemitteilungen
- Weitere relevante Dokumente

Siehe `input/README.md` für detaillierte Anleitung.

## Output Directory

`output/` - Directory for generated analysis reports and assessments
