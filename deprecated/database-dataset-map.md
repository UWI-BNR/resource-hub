---
title: "Welcome" 
hide:
#  - navigation
  - toc
---

Updated: **October 27th, 2025**

| DATABASE | INTERIM DATASET | FINAL DATASET | DESCRIPTION | Comments | DECISION |
|--------------|---------|---------|------------------| | |
| -- | pid |eid| **KEY**<br>**ANALYSIS**<br>Event ID (Unique) | ➤ Keep in shared datasets as non-identifying uniqueness | **KEEP**. |
| -- | sd_db || **PROCESS**<br>In-house database used  | ➤ Background interest. (E.g.) might metrics differ across BNR phases? | **DROPPED**|
| -- | jc_etype |etype| **PRIMARY**<br>**ANALYSIS**<br>Event type  |==➤ Does not match *redcap_event_name*?== | **DROPPED / RECALCULATED** |
| -- | sd_eyear |yoe| **PRIMARY**<br>**ANALYSIS**<br>Event year  |  | **DROPPED / RECALCULATED**|
| -- | sd_abstracted |dco| **PROCESS**<br>Abstraction type (abstracted, DCO) | ==➤ There is a third abstracted status = *partial abstraction*?==|  **KEEP**|
| recid | recid |rid| **PREP ONLY**<br>Original REDCap Unique ID   | ==➤ Lots of missing entries?== | **KEEP** |
| -- | redcap_event_name |etype| **PREP ONLY**<br>initial distinction between AMIs and strokes | ==➤ There is a third abstracted status** = *death_data_collect_arm_1*. How to tell if AMI or stroke?== | **KEEP** |
| cfdoa | cfdoa |docf| **PROCESS**<br>Date of entry to database | |**KEEP** |
| cfdoat | cfdoat || **NOT NEEDED**<br>Time of entry to database |  |**DROPPED** |
| cfda | cfda || **NOT NEEDED**<br>Person doing data entry | |**DROPPED** |
| **Process Info** |  |  |  | ||
| cfsource | cfsource__1 || **PROCESS**<br>Casefinding source (Ward A1) | ➤ Casefinding now medical records only | **DROPPED** |
| cfsource | cfsource__2 || **PROCESS**<br>Casefinding source (Ward A2) | | **DROPPED**|
| cfsource | cfsource__3 || **PROCESS**<br>Casefinding source (Ward A3/HDU) |  | **DROPPED**|
| cfsource | cfsource__4 || **PROCESS**<br>Casefinding source (Ward A5) |  | **DROPPED**|
| cfsource | cfsource__5 || **PROCESS**<br>Casefinding source (Ward A6) |  | **DROPPED**|
| cfsource | cfsource__6 || **PROCESS**<br>Casefinding source (MICU) |  | **DROPPED**|
| cfsource | cfsource__7 || **PROCESS**<br>Casefinding source (SICU) |  | **DROPPED**|
| cfsource | cfsource__8 || **PROCESS**<br>Casefinding source (Ward B5) |  | **DROPPED**|
| cfsource | cfsource__9 || **PROCESS**<br>Casefinding source (Ward B6) |  | **DROPPED**|
| cfsource | cfsource__10 || **PROCESS**<br>Casefinding source (Ward B7) |  | **DROPPED**|
| cfsource | cfsource__11 || **PROCESS**<br>Casefinding source (Ward B8) |  | **DROPPED**|
| cfsource | cfsource__12 || **PROCESS**<br>Casefinding source (Ward C5) |  | **DROPPED**|
| cfsource | cfsource__13 || **PROCESS**<br>Casefinding source (Ward C6) |  | **DROPPED**|
| cfsource | cfsource__14 || **PROCESS**<br>Casefinding source (C7/PICU) |  | **DROPPED**|
| cfsource | cfsource__15 || **PROCESS**<br>Casefinding source (C8) |  | **DROPPED**|
| cfsource | cfsource__16 || **PROCESS**<br>Casefinding source (C9) |  | **DROPPED**|
| cfsource | cfsource__17 || **PROCESS**<br>Casefinding source (C10/Stroke Unit) | |**DROPPED** |
| cfsource | cfsource__18 || **PROCESS**<br>Casefinding source (C12) |  | **DROPPED**|
| cfsource | cfsource__19 || **PROCESS**<br>Casefinding source (Cardiac Unit) |  | **DROPPED**|
| cfsource | cfsource__20 || **PROCESS**<br>Casefinding source (Medical Record) |  | **DROPPED**|
| cfsource | cfsource__21 || **PROCESS**<br>Casefinding source (Death Record) |  | **DROPPED**|
| cfsource | cfsource__22 || **PROCESS**<br>Casefinding source (A&E) |  | **DROPPED**|
| cfsource | cfsource__23 || **PROCESS**<br>Casefinding source (Polyclinic) |  | **DROPPED**|
| cfsource | cfsource__24 || **PROCESS**<br>Casefinding source (Private Physician) |  |**DROPPED** |
| cfsource | cfsource__25 || **PROCESS**<br>Casefinding source (Emerg.Clinic) |  | **DROPPED**|
| cfsource | cfsource__26 || **PROCESS**<br>Casefinding source (Nursing Home) |  | **DROPPED**|
| cfsource | cfsource__27 || **PROCESS**<br>Casefinding source (MedData) |  | **DROPPED**|
| **DEMOGRAPHICS**|  |  |  | ||
| fname | fname |id_fname| First Name | ➤ Identifiable | **KEEP** |
| mname | mname |id_mname| Middle Name | ➤ Identifiable | **KEEP**|
| lname |  lname |id_lname| Last Name | ➤ Identifiable| **KEEP**|
| sex | sex |sex| **PRIMARY**<br>**ANALYTICS**<br>Patient sex | ==Missing *sex* in 2022 and 2023 if DCO?== | **KEEP**|
| dob | dob |dob| **PRIMARY**<br>**ANALYTICS**<br>Patient date of birth | ==➤ A lot of mssingness?==  |**KEEP**|
| cfage | cfage || **NOT NEEDED?**<br>This is called age at casefinding (auto-calculated).  |==➤ We need a definitive age variable.<br> ➤ This needs a hierarchy of dates, **with an accompanying indicator showing that hierarchy**.== E.g.<br><br> ➤ (cat 1) Symptom onset date<br> ➤ (cat 2) If no symptom date, A&E date<br> ➤ (cat 3) If no symptom or A&E date, admission date, and so on<br> ➤ (cat 4) Discharge date<br> ➤ (cat 4) Death date.<br><br> We then calculate age using this *event date* and *date of birth* | **DROPPED**|
| cfage_da | -- || **NOT NEEDED?**<br>This is called age at casefinding (data entered).  |  | **DROPPED**|
| natregno | natregno |nid| **NOT NEEDED**<br>Unique National ID identifier | ➤ Do not export | **KEEP**|
| recnum | recnum |hid| **NOT NEEDED**<br>Unique Hospital identifier | ➤ Do not export |**KEEP** |
| cfadmdate | cfadmdate |doa| **PREP ONLY**<br>Admission Date | ➤ Important preparatory variable used to calculate age and age groups| **KEEP**|
| admtime | admtime |htoa, mtoa| **PREP ONLY**<br>Admission Time (hrs, minutes) | ➤ Used to calculate time until reperfusion | **KEEP** |
| initialdx | initialdx || **NOT NEEDED**<br>Text-based diagnosis | ➤ Do not export | **DROPPED** |
| hstatus| hstatus || **NOT NEEDED**<br>Text-based statusdischarged/on ward | ➤ Whether on ward at a point in time. No use for analyses. | **DROPPED** |
| slc | slc || **NOT NEEDED**<br>Vital status at last known contact | ➤ Changed meaning in 2023. No longer useful.  | **DROPPED** |
| dlc | dlc |dodi| **PREP ONLY**<br>Discharge date | ➤ Used to calculate time in hospital, then drop. |**KEEP**  |
| cfdod | dod |dod| **PREP ONLY**<br>Date of death | ➤ For DCO cases only.<br>==Need to understand full death casefinding process== | **KEEP** |
| finaldx | finaldx || **NOT NEEDED**<br>Final diagnosis - does not look complete? |  | **DROPPED**|
| cfcods| cfcods || **NOT NEEDED**<br>Another final diagnosis - does not look complete? |  |**DROPPED** |
| cstatus | cstatus || **NOT NEEDED**<br>Always "eligible"? |  |**DROPPED** |
| eligible | eligible || **NOT NEEDED**<br>Looks to be an eligibility status, that would need regular updating within record? | ➤ Eligibility and duplicate fields should move to a sign-off process |**DROPPED** |
| ineligible | ineligible || **NOT NEEDED**<br>Empty field |  | **DROPPED**|
| duplicate | duplicate || **NOT NEEDED**<br>Duplicate information | ➤ Should be part of a query system, going forwards? |**DROPPED** |
| duprec | duprec || **NOT NEEDED**<br>Duplicates information | ➤ Should be part of a query system, going forwards? |**DROPPED** |
| dupcheck | dupcheck || **NOT NEEDED**<br>Duplicate information | ➤ Should be part of a query system, going forwards? | **DROPPED**|
| toabs| toabs || ➤ **NOT NEEDED**<br>Internal process field | ➤ Do not export | **DROPPED**|
| mstatus | mstatus || **NOT NEEDED**<br>Marital status | ➤  Do not export. Probably no longer used. | **DROPPED** |
| resident | resident || **NOT NEEDED**<br>Is this used | ➤ Code errors. Some "0" codes. Many missing - can't be used when incorporating DCOs  |**DROPPED**|
| citizen | citizen || **NOT NEEDED**<br>Is this used | ➤ Code errors. Some "0" codes. Many missing. Can't be used when incorporating DCOs | **DROPPED**|
| addr |addr || **NOT NEEDED**<br>Address | ➤ Do not export | **DROPPED**|
| parish | parish |parish| **ANALYSIS**<br>Parish | ➤ Distance to hospital as a predictor of outcome? |**KEEP**|
| ward | ward__1 |treatloc1| **ANALYSIS**<br>Treatment in ICU/HDU | ➤ Treatment ward as a predictor of outcome? | **KEEP** |
| ward | ward__2 |treatloc2| **ANALYSIS**<br>Treatment in A&E | ➤ Treatment ward as a predictor of outcome? |**KEEP** |
| ward | ward__3 |treatloc3| **ANALYSIS**<br>Treatment in Med Wards | ➤ Treatment ward as a predictor of outcome? |**KEEP**|
| ward | ward__4 |treatloc4| **ANALYSIS**<br>Treatment in Stroke Unit | ➤ Treatment ward as a predictor of outcome? | **KEEP**|
| ward | ward__5 |treatloc5| **ANALYSIS**<br>Treatment in Cardiac Unit | ➤ Treatment ward as a predictor of outcome? | **KEEP**|
| **EVENT** | | | | ||
| htype |htype |htype| ➤ **PRIMARY**<br>**ANALYTICS**<br>AMI subtype | ==➤ Over 50% missing<br>➤ Some events classified as:<br>➤ Sudden cardiac death<br>➤ definite SMI<br>➤ Probable AMI==  |**KEEP** |
| stype | stype |stype| ➤ **PRIMARY**<br>**ANALYTICS**<br>Stroke subtype | ➤ Primary analysis field.  | **KEEP**|
| dxtype | dxtype || **PROCESS**<br>How AMI subtype diagnosed   |  | **DROPPED** |
| dstroke |dstroke || **PROCESS**<br>This feels like an internal variable  | | **DROPPED** |
| edate | edate |doe| **ANALYSIS**<br>Event Date | ==➤ What does this actually mean? Date of self-reported symptom onset, perhaps?==  | **KEEP** |
| edateyr | -- |yoe| **ANALYSIS**<br>Derived date | ➤ Do not export |**DROPPED / RECALCULATED** |
| edatemon | -- |moe| **NOT NEEDED**<br>Derived date | ➤ Do not export | **DROPPED / RECALCULATED**|
| edatemondash | -- || **NOT NEEDED**<br>Derived date | ➤ Do not export | **DROPPED**|
| inhosp | inhosp || **NOT NEEDED**<br>Mostly blank | ➤ Do not export | **DROPPED** |
| etime | etime | htoe, mtoe| **ANALYSIS**<br>Event time (hrs, minutes) | ==➤ What is this "event" time. Self reported time of sympton onset, for example?== | **KEEP** |
| etimeampm | etimeampm || **NOT NEEDED**<br>Seem incomplete | ➤ Do not export | **DROPPED** |
| **Previous Event**| |   |  | | |
| pstroke| pstroke |pstroke| **ANALYTICS**<br>Previous stroke | ➤ Export, but look at completeness | **KEEP**  |
| pstrokeyr | pstrokeyr |pstrokeyr| **ANALYTICS**<br>Previous stroke year |➤ Export, but look at completeness   |**KEEP**|
| pami | pami |pami| **ANALYTICS**<br>Previous AMI | ➤ Export, but look at completeness | **KEEP**|
| pamiyr | pamiyr |pamiyr|  **ANALYTICS**<br>Previous AMI year |➤ Export, but look at completeness   | **KEEP**|
| **Risk Factors** | | | | |
| rfany | fany || **ANALYTICS**<br>Any risk factors? | ➤ Can't see usefulness of this - too broad | **DROPPED** |
| htn | htn |htn|  **ANALYTICS**<br>Hypertension? | ➤ Export - check completeness | **KEEP**|
| diab | diab |diab|  **ANALYTICS**<br>Diabetes? | ➤ Export - check completeness | **KEEP**|
| **TESTS** | | | | ||
| **Vital Signs** | |   | | |
| sysbp | sysbp |sbp| **ANALYTICS**<br>Blood pressure at admission | ➤ Export - check completeness.<br>==Possible poor quality. REDCap checks in place?==| **KEEP**|
| diasbp | diasbp |dbp| **ANALYTICS**<br>Blood pressure at admission | ➤ Export - check completeness.<br>==Possible poor quality. REDCap checks in place?== | **KEEP**|
| bgunit | bgunit || **NOT NEEDED**<br>Internal variable | ➤ Do not export |**DROPPED** |
| bgmg | bgmg || Blood glucose at admission (mg/dl) | ➤ Mostly empty. Do not export |**DROPPED** |
| bgmmol | bgmmol |bgmmol| **ANALYTICS**<br>Blood glucose at admission (mmol/l) | ➤ Export - check completeness.<br>==Possible poor quality. REDCap checks in place?== |**KEEP** |
| **Exam** || |  | ||
| dieany_2 | dieany_2 || **NOT NEEDED**<br>Diagnostic exam completed? | ➤ Do not export |**DROPPED** |
| decg | decg || **NOT NEEDED**<br>ECG completed? |  ➤ Do not export | **DROPPED**|
| ecg | ecg |ecg| **ANALYSIS**<br>ECG report available? | ➤ Use date as a proxy for ECG performed | **KEEP**|
| ecgd | ecgd |doecg| **ANALYSIS**<br>Date of ECG | ➤ Performance measure? | **KEEP**|
| ecgt | ecgt |htecg, mtecg| **ANALYSIS**<br>Time of ECG | ➤ Performance measure? | **KEEP** |
| ecgtampm | ecgtampm || **NOT NEEDED**<br>ECG Am/PM | ➤ Do not export. Incomplete | **DROPPED** |
| **Cardiac Enzymes** | | |  | ||
| tropdone | tropdone || Troponin completed? | ➤ Do not export |**DROPPED** |
| troptype | troptype || Lab or Spot? | ➤ Do not export |**DROPPED** |
| tropres | tropres |tropres| **ANALYSIS**<br>How many troponin results |  | **KEEP**|
| trop1res | trop1res |trop1res| **ANALYSIS**<br>Troponin Result 1 |   | **KEEP**|
| trop2res | trop2res |trop2res| **ANALYSIS**<br>Troponin Result 2 |   | **KEEP**|
| **Assessments** | | |  | ||
| assess | assess |assess| **ANALYSIS**<br> Evaluation by any therapist |  |**KEEP** |
| assess1 | assess1 |assess1| **ANALYSIS**<br> Evaluation by occupational therapist |  |**KEEP** |
| assess2 | assess2 |assess2| **ANALYSIS**<br> Evaluation by physiotherapist |  |**KEEP** |
| assess3 | assess3 |assess3| **ANALYSIS**<br> Evaluation by speech therapist |  |**KEEP** |
| assess4 | assess4 |assess4| **ANALYSIS**<br> Evaluation by swallowing assessment |  |**KEEP** |
| dieany | dieany || **NOT NEEDED**<br>Any evaluation? | ➤ Do not export. `ct` used as proxy | **DROPPED**|
| dct | dct || **NOT NEEDED**<br>CT done | ➤ Do not export. `ct` used as proxy | **DROPPED**|
| ct | ct |ct| **ANALYSIS**<br>Is CT report available | ➤ Contribution to a performance measure? |**KEEP** |
| doct | doct |doct| **ANALYSIS**<br>Date of CT | ➤ Contribution to a performance measure? |**KEEP** |
| **TREATMENT DISCHARGE** || | |  | |
| **Reperfusion** | | || Is this a performance metric? But is it always completed?| |
| reperf | reperf ||**NOT NEEDED**<br>Reperfusion attempted | ➤ Does missingness allow use. Or is it really quite a rare event? | **DROPPED**|
| repertype | repertype |repertype| **ANALYSIS**<br>Reperfusion type | ➤ Does missingness allow use? |**KEEP / DEID** |
| reperfd | reperfd |dore| **ANALYSIS**<br>Reperfusion date | ➤ Does missingness allow use? |**KEEP / DEID** |
| reperft | reperft |htore, mtore| **ANALYSIS**<br>Reperfusion time | ➤ Does missingness allow use? | **KEEP / DEID**|
| **Medications** | | | | ||
| asp | asp__1 |asp1| **ANALYSIS**<br>Aspirin - acute use | ➤ Performance metric? |  **KEEP**|
| asp | asp__2 |asp2| **ANALYSIS**<br>Aspirin - chronic use | ➤ Performance metric? | **KEEP** |
| asp | asp__3 |asp3| **ANALYSIS**<br>Aspirin - contraindicated | ➤ Performance metric? |  **KEEP**|
| asp | asp__99 || **ANALYSIS**<br>Aspirin - no record of use | ➤ Performance metric? |  **NOT EXPORTED (n=0)**|
| asp | asp__88 || **NOT NEEDED**<br>Aspirin - ?? | ➤ Performance metric? | **NOT EXPORTED (n=0)**|
| asp | asp__999 || **NOT NEEDED**<br>Aspirin - ?? | ➤ Performance metric? | **NOT EXPORTED (n=0)**|
| asp | asp__9999 || **NOT NEEDED**<br>Aspirin - ?? | ➤ Performance metric? | **NOT EXPORTED (n=0)**|
| aspdose | aspdose |aspdose| **ANALYSIS**<br>Aspirin - acute use dose | ➤ Performance metric? | **KEEP** |
| aspd | aspd |doasp| **ANALYSIS**<br>Aspirin - acute use dose date | ➤ Performance metric? | **KEEP** |
| aspt | aspd |htoasp, mtoasp| **ANALYSIS**<br>Aspirin - acute use dose time | ➤ Performance metric? | **KEEP** |
| asptimeampm_2 | asptimeampm_2 || **NOT NEEDED**<br>Aspirin - acute use dose AM/PM | ➤ Do not export |  **DROPPED** |
| vstatus | vstatus |sadi| **PRIMARY**<br>**ANALYSIS**<br>Vital status at discharge | ➤ Primary variable. Associated date of discharge = dodi? <br>==A lot of missing right now? (almost 5,000 missing - 4,377 related to DCO, 376 when abstracted)== |  **KEEP** |
| **Discharge Meds** | | || | |
| dismeds | dismeds___1 |dmed1| **ANALYSIS**<br>Discharge meds: Aspirin | ➤ Performance metric? |  **KEEP**|
| dismeds | dismeds___2 |dmed2| **ANALYSIS**<br>Discharge meds: warfarin | ➤ Performance metric? | **KEEP** |
| dismeds | dismeds___3 |dmed3| **ANALYSIS**<br>Discharge meds: heparin | ➤ Performance metric? |  **KEEP**|
| dismeds | dismeds___4 |dmed4| **ANALYSIS**<br>Discharge meds: antiplatelet | ➤ Performance metric? |  **KEEP**|
| dismeds | dismeds___5 |dmed5| **ANALYSIS**<br>Discharge meds: statin | ➤ Performance metric? |  **KEEP**|
| dismeds | dismeds___6 |dmed6| **ANALYSIS**<br>Discharge meds: ACE inhibitor | ➤ Performance metric?= | **KEEP** |
| dismeds | dismeds___7 |dmed7| **ANALYSIS**<br>Discharge meds: ARBs|➤ Performance metric? | **KEEP** |
| dismeds | dismeds___8 |dmed8| **ANALYSIS**<br>Discharge meds: Beta blockers | ➤ Performance metric? | **KEEP** |
| dismeds | dismeds___9 |dmed9| **ANALYSIS**<br>Discharge meds: Bivalrudin | ➤ Performance metric?  |**KEEP**|
| dismeds | dismeds___10 |dmed10| **ANALYSIS**<br>Discharge meds: Antihypertensives | ➤ Performance metric? | **KEEP**|
| aspdosedis | aspdosedis |daspdose| **ANALYSIS**<br>Dose of ASA at discharge | ➤ Performance metric? | **KEEP** |
| **Discharge Vital Signs** | | ||  | |
| dissysbp | dissysbp || **NOT NEEDED**<br>At discharge: SBP | ➤ Do not export |  **DROPPED**|
| disdiasbp | disdiasbp || **NOT NEEDED**<br>At discharge: SBP | ➤ Do not export |  **DROPPED**|
| disbgmmol | disbgmmol || **NOT NEEDED**<br>At discharge: Blood glucose | ➤ Do not export |  **DROPPED**|
| carunit | carunit || **ANALYSIS**<br>Admitted to cardiac unit | ➤   AMI equiv of admitted to stroke unit | **DROPPED** |
| **Stroke Unit** | | |  ||  |
| strunit | strunit |sunit| **ANALYSIS**<br>Admitted to stroke unit |  | **KEEP**|
| sunitadmsame | sunitadmsame |doasu_same| **ANALYSIS**<br> Can use date to recalculate | ➤ Do not export | **KEEP** |
| astrunitd | astrunitd |doasu| **ANALYSIS**<br>date of stroke unit admission | ➤ Use to calculate if admitted "immediately" - i.e. same day | **KEEP**|
| sunitdissame | sunitdissame |dodisu_same| **NOT NEEDED**<br> Can use date to recalculate | ➤ Do not export | **KEEP**|
| dstrunitd | dstrunitd |dodisu| **ANALYSIS**<br>Date of stroke unit discharge | ➤ Use to calculate if discharged "on same day" - as hospital discharge | **KEEP**|

<br>
