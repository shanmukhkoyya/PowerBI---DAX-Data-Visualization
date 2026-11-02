<div align="center"><h1>⚡ DAX & POWER BI — TECHNICAL HAND-OFF</h1><b>Focused report-file review</b><img src="https://img.shields.io/badge/Power%20BI-PBIX-F2C811?logo=powerbi"/> <img src="https://img.shields.io/badge/DAX-MEASURES-4479A1"/></div>

## Report asset card
| Main file | Supporting material |
|---|---|
| [Power BI report](PowerBI%20DAX%20Data%20Visualization.pbix) | [Technical review](docs/TECHNICAL_REVIEW.md) |
| [Project overview SVG](images/project-overview.svg) | Concept illustration |

## Inspection route
<p align="center">📁 PBIX → 🧱 MODEL → 🧮 MEASURES → 🎛️ FILTERS → 📊 VISUALS → ✔️ VALIDATION</p>

## Technical review matrix
| Area | Reviewer question |
|---|---|
| Measure logic | Are aggregations and filter context correct? |
| Relationships | Do dimensions filter intended fact tables? |
| Time logic | Is the date table valid? |
| Formatting | Are units and percentages consistent? |
| Interaction | Do slicers behave as expected? |

> Evidence limitation: The SVG is conceptual. No verified screenshot gallery or complete DAX inventory is currently documented. Inspect the PBIX before making claims about specific measures or interactions.

## Reviewer checklist
- [ ] Inventory measures and definitions.
- [ ] Check relationship cardinality.
- [ ] Reconcile headline values to source data.
- [ ] Test blank, zero and multi-select cases.
- [ ] Capture genuine report screenshots.