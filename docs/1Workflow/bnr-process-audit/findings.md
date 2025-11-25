# BNR Process Audit: Findings

The [Executive Summary](index.md) presents the key findings from the Barbados National Registry (BNR) Process Audit, conducted as part of the ongoing system refit to enhance efficiency, accuracy, and sustainability. The audit’s initial focus was on post-REDCap activities—particularly the Stata-based analysis and reporting algorithms used for the cardiovascular disease (CVD) registry.  

During this review, several fundamental issues were identified in the underlying dataset and related processes. These revealed that some challenges affecting data accuracy originate earlier in the data pipeline—within data collection, quality control, and database design. In consultation with the BNR Technical Lead, the scope of work was therefore expanded to assess the broader data process, from case capture through to reporting.  

This review was undertaken to strengthen the efficiency, accuracy, and long-term sustainability of the Barbados National Registry’s Cardiovascular Disease (BNR–CVD) system. It builds on strong national progress since the registry’s establishment and responds to new opportunities to modernise data capture, quality control, and reporting as Barbados moves further into the digital era.

This review provides an integrated assessment of technical and procedural systems supporting the generation of BNR outputs. The findings offer practical steps toward a more reliable, efficient, and sustainable registry.

!!! info "Project Deliverables"
    The proposed consultancy deliverables are detailed in the following website pages:  [Process Improvements](../updates/process-new.md) ○ [Data Improvements](../updates/dataset-new.md) ○ [Analytics Improvements](../updates/analytics-new.md) ○ [Reporting Improvements](../updates/reporting-new.md) ○ [Improvements by Audit Recommendation](../updates/recommendations-new.md).

---

## 1. Our Methods
The process audit was undertaken to assess the efficiency, reliability, and coherence of the Barbados National Registry (BNR) data-handling and analytics systems, to inform the forthcoming refit of the cardiovascular registry (BNR-CVD).

### Scope and Design

The audit was originally conceived as a review of the BNR-CVD analytics workflow—specifically, the Stata-based data processing algorithms used to produce routine reports. However, early examination of these algorithms identified upstream data-quality challenges that affected downstream analytics. Accordingly, the scope was broadened to include all aspects of post-abstraction data handling: dataset creation, version control, data cleaning, coding conventions, storage, analytics, and reporting.

### Approach

This was a desk-based, documentary review drawing on internal BNR documents, datasets, and process records. The audit team reviewed existing workflows, code files, data management documentation, standard operating procedures (SOPs), and output reports to assess consistency, efficiency, and accuracy. Where appropriate, algorithms were duplicated in a controlled test environment and “stress-tested” to confirm functional integrity and reproducibility. A structured framework was used to guide assessment, covering:

- **Process** – completeness of documentation and alignment with current practice. Integration between data capture, curation, and reporting systems.

- **Data** – governance processes for dataset sign-off, storage, and change tracking.

- **Analytics** – structure, readability, efficiency, and internal logic of Stata code.

- **Reporting** – timeliness, usefulness, reporting gaps, dissemination strategies.

### Evidence Sources

Evidence was drawn from a combination of registry documentation (including SOPs, annual and quarterly reports, and process manuals), existing code and datasets, and internal correspondence relating to data release and reporting cycles. The review also drew on insights from earlier process reviews (2018 and 2019) and relevant publications describing the BNR methodology and evolution.

### Analysis

Each process element was evaluated for clarity, efficiency, and risk of data loss or error propagation. The audit identified dependencies between stages and prioritised recommendations based on feasibility, impact, and alignment with contractual obligations. Further improvement plan stages have been proposed to account for recommendations that fall outside the scope of this initial consultancy.

### Limitations and Next Steps

This was a desk-based assessment without direct staff interviews or observation of live workflows. Consequently, the findings reflect documented and testable practice rather than day-to-day implementation. The next phase should include semi-structured interviews with key stakeholders to validate findings, explore contextual factors influencing workflow, and refine recommendations for sustainable system improvement.

## 1. Overview of Major Findings

The audit identified a limited number of high-impact issues that collectively constrain the accuracy, reproducibility, and timeliness of BNR outputs. The findings are grouped according to the three main stages of the data process:

- **Case Capture and Preparation (Pre-REDCap)** – activities before data entry, including case finding, eligibility checks, and death-data management.  
- **Data Entry and Quality Control (Within-REDCap)** – activities linked to database design, data entry, and internal validation or cleaning.  
- **Analysis and Reporting (Post-REDCap)** – activities after data export, including dataset curation, analytics, and report generation.

