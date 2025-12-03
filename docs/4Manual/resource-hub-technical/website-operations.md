# How the BNR Website Was Built — and How We Keep It Updated

The BNR Resource Hub is built using **Material for MkDocs**, a simple and modern documentation system.  
Everything lives inside a GitHub repository:  
https://github.com/UWI-BNR/resource-hub

There is **no traditional server**, no complex CMS, and no coding required. The website is made from plain text files written in Markdown. When files are updated and pushed to GitHub, the site automatically rebuilds itself.

The goal is to keep the site **easy to maintain**, even for colleagues who have never edited a website before.

---


???- info "(1) Our Website Structure"

    ## 1. The Actual Structure of the Website (`docs/` folder)

    Your repository structure (as provided) looks like this:

        docs/
        ├── 1Workflow/
        ├── 2Data/
        ├── 3Reporting/
        ├── 4Manual/
        ├── 5Downloads/
        ├── assets/
        ├── downloads/
        ├── js/
        ├── styles/
        └── index.md

    Other important files:

        mkdocs.yml        <- main MKDocs configuration
        .nav.yml          <- custom navigation structure
        site/             <- auto-generated output folder (never edit manually)

    Each numbered folder (1Workflow, 2Data, etc.) represents a **top-level section** of the website.  
    Inside each folder you’ll normally find:

    - one `index.md` file (main page for that section)
    - additional `.md` pages
    - sometimes a `nav.yml` file controlling the sidebar menu for that section

    This structure makes the site modular, clean, and easy to expand.

---

