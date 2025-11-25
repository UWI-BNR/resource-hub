# Process Changes

**Notes:**  

1. Suggestions for process change that occur *before* REDCap entry or *within* the REDCap environment itself are **beyond the scope** of this post-REDCap project.  
2. The process changes listed below are vital to ensure the BNR Refit automation remains usable into the future. The entire system depends on the continued ability to automatically extract and append new cases to a standard-structure cumulative dataset.

**Key:**  ❌ Not started 🟨 Underway ✅ Completed

| SUGGESTED CHANGE | RATIONALE | HOW WILL WE HELP | RESOURCE | **LINKED RECOMMENDATIONS** |
|--------------|---------|------------------|--------------|-----------------------------|
| **REDCap database audit** | ➤ The database structure has been changed repeatedly without a full change record.<br>➤ An audit will identify discrepancies and reset to best practice. | ⓘ Advise | 🟨 <br>[See Data Handling Process Audit](../bnr-process-audit/index.md) | 🔴 **Rec 2** (REDCap Quality Controls)<br>🟠 **Rec 7** (Data Dictionary & Metadata Management) |
| **REDCap database alignment** | ➤ The cumulative dataset now aligns with the current REDCap database, but additional harmonisation is likely required. | ⚙ Contribute | ❌ <br>[See data dictionary](../../Data/structure.md) | 🔴 **Rec 1** (Dataset Governance)<br>🟠 **Rec 7** (Data Dictionary & Metadata Management) |
| **Duplicates handled within REDCap**<br><br>**Use query system within REDCap** | ➤ Manage and resolve duplicate cases at source rather than post-export.<br>➤ Re-establish the internal REDCap query and resolution workflow.<br>➤ Restore clear separation between data cleaning (within REDCap) and analytics (post-REDCap). | ⓘ Advise | ❌ | 🟠 **Rec 2** (REDCap Quality Controls)<br>🔴 **Rec 3** (Core Variable Set)<br>🟠 **Rec 9** (Continuous Data-Quality Monitoring) |
| **Develop process for final case review and sign-off** | ➤ To ensure all fields are complete and verified by a senior staff member before dataset release. | ⓘ Advise | 🟨 <br>[See dataset release process (Step 5)](../../Data/dataset-release.md) | 🔴 **Rec 1** (Dataset Governance & Version Control)<br>🟢 **Rec 14** (Sustainability & Governance Enhancements) |
| **Initiate case-level record lock in database** | ➤ To prevent further edits to verified records and protect integrity before export.<br>➤ To designate records as ready for extraction. | ⓘ Advise | ❌ | 🔴 **Rec 2** (REDCap Quality Controls)<br>🟠 **Rec 9** (Continuous Data-Quality Monitoring) |
| **Reduce number of database variables further** | ➤ To simplify the data model and improve long-term maintainability of the system. | ⓘ Advise | ❌ | 🔴 **Rec 3** (Core Variable Set Definition)<br>🟢 **Rec 13** (Revamped Reporting Framework) |
| **Automate monthly data extractions of locked cases only** | ➤ To ensure each extraction is clean, reproducible, and limited to verified data ready for reporting. | 🗹 Lead | ❌ | 🔴 **Rec 1** (Dataset Governance)<br>🟠 **Rec 6** (Analytics Workflow Redesign)<br>🟠 **Rec 9** (Continuous Data-Quality Monitoring) |
| **Reassess how to use death data** | ➤ To evaluate death record completeness and the most appropriate method for use in future analytics. | 🗹 Lead | 🟨 <br>[See statistical analysis plan](../../3Reporting/sap.md) | 🔴 **Rec 4** (Hospital-Based Re-focus)<br>🔴 **Rec 5** (Automated UCOD Assignment – IRIS)<br>🟢 **Rec 12** (Research Analytics Workstream) |

<br>
