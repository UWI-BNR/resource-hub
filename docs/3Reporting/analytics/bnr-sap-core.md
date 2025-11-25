# Barbados National Registry (BNR) – Core Statistical Analysis Plan  




**Date:** November 2025  
**Version:** 1.0  <br/>
**Prepared by:** Ian Hambleton for the BNR Analytics Team  

---

## 1. Purpose and Scope
This Core Statistical Analysis Plan (Core SAP) defines the analytical framework used for all BNR cardiovascular surveillance outputs. It provides a consistent foundation for producing reproducible, auditable analyses across all BNR briefings. Individual briefings (e.g., *Hospital Cardiovascular Cases in Barbados*) include only the elements that differ from this core framework and link back to this document for shared methodology.  

---

## 2. The Three-Tier SAP Framework
| Tier | Description | Example File | Update Frequency |
|------|--------------|--------------|-----------------|
| **Tier 1 – Core SAP (this document)** | Describes the common analytical environment, dataset structures, inclusion/exclusion rules, and quality assurance processes. | `bnr_sap_core.md` | Annual or when methods change |
| **Tier 2 – Template SAP** | A short reusable markdown template that references this document and defines the structure for each briefing SAP. | `bnr_sap_template.md` | Occasional (if structure changes) |
| **Tier 3 – Briefing SAP** | A single-page analysis plan for a specific output (e.g., counts, incidence, mortality, case fatality). | `bnr_sap_<briefing>.md` | Every briefing |

Together, these tiers balance **completeness**, **clarity**, and **ease of updating**.  

---

## 3. Software and Analytical Environment
- **Statistical Software:** Stata 19 SE (or latest version approved by BNR)  
- **Operating System:** Windows 11 (UWI GA-CDRC standard)  
- **Version Control:** GitHub (`uwi-bnr/bnr-refit`)  
- **Data Management:** Only use the official BNR-data releases in analyses.  
- **Automation:** All analytics are executed through linked `.do` and `.ado` files in the `/do` and `/ado` subfolders.  

All scripts include a header specifying:  

        /**************************************************************************
         DO-FILE:     bnrcvd-<yyyymm>-<briefing>.do
         PROJECT:     BNR Refit Consultancy
         PURPOSE:     Describe goal of .do file 
        
         AUTHOR:      Ian R Hambleton
         DATE:        [2025-11-02]
         VERSION:     [v1.0]
        
         METADATA:    bnrcvd-<yyyymm>-<briefing>.yml (same dirpath/name as dataset)
        
         NOTES:       <Give more technical information as relevant>
                      E.g. for count briefing:
                      BNR simple CVD counts:
                        - by type (AMI, stroke)
                        - by year
                        - by sex 
                        - by age groups
        **************************************************************************/
 

---

## 4. Data Sources and Definitions
- **Primary Sources:**  
    - BNR-CVD Registry Database (validated, approved (with sign-off), locked case-level data).  
    - Death certificate data from the Barbados Civil Registry (DCO cases).  
- **Population Denominators:** Mid-year estimates from UN WPP (latest version).  
- **Inclusion Criteria:** Confirmed incident cardiovascular event in a Barbados resident during the analysis period.  
- **Exclusion Criteria:** Non-residents, duplicates, or DCO cases (if analysing hospital-only events). See individual briefing SAP for additional restrictions.  

---

## 5. Variable Conventions
| Variable | Description | Format |
|-----------|--------------|--------|
| `eid` | Unique event identifier. Stata generated for deidentified uniqueness  | numeric |
| `sex` | Female (1), Male (2) | numeric |
| `dob`| Date of birth | %td |
| `doe`| Dates of CVD event | %td |
| `doa`| Dates of hospital admission | %td |
| `dodi` | Dates of discharge | %td |
| `dod` | Dates of death (if applicable) | %td |
| `agey` | Age in years at admission | numeric |
| `etype` | Stroke (1), AMI (2) | numeric |
| `yoe`, `moe`, `woe` | Year / month / week of event | numeric |
| `dco` | 0 = in-hospital event, 0 = DCO only | numeric |

---

## 6. Analytics Folder Structure
    /bnr/
     ├── analytics/
     │    ├── ado/
     │    ├── data/
     │    ├── do/
     │    ├── graphics/
     │    ├── log/
     │    ├── outputs/
     │    ├── temp/

---

## 7. Data Preparation (Applies to All Analyses)

1. Load the approved `BNR-<TYPE>-<TIER>-<YYYYMM>.dta` dataset to `data/` folder. <br/>For example: `BNR-AMI-DEID-202509.dta`  
2. Load and create new version of analysis `.do` file as necessary:
   > a. For example, for *CVD Cases Briefing*, <br/>use `.\analytics\do\bnrcvd-<yyyymm>-count.do` 
3. Verify dataset signature (`datasignature` or version ID).  
4. Confirm / apply standard inclusion/exclusion filters (will be pre-coded in `.do` file).  
5. Confirm key variables: `agey`, `sex`, `etype`, `doe`, `doa`, `dodi`, `dod`.
6. Confirm expected numbers, in discussion with BNR QA personnel  
7. Generate derived indicators as needed (e.g., weekly counts, age groups, case fatality).  
8. Save interim processed analytic datasets to `/analytics/temp/`. The `/temp` folder should be occasionally emptied - all interim datasets can be re-created using the analytics `.do/` files. 

---

## 8. Analytical Principles
- Analyses are **replicable** through Stata `.do` files.  
- Methods are **consistent** across months / years.  
- All summaries include **crude** and **age-standardised** (using WHO standard population) metrics when appropriate.  
- Statistical uncertainty is expressed using 95% confidence or uncertainty intervals.  
- All figures are labelled and archived.  

---

## 9. Quality Assurance
- Two-person review of analytic output.  
- Validation against previous years’ totals.  
- Analytics logs - generated from Stata `.do` files - stored in `/analytics/logs/`.  
- Any deviation from the Core SAP is documented in the briefing-specific SAP.  

---

## 10. Ethical and Data Governance
- Data are deidentified prior to analysis.  
- Dataset access is restricted to authorised BNR personnel.  
- All outputs are aggregated and non-identifiable.
- Analytics and data are stored on computers with full-disk or container-level encryption (AES-256). 

---

## 11. Change Management
| Version | Date | Description | Author |
|----------|------|--------------|--------|
| 1.0 | Nov 2025 | First implementation of modular SAP system | BNR Analytics Team |

<br/>