???- info "(2) A Guide to Creating Content using Markdown"

    ## 2. Using Markdown: A Guide 

    Markdown is a lightweight writing format.  
    If you can type an email, you can write Markdown.

    Below is a **practical, extended guide** covering everything you’re likely to need.

    ### 2.1 Editing a Markdown Page in GitHub

    1. Go to the repository:  
    https://github.com/UWI-BNR/resource-hub
    2. Navigate to:  
    `docs/` → choose the correct folder → choose the `.md` file.
    3. Click the **pencil icon** (✏️) to edit.
    4. Make your changes in the text editor.
    5. Write a short commit message, e.g.  
    `Updated 2Data/quality-overview.md`
    6. Click **Commit changes**.

    Your edits will appear on the live website after the automatic rebuild.

    ---

    ### 2.2 Essential Markdown Formatting

    #### Headings
    Use `#` symbols to create headings:

        # Main heading
        ## Sub heading
        ### Smaller heading
        #### Fourth-level heading

    E.g. for header levels 3 and 4, these become:
    ### Smaller heading
    #### Fourth-level heading

    Material for MkDocs automatically generates the right fonts and sizes.

    ---

    #### Paragraphs
    Just write normally:

        This is a paragraph of standard text. No formatting needed.

    Leave a blank line between paragraphs.

    ---

    #### Bold and Italic

        **Bold text**
        *Italic text*
        ***Bold and italic together***

    These becomes:<br/>
    **Bold text**<br/>
    *Italic text*<br/>
    ***Bold and italic together***

    ---

    #### Bullet Lists

        - Item one
        - Item two
            - Nested bullet
        - Item three

    These becomes:<br/>

      - Item one
      - Item two
          - Nested bullet
      - Item three

    ---

    #### Numbered Lists

        1. First step
        2. Second step
        3. Third step

    These becomes:<br/>

     7. First step
     8. Second step
     9. Third step

    ---

    #### Links

        [BNR homepage](https://uwi-bnr.github.io/resource-hub/)

    This becomes:<br/> 
    [BNR homepage](https://uwi-bnr.github.io/resource-hub/)


    You can link to other pages inside your docs folder:

        [Introducing the BNR Refit](../../1Workflow/index.md)

    This becomes:<br/> 
    [Introducing the BNR Refit](../../1Workflow/index.md)

    ---

    #### Images

    Place images in `docs/assets/images/`.

        ![Figure 1](../../assets/images/bnrcvd-count-figure1.png)

    This becomes:<br/> 
    ![Figure 1](../../assets/images/bnrcvd-count-figure1.png)

    Note: MkDocs will resize automatically.

    ---

    #### Horizontal Rule

    A simple divider:

        ---

    This becomes:<br/> 

    ---

    #### Code Blocks

    Use triple backticks:

        ```stata
        summarize age, detail
        ```

    This becomes:<br/> 
    ```stata
    summarize age, detail
    ```

    Supported languages include: stata, python, r, bash, yaml, markdown, json.

    ---

    #### Blockquotes

        > This is a quote or highlighted note.

    This becomes:<br/> 
    > This is a quote or highlighted note.

    ---

    #### Tables

    A basic table:

        | Variable | Description             | Type  |
        |---------|--------------------------|-------|
        | age     | Age of participant       | int   |
        | sex     | Biological sex           | string|

    This becomes:<br/> 

    | Variable | Description             | Type  |
    |---------|--------------------------|-------|
    | age     | Age of participant       | int   |
    | sex     | Biological sex           | string|

    ---

    #### Admonition Blocks (Important for MkDocs!)

    MkDocs Material supports *admonitions*, which highlight information clearly:

        !!! note
            This is a note.
        
        !!! warning
            This is a warning block.
        
        !!! tip
            This is a helpful tip.

    These become:<br/> 

    !!! note
        This is a note.
    
    !!! warning
        This is a warning block.
    
    !!! tip
        This is a helpful tip.

    And you can include other types of markdown formatting within these boxes.

    ---

    #### Callouts with Titles

        !!! info "Why this matters"
            Key context or explanation here.

    This becomes:<br/> 

    !!! info "Why this matters"
        Key context or explanation here.

    ---

    #### Collapsible Sections (useful for long technical content)

        ??? note "Click to expand"
            Hidden content goes here.
            More details here.

    This becomes:<br/> 

    ??? note "Click to expand"
        Hidden content goes here.
        More details here.

    ---

    #### Footnotes

        Here is a statement that needs a reference.[^1]

        [^1]: This is the footnote text.

    This becomes:<br/> 

    Here is a statement that needs a reference.[^1]

    [^1]: This is the footnote text.

    And you can spot the footnote at the end of this page.

    ---

    #### Inline HTML (allowed when needed)

    You can embed simple HTML:

        <span style="color: #E87A00; font-weight: bold;">Orange and Bold</span>

    This becomes:<br/> 

    <span style="color: #E87A00; font-weight: bold;">Orange and Bold</span>

    ---

    ### 2.3 Tips for Writing Pages That Look Good in MkDocs

    - Keep headings short and meaningful.
    - Use bullet points instead of long paragraphs.
    - Break long pages into sections using `##` and `###`.
    - Use admonitions (e.g., !!! note) to draw attention to key details.
    - Use tables sparingly but effectively.
    - For long code examples, prefer fenced code blocks.
    - Use relative links (e.g., `../4Manual/index.md`) so pages remain portable.

---

???- info "(3) Creating a New Markdown Page"

    ## (3) Creating a New Markdown Page

    Creating a new page is simply creating a new `.md` file.

    ### Steps

    1. Navigate to the appropriate folder, e.g.  
    `docs/3Reporting/`
    2. Click **Add file → Create new file**.
    3. Name it something like:

        `interpretation-guide.md`

    4. Add content, for example:
   
        > ### Interpretation Guide
        This page explains…

    5. Commit the new file.

    ### Adding the Page to Navigation

    The sidebar is controlled by:

    - the project-wide `mkdocs.yml`, and  
    - your local `.nav.yml` files (per section)

    Example entry for `.nav.yml`:

        nav:
        - Reporting Home: index.md
        - Interpretation Guide: interpretation-guide.md

    Commit the update and your page appears in the menu.

---

???- info "(4) Who Maintains the Site"

    ## (4) Who Maintains the Site and Who Can Upload Content

    ### Site Maintainer
    The **BNR Technical Lead** oversees:

    - the overall structure  
    - ensuring consistency across sections  
    - approving new pages or reorganisations  
    - managing navigation files  

    ### Content Contributors
    An assigned BNR team member may edit or create `.md` files if:

    - content is approved by the Technical Lead  
    - the structure is followed  
    - filenames are sensible  
    - the navigation file is updated if needed  

    ### Technical Support
    For errors or advanced features, support comes from:

    - the analytics/technical consultant  
    - repository administrator

---

???- info "(5) Website Maintainance"

    ## (5) Why This Website Is Easy to Maintain

    - Markdown is extremely simple and readable  
    - GitHub editing requires no software  
    - MkDocs handles formatting, layout, menus, and themes  
    - The site rebuilds automatically  
    - Content remains stable as staff change  
    - Website hosting via GitHub Pages is free! 

    This (hopefully) ensures long-term sustainability of the BNR Resource Hub.
