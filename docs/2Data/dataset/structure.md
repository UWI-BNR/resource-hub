---
title: "Welcome" 
hide:
#  - navigation
  - toc
---

# BNR Data Structure (Data Dictionary)
## Updated: **November 21st, 2025**

## **DATA MAP** - REDCap database ➡️ Final Dataset

???+ info "REDCap Database ➡️ Dataset Release"

    This data dictionary includes **three sets** of variables representing:

    - **COLUMN 1: REDCap database.** Variables collected and extracted from the BNR event database (**DO FILE:** ```bnrcvd-2025-redcap-format.do```)
    - **COLUMN 2: interim Dataset.** Variables in the interim cumulative dataset (2009-2023). These are presented for completeness.
    - **COLUMN 3: Analytics Dataset.** Variables for analytics use, after firther DO file preparation (**DO FILE:** ```bnrcvd-2023-prep1.do```) 


    | REDCap<br/>database variable | Cumulative<br/>dataset variable | Analytics<br/>dataset variable | Variable<br/>label | Display<br/>format |
    |---|---|---|---|---|
    |**Key Classifiers**| | | | |
    | -- | pid | eid | CVD Event Unique Identifier | %9.0g |
    | recid | recid | rid | * REDCap Record ID | %16s |
    | -- | -- | dco | * Death Certificate Only (DCO) Case (0=Hospital Event, 1=DCO) | %10.0g |
    | -- | -- | dco_alt | * Death Certificate Only (DCO) Case (0=Hospital Event, 1=DCO, 2-partial abstraction) classification | %20.0g |
    | -- | jc_etype | etype | CVD Event Type (AMI=2, Stroke=1) | %9.0g |
    |**Key Dates and Times**| | | | |
    | cfdoa | cfdoa | docf | CVD casefinding date (dd-mon-yyyy) | %dD_m_CY |
    | dob | dob | dob | Patient date of birth (dd-mon-yyyy) | %dD_m_CY |
    | edate | edate | doe | CVD event date (dd-mon-yyyy) | %dD_m_CY |
    | edateyr | eyear | yoe | CVD event year (yyyy) | %9.0g |
    | edatemon | -- | moe | CVD event month (mm) | %9.0g |
    | etime | etime | htoe | Patient hour of event (hh) | %9.0g |
    | etime | etime | mtoe | Patient minute of event (mm) | %9.0g |
    | cfadmdate | cfadmdate | doa | Patient date of admission (dd-mon-yyyy) | %dD_m_CY |
    | admtime | admtime | htoa | Patient hour of admission (hh) | %9.0g |
    | admtime | admtime | mtoa | Patient minute of admission (mm) | %9.0g |
    | dlc | dlc | dodi | Patient date of discharge (dd-mon-yyyy) | %dD_m_CY |
    | vstatus | vstatus | sadi | Patient vital status at discharge (1=Alive; 2=Dead) | %8.0g |
    | cfdod | dod | dod | Patient date of death (dd-mon-yyyy) | %dD_m_CY |
    |**Key Demographics**| | | | |
    | sex | sex | sex | Patient sex (1=female, 2=male) | %8.0g |
    | -- | -- | agey | Patient age at event (years as integer). *Note: Constructed from multiple past files. Not directly extracted from REDCap database.* | %9.0g |
    | -- | -- | age5 | Patient age at event (5-year age groups) | %9.0g |
    | -- | -- | age70 | Patient age group (<70 yrs; 70+ yrs) | %18.0g |
    | parish | parish | parish | Patient parish of residence | %13.0g |
    |**Ward Information**| | | | |
    | ward | ward__1 | treatloc1 | Treated in ICU/HDU (1=Yes; 0=No) | %9.0g |
    | ward | ward__2 | treatloc2 | Treated in A&E (1=Yes; 0=No) | %9.0g |
    | ward | ward__3 | treatloc3 | Treated in Medical wards (1=Yes; 0=No) | %9.0g |
    | ward | ward__4 | treatloc4 | Treated in Stroke Unit (1=Yes; 0=No) | %9.0g |
    | ward | ward__5 | treatloc5 | Treated in Cardiac Unit (1=Yes; 0=No) | %9.0g |
    |**Event Classifiers / Risk factor Information**| | | | |
    | htype | htype | htype | AMI subtype (1=STEMI; 2=NSTEMI; other categories) | %20.0g |
    | stype | stype | stype | Stroke subtype (1=Ischemic; 2/3=Hemorrhagic; other categories) | %25.0g |
    | pstroke | pstroke | pstroke | History of previous stroke (1=Yes; 2=No) | %8.0g |
    | pstrokeyr | pstrokeyr | pstrokeyr | Year of previous stroke event (yyyy) | %8.0g |
    | pami | pami | pami | History of previous AMI (1=Yes; 2=No) | %8.0g |
    | pamiyr | pamiyr | pamiyr | Year of previous AMI event (yyyy) | %8.0g |
    | htn | htn | htn | History of hypertension (1=Yes; 2=No) | %8.0g |
    | diab | diab | diab | History of diabetes mellitus (1=Yes; 2=No) | %8.0g |
    | sysbp | sysbp | sbp | Systolic blood pressure on admission (mmHg) | %8.0g |
    | diasbp | diasbp | dbp | Diastolic blood pressure on admission (mmHg) | %8.0g |
    | bgmmol | bgmmol | bgmmol | Blood glucose on admission (mmol/L) | %9.0g |
    | **Exam** || |  | ||
    | ecg | ecg | ecg | ECG performed during event admission (1=Yes; 2=No) | %8.0g |
    | ecgd | ecgd | doecg | Date of ECG during event admission (dd-mon-yyyy) | %dD_m_CY |
    | ecgt | ecgt | htecg | Hour of ECG during event admission (hh) | %9.0g |
    | ecgt | ecgt | mtecg | Minute of ECG during event admission (mm) | %9.0g |
    | **Cardiac Enzymes** | | |  | ||
    | tropres | tropres | tropres | Number of troponin tests completed | %13.0g |
    | trop1res | trop1res | trop1res | Result of troponin test 1 (ng/L) | %9.0g |
    | trop2res | trop2res | trop2res | Result of troponin test 2 (ng/L) | %9.0g |
    | **Assessments** | | |  | ||
    | assess | assess | assess | Assessment by any therapist (1=Yes; 2=No) | %8.0g |
    | assess1 | assess1 | assess1 | Evaluated by occupational therapist (1=Yes; 2=No; 3=Referred) | %12.0g |
    | assess2 | assess2 | assess2 | Evaluated by physiotherapist (1=Yes; 2=No; 3=Referred) | %12.0g |
    | assess3 | assess3 | assess3 | Evaluated by speech therapist (1=Yes; 2=No; 3=Referred) | %12.0g |
    | assess4 | assess4 | assess4 | Evaluated by swallowing assessment (1=Yes; 2=No; 3=Referred) | %12.0g |
    | ct | ct | ct | CT scan report available (1=Yes; 2=No) | %8.0g |
    | doct | doct | doct | Date of CT scan report (dd-mon-yyyy) | %dD_m_CY |
    | reperf | reperf | reperf |  Reperfusion attempted (1=Yes; 02=No) |  |
    | repertype | repertype | repertype | Type of reperfusion therapy (1=Fibrinolytic; 2=PCI) | %20.0g |
    | reperfd | reperfd | dore | Date of reperfusion therapy (dd-mon-yyyy) | %dD_m_CY |
    | reperft | reperft | htore | Hour of reperfusion therapy (hh) | %9.0g |
    | reperft | reperft | mtore | Minute of reperfusion therapy (mm) | %9.0g |
    | asp | asp__1 | asp1 | Aspirin - acute use (1=Yes; 0=No) | %9.0g |
    | asp | asp__2 | asp2 | Aspirin chronic use (1=Yes; 0=No) | %9.0g |
    | asp | asp__3 | asp3 | Aspirin contraindicated (1=Yes; 0=No) | %9.0g |
    | aspdose | aspdose | aspdose | Aspirin dose (mg) | %8.0g |
    | aspd | aspd | doasp | Date aspirin prescribed (dd-mon-yyyy) | %dD_m_CY |
    | aspt | aspd | htoasp | Hour aspirin prescribed (hh) | %9.0g |
    | aspt | aspd | mtoasp | Minute aspirin prescribed (mm) | %9.0g |
    | asptimeampm_2 | asptimeampm_2 | asp_ampm |  Approximate time aspirin prescribed | %8.0g |
    | **Discharge Information** | | |  | ||
    | dismeds | dismeds___1 | dmed1 | Aspirin prescribed at discharge (1=Yes; 0=No) | %9.0g |
    | dismeds | dismeds___2 | dmed2 | Warfarin prescribed at discharge (1=Yes; 0=No) | %9.0g |
    | dismeds | dismeds___3 | dmed3 | Heparin prescribed at discharge (1=Yes; 0=No) | %9.0g |
    | dismeds | dismeds___4 | dmed4 | Antiplatelet prescribed at discharge (1=Yes; 0=No) | %9.0g |
    | dismeds | dismeds___5 | dmed5 | Statin prescribed at discharge (1=Yes; 0=No) | %9.0g |
    | dismeds | dismeds___6 | dmed6 | ACE inhibitor prescribed at discharge (1=Yes; 0=No) | %9.0g |
    | dismeds | dismeds___7 | dmed7 | ARB prescribed at discharge (1=Yes; 0=No) | %9.0g |
    | dismeds | dismeds___8 | dmed8 | Beta-blocker prescribed at discharge (1=Yes; 0=No) | %9.0g |
    | dismeds | dismeds___9 | dmed9 | Bivalrudin prescribed at discharge (1=Yes; 0=No) | %9.0g |
    | dismeds | dismeds___10 | dmed10 | Anti-hypertensive prescribed at discharge (1=Yes; 0=No) | %9.0g |
    | aspdosedis | aspdosedis | aspdose_dis | Aspirin dose at discharge (mg) | %8.0g |
    | **Stroke Unit** | | |  | ||
    | strunit | strunit | sunit | Admitted to stroke unit (1=Yes; 2=No) | %8.0g |
    | astrunitd | astrunitd | doasu | Date of stroke unit admission (dd-mon-yyyy) | %dD_m_CY |
    | dstrunitd | dstrunitd | dodisu | Date of stroke unit discharge (dd-mon-yyyy) | %dD_m_CY |
    | sunitadmsame | sunitadmsame | doasu_same |  | %8.0g |
    | sunitdissame | sunitdissame | dodisu_same |  | %8.0g |
    | -- | redcap_event_name | redcap_event_name | Event Type using REDCap format for all years | %12s.
    | **Identifiable Information** | |  |  |
    | fname | fname | id_fname | First Name | %29s |
    | mname | mname | id_mname | Middle Name(s)/Initial(s) | %30s |
    | lname | lname | id_lname | Last Name(s) | %22s |
    |  |  | id_nid | * Patient hospital number | %11s |
    |  |  | id_hid | * Hospital / Patient Record Number | %13s |
    | **In REDCap database - not currently exported to analytics dataset** |  |  |  |  |
    | -- | sd_db | -- | The database used by the BNR team (e.g. Epi-Info, REDCap)  |  |
    | cfdoat | cfdoat | -- | Time of entry to database |  |
    | cfda | cfda | -- | Person performing data entry |  |
    | cfsource | cfsource__1 | --  | Casefinding Source (Ward A1) |  |
    | cfsource | cfsource__2 | --  | Casefinding Source (Ward A2) |  |
    | cfsource | cfsource__3 | --  | Casefinding Source (Ward A3) |  |
    | cfsource | cfsource__4 | --  | Casefinding Source (Ward A5) |  |
    | cfsource | cfsource__5 | --  | Casefinding Source (Ward A6) |  |
    | cfsource | cfsource__6 | --  | Casefinding Source (MICU) |  |
    | cfsource | cfsource__7 | --  | Casefinding Source (SICU) |  |
    | cfsource | cfsource__8 | --  | Casefinding Source (Ward B5) |  |
    | cfsource | cfsource__9 | --  | Casefinding Source (Ward B6) |  |
    | cfsource | cfsource__10 | --  | Casefinding Source (Ward B7) |  |
    | cfsource | cfsource__11 | --  | Casefinding Source (Ward B8) |  |
    | cfsource | cfsource__12 | --  | Casefinding Source (Ward C5) |  |
    | cfsource | cfsource__13 | --  | Casefinding Source (Ward C6) |  |
    | cfsource | cfsource__14 | --  | Casefinding Source (Ward C7/PICU) |  |
    | cfsource | cfsource__15 | --  | Casefinding Source (Ward C8) |  |
    | cfsource | cfsource__16 | --  | Casefinding Source (Ward C9) |  |
    | cfsource | cfsource__17 | --  | Casefinding Source (Ward C10/Stroke Unit) |  |
    | cfsource | cfsource__18 | -- | Casefinding Source (Ward C12) |  |
    | cfsource | cfsource__19 | -- | Casefinding Source (Cardiac Unit) |  |
    | cfsource | cfsource__20 | -- | Casefinding Source (Medical Record) |  |
    | cfsource | cfsource__21 | -- | Casefinding Source (Death Record) |  |
    | cfsource | cfsource__22 | -- | Casefinding Source (A&E) |  |
    | cfsource | cfsource__23 | -- | Casefinding Source (Polyclinic) |  |
    | cfsource | cfsource__24 | -- | Casefinding Source (Private Physician) |  |
    | cfsource | cfsource__25 | -- | Casefinding Source (Emerg Clinic) |  |
    | cfsource | cfsource__26 | -- | Casefinding Source (Nursing Home) |  |
    | cfsource | cfsource__27 | -- | Casefinding Source (MedData) |  |
    | cfage | cfage | -- | Age at casefinding.  |  |
    | cfage_da | -- | -- | Age at casefinding - date abstracted |  |
    | recnum | recnum | hid | Unique National ID identifier |  |
    | initialdx | initialdx | -- | Text-based diagnosis |  |
    | hstatus | hstatus | -- | Text-based statusdischarged/on ward |  |
    | slc | slc | -- | Vital status at last known contact. *Changed meaning in 2023. No longer useful.* |  |
    | finaldx | finaldx | -- | Final diagnosis. *IRH: does not look complete?* |  |
    | cfcods | cfcods | -- | Another final diagnosis. *IRH: does not look complete?*  |  |
    | cstatus | cstatus | -- | *IRH: Always recorded as "eligible". No variation.* |  |
    | eligible | eligible | -- | *IRH: Looks to be an eligibility status, that would need regular updating within ech record. Does not seem to be used now.* |  |
    | ineligible | ineligible | -- | *IRH:Empty field*  |  |
    | duplicate | duplicate |--  | *IRH: Duplicate information. Unclear how this is operationalised?* |  |
    | duprec | duprec | -- | Duplicates information. *IRH: Should be part of a query system, going forwards?*  |  |
    | dupcheck | dupcheck | -- | Duplicate information. *IRH: Should be part of a query system, going forwards?* |  |
    | toabs | toabs | -- | Internal process field. *IRH: No information on how this is used?* |  |
    | mstatus | mstatus |--  |Marital status  |  |
    | resident | resident | -- | Resident in Barbados. *IRH: Is this used?* |  |
    | citizen | citizen | -- | Citizen of Barbados. *IRH: Is this used / relevant?* |  |
    | addr | addr | -- | Patient known address |  |
    | dxtype | dxtype | -- | How is AMI subtype diagnosed?  |  |
    | dstroke | dstroke | -- | Unclear variable. *IRH: how is this operationalized?* |  |
    | edatemondash | -- | -- | Derived date. *IRH: Meaning unclear*  |  |
    | inhosp | inhosp | -- | *IRH: Meaning unclear*  |  |
    | etimeampm | etimeampm | -- | Approximate event time (am/pm)  |  |
    | rfany | fany | -- | Any risk factors? *IRH: Doesn't feel useful - unhealpfully broad?* |  |
    | bgunit | bgunit | -- | *IRH: Meaning?* |  |
    | bgmg | bgmg | -- | *IRH: Mostly empty* |  |
    | dieany_2 | dieany_2 | -- | Diagnostic exam completed? |  |
    | decg | decg | -- | ECG completed? |  |
    | ecgtampm | ecgtampm | -- | ECG time AM/PM |  |
    | tropdone | tropdone | -- | Troponin completed? |  |
    | troptype | troptype | -- | Lab or Spot? |  |
    | dieany | dieany | -- | Any evaluation?  |  |
    | dct | dct | -- | CT done |  |
    | asp | asp__99 | -- | Aspirin - no record of use |  |
    | asp | asp__88 | -- | Aspirin. IRH: Meaning? |  |
    | asp | asp__999 |--  | Aspirin. IRH: Meaning? |  |
    | asp | asp__9999 | -- | Aspirin. IRH: Meaning? |  |
    | dissysbp | dissysbp | -- | At discharge: SBP |  |
    | disdiasbp | disdiasbp | -- | At discharge: DBP |  |
    | disbgmmol | disbgmmol | -- | At discharge: Blood glucose |  |
    | carunit | carunit | -- |Admitted to cardiac unit  |  |
    | natregno | natregno | nid | Barbados National Rregistration Number |  |

<br/>