Each table summarises the issues, their relative urgency, and their implications for the national data system.

### Priority Scale

|| **Priority** | **Definition** |
|-|---------------|----------------|
|🔴| **Critical** | Should be addressed immediately to stabilise the registry, protect data integrity, or prevent reporting errors. |
|🟠| **High** | Major improvements to strengthen data quality, governance, and efficiency; begin once critical actions are underway. |
|🟢| **Medium** | Developmental or strategic actions to enhance sustainability, scalability, and research capacity. |

---

## (a) Case Capture and Preparation (Pre-REDCap)

| **Priority / Issue** | **What’s Happening** | **Why It Matters** |
|-----------------------|----------------------|--------------------|
| 🔴 **Death data not yet fit for purpose** | The registry depends on death certificate data abstracted by the BNR team from hard copy records at the Barbados Registrar General. While all deaths are medically certified, the underlying cause of death (UCOD)—formally coded using internationally-accepted rules—is not provided by the Barbados Government. The current registry workaround—keyword searches of free text—does not achieve the precision or reproducibility required for national or WHO reporting. | The absence of coded UCOD data limits the accuracy of mortality statistics and complicates linkage between deaths and prior events. |
| 🔴 **Inconsistent inclusion criteria** | Definitions of “eligible” and “ineligible” cases have varied over time, and trace-back periods before dataset closure have been inconsistently applied. | These inconsistencies affect the comparability of trends and can distort incidence estimates. |
| 🟠 **Weak duplication controls at abstraction** | Current case-finding procedures do not consistently include a step to check for existing records before creating new entries. | Duplicated records can inflate event counts and compromise trend accuracy. |
| 🟢 **Loss of historical identifiers (2009–2017)** | Certain analysis files have lost key identifiers over time due to the blending of data cleaning and analytical processes and limited control of Stata algorithms. While most (**potentially not all**) identifiers remain in the source data, their removal from intermediate files has complicated longitudinal linkage and required retrospective reconstruction to restore completeness. | Missing identifiers reduce the ability to assess repeat events and survival.<br/><br/>It remains possible that datasets without full age information have been used in past annual reports. |

!!! warning "Most Urgent Actions (Recommendations 3–5 - See Below)"
    - Re-establish a **hospital-based registry model** to ensure consistent, verifiable case capture of incident cases.  
    - Introduce and lead on national **UCOD assignment** using World Health Organization IRIS software.  
    - Standardise eligibility definitions and strengthen duplicate checking as a key part of the abstraction process.
    - Build and document a single cumulative data record (2009-2023)

**Summary:**  
The pre-REDCap phase presents several foundational data-quality risks that directly affect national comparability. Addressing these will require structural adjustments rather than additional resources. The registry can move quickly toward improvement through a quality-managed hospital-based verification process, standardised inclusion rules, and adoption of IRIS for formal UCOD coding—changes that will align BNR methods with international best practice.

---

## (b) Data Entry and Quality Control (Within-REDCap)

| **Priority / Issue** | **What’s Happening** | **Why It Matters** |
|-----------------------|----------------------|--------------------|
| 🔴 **2023 database rebuild left incomplete** | The database remained in *“development”* mode during live use, allowing field edits and changes without formal version control. | This has caused variation in variable meaning and reduced the reliability of year-on-year comparison. |
| 🔴 **Limited in-system data validation** | Required-field and logic checks were removed for several variables during updates. | The absence of automated validation increases risk of missing or inconsistent values. |
| 🟠 **Minimal documentation of variable definitions** | There is no unified data dictionary, and field meanings have diverged over time. | Analysts cannot always verify which variable versions are current, making automation and reproducibility difficult. |
| 🟠 **Incomplete REDCap-level data cleaning** | Within-REDCap cleaning and verification have not yet been consistently implemented. | Errors that should be intercepted during data entry QC instead appear at the analysis stage, creating additional workload, reporting delays, and potential for error. |

!!! warning "Most Urgent Actions (Recommendations 2 & 7 - See Below)"
    - **Lock the production REDCap version** and reinstate automated validation.  
    - Develop and maintain a **comprehensive data dictionary and metadata log**.  
    - Reinforce feedback loops between abstraction and quality control.

**Summary:**  
Quality assurance within REDCap has weakened due to incomplete validation, undocumented variable changes, and limited feedback mechanisms. These gaps are correctable and will deliver immediate gains in efficiency and reliability once validation rules and documentation standards are restored. Strengthening this phase will provide the backbone for future automation and consistent monthly reporting.

