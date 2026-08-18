# Lab 3- Intelligent File Organizer with Copilot Cowork

Estimated Time -30 minutes

Apps -Copilot Cowork, OneDrive, SharePoint, Excel, Microsoft Teams

## Lab Objectives

By the end of this lab, you will be able to:

- Classify and rename enterprise files using AI-generated naming
  conventions

- Apply the YYYY-MM-DD_Topic_DocType rename convention across an entire
  OneDrive folder

- Execute a full governance audit covering duplicates, staleness,
  sharing risks, and ownership gaps

- Use human-in-the-loop approval gates before every bulk file operation

- Generate an Excel governance tracker and post a Teams summary from a
  single instruction

- Reorganise HR documents into category subfolders with a
  department-aware naming scheme

- Apply responsible AI principles --- understanding which governance
  actions require human approval

## Lab Scenario

You are a Power User or IT Administrator at Zava Retail, overseeing a
shared OneDrive environment containing 28 mixed files across retail, HR,
finance, and project folders. File naming is inconsistent, governance is
weak, and a compliance review is approaching.

You will use Microsoft 365 Copilot Cowork --- an agentic AI layer that
orchestrates OneDrive, SharePoint, Excel, and Teams --- to classify,
rename, audit, report on, and reorganise these files. Every bulk action
requires your explicit approval before it executes.

## Lab prerequisites

Complete the following setup steps before starting the lab (estimated:
15--20 minutes):

- Required Microsoft 365 Environment

- Microsoft 365 Copilot with Copilot Cowork enabled

- Microsoft Teams with permission to post to channels

- OneDrive for Business and SharePoint Online

- Microsoft Excel (Web or Desktop)

- Microsoft Graph-connected M365 tenant

- Required OneDrive folder structure

- Create a Lab Files folder in OneDrive with these four subfolders:

- Lab Files / HR --- upload provided HR document samples

- Lab Files / Retail --- upload provided retail document samples

- Lab Files / Shared Files --- configure 'Anyone with the link'
  sharing on at least 3 files

- Lab Files / Archive Candidates --- optional pre-populated stale
  documents

- Required Teams environment

- Team: Zava Retail (or equivalent)

- Channel: General (Standard) --- target for Exercise 3 Teams post

## Exercise 1 -- Automated file classification and renaming

Task 1: Create the SharePoint site

1.  From a new browser, navigate to
    <https://m365.cloud.microsoft/chat/> 
     
2.  Sign in with 
    - **Email/Username:** <inject key="AzureAdUserEmail"></inject>

       ![](media/media/de1s1.png)

	- **Password:** <inject key="AzureAdUserPassword"></inject>

        ![](media/media/de1s2.png)

2. When prompted with the **Stay signed in?** dialog, select **No** to continue.

    ![](media/media/de1s3.png)

2.  Select **Apps** from the left pane and then
    select **SharePoint** once the Apps are loaded.

    ![](media/media/de2s2.png)

    ![](media/media/de2s2.0.png)

1. In SharePoint, select **Build (1)** from the left navigation pane, then under **Start building**, choose **Site (2)** to begin creating a new SharePoint site.

    ![](media/media/de2s3.png)

4.  Select **Communication site (1)** from the Select the site template page, then select a **template (2)** to be used.

    ![](media/media/de2s4.png "A screenshot of a computer AI-generated content may be incorrect.")

5. Select **Use template** to create the site using the displayed template.

    ![](media/media/de2s5.png "A screenshot of a website AI-generated content may be incorrect.")

7. On the **Set up your site** page, enter **Zava Site** in the **Site name (1)** field, verify that the **Site address (2)** is available, and then select **Create site (3)** to create the SharePoint site.

    ![](media/media/de2s6.png)

    >**Note:** If you receive the message **"The site address is available with modification"**, update the **Site address** by adding the suffix **`2 or 3`** to the end of the site name (for example, `ZavaSite2`), and then continue with the site creation process.

1. Wait until the **Your site is ready!** message appears, and then select **Go to site** to open the newly created SharePoint site.

    ![](media/media/de2s6.0.png)

