# Refit: What’s Changing (at a glance)

The **BNR Refit** is a full system modernisation of the Barbados National Registry for Chronic Non-Communicable Disease (BNR). It rebuilds the data pipeline to make the registry **accurate, efficient, auditable, and sustainable**.  

The refit responds directly to the **BNR Process Audit**, which identified gaps in data governance, validation, and workflow design. It introduces new systems that separate data cleaning from analysis, strengthen version control, and automates report production — all while improving transparency and long-term maintainability.

---

## Implementation Stages

| **Stage** | **Timeline** | **Focus** | **Key Actions** |
|------------|---------------|------------|-----------------|
| **1 — Stabilise & Secure** | 0–9 months | Fix core governance and data-quality issues. | Finalise cumulative dataset; lock REDCap; define core variables; introduce IRIS cause-of-death coding. |
| **2 — Modernise & Automate** | 9–18 months | Redesign workflows for efficiency. | Separate cleaning from analytics; automate reporting; develop data dictionary; implement monthly QC dashboards. |
| **3 — Sustain & Expand** | 18–36 months | Embed governance and extend capacity. | Add new condition modules; create research analytics stream; refresh reporting; strengthen governance. |

See the full staging plan in the [Process Audit Findings and Recommendations](../bnr-process-audit/findings.md#implementation-stages).

---

## The Four Core Workstreams

### 1. Process
We are re-establishing a clean, traceable workflow from REDCap to reporting.  
This includes rebuilding REDCap validation, restoring record locking, and ensuring every exported dataset is verified and ready for analysis.

??? "**Key improvements:**"

    - Reinstate required-field and logic validation in REDCap.  
    - Separate data cleaning (in REDCap) from analytics (in Stata).  
    - Lock verified records before monthly export.  
    - Reintroduce senior review and sign-off before dataset release.  
    - Document all processes as Standard Operating Procedures (SOPs).

    ➡️ [See full details → Process Improvements](process-new.md)

### 2. Data
We are defining a single, auditable dataset structure covering all cardiovascular data from 2009–2023, ensuring that every subsequent update builds upon an approved, version-controlled base.

??? "**Key improvements:**"

    - Create a unified **data dictionary** and metadata register.  
    - Introduce dataset sign-off and release logs.  
    - Store identifiable, de-identified, and anonymised data in controlled locations.  
    - Restore historical identifiers and rebuild complete longitudinal linkages.  
    - Implement SOPs for dataset storage, release, sharing, and dissemination.

    ➡️ [See full details → Data Improvements](dataset-new.md)

### 3. Analytics
We are redesigning the entire analytics workflow to move from manually edited scripts to a structured, more automated Stata environment. The new system allows consistent, reproducible analysis for monthly and annual reports.

??? "**Key improvements:**"

    - Separate data-cleaning code from analytic code.  
    - Develop modular Stata programs and ado-file wrappers.  
    - Automate calculation of incidence, mortality, and health-system indicators.  
    - Embed built-in data quality and completeness checks.  
    - Prepare for long-term integration with a “no-code” interface for sustainability.

    ➡️ [See full details → Analytics Improvements](analytics-new.md)

### 4. Reporting
We are aligning outputs with national and WHO standards through an overhaul of the reporting framework. Automated analytics feed directly into publication-ready templates for internal and external reporting.

??? "**Key improvements:**"

    - Automated **Monthly Reports** with counts, rates, and quality KPIs.  
    - Automated **Annual Reports** integrating incidence, mortality, and performance metrics.  
    - Streamlined **Health-System Performance reporting** using international indicators.  
    - SOPs for dataset versioning, export, and sign-off.  
    - Consistent templates for technical and policy audiences.

    ➡️ [See full details → Reporting Improvements](reporting-new.md)

---

## Grounded in the Process Audit

The **BNR Process Audit** identified three broad areas for improvement:

| Stage | Core Issues | Response in the Refit |
|-------|--------------|-----------------------|
| **Pre-REDCap** | Inconsistent inclusion criteria, weak duplication controls, incomplete use of death data | Standardised case definitions, strengthened duplicate checking, IRIS implementation for cause-of-death coding |
| **Within-REDCap** | Missing validation rules, undocumented field changes, limited QC | Locked production database, restored required-field checks, comprehensive data dictionary |
| **Post-REDCap** | No definitive cumulative dataset, mixed cleaning and analytics scripts, inconsistent reporting | Single verified dataset, modular Stata analytics, automated version-controlled reporting |

These findings have been translated into **14 actionable recommendations**, now embedded across the four refit workstreams. Together, they provide a roadmap to restore data integrity and move toward a sustainable registry model, ready to align with national and regional digital health transformation initiatives.

➡️ [See full list → Audit Findings and Recommendations](../bnr-process-audit/findings.md)

---

## What This Delivers

- **Accuracy** — Verified, sign-off datasets and consistent definitions.  
- **Efficiency** — Automated analytics and scheduled reporting.  
- **Transparency** — Clear documentation and version control.  
- **Sustainability** — Shared systems and reduced reliance on individuals.  
- **National value** — A modern registry that meets global standards for health data governance and reporting.

---

### Next Steps
Explore each area of improvement:  
[Process](process-new.md) ○ [Data](dataset-new.md) ○ [Analytics](analytics-new.md) ○ [Reporting](reporting-new.md) ○ [By Recommendation](../updates/recommendations-new.md)