---

## (c) Analysis and Reporting (Post-REDCap)

| **Priority / Issue** | **What’s Happening** | **Why It Matters** |
|-----------------------|----------------------|--------------------|
| 🔴 **No definitive cumulative dataset** | The historical CVD record has never been finalised or version-controlled. Multiple parallel copies exist&mdash;regularly with subtle variation&mdash;in different folders. | Analysts cannot be confident which dataset is authoritative, undermining reproducibility. |
| 🟠 **Persistent missingness in key fields** | Some identifiers and event dates remain incomplete even after recovery efforts. | Missing data reduce the accuracy of linkages and downstream analytics. |
| 🟠 **Dependence on legacy Stata code** | Stata `.do` files combine cleaning and analysis and have evolved incrementally. | Each export requires modification, increasing risk of error and reducing analytic efficiency. |
| 🟢 **Lack of dataset release and sign-off process** | There is no consistent process for dataset approval prior to analysis. | Without an approval mechanism, unverified data may enter analyses or reports. |

!!! warning "Most Urgent Actions (Recommendations 1, 6 & 13 - See Below)"
    - Establish a **single, version-controlled cumulative dataset** with formal sign-off.  
    - **Redesign the analytics workflow** to separate cleaning from analysis.  
    - Introduce **shorter, more frequent reporting cycles** that can flag quality issues early.

**Summary:**  
The post-REDCap phase requires clear data governance and modernisation of the analytic workflow. The absence of a definitive dataset and reliance on legacy scripts limit transparency and efficiency but can be resolved through version control, automation, and clearer dataset release procedures. These changes will substantially increase confidence in reported national figures.

---

## 2. Recommendations

### Priority Scale

|| **Priority** | **Definition** |
|-|---------------|----------------|
|🔴| **Critical** | Should be addressed immediately to stabilise the registry, protect data integrity, or prevent reporting errors. |
|🟠| **High** | Major improvements to strengthen data quality, governance, and efficiency; begin once critical actions are underway. |
|🟢| **Medium** | Developmental or strategic actions to enhance sustainability, scalability, and research capacity. |

---

### Summary Table of Recommendations

| **No.** | **Focus Area** | **Key Actions** | **Intended Outcome** |
|:--:|----------------------|-----------------|----------------------|
| **1** | 🔴 **Dataset Governance and Version Control** | • Approve a definitive cumulative dataset (to Dec 2023) as the single official record.<br>• Implement dataset sign-off protocols and release logs.<br>• Apply version numbering to all analytical datasets. | A verified, auditable foundation for all future analyses and reporting. |
| **2** | 🔴 **REDCap Quality Controls** | • Lock the production database and reinstate validation rules.<br>• Reintroduce required fields and range checks.<br>• Produce monthly REDCap data-quality snapshots. | Improved accuracy and early detection of issues at the point of entry. |
| **3** | 🔴 **Core Variable Set Definition** | • Identify and protect a 30–40-variable Core Dataset essential for reporting.<br>• Prioritise validation of these variables before others. | Completeness of the most critical indicators for national health monitoring. |
| **4** | 🔴 **Pre-REDCap Process and Hospital-Based Re-focus** | • Revert to a hospital-only based model for verified case capture.<br>• Treat annual mortality separately until formal UCOD coding is implemented.<br>• Formalise collaboration with MoHW on UCOD-data sharing. | Reliable incidence monitoring and improved consistency in data capture. |
| **5** | 🔴 **Formal UCOD Assignment (IRIS)** | • Test then implement WHO-endorsed **IRIS** software for UCOD coding.<br>• Train designated BNR and MoHW staff.<br>• Establish a quarterly reconciliation process. | A national automated mortality-coding capability meeting WHO standards.<br/><br/>Would represent a new national public good. |
| **6** | 🟠 **Analytics Workflow Redesign** | • Separate data-cleaning scripts from analysis scripts.<br>• Introduce modular, annotated Stata programs.<br>• Automate production of tables, figures and (optionally) dashboards. | Faster, reproducible, and transparent analysis workflows. |
| **7** | 🟠 **Data Dictionary and Metadata Management** | • Create a unified, version-controlled data dictionary.<br>• Archive (if possible) all prior definitions and mappings.<br>• Assign a metadata steward for ongoing maintenance. | Greater transparency and cross-year comparability of variables. |
| **8** | 🟠 **Open Standards and Documentation** | • Transition documentation from proprietary tools (eg. OneNote) to open standards (Markdown, MkDocs, GitHub) to open-publish BNR methods.<br>• Adopt international coding standards at all times (e.g. ICD-10/11, WHO HEARTS). | Sustainable, accessible documentation aligned with global open-data and open-science practice. |
| **9** | 🟠 **Continuous Data-Quality Monitoring** | • Re-assert/implement within-database checks for missingness, duplicates, and validation breaches.<br>• Publish a monthly data-quality report (optionally dashboard).<br>• Integrate metrics into BNR performance monitoring. | Moves the registry from reactive correction to continuous improvement. |
| **10** | 🟠 **Automation in Data Abstraction** | • Continue to explore the extent of possible abstraction automation.<br>• Pilot test for high-volume variables such as admission/discharge data. | Reduced manual workload and improved timeliness of updates. |
| **11** | 🟢 **Expansion to Additional Conditions** | • With QEH partners, pilot simplified modules for injury or other high-priority conditions.<br>• Conduct feasibility assessments before scaling. | Incremental broadening of surveillance capacity using existing structures. |
| **12** | 🟢 **‘Research Analytics’ Workstream** | • Establish periodic research cycles (e.g., every 3–5 years) for survival analysis and linkage studies.<br>• Keep outside routine operations. | Supports in-depth research while protecting routine registry stability. |
| **13** | 🟢 **Revamped Reporting Framework** | • Develop shorter, visually clear quarterly or bi-annual reports.<br>• Retain an annual detailed technical report.<br>• Introduce infographics for broader communication. | Timely, accessible outputs supporting evidence-based decision-making. |
| **14** | 🟢 **Sustainability and Governance Enhancements** | • Define and document registry roles and responsibilities.<br>• Maintain a formal risk log and review report (optionally dashboard) quarterly.<br>• Schedule independent audits every 2–3 years. | Institutionalises accountability and continuous system improvement. |

