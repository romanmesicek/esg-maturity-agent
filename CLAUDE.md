# Company Sustainability Agent v3

## Project Overview

This project contains resources for building an AI agent focused on corporate sustainability assessment and analysis, combining the Ainsbury-Grayson Corporate Responsibility Maturity Model with the EU's ESRS (European Sustainability Reporting Standards) framework.

**Version:** v3
**Programmierung und Optimierung:** Roman Mesicek | [www.mesicek.com](https://www.mesicek.com)

## Source Materials Inventory

### 1. Core Framework: Ainsbury-Grayson 5 Stages of Maturity

**File:** `source/Grayson-5-Stages-of-Responsibility-2014.pdf`

Academic paper from Cranfield University's Doughty Centre for Corporate Responsibility (2014) by Ron Ainsbury and David Grayson. Defines five stages of corporate responsibility maturity:

| Stage | Name | Description |
|-------|------|-------------|
| 1 | **Denier** | No recognition of responsibility for Social, Environmental, Economic (SEE) impacts |
| 2 | **Complier** | Following laws and common business practices |
| 3 | **Risk Mitigator** | Identifying material SEE impacts, reducing negative impacts to mitigate risks |
| 4 | **Opportunity Maximiser** | Systematically seeking business opportunities from positive impacts |
| 5 | **Champion** | Embracing sustainability in value-chain, collaborating with others, advocating policy changes |

### 2. The Embedding Sustainability Model (11 Categories)

**File:** `source/Ainsbury Grayson Top-Level Categories.md`

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

### 3. ESRS Mapping

**File:** `source/ESRS Implementation Guidance for Ainsbury-Grayson Indicators.md`

Maps each of the 11 Ainsbury-Grayson categories to specific ESRS disclosure requirements:

- **ESRS 2** - General disclosures (SBM-1, SBM-2, SBM-3, GOV-1 through GOV-5, IRO-1, MDR-M, MDR-T)
- **ESRS S1** - Own workforce
- **ESRS G1** - Business conduct (G1-1 through G1-5)
- Cross-cutting environmental and social requirements

### 4. Framework Integration Analysis

**File:** `source/Mapping between Maturity Stages and ESRS Framework.md`

Key insights:
- **ESRS** provides the "what" (reporting requirements)
- **Maturity Model** provides the "how" (development journey)
- ESRS requirements can serve as indicators for assessing maturity stage
- Maturity stage indicates readiness for ESRS compliance

Stage-to-ESRS mapping:
- Stage 1 (Denier): Fails basic ESRS requirements
- Stage 2 (Complier): Meets minimum disclosure requirements
- Stage 3 (Risk Mitigator): Comprehensive reporting, established governance
- Stage 4 (Opportunity Maximiser): Full compliance with detailed disclosures
- Stage 5 (Champion): Exceeds requirements, industry-leading disclosures

### 5. Assessment Template (Excel)

**File:** `source/AinsburyGrayson_StageOfMaturity.xlsx`

German-language assessment template with two sheets:

**Sheet "Bewertung" (Assessment):**

Quantitative rating section (1-5 scale matching the 5 maturity stages):
| Scale Value | Stage |
|-------------|-------|
| 1 | Denier |
| 2 | Complier |
| 3 | Risk Mitigator |
| 4 | Opportunity Maximiser |
| 5 | Champion |

11 Categories to rate:
1. Purpose, Vision, Values & Strategy
2. Tone from the Top: Leadership
3. Tone from the Top: Board Oversight and Governance
4. Key Targets Incentives and Measurement
5. Embedded in Strategic Business Units and Functions
6. Everybody's Business: Engaging Employees
7. Everybody's Business: Energising the Value Chain
8. Skills, Knowledge Management and Training
9. Stakeholder Engagement, Communications, including to investors
10. Collaborations, Partnerships and Sustainability Networks
11. Specialist CR Function

Qualitative assessment sections (Strengths/Weaknesses - "Stärken/Schwächen"):
- **Strategie** (Strategy): Future orientation, addressing challenges
- **Prozesse** (Processes): Management systems, standards
- **Kommunikation** (Communication): Reporting, website

**Sheet "Diagramm" (Diagram):**
Empty template - intended for radar/spider chart visualization of assessment results.

### 6. Ainsbury-Grayson Komplettreferenz

**File:** `source/ainsbury_grayson_referenz.md`

Umfassende deutschsprachige Referenzdokumentation des Frameworks mit:
- Theoretischer Hintergrund und akademische Einordnung
- Die 5 Reifegradstufen im Detail
- Die 11 Embedding-Kategorien
- **APPENDIX 1:** Detaillierte Stufenmatrix für alle 11 Kategorien (A1.1-A1.11)
- **APPENDIX 2:** Funktionale Bereiche - Operations, Marketing, Finance, HR, R&D, External Affairs (A2.1-A2.6)
- **APPENDIX 3:** Dunphy's Höchste Reifegradstufen (Vergleichsmodell)

### 7. Customer Analysis Template (German)

**File:** `source/Vorlage Kunden Analyse Prompt.md`

Sales briefing template for company/person research including:
- Company overview and positioning
- Financial data and market analysis
- Target person profiling
- SWOT analysis
- Conversation preparation (openers, trigger questions, objection handling)

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

### ESRS Compliance Pathways

Companies at different maturity stages have different pathways to ESRS compliance:
- Lower stages: Focus on basic compliance requirements
- Higher stages: Comprehensive integration and continuous improvement

## Project Structure

```
company-sustainability-agent/
├── .claude/
│   ├── agents/
│   │   └── sustainability-analysis-agent.md # Hauptagent für Nachhaltigkeitsanalyse v3
│   └── settings.json                        # Auto-Approval Konfiguration
├── source/                                  # Referenzmaterial
│   ├── Grayson-5-Stages-of-Responsibility-2014.pdf
│   ├── ainsbury_grayson_referenz.md         # Komplettreferenz mit Appendices
│   ├── Ainsbury Grayson Top-Level Categories.md
│   ├── ESRS Implementation Guidance for Ainsbury-Grayson Indicators.md
│   ├── Mapping between Maturity Stages and ESRS Framework.md
│   ├── AinsburyGrayson_StageOfMaturity.xlsx
│   ├── Vorlage Kunden Analyse Prompt.md
│   └── templates/
│       └── bericht_template.html            # HTML-Template v3 mit Radar-Diagramm
├── input/                                   # Kundenmaterial für Analysen
│   └── README.md                            # Anleitung für Input-Materialien
├── output/                                  # Generierte Analyseberichte
└── CLAUDE.md                                # Diese Dokumentation
```

## Sustainability Analysis Agent v3

### Aufruf
Der Agent wird über das Task-Tool mit `subagent_type="sustainability-analysis-agent"` aufgerufen.

Beispiel-Prompt:
```
Führe eine Nachhaltigkeitsanalyse für [Firmenname] durch.
Branche: [Branche]
Fokus: [optional: spezifische Schwerpunkte]
```

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

**Hinweis:** Ergebnisordner enthalten keine Versionsnummer im Namen.

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
