
# BNR Process Audit: Executive Summary

This executive summary presents the key findings from the Barbados National Registry (BNR) Process Audit, conducted as part of the ongoing system refit to enhance efficiency, accuracy, and sustainability. The initial remit of this audit focused exclusively on post-REDCap activities—specifically, the review and updating of Stata analysis algorithms used for data extraction, cleaning, and reporting from the cardiovascular disease (CVD) database.

During this review, however, several critical issues were identified in the underlying dataset and related data-handling processes. These findings revealed that many of the challenges affecting data analysis originate earlier in the data pipeline, within processes of data collection, quality control, and database design. Accordingly, and in consultation with the BNR Technical Lead, the scope of this audit was extended to include process-level considerations—covering data flow, database architecture, data cleaning practices, and governance mechanisms underpinning the BNR-CVD system.

This expanded audit therefore provides an integrated assessment of both technical and procedural systems that support the generation of BNR analytics and reports. The sections that follow summarise the major findings, highlight cross-cutting issues affecting data quality and workflow, and propose key actions to strengthen the reliability and efficiency of the BNR data environment.    


!!! info "Project Deliverables"

    The proposed consultancy deliverables are detailed in the following website pages:  [Process Changes](../updates/process-new.md) ○ [Data Changes](../updates/dataset-new.md) ○ [Analytics Changes](../updates/analytics-new.md) ○ [Reporting Changes](../updates/3Reporting-new.md).

## 1. Major Findings
The audit identified a small number of high-impact issues that together limit the accuracy, reproducibility, and timeliness of BNR outputs. These include inconsistencies in variable naming and dataset structure between years, incomplete or ambiguous data entry fields within REDCap, and non-standardised procedures for dataset “sign-off” prior to analysis. Several Stata .do files rely on legacy dataset formats, creating downstream inefficiencies and errors in automated reporting. Importantly, many of these problems stem from upstream process gaps—particularly in data validation at the point of abstraction and in the management of database version control.

We present a series of issues under the following three process-driven headings. 

- **Pre-REDCap.** Activities occuring before data are entered in REDCap 
- **Within-REDCap.** Activities related to REDCap data entry and data cleaning
- **Post-REDCap.** Activities occuring after data have been exported from REDCap
  
## (a) Pre-REDCap Findings
|#| ISSUE | DESCRIPTION | CONSEQUENCE |
|--- | ---- | ---- | --- |
|x| Death data not currently fit for purpose | ➤ Problem exists because underlying CoD (UCOD) not provided by MoHW.<br>➤ The current BNR solution is flawed in several ways:
|| | ➤➤ (a) BNR opts for post-REDCap data cleaning. This mixes data prep + analytics. | ➤ Proposed analytics automation becomes difficult. Each monthly export requires updated data cleaning `.do` files. More automation = more points of failure.| 
|| | ➤➤ (b) The current BNR approach uses all listed causes, not UCOD. Will likely overestimate UCOD | ➤ Simply. We don't know... Sensitivity work required.|
|| | ➤➤ (c) Also, with a proportion of the data having missing Names and National IDs between 2009 and 2017, DCOs become more likely, as linking a death to a previous event becomes less likely.  | ➤ Bottom-up re-vamp of the UCOD assignment necessary.<br>➤ Until then, hospital-based registry reporting advised |
| | | ➤➤ (d) The current BNR UCOD approach also ignores the 'proximal / causal' importance of free text. It simply finds keywords. So terms like *due to*, *secondary to*, *as a result of* and so on, are probably ignored. These are key for UCOD coding. | ➤ Again - implications unclear at this point.|

## (b) Within-REDCap Findings
|#| ISSUE | DESCRIPTION | CONSEQUENCE |
|--- | ---- | ---- | --- |
|x | The 2023 REDCap database revamp | ➤ Poorly executed. <br />➤ System left in development throughout - changes therefore not audited by our system<br /> | ➤ We know of some consequences. Perhaps not all... <br />➤ Certain key variables underwent change of meaning. We will create a mapping of key variables.<br /> |
|x| Within-REDCap data cleaning process seems minimal, or at best incomplete. | ➤ Within-REDCap data cleaning has - at least in part - broken down. <br>➤ Or perhaps within-REDCap data processing was never fully initiated by the BNR leads? | ➤ This problem - over the years - has been patched by mixing post-REDCap data cleaning with analytics.<br />➤ This has created *"hard to manage"* analytical code that needs substantial alteration for each analysis run. <br />➤ Code recycling (without implementing those important alterations) has likely led to analysis errors.<br />➤ Potentially, old errors are being re-introduced |