1. In the **Documents (1)** library, select **Create or upload (2)** and then choose **Folder upload (3)** to upload files to the SharePoint site.

    ![](media/media/dze1s10.png)

1. Navigate to **`C:\LabFiles\labfile\lab 3 files\files (10)`**

9.  Upload the following files in the Document center:

    - Active Candidates folder

    - HR folder

    - Retail folder

    - Shared files folder

        ![](media/media/dze1s11.png)

        ![](media/media/dze1s12.png)

        >**Note:** Select each folder individually from the list, starting with **Archive Candidates**, then **HR**, **Retail**, and **Shared Files**, and choose **Upload (2)** after selecting each folder to upload them one at a time.

Task 2: File Classification and renaming

1.  Open your browser and navigate to ```m365.cloud.microsoft```.

1. In Microsoft Copilot, select the **Cowork** tab from the left navigation pane to access the Copilot Cowork experience.

    ![](media/media/dze1t2s2.png)

3.  In the Cowork chat box, paste the following classification prompt,
    and select, then click the blue ↑ send arrow on the right side of
    the box:

    ```
    Analyze the files in the "Documents" library on the Zava
    SharePoint site. Classify each by type and topic, then propose a
    renaming scheme of the form YYYY-MM-DD\_<Topic>\_<DocType> based on
    each file's content and metadata. Show me the full old-name → new-name
    mapping before renaming anything.
    ```

    ![](media/media/dze1t2s3.png)
    
4. After content analysis, Cowork
produces the full old-name → new-name mapping table and stops --- it
will not rename anything until you approve.

    ![](media/media/dze1t2s4.png)

    >**IMPORTANT:** The message input box has returned to 'Message Cowork' ---
    Cowork has STOPPED. NO changes have been made in OneDrive yet. This is
    the Human-in-the-Loop preview gate.

    >**Note:** The exact output generated by Copilot Cowork may differ depending on the prompt, context, and model behavior. Minor variations in the generated content are expected.

Task 3: Creating a new folder

1.  In the message box, paste the following prompt and select execute
    button:
    
    ```
    Proceed with suggesting renaming and create new folder for all latest renamed files.
    ```

    ![](media/media/dze1t2s5.png)

2. When Copilot prompts to create the **Renamed - Current Files** folder, select **Create** to approve the action and continue the workflow.

    ![](media/media/dze1t2s6.png)

3.  Cowork would ask you to approve the names for all the files. Click
    Approve All.

    ![](media/media/dze1t2s7.png)

    ![](media/media/dze1t2s8.png)

4.  Review the output:

    ![](media/media/dze1t2s9.png)

## Exercise 2 -- OneDrive and SharePoint governance audit

Audit the Lab Files folder for governance issues --- duplicate files,
stale content, external sharing risks, and ownership gaps. Produce a
structured audit report with recommendations, then execute one approved
governance action.

### Task 1: Submit the governance audit prompt

1.  In the Cowork chat box, paste the following prompt:

    ```
    Audit my 'Lab Files' folder for governance issues: duplicate
    files, files not modified in over 6 months, files shared externally or
    with 'anyone' links, and files with no clear owner or topic. Recommend
    an action per finding (archive, delete, restrict sharing) but take no
    action
    ```

    ![](media/media/dze2t1s1.png)

2.  Review the output:

    ![](media/media/dze2t1s2.png)

### Task 2: Review the Audit Report

1.  READ Section 1 --- Duplicate files 🔴 (biggest issue):
    duplicates identified by byte-identical content hash and 2 versioned
    near-duplicate pairs.

    ![](media/media/dze2t1s3.png)

2.  READ Section 2 --- Stale files ⭕: files identified as archive
    candidates based on filename-embedded dates (metadata dates were
    updated by the Exercise 1 renames).

    ![](media/media/dze2t1s4.png)

3.  READ Section 3 --- External shares ✅: all 28 files show owner-only
    permissions (CLEAN --- no action needed).

    ![](media/media/dze2t1s5.png)

4.  READ Section 4 --- No clear owner 🟡: LegacyPolicy and all 13 empty
    .xlsx placeholder files flagged.

    ![](media/media/dze2t1s6.png)

