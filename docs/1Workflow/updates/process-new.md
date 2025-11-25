---
hide:
#  - navigation
  - toc
---

# Process Improvements

## Introduction

!!! info "Check this page for weekly updates on refit progress"

This section outlines the process improvements that will stabilise and strengthen the BNR workflow as part of *Stage 1 of the BNR Refit*. These actions focus on the foundational steps needed to secure data integrity — rebuilding validation, restoring record control, and ensuring each exported dataset is verified and analysis-ready.  

Each item below is linked to a specific recommendation from the BNR Process Audit and will feed into later stages of the refit: *Stage 2 – Modernise and Automate*, where redesigned analytics and automation will be implemented, and *Stage 3 – Sustain and Expand*, where governance and long-term operational processes will be institutionalised.  

### How Will We Help

The *“How Will We Help”* column indicates the level of engagement for each activity under *Stage 1 of the BNR Refit*. While the refit’s initial scope focused on post-REDCap processes, the audit highlighted wider opportunities for improvement that will continue across later stages of implementation.

| **Icon** | **Meaning** | **Interpretation within the Refit Programme** |
|-----------|--------------|----------------------------------------------|
| 🗹 **Lead** | Tasks delivered directly within this consultancy’s scope. | Core actions already funded and underway as part of Stage 1. These lay the technical foundation for later phases. |
| ⚙ **Contribute** | Tasks that extend beyond the formal project scope but are closely connected to Stage 1 goals. | The team provides targeted technical input or coordination support to help maintain alignment across the wider refit. |
| ⓘ **Advise** | Tasks primarily owned by partners or future workstreams. | The team offers strategic guidance and documentation to support smooth handover into subsequent stages of the refit. |

Together, these process improvements form the operational base on which the refit’s later automation and governance systems will be built.

---

### The Process Improvements

**Key:**  ❌ Not started 🟨 Underway ✅ Completed

| SUGGESTED CHANGE | RATIONALE | HOW WILL WE HELP | RESOURCE | **LINKED RECOMMENDATIONS** |
|--------------|---------|------------------|--------------|-----------------------------|
| **REDCap database audit** | ➤ The database structure has been changed repeatedly without a full change record.<br>➤ An audit will identify discrepancies and reset to best practice. | ⓘ Advise | ✅ <br>[See Data Handling Process Audit](../bnr-process-audit/index.md) | 🔴 **Rec 2** (REDCap Quality Controls)<br>🟠 **Rec 7** (Data Dictionary & Metadata Management) |
| **REDCap<br/>dataset&mdash;database alignment** | ➤ The cumulative dataset must be re-aligned to mimic the structure of the current (as of Nov-2025) REDCap database. Harmonisation is required. | 🗹 Lead | ✅ <br>[See data dictionary](../../2Data/dataset/structure.md) | 🔴 **Rec 1** (Dataset Governance)<br>🟠 **Rec 7** (Data Dictionary & Metadata Management) |
| **Reassess how to use death data** | ➤ To evaluate death record completeness and the most appropriate method for use in future analytics. | ⚙ Contribute | ✅ <br>[See statistical analysis plan](../../3Reporting/analytics/index.md) | 🔴 **Rec 4** (Hospital-Based Re-focus)<br>🔴 **Rec 5** (Automated UCOD Assignment – IRIS)<br>🟢 **Rec 12** (Research Analytics Workstream) |
| **Develop process for final case review and sign-off** | ➤ To ensure all fields are complete and verified by a senior staff member before dataset release. | ⚙ Contribute | 🟨 <br>[See dataset release process (Step 5)](../../2Data/dataset-release.md) | 🔴 **Rec 1** (Dataset Governance & Version Control)<br>🟢 **Rec 14** (Sustainability & Governance Enhancements) |
| **Automate monthly data extractions of locked cases only** | ➤ To ensure each extraction is clean, reproducible, and limited to verified data ready for reporting. | 🗹 Lead | ❌ | 🔴 **Rec 1** (Dataset Governance)<br>🟠 **Rec 6** (Analytics Workflow Redesign)<br>🟠 **Rec 9** (Continuous Data-Quality Monitoring) |
| **Duplicates handled within REDCap**<br><br>**Use query system within REDCap** | ➤ Manage and resolve duplicate cases at source rather than post-export.<br>➤ Re-establish the internal REDCap query and resolution workflow.<br>➤ Restore clear separation between data cleaning (within REDCap) and analytics (post-REDCap). | ⓘ Advise | ❌ | 🟠 **Rec 2** (REDCap Quality Controls)<br>🔴 **Rec 3** (Core Variable Set)<br>🟠 **Rec 9** (Continuous Data-Quality Monitoring) |
| **Initiate case-level record lock in database** | ➤ To prevent further edits to verified records and protect integrity before export.<br>➤ To designate records as ready for extraction. | ⓘ Advise | ❌ | 🔴 **Rec 2** (REDCap Quality Controls)<br>🟠 **Rec 9** (Continuous Data-Quality Monitoring) |
| **Reduce number of database variables further** | ➤ To simplify the data model and improve long-term maintainability of the system. | ⓘ Advise | ❌ | 🔴 **Rec 3** (Core Variable Set Definition)<br>🟢 **Rec 13** (Revamped Reporting Framework) |

<br>
