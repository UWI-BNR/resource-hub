
# How To: Export Data from REDCap using the REDCap API 
This short guide walks you through six simple steps needed to export data safely from REDCap.  

---

???- example "Step 1 - Ensure Active REDCap API Token"

    ## **Step 1 — Make sure your REDCap API token is active**

    Your API token is the key that lets Stata talk to REDCap.  

    - If your token has expired, the export will *not* work.  
    - Ask your REDCap administrator to confirm your token is active.  
    - Never share your token with anyone.


???- example "Step 2 - Check your Local API Token"

    ## **Step 2 — Check the API token stored in your Stata DO file**

    Your token should be recorded in the secure local file: `bnrcvd-2023-redcap-token.do`.  

    - Make sure the token written in the file matches the token in REDCap.  
    - If you paste in a new token, save the DO file again before exporting the data.  
    - Keep this token file secure on your encrypted PC.


???- example "Step 3 - Update the Export Date Range "

    ## **Step 3 — Update the export date range**

    In the DO file (`bnrcvd-2023-redcap-format.do`), update the following:

    ``` stata
    global REDCAP_START "YYYY-MM-DD"
    global REDCAP_END   "YYYY-MM-DD"
    global EXPORT_YR    "YYYY"
    global EXPORT_MO    "MM"
    global EXPORT_DT    "YYYYMM"
    global EXPORT_VS    "v01"
    ```

    Simple rules:

    - Use whole calendar months for easy checking.  
    - The date range should match what you expect to see in REDCap.  
    - If unsure, start small (e.g., one week or one month) and check the results.


???- example "Step 4 - Confirm the variables you want to export"

    ## Step 4 - Confirm the variables you want to export


    Inside the same DO file `bnrcvd-2023-redcap-format.do` you will see a long list of variables.  

    - These are the variables REDCap will send to Stata.  
    - Only change this list if you *know* what you are doing.  
    - If you add variables in REDCap, add them here too.  
    - Every field must be typed exactly as it appears in REDCap.

    If the export fails unexpectedly, this section is the most common cause.

    ???- info "The default variables for export" 
        
        ``` python
        # BEGIN: your existing field list
        fields = [
        "recid",                
        "cstatus",
        "eligible",
        "ineligible",
        "duplicate",
        "duprec",
        "dupcheck",
        "toabs",
        "cfdoa",              
        "fname",              
        "mname",              
        "lname",              
        "sex",                
        "dob",                
        "cfage",              
        "cfage_da",           
        "natregno",           
        "recnum",             
        "cfadmdate",          
        "admtime",            
        "dlc",                
        "cfdod",              
        "parish",             
        "ward___1",           
        "ward___2",           
        "ward___3",           
        "ward___4",           
        "ward___5",           
        "htype",              
        "stype",              
        "edate",              
        "etime",              
        "pstroke",            
        "pstrokeyr",          
        "pami",               
        "pamiyr",             
        "htn",                
        "diab",               
        "sysbp",              
        "diasbp",             
        "bgmmol",             
        "ecg",                
        "ecgd",               
        "ecgt",               
        "tropres",            
        "trop1res",           
        "trop2res",           
        "assess",             
        "assess1",            
        "assess2",            
        "assess3",            
        "assess4",            
        "ct",                 
        "doct",               
        "reperf",             
        "repertype",          
        "reperfd",            
        "reperft",            
        "asp___1",            
        "asp___2",            
        "asp___3",            
        "aspdose",            
        "aspd",               
        "aspt",               
        "asptimeampm_2",      
        "vstatus",
        "dismeds___1",
        "dismeds___2",
        "dismeds___3",
        "dismeds___4",
        "dismeds___5",
        "dismeds___6",
        "dismeds___7",
        "dismeds___8",
        "dismeds___9",
        "dismeds___10",
        "aspdosedis",
        "strunit",
        "sunitadmsame",
        "astrunitd",
        "sunitdissame",
        "dstrunitd"
        ]
        # END: your existing field list  
        ```

???- example "Step 5 - Make Sure Your Local Folder Structure Exists"

    ## Step 5 - Make sure Your Local Folder Structure Exists`

    Ensure you have created the required sub-folder to house the exported data files. 

    ``` markdown
    bnr-analytics/
    └── data/
        └── releases/
            ├── y2023/
            │   ├── m01/
            │   ├── m02/
            │   ├── m03/
            │   ├── m04/
            │   ├── m05/
            │   ├── m06/
            │   ├── m07/
            │   ├── m08/
            │   ├── m09/
            │   ├── m10/
            │   ├── m11/
            │   └── m12/
            ├── y2024/
            │   ├── etc.
            └── y2025/
                ├── etc.

    ```

    Tips:

    - If the month folder does not exist, Stata cannot save the file.  
    - Create folders ahead of time to avoid failed exports.


???- example "Step 6 - Carefully check the exported dataset"

    ## Step 6 - Check the exported dataset

    Never assume the export worked perfectly. After the export finishes:

    1. Open the exported `.dta` file.  
    2. Scan for obvious problems (unexpected blanks, strange dates).  
    3. Look for missing data using the built‑in Stata checks already in your DO file.

    If something looks wrong:

    - Re‑run the export for a small date range.  
    - Check variable names again.  
    - Confirm REDCap has the expected data.
    
    The code block below already exists in the export `.do` file `bnrcvd-2023-redcap-format.do` to help you check for missing data.

    ``` stata
    *-------------------------------------------------------------*
    * CHECKING LEVELS OF MISSING DATA IN THIS NEW FILE 
    *-------------------------------------------------------------*
    * A. Define lists of numeric and string variables
    *-------------------------------------------------------------*
        * Numeric variables (missing if == .)
        local numvars pid cfdoa sex dob cfage cfage_da cfadmdate dlc cfdod ///
            parish htype stype edate pstroke pstrokeyr pami pamiyr htn diab ///
            sysbp diasbp bgmmol ecg ecgd tropres trop1res trop2res assess ///
            assess1 assess2 assess3 assess4 ct doct reperf repertype reperfd ///
            aspdose aspd asptimeampm_2 vstatus aspdosedis sunitadmsame ///
            astrunitd sunitdissame dstrunitd

        * String variables (missing if == "" or == "99")
        local strvars recid redcap_event_name fname mname lname natregno ///
            recnum admtime etime ecgt reperft aspt
        *-------------------------------------------------------------*
        * B. Loop through numeric variables
        *-------------------------------------------------------------*
        di "---- Missing counts for NUMERIC variables ----"
        foreach v of local numvars {
            qui count if missing(`v')
            di "`v' : " r(N)
        }
        *-------------------------------------------------------------*
        * C. Loop through string variables
        *-------------------------------------------------------------*
        di "---- Missing counts for STRING variables ----"
        foreach v of local strvars {
            qui count if `v' == "" | `v' == "99"
            di "`v' : " r(N)
        }
        *-------------------------------------------------------------*
    ```

<br/> 