5.  READ the 'Suggested next steps (on your go-ahead)' numbered action
    menu at the bottom.
    
    ![](media/media/image17.png)

    >**Note:** If Copilot does not provide the suggested next steps automatically, use the following prompt and submit it:
    >**Based on the governance audit above, list your suggested next steps as a numbered action menu (one action per recommendation), so I can approve them individually.**
    >Responses may vary, but the output should provide actionable recommendations that can be reviewed and approved individually.

### Task 3: Execute one governance recommendation

1.  In the message box, type: '2' (to approve action #2: archive the
    2024/2025/legacy items) and click Execute button.

    >Note: Cowork executes ONLY action #2. Actions #1, #3, #4, and #5 remain
    pending --- approval of one does not authorize it all.*

    ![](media/media/image18.png)

2.  Cowork puts forth 4 option "How should I resolve the ownerless
    legacy policy?" Select option 1: Move to Archive Candidates.

    ![](media/media/image19.png)

3.  An approval prompt pops-up asking for your approval. Select Approve.

    ![](media/media/image1a.png)

    >**Note:** Cowork's autonomy boundary: 'Safe without approval' =
read-only analysis only. 'Needs human approval' = any action that
changes state.*

## Exercise 3 -- AI-generated Excel tracking and Teams reporting

Generate an Excel governance tracker with one row per file, then post a
3-line summary to Teams with a workbook link --- demonstrating OneDrive
→ Excel → Teams cross-app workflow orchestration from a single
instruction.

### Task 1: Submit the Excel and Teams prompt

1.  In the Cowork chat box, paste the following prompt and select
    Execute button:

    ```
    Create an Excel workbook 'File Governance Tracker.xlsx' in Lab Files with one row per file: name, type, topic, last modified, sharing status, action taken. Then post a 3-line summary of today's cleanup to my Teams channel with a link to the workbook.
    ```

    ![](media/media/dze2t1s7.png)

2.  An approval prompt opens up asking for approval for the drive.
    Select Approve.

    ![](media/media/image1c.png)

1. Review the Teams channel post prepared by Copilot Cowork, confirm the **File Governance Tracker.xlsx** attachment is included, and then select **Send** to post the audit summary to the specified Teams channel.

    ![](media/media/dze2t1s8.png)

3.  Open the File Governance Tracker.xlsx from the Workspace Output
    panel link. Verify: 28 rows (one per file), 6 columns (File Name,
    Type, Topic, Last Modified, Sharing Status, Action Taken).

    ![](media/media/image1d.png)

4.  Confirm yellow-highlighted rows identify duplicate/flagged files ---
    these carry forward from the Exercise 2 duplicate analysis.

    ![](media/media/image1e.png)

5.  Review the teams message:

    ![](media/media/image1f.png)

## Lab summary

In this lab, you used Microsoft 365 Copilot Cowork to execute a complete
enterprise file governance workflow from natural language prompts. You
applied AI-powered file classification with an explicit
preview-before-action safety gate, ran a full governance audit across 28
files using cross-exercise session memory, and orchestrated a cross-app
reporting workflow spanning OneDrive, Excel, and Microsoft Teams.

Key Cowork capabilities demonstrated throughout:

- Multi-Step Workflow Decomposition --- natural language prompt →
  structured multi-step plan in the Workspace panel

- Human-in-the-Loop Preview Gates --- mandatory approval dialogs before
  every bulk file operation

- Progressive Batch Permission (Always allow Call graph) ---
  session-scoped consent for repeated Graph API calls

- Cross-Exercise Context Retention --- Exercise 1 content hashes and
  metadata reused directly in Exercise 2 and 4

- Graceful Failure Isolation --- locked files flagged and retried
  automatically without aborting the batch

- Responsible AI Self-Articulation --- Cowork accurately describes its
  own 'Safe without approval' vs 'Needs human approval' boundary

- Cross-App Workflow Orchestration --- OneDrive file data → Excel
  governance tracker → Teams stakeholder communication

- HR Domain Classification --- PII awareness, HR business function
  taxonomy, duplicate persistence across exercises
