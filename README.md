# ESG Maturity Agent

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
esg-maturity-agent/
├── .claude/
│   └── agents/
│       └── esg-maturity-agent.md
├── source/                    # Referenzmaterial
├── templates/                 # HTML-Report-Templates
├── input/                     # Kundenmaterial (lokal)
├── output/                    # Generierte Berichte (lokal)
├── CLAUDE.md                  # Agent-Dokumentation
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
