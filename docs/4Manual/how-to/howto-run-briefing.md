
# How To: Update a BNR Analytics Briefing 
In this *How To Guide* we describe how to update an BNR BRiefing. We use the briefing known as "Hospital Cardiovascular Cases in Barbados" as our example. This is created using the `.do` file `bnrcvd-2023-count.do`

---

???- example "Step 1 - Dataset Preparation"

    ## Step 1 - Dataset Preparation

    Each briefing initially calls two `.do` files:

    > **bnrcvd-globals.do** — sets up global settings used everywhere.

    > **bnrcvd-2023-prep1.do** — prepares the cleaned dataset used in your briefing.

    In the **prep1 DO file**, the main section needing updates is at the end of the file, where the datasets with associated metadata are created.
  
???- example "Step 2 - Create DO file Copy"

    ## Step 2 - Create DO file Copy

    Always make a copy of last year’s briefing file.  
    Use a clear naming system such as:

    - `bnrcvd-2024-count.do`
    - `bnrcvd-2025-count.do`

    or perhaps,

    - `bnrcvd-2024-06-count.do` if choosing to release the briefing at more regular intervals.

    This prevents accidental edits to previous briefings and ensures a 1-to-1 match between each briefing and it's associated DO file and dataset - which will help future analysts understand past analytic efforts. 


???- example "Step 3 - Updating the briefing DO file"

    ## Step 3 - Updating the Briefing DO file

    New data will inevitably mean that certain parts of the briefing DO file will need to be updated. Each Briefing DO files makes it very clear the points that changes should be considered. At these points, the DO file contains comments like the following:

    ``` stata
    /// --- UPDATE AS NEEDED -- ///
    ```

    Below is a example list of all UPDATE comments inside `bnrcvd-2023-count.do`, with simple explanations. Similar comment points exist in each briefing DO file:

    **1. `UPDATE 5-YEAR AVERAGE AS NEEDED`**  

    - Update the comparison years used to calculate rolling averages.

    **2. `UPDATE RANGE AS NEEDED`**  
    
    - Potentially adjust y-axis range used in graphic.

    **3. `UPDATE GRAPH NAME AS NEEDED`**  

    - Update the filename of the graph that will be saved.

    **4. `UPDATE GRAPH METADATA FILE AS NEEDED`**  

    - Update the `.yml` metadata file used for graph descriptions.

    **5. `BRIEFING LAYOUT FROM HERE. UPDATE AS NEEDED`**  

    - Potentially edit the style and layout of the briefing as required.

    **6. `BRIEFING TEXT. UPDATE AS NEEDED`**  

    - Update the written text that will appear in the briefing (e.g., explanations of trends).

    **7. `BRIEFING FILENAME. UPDATE AS NEEDED`**  

    - Change the filename of the final exported briefing.

<br/>








