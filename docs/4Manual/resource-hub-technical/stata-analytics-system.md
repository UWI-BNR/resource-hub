# Stata Analytics System

!!! note "Overview"
    This page outlines **The BNR Stata Analytics system, and how to set this up on a local PC**.

## Page Layout
The Stata Analytics system has been built to partially automate a series of reporting tasks for the BNR. The system is currently prepared for the CVD arm of the BNR, for data between 2010 and 2023, with plans to extend the timeframe, and (later) to extend it to include cancers, hypertension control and diabetes control. This page describes the system, and how to set it up on a local PC. The page is organised as follows:

1. The Stata DO files
2. Location of Stata DO files
3. Dependencies: Visual Studio Code (free DO file editor)
4. Dependencies: Git
5. Dependencies: Python
6. Dependencies: Analytics Folder structure 
7. Dependencies: Stata `profile.do`
8. Setting up the system on a local PC
   

???+ info "(1) The Stata DO files"

    ## (1) Description of Stata `.do` Files  
    This document provides a structured, hyperlink-enabled catalogue of all Stata `.do` files contained within the **BNR Analytics** repository. Each entry includes the file name, and a concise description of the file’s purpose within the BNR-CVD data processing and reporting workflow. Full commenting for each DO file is contained as part of the DO file itself. 

    | NAME | DESCRIPTION |
    | --- | --- |
    | 2023 ANALYTICS |
    | [`bnrcvd-2023-prep1.do`](https://github.com/UWI-BNR/bnr-analytics/blob/main/do/bnrcvd-2023-prep1.do){ target="_blank"} |  Uses the full cumulative dataset (2009–2023) to create an analysis-ready but still identifiable dataset. Is called from all subsequent 2023 Analytics DO files. |
    | [`bnrcvd-2023-count.do`](https://github.com/UWI-BNR/bnr-analytics/blob/main/do/bnrcvd-2023-count.do){ target="_blank"} | Creates the 2023 Briefing called<br/>*Hospital Cardiovascular Cases in Barbados* |
    | [`bnrcvd-2023-incidence.do`](https://github.com/UWI-BNR/bnr-analytics/blob/main/do/bnrcvd-2023-incidence.do){ target="_blank"} | Creates the 2023 Briefing called<br/>*Hospital Cardiovascular Event Rate in Barbados* |
    | [`bnrcvd-2023-case-fatality.do`](https://github.com/UWI-BNR/bnr-analytics/blob/main/do/bnrcvd-2023-case-fatality.do){ target="_blank"} | Creates the 2023 Briefing called<br/>*In-Hospital Cardiovascular Deaths in Barbados* |
    | [`bnrcvd-2023-length-of-stay.do`](https://github.com/UWI-BNR/bnr-analytics/blob/main/do/bnrcvd-2023-length-of-stay.do){ target="_blank"} | Creates the 2023 Briefing <br/>*Hospital Stay Among Cardiovascular Patients in Barbados* |
    | [`bnrcvd-2023-tabulations.do`](https://github.com/UWI-BNR/bnr-analytics/blob/main/do/bnrcvd-2023-tabulations.do){ target="_blank"} | Creates a series of MARKDOWN and EXCEL data tables that can be seen on the BNR web page: [Data Tables 2023](https://uwi-bnr.github.io/resource-hub/3Reporting/datatables/) |
    | [`bnrcvd-2023-missing.do`](https://github.com/UWI-BNR/bnr-analytics/blob/main/do/bnrcvd-2023-missing.do){ target="_blank"} | Creates a single Excel spreadsheet containing a series of tables looking at levels of missing data in key BNR registry variables through time (2010 - 2023). The Excel spreadsheet is available [on the BNR website](https://uwi-bnr.github.io/resource-hub/2Data/dataset/dataquality/) |
    | 2023 UTILITIES | |
    | [`bnrcvd-2023-redcap.do`](https://github.com/UWI-BNR/bnr-analytics/blob/main/do/bnrcvd-2023-redcap.do){ target="_blank"} | Exports data from the REDCap Core BNR-CVD database (PID 670), capturing raw data as strings for downstream processing. Uses python (PyCap) for this API export. |
    | [`bnrcvd-globals.do`](https://github.com/UWI-BNR/bnr-analytics/blob/main/do/bnrcvd-globals.do){ target="_blank"} | Defines global macros used across all BNR-CVD analytics scripts, including directory paths, color HEX values, UNICODE graphics markers, and more. Is called from each 2023 Analytics DO file. |
    | [`bnrcvd-unwpp.do`](https://github.com/UWI-BNR/bnr-analytics/blob/main/do/bnrcvd-unwpp.do){ target="_blank"} | Uses the United Nationas WPP API to extract the UN World Population Prospects data for Barbados into analysis-ready population denominators for rate calculations. Uses python to complete this API export. |
    | [`bnrcvd-2023-missing-collect.do`](https://github.com/UWI-BNR/bnr-analytics/blob/main/do/bnrcvd-2023-missing-collect.do){ target="_blank"} | A short DO file utility that is called repeatedly in the main *missing* DO file `bnrcvd-2023-missing.do`. Simply to make the main DO file more manageable - should formatting changes ever be wanted for the many tables, they can be performed in this single block of code.|
    | 2023 LEGACY DO FILES | |
    | [`bnrcvd-2023-forensics1.do`](https://github.com/UWI-BNR/bnr-analytics/blob/main/do/bnrcvd-2023-forensics1.do){ target="_blank"} |  This DO file is not part of the main analytics. It explores alternative datasets as possible candidates to contribute to the cumulative dataset. |
    | [`bnrcvd-2023-forensics2.do`](https://github.com/UWI-BNR/bnr-analytics/blob/main/do/bnrcvd-2023-forensics2.do){ target="_blank"} | This DO file is not part of the main analytics. It highlights the poor DM/ folder and file structure in the BNR file repository as of Nov-2025. The resulting output from this DO file is presented on the BNR website: [Duplicate Datasets](https://uwi-bnr.github.io/resource-hub/2Data/dataset/forensics/#case-example-2-duplicate-datasets-in-the-bnr-document-repository)  |
    | 2023 ADO FILES | |
    | [`bnrpath.ado`](https://github.com/UWI-BNR/bnr-analytics/blob/main/ado/bnrpath.ado){ target="_blank"} |  This ADO file sets the root path for the project.<br/>**Each approved analyst should set the local path in this **`.ado`** file to their `bnr-analytics` repository** |
    | [`bnryaml.ado`](https://github.com/UWI-BNR/bnr-analytics/blob/main/ado/bnryaml.ado){ target="_blank"} |  This ADO file creates a simple .yml (YAML) file, containing dataset-level metadata. Review its use in any briefing DO file (such as `bnrcvd-2023-count.do`). <br/><br/> The idea is that each dataset will have an associated `.yml` file. A .yml file is a human-readable configuration file (it is effectively a `.txt` file) written in the YAML format, which is useful for storing dataset-level metadata because it allows you to organise information such as variable names, types, labels, and descriptions in a clean, structured, machine-readable format that is easy for both humans and software tools to interpret.<br/><br/>It has an associated help file (`bnryaml.sthlp`). |
    | [`make_meta-xlsx.ado`](https://github.com/UWI-BNR/bnr-analytics/blob/main/ado/make_meta_xlsx.ado){ target="_blank"} |  This ADO file has one sepecific use - to attach dataset-level and variable-level metadata to an exported Excel aggregated dataset. For an example of its use, see `bnrcvd-2023-count.do`. |
    | 2024 ANALYTICS |
    | [`bnrcvd-2024-redcap-format.do`](https://github.com/UWI-BNR/bnr-analytics/blob/main/do/bnrcvd-2024-redcap-format.do){ target="_blank"} |  Uses python coding (the package: PyCap) to extract data directly from the REDCap API. The `.do` file extracts variables and associated variable-level metadata (variable labels, category labelling) directly into a Stata dataset via a python-pandas dataframe. The variable list to be exported and the export timeframe can be easily edited in this `.do` file. This export process is explained in the [associated help file](../how-to/howto-export.md). |
    | [`bnrcvd-2024-redcap-noformat.do`](https://github.com/UWI-BNR/bnr-analytics/blob/main/do/bnrcvd-2024-redcap-format.do){ target="_blank"} |  The main REDCap export `.do` file (`bnrcvd-2024-redcap-format.do`) contains a fair bit of Python coding. I have created this alternative (much simpler) `.do` file that simply extracts variables from REDCap in string format and without associated metadata - to leave all subsequent data preparation in the more familiar Stata environment. (This might be useful for the future...).  |
    | [`bnrcvd-2024-prep1.do`](https://github.com/UWI-BNR/bnr-analytics/blob/main/do/bnrcvd-2024-prep1.do){ target="_blank"} |  Joins monthly releases from 2024 to the (2009-2023) cumulative dataset. Otherwise, coding is much the same as for the 2023 version of the DO file. Exported files are placed in the BNR `temp/` folder and are not for general release. |
    | [`bnrcvd-2024-count.do`](https://github.com/UWI-BNR/bnr-analytics/blob/main/do/bnrcvd-2024-count.do){ target="_blank"} | This `.do` file is similar in style to the 2023 version of this file, but does not go beyond the creation  of a week-by-week count of CVD event, stratified by type (strokes, heart attacks). The 2024 charts are compared against the average of the previous 5 years (2018-2023). The chart can be built slowly over time as more data from the year become available, and give an ongoing sense of case-load compared to recent years.  |
---

???- info "(2) Location of Stata DO files"

    ## (2) The Stata **`.do`** file repository

    All Stata **`.do`** files described in the table above are stored in the public GitHub repository:

    **https://github.com/UWI-BNR/bnr-analytics**

    To use the **`.do`** files, you can copy (or clone) this repository to any local PC. In section 8 below we show you how to do this as part of the full setup instructions.   

---

???- info "(3) Dependencies: Visual Studio Code (free DO file editor)"

    ## (3) Dependency: Visual Studio Code

    Although not compulsory, we recommend the use of Visual Studio Code - a free text editor - to view and edit the Stata **`.do`** files. 

    ### How to Install Visual Studio Code (VS Code)

    If you have never installed a code editor before, VS Code is a simple, free option that makes it much easier to work with Stata `.do` files.

    Follow these steps:

    1. **Download VS Code**
    - Go to: https://code.visualstudio.com/
    - Click **Download for Windows** (or Mac, if you use a Mac).
    - When the installer downloads, double-click it and follow the prompts (accept the defaults).

    1. **Open VS Code**
    - After installation, open VS Code like any normal program.

    1. **Install the “Stata Enhanced” Extension**
    - In VS Code, look on the left for the square “Extensions” icon.
    - Click it, then type **Stata Enhanced** into the search bar.
    - Choose the extension created by **Kyle Barron**.
    - Click **Install**.
    
    This extension adds:
    - Stata-coloured syntax highlighting  
    - Better readability for `.do` files  
    - Helpful indentation and formatting

    1. **(Optional) Associate `.do` Files with VS Code**
    - Right-click any `.do` file on your computer.
    - Choose **Open With… → Choose another app → Visual Studio Code**.
    - Tick **Always use this app**.
    - Now all `.do` files will open in VS Code by default.

    You’re now ready to browse, edit and run your Stata scripts with clearer formatting and easier navigation.

---

???- info "(4) Dependencies: Git and GitHub"

    ## (4) Dependency: Git and GitHub

    ### How to Install Git and Connect to GitHub (Using VS Code)

    You will need Git so that VS Code can download (“clone”) the `bnr-analytics` repository from GitHub.

    #### 1. Install Git
    1. Visit: https://git-scm.com/downloads  
    2. Download **Git for Windows**.
    3. Run the installer.  
    - You can accept the default settings.
    4. When complete, restart VS Code (if it was already open).

    To confirm Git is working:
    - In VS Code, press **Ctrl+Shift+`** to open the terminal.
    - Type:

    git --version

    You should see something like: `git version 2.xx.x`

    #### 2. Create a GitHub Account
    1. Go to https://github.com  
    2. Click **Sign Up**.
    3. Choose a username, enter your email, and create a password.

    #### 3. Sign in to GitHub inside VS Code
    1. In VS Code, click the **Accounts** icon (bottom-left).
    2. Choose **Sign in to GitHub**.
    3. A GitHub login page will appear — sign in.
    4. Approve VS Code’s request to access your GitHub account.

    You have now linked your computer, Git, VS Code, and GitHub together.

    #### 4. Verify That You Can Access the Repository
    The BNR analytics repository is here:

    - https://github.com/UWI-BNR/bnr-analytics

    In VS Code:

    1. Open the **Source Control** panel (left toolbar).
    2. Click **Clone Repository**.
    3. Paste the URL above.
    4. Choose a location on your PC where the files should be stored.

    If it downloads successfully, your Git setup is working correctly.

---

???- info "(5) Dependencies: Python"

    ## (5) Dependency: Python

    Several Stata **`.do`** files contain small snippets of `python` code, for example to export data from REDCap, or to build metadata to accompany published graphics and datasets.

    ### How to Install (or Update) Python and Verify It Works with Stata

    This section shows how to (A) check whether Python already exists on your PC, (B) install or update Python if needed, and (C) verify that Stata can use Python correctly. All steps are written for beginners.

    ### A. Check Whether Python Is Already Installed

    1. Open VS Code.
    2. Press Ctrl+Shift+` (Ctrl + Shift + backtick) to open the Terminal.
    3. Type the command `python --version` and press Enter.
    4. If that does not work, type `py --version` and press Enter.

    If Python is installed, you will see something like `Python 3.11.6`.  
    If you see an error such as `'python' is not recognized`, then Python is not installed or not on your PATH.

    If the version shown is `Python 3.x`, you are fine.  
    If it shows `Python 2.x`, or no Python at all, you should install or update Python.

    ---

    ### B. Install or Update Python

    1. Open a web browser and go to: https://www.python.org/downloads/
    2. Click the main button that says something like `Download Python 3.x`.
    3. Run the installer that you downloaded.
    4. On the first screen of the installer, tick the box that says `Add Python to PATH`.
    5. Click `Install Now` and follow the prompts until it finishes.

    To confirm that it worked:

    1. Open VS Code again and open the Terminal (Ctrl+Shift+`).
    2. Type `python --version` and press Enter.

    You should now see a Python 3.x version.

    ---

    ### C. Verify the Python Installation Inside Stata

    1. Open Stata.
    2. In the Stata Command window, type `python query` and press Enter.

    Stata should show:

    - The Python executable path (where Python lives on your computer)  
    - The Python version (must be 3.x)  
    - A message that shows Python is configured

    If Stata shows the wrong Python path, you can set it manually.

    1. In VS Code Terminal, type `where python` and press Enter.  
    This shows the full path to `python.exe` on your PC, for example:  
    `C:\Users\Joan\AppData\Local\Programs\Python\Python312\python.exe`
    2. Copy that full path.
    3. In Stata, type the command below, replacing the path with your own:

    `python set exec "C:/Users/Joan/AppData/Local/Programs/Python/Python312/python.exe", permanently`

    4. Press Enter, then type `python query` again in Stata.

    Once Stata reports a valid Python 3.x path and no errors, your Python setup is complete.

---

???- info "(6) Dependencies: Analytics Folder Structure" 

    ## (6) Dependency: Analytics Folder Structure
    You will need to setup the The BNR Analytics folder structure will look like this:

    ```
    .
    ├── bnr-analytics/      
    │   ├── ado             
    │   ├── data
    │   ├── do
    │   ├── graphics
    │   ├── log
    │   ├── outputs
    │   ├── tables
    │   ├── temp
    │   ├── data
    ```

    Each folder has the following use:

    ### bnr-analytics 
    This is the name of GitHub repository containing all analytics **`.do`** files.
    
    ### /ado 
    Contains `.ado` utility programs built as part of the BNR analytics system.
    
    ### /data 
    Contains key datasets needed as **`.do`** file inputs.     
    
    ### /do
    Contains all **`.do`** files.
    
    ### /graphics
    Contains published BNR graphics published as part of "BNR briefings" series.
    
    ### /log
    Contains Stata log (`.smcl`) files.
    
    ### /outputs
    Contains **`.pdf`** files generated by the Stata analytics **`.do`** files.
    
    ### /tables
    Contains tables generated by the Stata analytics **`.do`** files.
    
    ### /temp
    Contains all files generated by **`.do`** files that are not final outputs. Can delete this `/temp` folder at intervals without data loss.

    !!! warning 
    
        The **/data** and **/temp** folders contain identifiable data, should NOT be stored on GitHub, and should only be stored on a local PC with full-disk encryption or with an encrypted container."

---

???- info "(7) Dependencies: Stata `profile.do`"

    ## (7) Dependency: **`profile.do`**

    The Stata **`profile.do`** is a simple set of instructions that Stata runs automatically every time you start a new session of Stata.  The template is a very simple **`profile.do`**, and looks somthing like this:

    ```
    *────────────────────────────────────────────────────────────────────────────*
    *  profile.do – run automatically at Stata startup
    * Created by Ian Hambleton: 09-JUL-2025
    * Last Modified: 02-DEC-2025
    * ────────────────────────────────────────────────────────────────────────────*

    ** BNR Refit Directories (EDIT ALL THREE FILEPATHS for LOCAL location) 
    ** It is likely that you will edit just the first part of each line:
    **          C:/yasuki/Sync/BNR-sandbox/006-dev/
    capture noisily adopath + "C:/yasuki/Sync/BNR-sandbox/006-dev/github/bnr-analytics/"
    capture noisily adopath + "C:/yasuki/Sync/BNR-sandbox/006-dev/github/bnr-analytics/do/"
    capture noisily adopath + "C:/yasuki/Sync/BNR-sandbox/006-dev/github/bnr-analytics/ado/"

    ** Python. Added 02-DEC-2025 (EDIT FILEPATH for LOCAL Python location)
    python set exec "C:/Users/ianha/AppData/Local/Programs/Python/Python313/python.exe", permanently
    noisily python query
    ``` 

    ### How to Place and Edit Your `profile.do` File

    Stata automatically runs a file called `profile.do` every time it starts. For the BNR Analytics System, this file tells Stata where your `bnr-analytics` folders are and where Python is installed.

    ### Step 1 — Find (or Create) Your `profile.do`

    1. Open Stata.
    2. In the Command window, type `sysdir` and press Enter.
    3. Look for the line labelled `PERSONAL`. It will look like:

    `PERSONAL   C:\Users\YourName\Documents\Stata`

    4. Open that `PERSONAL` folder in File Explorer.
    5. If there is already a file called `profile.do`, open it in VS Code.
    6. If there is no `profile.do`, create a new text file named `profile.do` in that folder and open it in VS Code.

    ---

    ### Step 2 — Edit the Paths to Match Your PC

    You need to tell Stata where your local copy of the `bnr-analytics` repository lives and where Python is installed.

    #### A. Set the BNR Analytics paths

    Suppose you cloned the repository into:

    `C:/Users/Joan/BNR/bnr-analytics/`

    Then your `profile.do` should contain lines like:

    `capture noisily adopath + "C:/Users/Joan/BNR/bnr-analytics/"`  
    `capture noisily adopath + "C:/Users/Joan/BNR/bnr-analytics/do/"`  
    `capture noisily adopath + "C:/Users/Joan/BNR/bnr-analytics/ado/"`

    Make sure the path inside the quotes matches where the `bnr-analytics` folder actually is on your PC.

    #### B. Set the Python executable path

    7. In VS Code, open the Terminal (Ctrl+Shift+`).
    8. Type `where python` and press Enter.
    9. Copy the full path shown, for example:

    `C:\Users\Joan\AppData\Local\Programs\Python\Python312\python.exe`

    10. In `profile.do`, add a line like:

    `python set exec "C:/Users/Joan/AppData/Local/Programs/Python/Python312/python.exe", permanently`

    Use forward slashes `/` in the path inside the quotes, as in the example above.

    Save `profile.do` when you are finished editing.

    ---

    ### Step 3 — Test That Stata Recognises Your Setup

    11. Close Stata completely.
    12. Re-open Stata (this will cause `profile.do` to run).
    13. In the Command window, type `adopath` and press Enter.

    Check that the output includes entries pointing to your `bnr-analytics`, `bnr-analytics/do`, and `bnr-analytics/ado` folders.

    14. Then type `python query` and press Enter.

    Check that:

    - The Python version is 3.x  
    - The Python executable path is the one you set  
    - There are no error messages

    If both `adopath` and `python query` look correct, your `profile.do` is working and your Stata startup environment is correctly configured.
 
<br/>
