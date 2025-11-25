# BNR Statistical Analysis Plan – Hospital Cardiovascular Cases in Barbados (2023)  

**Version:** 1.0<br/>
**Date:** 11 November 2025  
**Linked Core Document:** [BNR Core SAP](./bnr-sap-core.md)  
**Linked DO File:** `bnrcvd-2023-count.do`  
**Prepared by:** Ian Hambleton for the BNR Analytics Team  

---

## 1. Purpose
This briefing summarises *hospital-registered* cardiovascular disease (CVD) events in Barbados for **2023**, focusing on **strokes** and **acute myocardial infarctions (AMI)**. We compare 2023 weekly counts with the five-year baseline (2018–2022) to show deviations from recent hospital activity. All analyses are based on confirmed hospital events from the BNR-CVD database.

---

## 2. Analysis Scope
| Aspect | Specification |
|---------|---------------|
| **Index year** | 2023 |
| **Baseline period** | 2018 – 2022 |
| **Events included** | Hospital-confirmed stroke and acute MI |
| **Population** | Barbados residents (≥ 6 months of the previous 12 months) |
| **Data source** | `bnr-cvd-count-${today}-prep1.dta` (interim dataset prepared upstream) |
| **Unit of analysis** | Events (not persons) |
| **Exclusions** | DCO-only cases, non-residents, duplicates |
| **Output granularity** | Weekly summaries by sex and event type |
| **Objective** | Compare 2023 weekly CVD counts with the five-year baseline mean |

---

## 3. Analytic Workflow
Analysis is executed in **Stata 18** through `bnrcvd-2023-count.do`.  
The script follows five broad phases:

1. **Dataset assembly** – as needed, combine validated registry data for 2018–2023 and apply standard filters for hospital-confirmed events.  
2. **Variable setup** – create basic time, age and event flags required for trend and sub-group analysis.  
3. **Descriptive summaries** – generate totals and percentages for 2023 and for the five-year baseline.  
4. **Figure production** – build and export two standard graphics (weekly cumulative comparison and age/sex composition).  
5. **Automated report creation** – assemble the briefing PDF using `putpdf`, embedding the two figures and core text elements.  

The script also generates a Stata log and metadata (YAML) file to document execution.

---

## 4. Outputs
The `.do` file produces the following artefacts (exact paths/macros appear in the code):

| Artefact | Creation method |
|-----------|----------------|
| `${graphs}/bnrcvd-count-figure1.png` | Export of Figure 1 (cumulative 2023 vs five-year average) |
| `${graphs}/bnrcvd-count-figure1.dta` | Saved plotting dataset for Figure 1 |
| `${graphs}/bnrcvd-count-figure1.xlsx` | Excel version of Figure 1 data |
| `${graphs}/bnrcvd-count-figure2.png` | Export of Figure 2 (age/sex comparison graphic) |
| `${outputs}/bnr-cvd-count-${today}.pdf` | Final PDF report assembled with `putpdf save` |
| *(Metadata)* | YAML file written by `bnryaml using ...` alongside the Figure 1 dataset |

---

## 5. Limitations
- Hospital events only – community and private-sector cases are not-represented.  
- Fixed 52-week calendar may introduce minor end-of-year boundary effects.  
- Late 2023 abstractions will enter dataset v2024.1.  

---

## 6. Change Log
| Version | Date | Summary | Author |
|----------|------|----------|--------|
| 1.0 | 11 Nov 2025 | Initial SAP under modular framework | Ian Hambleton for the BNR Analytics Team |

---
