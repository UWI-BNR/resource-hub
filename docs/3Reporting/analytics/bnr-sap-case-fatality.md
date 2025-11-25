# BNR Statistical Analysis Plan – Hospital Cardiovascular Case Fatality in Barbados (2023)  
**Version:** 1.0 <br/> **Date:** 11 November 2025  
**Linked Core Document:** [BNR Core SAP](./bnr-sap-core.md) <br/>
**Linked DO File:** `bnrcvd-2023-case-fatality.do`  
**Prepared by:** Ian Hambleton for the BNR Analytics Team  

---

## 1. Purpose
This briefing reports **in-hospital case fatality** following hospitalised **stroke** and **acute myocardial infarction (AMI)** during **2023**, comparing results with the five-year period **2018–2022**. Analyses quantify differences by sex and age, and provide age-adjusted case-fatality percentages with 95% confidence intervals.

---

## 2. Analysis Scope
| Aspect | Specification |
|---------|----------------|
| **Index year** | 2023 |
| **Baseline period** | 2018–2022 |
| **Events included** | Hospitalised, confirmed stroke and acute MI cases |
| **Outcome** | Death before discharge (in-hospital fatality) |
| **Measure** | Crude and age-adjusted case-fatality (%) |
| **Denominator** | All hospitalised cases with known discharge outcome |
| **Exclusions** | DCO-only, unknown outcome, non-residents, duplicates |
| **Objective** | To assess short-term mortality in hospitalised CVD events and monitor change over time |

---

## 3. Analytic Workflow
The analysis is implemented in **Stata 18** using `bnrcvd-2023-case-fatality.do`.

The script is organised into the following phases:

1. **Data assembly** – Import confirmed hospital events for 2010–2023 and restrict to cases with known discharge status.  
2. **Variable setup** – Create binary death indicator, year-of-event (`yoe`), and relevant demographic groupings.  
3. **Computation** –  
      - Calculate annual crude case-fatality (%) by event type and sex.  
      - Derive age-adjusted case-fatality using logistic models.  
      - Generate 95% confidence intervals using binomial methods.  
4. **Visualisation** –  
      - Figure 1: Trends in crude in-hospital case fatality (2010–2023).  
      - Figure 2: Average age at admission and death by sex (Visual Table).  
5. **Automated report generation** –  
      - Insert figures and summary text into a standard briefing layout using `putpdf`.  
      - Save the completed briefing PDF to the output directory.  

Each run generates a Stata log and a metadata YAML file recording dataset version, date, and analyst.

---

## 4. Outputs
The `.do` file produces the following artefacts:

| Artefact | Creation method |
|-----------|----------------|
| `${graphs}/bnrcvd-cfr-figure1.png` | Case-fatality trend by event type, sex, year |
| `${graphs}/bnrcvd-cfr-figure2.png` | Average age at admission and death by sex |
| `${outputs}/bnr-cvd-cfr-${today}.pdf` | Final PDF briefing created with `putpdf save` |
| *(Metadata)* | YAML metadata file written alongside the figures |

---

## 5. Limitations
- Outcome limited to *in-hospital* mortality; excludes deaths after discharge.  
- Case-fatality denominators rely on abstracted cases with complete discharge data.  
- Delayed abstraction may affect counts for the most recent year.  

---

## 6. Change Log
| Version | Date | Summary | Author |
|----------|------|----------|--------|
| 1.0 | 11 Nov 2025 | Initial SAP for case-fatality briefing | Ian Hambleton for the BNR Analytics Team |

<br/>


