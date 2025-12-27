# Templates

HTML-Templates für die Generierung von Analyseberichten.

## Dateien

### bericht_template.html

Haupttemplate für den Nachhaltigkeitsbericht mit:

- Responsive Layout
- Interaktives Radar-Diagramm (Chart.js)
- Farbcodierung nach Maturity Stage (1=rot bis 5=grün)
- Druckoptimiert
- Detailtabellen für alle 11 Kategorien
- Branchenvergleichs-Sektion

### Platzhalter

Das Template verwendet folgende Platzhalter:

| Platzhalter | Beschreibung |
|-------------|--------------|
| `{{FIRMENNAME}}` | Name des analysierten Unternehmens |
| `{{DATUM}}` | Analysedatum |
| `{{ANZAHL_QUELLEN}}` | Anzahl der verwendeten Quellen |
| `{{EXECUTIVE_SUMMARY}}` | Zusammenfassung |
| `{{RADAR_SCORES}}` | Komma-separierte Scores für Radar-Chart |
| `{{DETAIL_ROWS}}` | HTML-Zeilen für Detailtabelle |
| `{{QUELLEN_LISTE}}` | HTML-Liste der Quellen |

---

**Version:** v3
