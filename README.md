# Company Sustainability Agent v3

AI-Agent zur Nachhaltigkeitsanalyse von Unternehmen basierend auf dem Ainsbury-Grayson 5-Stages-of-Maturity-Modell.

## Funktionsweise

Der Agent analysiert Unternehmen anhand von 11 Kategorien und bewertet sie auf einer Skala von 1-5:

| Stage | Name | Beschreibung |
|-------|------|--------------|
| 1 | Denier | Keine Anerkennung von Nachhaltigkeitsverantwortung |
| 2 | Complier | Einhaltung gesetzlicher Mindestanforderungen |
| 3 | Risk Mitigator | Aktives Risikomanagement für Nachhaltigkeitsthemen |
| 4 | Opportunity Maximiser | Systematische Nutzung von Nachhaltigkeitschancen |
| 5 | Champion | Vorreiter mit integrierter Nachhaltigkeitsstrategie |

## Die 11 Bewertungskategorien

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

## Projektstruktur

```
company-sustainability-agent/
├── .claude/
│   └── agents/
│       └── sustainability-analysis-agent.md
├── source/                    # Referenzmaterial
├── templates/                 # HTML-Report-Templates
├── input/                     # Kundenmaterial (lokal)
├── output/                    # Generierte Berichte (lokal)
├── CLAUDE.md                  # Agent-Dokumentation
└── README.md
```

## Verwendung

### Im Terminal (Claude Code CLI)

Der Agent wird als eigenständige Session im Terminal gestartet:

```bash
# Agent direkt starten
claude --agent sustainability-analysis-agent

# Oder innerhalb einer Claude Code Session
/agent sustainability-analysis-agent
```

Dann den Prompt eingeben:

```
Führe eine Nachhaltigkeitsanalyse für [Firmenname] durch.
Branche: [Branche]
```

### In der IDE (VS Code Extension)

In der VS Code Extension kann der Agent nicht direkt über das Task-Tool aufgerufen werden, da lokale Custom Agents (`.claude/agents/`) als eigenständige Sessions konzipiert sind. Der Analyse-Workflow kann aber manuell oder über den Terminal-Aufruf durchgeführt werden.

## Output

- `analyse_roh.md` - Rohdaten und Volltext
- `analyse_bericht.html` - Formatierter Bericht mit interaktivem Radar-Diagramm

### Demo-Beispiel

Ein Beispiel-Bericht für ein anonymes Musterunternehmen ist verfügbar:

**[Demo-Bericht ansehen (bericht_demo.html)](templates/bericht_demo.html)**

Dieses Demo zeigt alle Funktionen des generierten Berichts:
- Interaktives Radar-Diagramm mit allen 11 Kategorien
- Executive Summary und Unternehmensprofil
- Detailbewertung mit Konfidenz-Indikatoren
- Top 3 Stärken und Entwicklungspotenziale
- Qualitative Analyse (Strategie, Prozesse, Kommunikation)
- Branchenvergleich mit Wettbewerbern

## Akademische Grundlage

Basierend auf:
- Ainsbury, R. & Grayson, D. (2014). *The 5 Stages of Corporate Responsibility*. Doughty Centre for Corporate Responsibility, Cranfield University.

---

**Programmierung und Optimierung:** Roman Mesicek | [www.mesicek.com](https://www.mesicek.com)
