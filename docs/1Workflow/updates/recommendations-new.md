# Deliverables by Recommendation

This page lists the **Barbados National Registry (BNR) Refit deliverables**, organised by **recommendation**.  

It provides a reverse view of implementation — showing how each process, data, analytics, and reporting activity contributes to the 14 recommendations identified in the BNR Process Audit.

Each table lists the specific deliverables drawn from the four implementation areas:  

- [Process Improvements](process-new.md)  
- [Data Improvements](dataset-new.md)  
- [Analytic Improvements](analytics-new.md)  
- [Reporting Improvements](reporting-new.md)

Deliverables may appear in more than one table, reflecting shared dependencies and overlapping objectives.  

!!! note "Implementation progress is tracked in the individual files listed above"

---

## Table of Contents

| Recommendation | Priority | Quick Link |
|----------------|-----------|-------------|
| 1. Dataset Governance and Version Control | 🔴 Critical | [Jump to Rec 1](#recommendation-1-dataset-governance-and-version-control) |
| 2. REDCap Quality Controls | 🔴 Critical | [Jump to Rec 2](#recommendation-2-redcap-quality-controls) |
| 3. Core Variable Set Definition | 🔴 Critical | [Jump to Rec 3](#recommendation-3-core-variable-set-definition) |
| 4. Pre-REDCap Process and Hospital-Based Re-focus | 🔴 Critical | [Jump to Rec 4](#recommendation-4-pre-redcap-process-and-hospital-based-re-focus) |
| 5. Automated UCOD Assignment (IRIS) | 🔴 Critical | [Jump to Rec 5](#recommendation-5-automated-ucod-assignment-iris) |
| 6. Analytics Workflow Redesign | 🟠 High | [Jump to Rec 6](#recommendation-6-analytics-workflow-redesign) |
| 7. Data Dictionary and Metadata Management | 🟠 High | [Jump to Rec 7](#recommendation-7-data-dictionary-and-metadata-management) |
| 8. Open Standards and Documentation | 🟠 High | [Jump to Rec 8](#recommendation-8-open-standards-and-documentation) |
| 9. Continuous Data-Quality Monitoring | 🟠 High | [Jump to Rec 9](#recommendation-9-continuous-data-quality-monitoring) |
| 10. Automation in Data Abstraction | 🟢 Medium | [Jump to Rec 10](#recommendation-10-automation-in-data-abstraction) |
| 11. Expansion to Additional Conditions | 🟢 Medium | [Jump to Rec 11](#recommendation-11-expansion-to-additional-conditions) |
| 12. Research Analytics Workstream | 🟢 Medium | [Jump to Rec 12](#recommendation-12-research-analytics-workstream) |
| 13. Revamped Reporting Framework | 🟢 Medium | [Jump to Rec 13](#recommendation-13-revamped-reporting-framework) |
| 14. Sustainability and Governance Enhancements | 🟢 Medium | [Jump to Rec 14](#recommendation-14-sustainability-and-governance-enhancements) |

---

## 🔴 Recommendation 1 – Dataset Governance and Version Control
| DELIVERABLE | SOURCE FILE | RATIONALE / CONTRIBUTION |
|--------------|--------------|---------------------------|
| **REDCap dataset—database alignment** | [Process Improv.](process-new.md) | ➤ The cumulative dataset must mimic the structure of the current REDCap database. Harmonisation is required. |
| **Develop process for final case review and sign-off** | [Process Improv.](process-new.md) | ➤ Ensure all fields are complete and verified by a senior staff member before dataset release. |
| **Automate monthly data extractions of locked cases only** | [Process Improv.](process-new.md) | ➤ Generate clean, reproducible extracts limited to verified data. |
| **Data structure** | [Data Improv.](dataset-new.md) | ➤ Standardised data dictionary & metadata for automation and long-term curation. |
| **Dataset release** | [Data Improv.](dataset-new.md) | ➤ SOP for controlled dataset release with traceability and auditability. |
| **Dataset sign-off** | [Data Improv.](dataset-new.md) | ➤ Formal approval for each monthly export confirming completeness and accuracy. |

---

## 🔴 Recommendation 2 – REDCap Quality Controls
| DELIVERABLE | SOURCE FILE | RATIONALE / CONTRIBUTION |
|--------------|--------------|---------------------------|
| **REDCap database audit** | [Process Improv.](process-new.md) | ➤ Identify discrepancies and reset to best practice. |
| **Duplicates handled within REDCap** / **Use query system within REDCap** | [Process Improv.](process-new.md) | ➤ Manage duplicates at source and re-establish the internal query/resolution workflow. |
| **Initiate case-level record lock in database** | [Process Improv.](process-new.md) | ➤ Prevent edits to verified records and designate records as ready for extraction. |

---

## 🔴 Recommendation 3 – Core Variable Set Definition
| DELIVERABLE | SOURCE FILE | RATIONALE / CONTRIBUTION |
|--------------|--------------|---------------------------|
| **Duplicates handled within REDCap** / **Use query system within REDCap** | [Process Improv.](process-new.md) | ➤ Restore separation between data cleaning (REDCap) and analytics (post-REDCap). |
| **Reduce number of database variables further** | [Process Improv.](process-new.md) | ➤ Simplify the data model to improve maintainability. |

---

## 🔴 Recommendation 4 – Pre-REDCap Process and Hospital-Based Re-focus
| DELIVERABLE | SOURCE FILE | RATIONALE / CONTRIBUTION |
|--------------|--------------|---------------------------|
| **Reassess how to use death data** | [Process Improv.](process-new.md) | ➤ Evaluate completeness and define appropriate use in analytics. |
| **Death data** | [Data Improv.](dataset-new.md) | ➤ Reimagine how incomplete death data are used while maintaining accuracy. |

---

## 🔴 Recommendation 5 – Automated UCOD Assignment (IRIS)
| DELIVERABLE | SOURCE FILE | RATIONALE / CONTRIBUTION |
|--------------|--------------|---------------------------|
| **Reassess how to use death data** | [Process Improv.](process-new.md) | ➤ Provide the evidence base for future automated UCOD coding. |
| **Death data** | [Data Improv.](dataset-new.md) | ➤ Linkage plan aligned to IRIS-coded UCOD integration. |

---

## 🟠 Recommendation 6 – Analytics Workflow Redesign
| DELIVERABLE | SOURCE FILE | RATIONALE / CONTRIBUTION |
|--------------|--------------|---------------------------|
| **Automate monthly data extractions of locked cases only** | [Process Improv.](process-new.md) | ➤ Core upstream dependency for automated analytics. |
| **New Analytics Plan** | [Analytic Improv.](analytics-new.md) | ➤ Statistical analysis plan covering the new reporting framework. |
| **Stata code for new reporting framework** | [Analytic Improv.](analytics-new.md) | ➤ Rebuild annual analytics using reusable, modular code blocks. |
| **(DO file) Counts** | [Analytic Improv.](analytics-new.md) | ➤ Hospital CVD cases. |
| **(DO file) Incidence** | [Analytic Improv.](analytics-new.md) | ➤ Hospital CVD event rate. |
| **(DO file) Case Fatality** | [Analytic Improv.](analytics-new.md) | ➤ In-hospital CVD deaths. |
| **(DO file) Length of Stay** | [Analytic Improv.](analytics-new.md) | ➤ Indicator related to health-system performance. |
| **Stata code for optional additional briefings** | [Analytic Improv.](analytics-new.md) | ➤ Modular code blocks for extended reporting. |
| **(DO file) Missing Data** | [Analytic Improv.](analytics-new.md) | ➤ Missing data in the BNR. |
| **(DO file) BNR & National Demographics** | [Analytic Improv.](analytics-new.md) | ➤ BNR in the context of ageing. |
| **(DO file) BNR & International Comparators** | [Analytic Improv.](analytics-new.md) | ➤ BNR in an international context. |
| **Example Stata code for BNR Monitoring** | [Analytic Improv.](analytics-new.md) | ➤ Regular summaries to support operations. |
| **(Monthly DO) Numbers)** | [Analytic Improv.](analytics-new.md) | ➤ Weekly and monthly case / cumulative totals. |
| **Briefing: Cases** | [Reporting Improv.](reporting-new.md) | ➤ Transparent summary of what is happening in hospital. |
| **Briefing: Incidence** | [Reporting Improv.](reporting-new.md) | ➤ Fair comparison over time (accounts for demographic change). |
| **Briefing: Case-Fatality** | [Reporting Improv.](reporting-new.md) | ➤ Proportion dying before discharge. |
| **Briefing: Length-of-Stay** | [Reporting Improv.](reporting-new.md) | ➤ Context on system performance. |
| **Potential Briefing: Missing Data** | [Reporting Improv.](reporting-new.md) | ➤ Levels of missing data among key variables. |
| **Potential Briefing: National Demographics** | [Reporting Improv.](reporting-new.md) | ➤ BNR in demographic context. |
| **Potential Briefing: International Comparisons** | [Reporting Improv.](reporting-new.md) | ➤ BNR in international context. |
| **Potential Briefing: Event Monitoring** | [Reporting Improv.](reporting-new.md) | ➤ Weekly and monthly event monitor. |

---

## 🟠 Recommendation 7 – Data Dictionary and Metadata Management
| DELIVERABLE | SOURCE FILE | RATIONALE / CONTRIBUTION |
|--------------|--------------|---------------------------|
| **REDCap database audit** | [Process Improv.](process-new.md) | ➤ Identify undocumented changes and validation gaps. |
| **REDCap dataset—database alignment** | [Process Improv.](process-new.md) | ➤ Harmonise structures for ongoing exchange. |
| **Data structure** | [Data Improv.](dataset-new.md) | ➤ Standardised dictionary and metadata framework. |
| **Define and describe data sources** | [Data Improv.](dataset-new.md) | ➤ Identify inputs and move toward full data provenance. |

---

## 🟠 Recommendation 8 – Open Standards and Documentation
| DELIVERABLE | SOURCE FILE | RATIONALE / CONTRIBUTION |
|--------------|--------------|---------------------------|
| **Data structure** | [Data Improv.](dataset-new.md) | ➤ Standard metadata documentation in open format. |
| **Dataset dissemination** | [Data Improv.](dataset-new.md) | ➤ SOP for responsible dissemination. |
| **Data sharing** | [Data Improv.](dataset-new.md) | ➤ SOP for data-sharing roles, permissions, approvals. |
| **Dataset storage** | [Data Improv.](dataset-new.md) | ➤ Document secure storage options aligned with law. |

---

## 🟠 Recommendation 9 – Continuous Data-Quality Monitoring
| DELIVERABLE | SOURCE FILE | RATIONALE / CONTRIBUTION |
|--------------|--------------|---------------------------|
| **Duplicates handled within REDCap** / **Use query system within REDCap** | [Process Improv.](process-new.md) | ➤ Routine duplicate tracking and query workflow. |
| **Initiate case-level record lock in database** | [Process Improv.](process-new.md) | ➤ Track verified vs. unverified records. |
| **Automate monthly data extractions of locked cases only** | [Process Improv.](process-new.md) | ➤ Scheduled, quality-controlled extracts. |

---

## 🟢 Recommendation 10 – Automation in Data Abstraction
| DELIVERABLE | SOURCE FILE | RATIONALE / CONTRIBUTION |
|--------------|--------------|---------------------------|
| _No Stage-1 deliverables mapped from current improvement lists._ |  |  |

---

## 🟢 Recommendation 11 – Expansion to Additional Conditions
| DELIVERABLE | SOURCE FILE | RATIONALE / CONTRIBUTION |
|--------------|--------------|---------------------------|
| _No Stage-1 deliverables mapped from current improvement lists._ |  |  |

---

## 🟢 Recommendation 12 – Research Analytics Workstream
| DELIVERABLE | SOURCE FILE | RATIONALE / CONTRIBUTION |
|--------------|--------------|---------------------------|
| **Reassess how to use death data** | [Process Improv.](process-new.md) | ➤ Groundwork for mortality linkage and research. |
| **Death data** | [Data Improv.](dataset-new.md) | ➤ Plan for integrating death data into research-ready datasets. |

---

## 🟢 Recommendation 13 – Revamped Reporting Framework
| DELIVERABLE | SOURCE FILE | RATIONALE / CONTRIBUTION |
|--------------|--------------|---------------------------|
| **New Analytics Plan** | [Analytic Improv.](analytics-new.md) | ➤ Statistical blueprint for reports. |
| **Stata code for new reporting framework** | [Analytic Improv.](analytics-new.md) | ➤ Modular code for annual analytics. |
| **Stata code for optional additional briefings** | [Analytic Improv.](analytics-new.md) | ➤ Extendable analytics for future reports. |
| **Example Stata code for BNR Monitoring** | [Analytic Improv.](analytics-new.md) | ➤ Reusable operational summaries. |
| **Briefing: Cases** | [Reporting Improv.](reporting-new.md) | ➤ Core briefing. |
| **Briefing: Incidence** | [Reporting Improv.](reporting-new.md) | ➤ Core briefing. |
| **Briefing: Case-Fatality** | [Reporting Improv.](reporting-new.md) | ➤ Core briefing. |
| **Briefing: Length-of-Stay** | [Reporting Improv.](reporting-new.md) | ➤ Core briefing. |
| **Potential Briefing: Missing Data** | [Reporting Improv.](reporting-new.md) | ➤ Optional briefing. |
| **Potential Briefing: National Demographics** | [Reporting Improv.](reporting-new.md) | ➤ Optional briefing. |
| **Potential Briefing: International Comparisons** | [Reporting Improv.](reporting-new.md) | ➤ Optional briefing. |
| **Potential Briefing: Event Monitoring** | [Reporting Improv.](reporting-new.md) | ➤ Optional briefing. |

---

## 🟢 Recommendation 14 – Sustainability and Governance Enhancements
| DELIVERABLE | SOURCE FILE | RATIONALE / CONTRIBUTION |
|--------------|--------------|---------------------------|
| **Develop process for final case review and sign-off** | [Process Improv.](process-new.md) | ➤ Governance at the point of data approval. |
| **Dataset release** | [Data Improv.](dataset-new.md) | ➤ Controlled, traceable approvals for dataset use. |
| **Dataset sign-off** | [Data Improv.](dataset-new.md) | ➤ Approval confirmation prior to analysis. |
| **Dataset dissemination** | [Data Improv.](dataset-new.md) | ➤ Responsible data dissemination procedures. |
| **Data sharing** | [Data Improv.](dataset-new.md) | ➤ SOP governing sharing activities. |
| **Data Sharing / Data Trust Agreements** | [Data Improv.](dataset-new.md) | ➤ Formalise agreements on data use and governance. |
| **Dataset storage** | [Data Improv.](dataset-new.md) | ➤ Secure storage guidance aligned with protection laws. |

<br>
