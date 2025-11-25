==IH Reviewed (16-Oct-2025)==

# BNR CVD Refit Project Plan  

|  | KEY MILESTONES | DATE | 
|----|------|------------------|
| ✅ | **Official Start:** | October 1st, 2024 |
| ✅ | **Contract Produced / Signed:**  | April 7th, 2025 |
| ✅ | **Cumulative CVD dataset reviewed by:**  | June 30th, 2025 |
| 🟨 | **Cumulative CVD dataset created by:**  | Oct 30th, 2025 |
| ❌ | **Hard Deadline:** Annual report 2023 | Nov 30th, 2025 |
| ❌ | **Project Completion:** | Feb 28th, 2026 |
 
## Introduction  

This page is our **living project tracker** for the BNR–CVD Refit. It provides a week-by-week breakdown of planned activities, a brief descriptions for each task, expected deliverables, and a simple note of whether the task is Not Started (❌), Underway (🟨), or Completed (✅).  

The aim of this refit is to create a **sustainable, reproducible and open analytical framework** for the Barbados National Registry (CVD component).  

By the end of February 2026, the project will:  

1. Deliver a semi-automated **Stata package (`bnrcvd.pkg`)** to generate reports from exported registry data.  
2. Produce a final **2023 Annual Report (PDF)** using the new automation pipeline.  
3. Produce suggested **Monthly** and **Administrative** reports as needed.
4. Establish clear **Data Sharing and Trust Agreements (DSTA)** for long-term data governance.  
5. Publish a **self-paced learning and documentation website**, currently hosted at [ianhambleton.github.io/bnr-refit](https://ianhambleton.github.io/bnr-refit).  

---

!!! warning

    The Refit project assumptions included the following caveat for successful operation:

    > The BNR must produce and share clean cardiovascular datasets for all years of operation.

    The BNR project was unable to produce a cumulative dataset of CVD cases. The Refit project therefore extended it's remit to include a pre-processing phase (Phase 0 below). **This phase aimed to produce a definitive cumulative record of CVD cases, from BNR initiation to end-2023.**

## Phase 0 – Pre-Project Dataset Preparation  
**Dates:** June - October 2025   
**Focus:** Reconstruction of BNR–CVD datasets (2009–2023)  
**Key:**  ❌ Not started 🟨 Underway ✅ Completed  

| ✅ | Task | Full Description | Result / Deliverable |
|----|------|------------------|----------------------|
| ✅ | Append 2021 data to 2009–2020 datasets | Combine historical stroke and heart datasets into unified 2009–2021 dataset using official dataset naming conventions. | Extended longitudinal dataset (2009–2021) ready for review. |
| ✅ | Evaluate historical cleaning do-files | Review 2022 legacy Stata scripts to understand prior data correction logic and identify inconsistencies. | Documented lessons from past cleaning workflows for reuse. |
| ✅ | Assess 2022 dataset usability | Test 2022 abstraction data for structure and completeness; determine whether safe to append. | Determined dataset not suitable for inclusion; corrective actions noted. |
| ✅ | Review 2022 ineligibles | Generate ineligibility flag variable categorising cases (e.g. clinical rejection, miscoding, discharge diagnosis). | 2022 dataset annotated with ineligibility classifications. |
| ✅ | Export 2023 dataset and initialise do-files | Extract latest REDCap data and create initial cleaning scripts for 2023 dataset. | Initial 2023 dataset and template do-files established. |
| 🟨 | Review 2023 ineligibles | Apply same flagging logic used for 2022 to maintain consistent categorisation. | 2023 dataset annotated with ineligibility classifications. |
| 🟨 | Combine 2022 + 2023 datasets | Merge 2022 and 2023 incidence data using restructured format compatible with prior years. | Combined two-year CVD dataset (2022–2023) prepared. |
| 🟨 | Clean 2022 + 2023 death data | Standardise variable names, date formats, and cause-of-death codes for death registry subset. | Clean death registry data ready for matching. |
| 🟨 | Clean combined 2022 + 2023 datasets | Conduct final cleaning and variable reconciliation for merged incidence datasets. | Harmonised 2022–2023 CVD dataset (pending final checks). |
| ✅ | Restructure 2009–2021 dataset | Align older variables with new 2023 schema to support longitudinal merging. | Restructured legacy dataset matching new schema. |
| ✅ | Combine heart and stroke datasets | Merge restructured BNR-Heart and BNR-Stroke datasets into a unified CVD dataset. | Single comprehensive CVD dataset (2009–2021). |
| ❌ | Merge 2022 + 2023 death data with legacy dataset | Link cleaned 2022–2023 death records to unified 2009–2021 dataset to generate full mortality linkage. | Complete CVD mortality-linked dataset (pending merge). |
| ❌ | Append cleaned 2022 + 2023 data | Append final 2022–2023 incidence data to legacy dataset post-merge. | Updated longitudinal CVD dataset (2009–2023). |
| ❌ | Create data-quality check table | Produce summary table of all cleaning checks (missingness, validity) for internal quality report and rule validation. | Data-quality summary table for IH and DQ rule development. |
| 🟨 | Generate flagged data issues report | Produce descriptive report using flag variables to summarise all identified data anomalies. | Internal issue log and DQ recommendations report. |
| 🟨 | Maintain queries log | Continue recording data issues and potential new DQ rules in “Queries Log for Christina.” | Updated ongoing data-quality tracking file. |
| ✅ | Locate raw data sources | Attempt to retrieve original raw case-finding and abstraction datasets (2009–2021) from shared drives and archives. | Confirmed archival status: only partial backups available. |
| ❌ | Develop audit report | Produce summary report of findings, corrective solutions, and outcomes. | Audit report posted to Refit website. |
| ❌ | Create current ```do``` file repo | Create annotated repo of active ```do``` files. | Active ```do``` files posted to GitHub repo. |
| ❌ | Create current ```document``` repo | Create annotated repo of active ```documents``` describing the new process. | Active ```documents``` posted to GitHub repo. |


**Outcomes:**  

- All major reconstruction tasks required for automation readiness completed.  
- The unified BNR–CVD dataset (2009–2023) existing in restructured form and can serve as the foundation for the forthcoming automated analytics system.

---

## Week 1 – 20 to 26 October 2025  
**Focus:** Data Reset & Analytics Planning  
Key: ❌ Not started 🟨 Underway ✅ Completed

|  | Task | Full Description | Result / Deliverable |
|----|------|------------------|----------------------|
| 🟨 | **(Analytics)** Statistical Analysis Plan | Draft SAP defining indicators, analytic methods, and frequency of updates. | (🗹 Lead) Draft SAP v1 completed and shared for review. |
| ❌ | **(Data)** Document Dataset Structure | Data Dictionary and metadata in `.dta` and as files. | (⚙ Contribute) Locked BNR–CVD data dictionary + metadata. |
| ❌ | **(Process)** Data Process Audit | Prepare audit for web upload. | (⚙ Contribute) Audit report with suggested actions. |
| ❌ | **(Process)** REDCap Database Alignment | Map REDCap database to suggested final dataset. | (⚙ Contribute) Change mapping table. |
| ❌ | **(Analytics)** Initial `.do` file Framework | Create repository folders, naming scheme and headers for Stata scripts. | (🗹 Lead) Project skeleton ready for code insertion. |
| ❌ | **(Data)** Dataset Sign-off Rules | Define approval and versioning workflow for monthly exports. | (⚙ Contribute) Dataset sign-off SOP draft. |
| ❌ | **(Process)** Develop Process for Final Case Review & Sign-off | Draft verification checklist and roles for senior review. | (⚙ Contribute) Case review SOP v1. |

---

## Week 2 – 27 October to 2 November 2025  
**Focus:** Initial Do-file Development & Report Foundations  
Key: ❌ Not started 🟨 Underway ✅ Completed

|  | Task | Full Description | Result / Deliverable |
|----|------|------------------|----------------------|
| ❌ | **(Reporting)** Annual Report Do-files | Code tables for incidence, mortality and health-system performance. | (🗹 Lead) Core annual analytics do-files drafted. |
| 🟨 | **(Data)** Data Release Process Outline | Define sequence for QC and export of locked cases. | (⚙ Contribute) Release process summary. |

---

## Week 3 – 3 to 9 November 2025  
**Focus:** Annual Report Drafting & QC Cycle 1  
Key: ❌ Not started 🟨 Underway ✅ Completed

|  | Task | Full Description | Result / Deliverable |
|----|------|------------------|----------------------|
| ❌ | **(Reporting)** Build Annual Report 2023 using `putpudf` | Integrate validated outputs and write narrative sections. | (🗹 Lead) Draft Annual Report 2023 v1. |
| ❌ | **(Analytics)** QC Indicator Validation | Cross-check outputs vs 2022 baseline values. | (🗹 Lead) QC log and validation report. |
| ❌ | **(Process)** Initiate Case-level Record Lock | Define technical steps for record locking before export. | (⚙ Contribute) Record lock SOP draft. |
| ❌ | **(Process)** Reassess How to Use Death Data | Evaluate use of death records for analytics and reporting. | (ⓘ Advise) Technical memo for BNR. |

---

## Week 4 – 10 to 16 November 2025  
**Focus:** SOP Development for Post-REDCap Processes  
Key: ❌ Not started 🟨 Underway ✅ Completed

|  | Task | Full Description | Result / Deliverable |
|----|------|------------------|----------------------|
| ❌ | **(Process)** Data Extraction `.do` file + SOP | Define monthly export of locked records procedure. | (🗹 Lead) Data Extraction `.do` file and SOP v1. |
| 🟨 | **(Process)** SOP – Dataset Versioning & Sign-off | Specify naming and archiving rules with examples. | (🗹 Lead) Version Control SOP v1. |
| ❌ | **(Process)** SOP – Data Transfer & Storage | Detail secure transfer and backup routine. | (⚙ Contribute) Data Handling SOP v1. |
| ❌ | **(Data)** Dataset Storage | Evaluate cloud vs local storage and document controls. | (⚙ Contribute) Storage guidance memo. |
| 🟨 | **(Data)** Dataset Dissemination | Define communication and access levels for shared datasets. | (⚙ Contribute) Dissemination SOP draft. |

---

## Week 5 – 17 to 23 November 2025  
**Focus:** Finalize Annual Report & QC Cycle 2  
Key: ❌ Not started 🟨 Underway ✅ Completed

|  | Task | Full Description | Result / Deliverable |
|----|------|------------------|----------------------|
| 🟨 | **(Reporting)** Annual Report Editorial Review | Revise format and figures after feedback. | (🗹 Lead) Proofed Annual Report v2. |
| ❌ | **(Reporting)** BNR Annual Report Review | Present draft to BNR Lead. | (⚙ Contribute) Feedback log. |
| ❌ | **(Reporting)** Prepare Public Summary Brief | One-page infographic summary for MoH. | (🗹 Lead) Summary graphic. |

---

## Week 6 – 24 to 30 November 2025  
**Focus:** Deliver Annual Report (Hard Deadline)**  
Key: ❌ Not started 🟨 Underway ✅ Completed

|  | Task | Full Description | Result / Deliverable |
|----|------|------------------|----------------------|
| 🟨 | **(Reporting)** Run *Annual* Analytics Pipeline | Execute final do-files and generate PDF outputs. | (🗹 Lead) Verified outputs locked for release. |
| ❌ | **(Reporting)** Submit Annual Report 2023 | Deliver final report and upload to website. | (🗹 Lead) Annual Report submitted Nov 30. |
| ❌ | **(Process)** Post-release Review Meeting | Review acceptance and document refinements. | (⚙ Contribute) Meeting minutes. |

---

## Week 7 – 1 to 7 December 2025  
**Focus:** Start Monthly Report Development   
Key: ❌ Not started 🟨 Underway ✅ Completed

|  | Task | Full Description | Result / Deliverable |
|----|------|------------------|----------------------|
| ❌ | **(Reporting)** Monthly Report Do-files (Part 1) | Build summary tables for case counts and rolling rates. | (🗹 Lead) Prototype monthly code. |
| ❌ | **(Reporting)** Monthly Report Do-files (Part 2) | Add trend plots and rolling averages. | (🗹 Lead) Monthly report code ready for testing. |
| ❌ | **(Data)** Dataset Release SOP v2 | Update based on first release experience. | (🗹 Lead) Revised SOP v2. |
| ❌ | **(Reporting)** Monthly Report Pilot | Produce pilot for Oct–Nov data and review with BNR team. | (⚙ Contribute) Validated monthly report v1. |

---

## Week 8 – 8 to 14 December 2025  
**Focus:** Documentation and Website Integration  
Key: ❌ Not started 🟨 Underway ✅ Completed

|  | Task | Full Description | Result / Deliverable |
|----|------|------------------|----------------------|
| ❌ | **(Reporting)** Ad-hoc Report Template | Create flexible do-file for custom queries and research summaries. | (🗹 Lead) Ad-hoc template tested. |
| ❌ | **(Process)** Public Web Documentation | Upload SOPs and guides to BNR website. | (ⓘ Advise) Process Online User Guide. |
| ❌ | **(Analytics)** User Guide for Analysts | Write step-by-step manual for running do-files. | (🗹 Lead) User Guide v1. |
| ❌ | **(Analytics)** Developer Notes / README | Summarise folder structure and naming rules. | (🗹 Lead) README committed. |

---

## Week 9 – 15 to 21 December 2025  
**Focus:** Pre-holiday Consolidation & Planning  
Key: ❌ Not started 🟨 Underway ✅ Completed

|  | Task | Full Description | Result / Deliverable |
|----|------|------------------|----------------------|
| ❌ | **(Process)** Internal Review Meeting | Confirm post-report actions and training needs. | (⚙ Contribute) Meeting minutes. |
| ❌ | **(Process)** Develop Training Schedule | Outline online training modules. | (⚙ Contribute) Training agenda. |
| ❌ | **(Data)** Data Governance Visual | Create flow diagram of data processes for website. | (ⓘ Advise) Governance graphic posted. |

---

## 🎄 Christmas Break – 22 December 2025 to 5 January 2026  
*No formal project work scheduled – holiday period for rest and review.*

---

## Week 10 – 6 to 12 January 2026  
**Focus:** Training & Operational Testing  
Key: ❌ Not started 🟨 Underway ✅ Completed

|  | Task | Full Description | Result / Deliverable |
|----|------|------------------|----------------------|
| ❌ | **(Analytics)** Review analytics outputs | Final versions of analytics deliverables. | (⚙ Lead) Attendance log completed. |
| ❌ | **(process)** Review SOP and advice outputs | FInal versions of website SOPs and advisories. | (🗹 Lead) Final versions of SOPs and advisories. |
| ❌ | **(Analytics)** Ad-hoc extra `.do` files | Final ad-hoc analyses. | (⚙ Lead) Ad-hoc `.do` files added to outputs. |
| ❌ | **(Analytics)** Refactor Do-files | Clean syntax and document line-by-line logic. | (🗹 Lead) Optimised scripts committed. |

---

## Week 11 – 13 to 19 January 2026  
**Focus:** Handover Preparation  
Key: ❌ Not started 🟨 Underway ✅ Completed

|  | Task | Full Description | Result / Deliverable |
|----|------|------------------|----------------------|
| ❌ | **(Process)** Compile Handover Package | Bundle SOPs, do-files and documentation. | (🗹 Lead) Handover ZIP v1. |
| ❌ | **(Process)** Handover Meeting Plan | Schedule final walk-through session. | (⚙ Contribute) Meeting date set. |

---

## Week 12 – 20 to 26 January 2026  
**Focus:** Formal Handover & Post-project Advice  
Key: ❌ Not started 🟨 Underway ✅ Completed

|  | Task | Full Description | Result / Deliverable |
|----|------|------------------|----------------------|
| ❌ | **(Process)** Final Handover Meeting | Present package and respond to queries. | (⚙ Contribute) Minutes + sign-off form. |
| ❌ | **(Process)** Post-project Recommendations | Summarise lessons and future automation advice. | (ⓘ Advise) Recommendations brief online. |
| ❌ | **(Analytics)** Repository Version | Lock main branch and tag v1.0 release. | (🗹 Lead) Tagged release v1.0. |

---

## Week 13 – 27 January to 2 February 2026  
**Focus:** Close-out Preparation  
Key: ❌ Not started 🟨 Underway ✅ Completed

|  | Task | Full Description | Result / Deliverable |
|----|------|------------------|----------------------|
| ❌ | **(Data)** Archive Project Materials | Store reports and code in secure repository. | (🗹 Lead) Versioned archive. |

---