## (c) Post-REDCap Findings

|#| ISSUE | DESCRIPTION | CONSEQUENCE |
|--- | ---- | ---- | --- |
|x | There is no definitive historical CVD dataset release (that we can find) | ➤ The BNR historical record has never been organised, and in disarray. <br />➤ Process documentation and dataset documentation, if they exist, are lost in the unorganised folder structures. | ➤ We are *'patching together'* our best guess of the historical data record.<br />➤ To some extent, we are doing the same for process, but this goes beyond the Refit scope. |
|x| As yet unfixed missingness | ➤ Identifiable information (IDs, names, dates) for the historical data record **(*2009 to 2017*)** remain missing | ➤ We have created new IDs. <br />➤ But this affects (e.g.) repeat strokes. <br />➤ **With time**, we hope to find the indentifiable historical record - work will be required to develop a definitive cumulative dataset following the 2023 database structure. |
|x| The planned Refit automation will rely on *dataset invariance*         | ➤ In this work, we had planned to append new cases to the cumulative data record each month.<br />➤ Each new monthly addition must have the same structure as the cumulative record. | ➤ Currently, data messyness within REDCap will likely be problematic.<br />➤ We are correcting the cumulative record to Dec 2023. Thereafter, with no *within-REDCap* process improvements, errors will likely re-appear |

## 2. Major Recommendations

| | Idea | Description |
|--- | --------------------------------------------------- | ------------------------------------------------------------ |
| | As part of this Refit, we could develop a longer-term *'Staged Improvement Plan'* | ➤ We create an uber Refit plan, with several major steps. <br/>➤ This consultancy would likely be Stage 1. Further stages will be needed, but I imagine will need Advisory Committee involvement?|
| | Initially (Stage 1?), reduce level of planned automation | ➤ We can improve project analytics a lot **without** full automation. A full set of *analysis only* `.do` files will be a huge improvement, without accompanying `.ado` files, menuing, or dialogue boxes. <br/>➤ More automation at this point = more points of failure.<br/>➤ Careful use of `do` files by approved personnel should be fine. |
| | Create new monthly outputs for continuous reporting | ➤ With monthly data exports - *I'll assume these will be possible without (or with minimal) errors at this point* - we could create a new series of **continuous output** results from the BNR - simple counts, smoothed incidence trends, charts compared to previous years. Dashboard?  <br>➤ Added benefit of early error flags|
| | Use monthly outputs to monitor performance KPIs     | ➤ These monthly reports could also be used to monitor BNR performance metrics. |
| | Reduce number of REDCap database variables further  | ➤ The exported dataset still contains close to 150 variables. Are they all needed? Could we still operate on a further reduced dataset, allied to simpler processing?<br/>➤ Not sure myself, but worth a discussion? Usefulness might be compromised a little, but quality right now is struggling, right? |
| | Create a new category of *research analytics*       | ➤ For example, for survival analysis, we might decide to shift the linkage of death records and incident cases to an 'occasional' research analysis - to remove the need for this time-consuming data preparation step. |
| | Simplify process wherever possible                  | ➤ Linked to the *'Staged Improvement Plan'*. Worth a discussion to think through how we might do this? |
| | *'Staged Improvement Plan'* = opportunity for radical revamp. | ➤ My personal favourite :)<br/>➤ E.g. a new BNR might include:<br/><br/>➤➤ Hospital-based AMI and CVD registry<br/>➤➤ Official UCOD reporting - Barbados currently judged as poor by WHO.<br/>➤➤ HEARTS monitoring<br/>➤➤ Other monitoring of outcomes available via electronic record  |

<br>

