
# How To: Set-up BNR Analytics on a local PC
In this *How To Guide* we bring together the various steps described in more detail on the [companion page](../resource-hub-technical/stata-analytics-system.md) into a simple checklist, so you can prepare your PC for the BNR Analytics System and verify that everything works.

---

???- example "Step 1 - Install Visual Studio (VS) Code"

    ## Step 1 - Install Visual Studio (VS) Code

    ### Step 1 — Install Visual Studio (VS) Code
    VS Code is a free text editor that allows you to edit your Stata DO files, and (if you want to do this) also edit markdown pages for the BNR website. If you don't yet use VS Code, this install is your first step.

    1. Go to [https://code.visualstudio.com/](https://code.visualstudio.com/){ target="_blank"} in your web browser.
    2. Download the installer for your operating system.
    3. Run the installer and accept the default settings.
    4. Open VS Code.
    5. Click the Extensions icon on the left (it looks like four squares).
    6. In the search bar, type `Stata Enhanced` (this creates syntax highlighting for Stata DO files).
    7. Find the extension called `Stata Enhanced` by Kyle Barron and click `Install`.

    ### Verification: 
    Open any `.do` file in VS Code and confirm that the text has coloured syntax highlighting.

    ---

???- example "Step 2 - Install Git and Connect to GitHub"

    ## Step 2 — Install Git and Connect to GitHub

    Git is a system for tracking changes in files, and GitHub is an online platform for storing and collaborating on those version-controlled files. Using them for the BNR analytics do-files provides a transparent, auditable history of every code change, supports safe collaboration across the team, and helps ensure the analytics system stays efficient, reliable, and reproducible as it evolves. Git and GitHub can be used entirely free of charge. You can work with Git and GitHub from within VS Code.

    ### Installing and Setting Up Git and GitHub in VS Code

    1. Check if Git Is Already Installed
    2. Open **VS Code**.
    3.  Press **Ctrl + Shift + P** (Windows/Linux) or **Cmd + Shift + P** (Mac) to open the *Command Palette*.
    4.  Type **Git: Show Git Output** and select it.
    - If Git is installed, the output panel will show a Git version (e.g., `git version 2.44.0`) near the top of the resulting output.
    - If Git is *not* installed, VS Code will display “Git not found” and may prompt you to install it.

    ### 2. Install Git (if needed)

    1. Go to [https://git-scm.com/downloads](https://git-scm.com/downloads){ target="_blank"}
    2. Download and install Git for your operating system (accept default options).
    3.  Create a free GitHub account at [https://github.com](https://github.com){ target="_blank"} if you do not already have one.
    4.  Open VS Code.
    5.  Click the Accounts icon in the bottom-left corner and choose the option to sign in to GitHub.
    6.  Authorise VS Code to access your GitHub account when prompted.

    To download (clone) the BNR Analytics repository:

    7.  In VS Code, open the Command Palette (Ctrl+Shift+P).
    8.  Type `Git: Clone` and press Enter.
    9.  Paste the repository URL: `https://github.com/UWI-BNR/bnr-analytics`
    10. Choose a folder on your PC where you want the repository to live.
    11. Wait for the download to complete, then open the newly downloaded folder in VS Code.

    ### Verification:  
    In the folder you chose, you should see subfolders such as `do`, `ado`, `tables`, `graphics`, `outputs`, and `temp`.

    ---

???- example "Step 3 - Checking and Installing Python Using the Windows Command Prompt"

    ## Step 3 - Checking and Installing Python Using the Windows Command Prompt

    ### 1. Check if Python Is Already Installed

    - Open the Windows **Command Prompt**:  
    - Press **Windows Key**  
    - Type **cmd**  
    - Press **Enter**

    1. In the Command Prompt window, type: `python --version`

    - If Python is installed, you will see something like:  

        > Python 3.13.5  

    - If Python is **not** installed, you will see a message such as:  

        > 'python' is not recognized as an internal or external command

    ### 2. Install Python (If Needed)

    1. Go to the official Python download page:  
    [https://www.python.org/downloads/](https://www.python.org/downloads/){ target="_blank"} 

    2. Download the latest stable Python 3 installer for Windows.

    3. Run the installer and **ensure you tick the box**:  
    “Add Python to PATH”

    4. Choose **Install Now** and complete the installation.

    5. Verify installation by opening a new Command Prompt and typing:
    `python --version`
    and:
    `pip --version`
    Both should return version numbers.

    ### 3. (Optional) Create and Activate a Virtual Environment

    A **virtual environment** is a self-contained folder that holds its own Python installation and libraries. It is useful because it keeps each project separate, preventing conflicts between different package versions and ensuring your code runs consistently on any system.

    6. In a `cmd` window, navigate to your project folder:
    > cd path\to\your\project

    7. Create a virtual environment:
    `python -m venv venv`

    8. Activate it by typing:
    `venv\Scripts\activate.bat`

    9. When activated, the command prompt will show something like:
    > (venv) C:\your\path>

    This confirms the virtual environment is active and ready for use.

    You can read more about python virtual environments here: [https://realpython.com/python-virtual-environments-a-primer/](https://realpython.com/python-virtual-environments-a-primer/){ target="_blank"}

    ---

???- example "Step 4 — Check your Analytics Folder Structure"

    ## Step 4 — Check your Analytics Folder Structure

    Once cloned, your `bnr-analytics` folder will contain the following subfolders:

    ```
    .
    ├── bnr-analytics/      
    │   ├── ado             
    │   ├── do
    ├── .gitignore
    ├── README.md
    ```

    As well as the ado/ and do/ subfolders containing `.ado` and `.do` files respectively, there are **two files**.

    > **.gitignore**<br/>
    This file is important. It tells GitHub which files and folders **it should not transfer** to the online GitHub repository. This ensures that identifiable data are not released to an online location by mistake.

    > **README.md**<br/>
    This file can be read at our online GitHub repository, and lists the available `.ado` and `.do` files. 

    You will also have received a *BNR Analytics* ZIP file (`bnr-analytics.zip`). This zip file contains the remaining *BNR Analytics* subfolders. 

    10. Place the zip file in the `bnr-analytics/` subfolder.
    11. Unzip to bnr-analytics/ (NOT TO a subfolder)
    12. Once unzipped, your `bnr-analytics` folder should look like this:
   
    ```
    .
    ├── bnr-analytics/      
    │   ├── ado             
    │   ├── data         <-- Contains identifiable datasets 
    │   ├── do           <-- Contains `bnrcvd-2023-redcap-token` DO file
    │   ├── graphics
    │   ├── log
    │   ├── outputs      <-- Contains briefings (will be replaced on running DO files)
    │   ├── tables
    │   ├── temp
    ├── .gitignore
    ├── README.md
    ```

    **Note:**  
    The `data` and `temp` folders, and the `bnrcvd-2023-redcap-token.do` DO file hold identifiable data and interim files. These must only exist on **secure, encrypted local storage** and must not be uploaded to GitHub or any other public service.

    ---

???- example "Step 5 — Configure profile.do in Stata"

    ## Step 5 — Configure `profile.do` in Stata

    The `profile.do` file is a Stata script that runs automatically every time you start Stata. You will use it to tell Stata where your local `bnr-analytics` repository is located, and where Python is installed on your PC.

    You have access to an example `profile.do` file in the `setup` folder of the `bnr_analytics.zip folder. You can copy this file to your Stata `PERSONAL` folder and edit it there, or create a new `profile.do` file from scratch in that folder.

    13. Open Stata and type `sysdir` in the Command window, then press Enter.
    14. Note the folder shown next to `PERSONAL`.
    15. In that `PERSONAL` folder, create or edit the provided `profile.do` file.
    16. Edit the lines that tell Stata where your `bnr-analytics` repository lives and where Python is installed.

    Example (you must change the paths to match your PC):

    `capture noisily adopath + "C:/Users/Joan/BNR/bnr-analytics/"`  
    `capture noisily adopath + "C:/Users/Joan/BNR/bnr-analytics/do/"`  
    `capture noisily adopath + "C:/Users/Joan/BNR/bnr-analytics/ado/"`  
    `python set exec "C:/Users/Joan/AppData/Local/Programs/Python/Python312/python.exe", permanently`

    17. Save `profile.do`.

    ### Verification:

    18. Close Stata completely.
    19. Open Stata again (this runs `profile.do`).
    20. Type `adopath` and press Enter. Confirm your `bnr-analytics` paths are listed.
    21. Type `python query` and press Enter. Confirm the Python path and version are correct.

    ---

???- example "Step 6 — Configure your GLOBAL settings"

    ## Step 6 — Configure your GLOBAL settings

    You have a simple Stata ADO file called `bnrpath.ado` in the `ado/` folder of your `bnr-analytics` repository. This file contains a single line of code that you should change to reflect the location of your *bnr-analytics* repository.

    > global BNRROOT "C:/yasuki/Sync/BNR-sandbox/006-dev/github/bnr-analytics"

    Change the path in quotes to match the location of your local `bnr-analytics` folder.

    You also have a local DO file called `bnrcvd-globals.do` in the `do/` folder of your `bnr-analytics` repository. This file is called by most subsequent analysis `.do` files, and contains a series of folder locations, system settings, and the BNR briefings color scheme. You can change any of these settings at any time, and these changes will be reflected across the subsequent DO files. 

    ---

???- example "Step 7 — Run a Simple Test DO File"

    ## Step 7 — Run a Simple Test DO File

    1.  In Stata, use the `cd` command to move to your `bnr-analytics` folder, or supply the full path in quotes.
    2.  Run the global setup file, for example: `do "C:/Users/Joan/BNR/bnr-analytics/do/bnrcvd-globals.do"`
    3.  Check that it runs without errors.

    ---

???- example "Step 8 — Run an Analytics Script as a Final Check"

    ## Step 8 — Run an Analytics Script as a Final Check

    25. In Stata, run one of the main analytics scripts, for example: `do "C:/Users/Joan/BNR/bnr-analytics/do/bnrcvd-2023-count.do"`
    26. Watch the Stata output window for any missing-file or path errors.
    27. When it finishes, look in the `outputs` or `tables` folder to confirm that new output files (for example Excel or PDF) have been created.

    If this script runs to completion and produces outputs in the expected folders, your local PC is fully configured for the BNR Analytics System.
  
  <br/> 
