# Technical Review — DAX & Data Visualization

## Review status

**Status: PBIX inspection required.**

This document records what can be verified from the repository and provides a reproducible checklist for completing a technical review. It deliberately does not invent report pages, table names, DAX measures, KPI values, or business findings that have not been confirmed from the PBIX in Power BI Desktop.

## Verified repository contents

| Artifact | Verified purpose |
|---|---|
| Power BI Assignment – DAX & Data Visualization.pbix | Editable Power BI report and data model |
| images/project-overview.svg | Static overview graphic; not a Power BI screenshot |
| README.md | Project entry point and instructions |

The repository does not currently include a source dataset, exported report screenshots, a DAX source listing, or a separate validated findings report.

## Technical review workflow

Open the PBIX in Power BI Desktop and record the following information before publishing findings.

### 1. Data model

- Record every table name and its role.
- Identify the source file or database for each table.
- Record the row count and key columns for each table.
- Inspect relationships: from-table, to-table, cardinality, cross-filter direction, and active/inactive status.
- Check whether dimension tables filter fact tables in the intended direction.
- Confirm that key columns have the correct data type and that relationship keys are unique on the one side.

### 2. DAX measures

For each measure, document:

| Field | What to record |
|---|---|
| Measure name | Exact name shown in the Fields/Data pane |
| DAX expression | Copy the exact formula from the formula bar |
| Business meaning | What the measure is intended to calculate |
| Filter context | How slicers, filters, and row/column context affect it |
| Validation | Recalculate the result independently or compare with a known total |
| Format | Currency, percentage, whole number, decimal, or date as applicable |

Check for common DAX issues:

- Measures that use SUM where a distinct count is needed.
- Incorrect use of COUNT versus COUNTROWS or DISTINCTCOUNT.
- Ratios with missing zero-denominator handling.
- Unintended filter removal through ALL or REMOVEFILTERS.
- Incorrect row context or missing context transition with CALCULATE.
- Measures that return misleading totals when evaluated at a different grouping level.
- Hard-coded assumptions that should be parameters or documented inputs.

### 3. Report visuals

For every report page, record:

- Page name and business question.
- Visual type and the fields/measures used.
- Slicers and their interactions.
- Drill-through, tooltip, bookmark, or navigation behaviour, if present.
- Accessibility: meaningful titles, readable labels, contrast, and alternative text.
- Whether totals and filters reconcile to the underlying data.

### 4. Validation and evidence

Before describing a finding as verified:

1. Refresh the report or record why refresh was not performed.
2. Check Power Query steps and resolve any source-path errors.
3. Reconcile headline values to source data or an independent calculation.
4. Test slicers and cross-highlighting.
5. Capture genuine screenshots from Power BI Desktop.

Recommended screenshot names:

- report-overview.png
- data-model.png
- dax-measures.png
- key-analysis-page.png

Save verified screenshots in a screenshots folder and reference them from the README. Do not replace genuine report captures with the overview SVG.

## Current limitations

- Exact table and column names have not been confirmed from the PBIX.
- DAX expressions and measure values have not been independently inspected.
- Report page names and visual interactions have not been verified.
- The source dataset is not included in the visible repository tree.
- No Power BI Desktop screenshots are currently included.

## What is required to complete this review

Open the PBIX in Power BI Desktop, complete the checklist above, and add the exact model details, DAX expressions, independently checked results, and genuine screenshots. Until that is done, the PBIX should be treated as the primary assignment artifact, not as an independently validated analytical case study.
