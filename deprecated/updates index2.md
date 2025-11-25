# Summarising the Refit changes

The BNR Refit Project is our step-by-step plan to modernise how we handle, analyse, and report national cardiovascular disease (CVD) data. It builds on more than a decade of registry experience and turns what was once a heavily manual process into one that is cleaner, faster, and so hopefully easier to maintain. I
    
The work is divided into five phases, each one laying the foundation for the next and connecting directly to the process, data, automation, analytics, reporting, and KPI changes that follow.

**Phase 0 – Building the foundation:**

We began by cleaning and combining all existing CVD datasets to create one complete cumulative record from the registry’s first year through to December 2023. This work produced a single *“source of truth”* dataset and the first set of reusable Stata scripts, forming the base for later automation.

**Phase 1 – Understanding our system:**  

Next, focussing on *Analysis & Reporting* (the post-REDCap phase), we had planned to examine active *pre-Refit* Stata analysis algorithms. 

➤ During this initial review, several fundamental issues were identified in the underlying dataset and related processes, revealing that process challenges affecting data accuracy originated earlier in the data pipeline—within data collection, quality control, and database design. In consultation with the BNR Technical Lead, the scope of work was therefore expanded to assess the broader data process, from case capture through to reporting. The work was also expanded to include **Phase 0**, described above.

**Phase 2 – Automating our analytics:**  

After these first foundational phases, we moved on to redesigning how the data are analysed. We created Stata programs that can run monthly and perform analyses with complete reproducibility and some level of automation. The automation removed the previous reliance on new algorithms for each analysis (primarily because of bespoke data cleaning), hopefully improving the consistency and timliness of results.

**Phase 3 – Making the system accessible:**  

To make sure staff can use the new tools without advanced coding skills, we had planned to build easy-to-install BNR Stata commands. These would have provided “low-code” access to the automated analytics and reports, making the system more inclusive and sustainable over time. 

➤ Because of process limitations identified during the **Phase 1** system audit, in consultation with the BNR Technical Lead we opted to defer this additional automation in favour of implementing several of the critical recommendations indentified in the Process Audit - see the audit [Executive Summary](../bnr-process-audit/index.md), see the audit [Full Findings](../bnr-process-audit/findings.md)). 

**Phase 4 – Sharing knowledge:**  

Finally, we developed an open-access Refit knowledge base to help BNR staff and external stakeholders understand the new system confidently. This is provided by an online website, ensuring that the knowledge behind the system is openly shared for the future.

Together, these phases mark the start of a shift from a person-dependent system to a process-driven one—where clean data, clear documentation, and simple automation keep the registry stronger for the longer term.  

➡️ Explore the next sections to see how each area of change unfolds: [Process Improvements](process-new.md) ○ [Data Improvements](dataset-new.md) ○ [Analytics Improvements](analytics-new.md) ○ [Reporting Improvements](reporting-new.md) ○ [Improvements by Audit Recommendation](../updates/recommendations-new.md).

<br>