---

### Implementation Stages

| **Stage** | **Timeline** | **Primary Focus** |
|------------|--------------|-------------------|
| **Stage 1** | 0–9 months | Implement all 🔴 *Critical* actions: governance, REDCap controls, hospital-based focus, IRIS deployment, and core-variable protection. |
| **Stage 2** | 9–18 months | Deliver 🟠 *High-priority* actions: analytics redesign, metadata management, open documentation, abstraction automation, and dashboards. |
| **Stage 3** | 36 months | Advance 🟢 *Medium-term* goals: expanded condition modules, research analytics stream, refreshed reporting, and governance consolidation. |

---

### Core Variable Set (for Early Stabilisation)

- Patient identifiers (NRN, hospital ID, DOB, sex, age groups)  
- Event identifiers (event type, dates of onset/admission/discharge)  
- Diagnostic confirmation (ICD-10/11 codes, test results)  
- Vital status at discharge, date of death if applicable  
- Primary risk factors (hypertension, diabetes)  
- Facility-level metrics (such as overall admission levels)

This **minimum viable dataset** supports monthly reporting, automation, and cross-year comparability while extended variables (further treatment information) are progressively standardised.

---

## 3. National Gains and Future Outlook

The audit identifies serious and correctable challenges but also outlines clear national benefits that will result from implementing the recommended actions. These gains extend beyond the registry to the wider health system and data ecosystem of Barbados.

| **Area of Progress** | **Expected National Gain** |
|-----------------------|----------------------------|
| **Reliable National Datasets** | A verified, reproducible record of cardiovascular disease incidence and outcomes, forming the basis for policy and international reporting. |
| **Formal Mortality Coding (IRIS)** | A national UCOD system aligned with WHO standards, improving the completeness and international comparability of Barbados death data. |
| **Modernised Analytics and Reporting** | Faster, clearer reports supporting evidence-based decisions and continuous monitoring of health-service performance. |
| **Open, Interoperable Documentation** | Transition to open data standards and transparent documentation ensures sustainability and reduces reliance on proprietary systems. |
| **Integration and Research Potential** | A data platform capable of linking with other national health datasets and supporting collaborative research across the Caribbean. |

**In summary:**  
The BNR stands at a pivotal point. The actions proposed in this audit will stabilise the registry, restore confidence in its outputs, and enable it to evolve into a modern, fully auditable national health information asset. By implementing these reforms, Barbados will be among the first small island developing states with a digitally ready registry that meets international data standards and supports long-term, data-driven decision-making.

<br>
