# BNR Statistical Analysis Plan – Hospital Cardiovascular Incidence in Barbados (2023)  
**Version:** 1.0  **Date:** 11 November 2025  
**Linked Core Document:** [BNR Core SAP](./bnr-sap-core.md)  
**Linked DO File:** `bnrcvd-2023-incidence.do`  
**Prepared by:** Ian Hambleton for the BNR Analytics Team  

---

## 1. Purpose
This briefing presents **incidence rates** for hospital-registered cardiovascular disease (CVD) events—**stroke** and **acute myocardial infarction (AMI)**—for the year **2023**. Analyses estimate **crude** and **age-standardised incidence** per 100,000 population and compare them with the previous five-year period (2018–2022).

---

## 2. Analysis Scope
| Aspect | Specification |
|---------|----------------|
| **Index year** | 2023 |
| **Baseline period** | 2018–2022 |
| **Events included** | Stroke or acute MI registered by the BNR |
| **Population denominator** | Mid-year population estimates (United Nations World Population Prospects) |
| **Measure** | Crude and age-standardised incidence per 100,000 population |
| **Standard population** | WHO World Standard Population (2000) |
| **Exclusions** | DCO-only, non-residents, duplicates |
| **Objective** | To describe temporal trends and sex differences in incident in-hospital cardiovascular events |

---

## 3. Analytic Workflow
All work is executed in **Stata 18** using the master script `bnrcvd-2023-incidence.do`.

The workflow follows five fixed phases:

1. **Dataset preparation** – As needed, merge annual datasets (2018–2023), retain hospital-confirmed events, and apply exclusions.  
2. **Variable setup** – Define event type, sex, age groups, and create year-specific population denominators.  
3. **Rate calculations** – Compute annual crude and age-standardised incidence rates (per 100,000), with 95% confidence intervals.  
4. **Visualisation** – Produce two standard figures:  
   - (a) Trends in crude incidence by sex and event type (2010–2023).  
   - (b) Trends in age-standardised incidence rates (2010–2023).  
5. **Automated report creation** – Assemble briefing PDF using `putpdf`, inserting both figures and summary text.  

A Stata log and YAML metadata file document execution and dataset lineage.

---

## 4. Outputs
The `.do` file produces the following artefacts (as specified in the script):

| Artefact | Creation method |
|-----------|----------------|
| `${graphs}/bnrcvd-incidence-figure1.png` | Export of age-standardised incidence trend, with and without added DCOs |
| `${graphs}/bnrcvd-incidence-figure2.png` | Export of Incidence Rate Ratios by CVD event type, by sex, by year |
| `${outputs}/bnr-cvd-incidence-${today}.pdf` | Final PDF report created with `putpdf save` |
| *(Metadata)* | YAML metadata file created alongside graph exports |

---

## 5. Limitations
- Population denominators are modelled (UN WPP) and may differ slightly from national census estimates.  
- In-hospital rates should not be interpreted as an authoratative national incidence rate, due to the exclusion of community cases and death-certificate only cases.
- Strictly, incidence would restrict to first ever event. We choose to use any stroke or AMI event for an estimate better aligned to hospital burden.

---

## 6. Change Log
| Version | Date | Summary | Author |
|----------|------|----------|--------|
| 1.0 | 11 Nov 2025 | Initial SAP for incidence briefing | Ian Hambleton for the BNR Analytics Team |

---
