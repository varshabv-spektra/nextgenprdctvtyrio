# Lab 2 - Copilot Cowork: AI Powered Digital Coworker in Action

Lab Duration: 30 minutes

## Lab Scenario: ZAVA Retail (AI-First Digital Transformation)

ZAVA Retail is a fast-growing omnichannel retail company operating
across India and Southeast Asia with 120+ stores and a rapidly scaling
e-commerce platform.

As ZAVA prepares for its Quarterly Business Review (QBR), leadership
needs:

- Regional revenue and performance analysis

- Demand and risk insights

- Executive-ready presentation (5 slides)

- Leadership summary email

- Cross-team coordination across Outlook and Teams

- Current Problem

- Today, the QBR process is:

- Fragmented across Excel, Word, PowerPoint, Outlook, and Teams

- Time-consuming and manual

- Dependent on multiple analysts and coordinators

- Slow to produce executive-ready outputs

## Lab Objectives

ZAVA Retail is piloting Microsoft 365 Copilot Cowork to transform this
into an AI-driven execution workflow powered by:

- Microsoft IQ → Unified intelligence layer across enterprise + web +
  tools

- Work IQ → Internal enterprise grounding (data, emails, meetings,
  files)

- Web IQ → External market intelligence and real-time insights

- Copilot Cowork → Autonomous AI execution across apps

- Scout Agents → Proactive task suggestions and prioritization

- Multi-model reasoning → OpenAI + Anthropic orchestration

- Teams + Researcher → Human-agent collaboration and critique loop

By the end of this lab, participants will experience how Copilot acts as
a digital coworker that can:

- Analyze enterprise retail data

- Generate executive insights

- Create multi-format business deliverables

- Coordinate communication workflows

## Exercise 1: The Intelligence Layer Kickstart 

1.  Navigate to <https://m365.cloud.microsoft/chat/> to
    open Microsoft 365 Copilot.

2. Sign in with 
    - **Email/Username:** <inject key="AzureAdUserEmail"></inject>

       ![](media/media/de1s1.png)

	- **Password:** <inject key="AzureAdUserPassword"></inject>

        ![](media/media/de1s2.png)

2. When prompted with the **Stay signed in?** dialog, select **No** to continue.

    ![](media/media/de1s3.png)

4.  After successful login, you will see **Copilot Chat** home page.

    ![](media/media/de1s4.png)

5.  In Copilot Chat, paste the following prompt:

    ```
    Explain Work IQ in the context of ZAVA Retail QBR preparation.
    What is Microsoft IQ and how does it unify intelligence layers?
    ```

    ![](media/media/de1s5.png)

6.  Verify the response:

    Work IQ → internal business data (sales, emails, meetings)

    Microsoft IQ → unified intelligence system across all layers

    ![](media/media/de1s6.png)

    ![](media/media/de1s7.png)

## Exercise 2: End-to-End QBR Story Builder

### Task 1: Create a SharePoint Site

In this exercise, you will create a Sharepoint site and upload the
sample documents there which will be used later in this lab.

1.  From a new browser, navigate to
    <https://m365.cloud.microsoft/chat/>  and login with your lab
    credentials.

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

    >**Note:** If you receive the message **"The site address is available with modification"**, update the **Site address** by adding the suffix **`2`** to the end of the site name (for example, `ZavaSite2`), and then continue with the site creation process.

1. Wait until the **Your site is ready!** message appears, and then select **Go to site** to open the newly created SharePoint site.

    ![](media/media/de2s6.0.png)

1. In the **Documents (1)** library, select **Create or upload (2)** and then choose **Files upload (3)** to upload files to the SharePoint site.

    ![](media/media/de2s7.png)

1. Navigate to **`C:\LabFiles\labfile\lab 2 files`**, select all four files in the folder, and then choose **Open** to upload them to the SharePoint document library.

    ![](media/media/de2s8.png)

8.  Upload the following files in the Document center:

    - Zava QBR Sales Q2.xlsx

    - Zava QBR Template.docx

    - Zava QBR Presentation Template.pptx

    - Leadership Distribution List

        ![](media/media/de2s9.png)

### Task 2: Analyzing Excel sheet with Copilot

1.  Open **Zava QBR Sales Q2.xlsx** from SharePoint.

    ![](media/media/de2s10.png)

2.  Open Copilot from lower right pane.

    ![](media/media/imagee.png)

3.  The Copilot pane opens up. Paste the following prompt:

    ``Analyze regional revenue trends and highlight underperforming
    stores.``

    ![](media/media/de2s11.png)

4.  Review the output:

    ![](media/media/de2s12.png)

    >**Note:** If this prompt appears, select Below target — Q2 revenue is below the store target, then click Submit to continue. The available options may vary, but choose the highlighted option shown in the screenshot and proceed with the analysis.
    >![](media/media/de2ns12.png)

### Task 3: Analyzing Word with Copilot

1.  Open **Zava QBR Template.docx** from SharePoint.

    ![](media/media/image11.png)

2.  Open Copilot from the lower right pane.

    ![](media/media/image12.png)

3.  Paste the following prompt in the Copilot chat box:

    ```Convert analysis into an executive summary for leadership```

    ![](media/media/de2s13.png)

4.  Review the output:\
    ![](media/media/image14.png)

    > **Note:** If the executive summary is not automatically added to the Word document, select **Yes, add the summary to the document (1)** from the Copilot suggestions. If the suggestion is not visible, enter **"Yes, add the summary to the document" (2)** in the prompt box and select **Send (3)** to insert the generated summary into the document.
    ![](media/media/de2s14.png)

### Task 4: Analyzing Presentation with Copilot

1.  Open **Zava QBR Presentation Template.pptx** from SharePoint.

    ![](media/media/image15.png)

2.  Open Copilot from lower right corner. The Copilot chat pane opens
    up.
    
    ![](media/media/de2s15.png)

3.  Paste the following prompt:

    ```Create a 5-slide QBR presentation based on the summary.```

    ![](media/media/de2s16.png)

4. Expected Outcome

    - Seamless flow across apps

    - Context retained via Work IQ

    - End-to-end executive deliverable generation

        ![](media/media/de2s17.png)

        ![](media/media/de2s18.png)

## Exercise 3: The Invisible Context Advantage 

1.  Navigate back to <https://m365.cloud.microsoft/chat/>

1. Select the **App launcher (1)** in the upper-left corner of the page, and then choose **Outlook (2)** to open Outlook in a new tab.

    ![](media/media/de2s19.png)

2.  Open Copilot from the upper right pane.

    ![](media/media/image19.png)

3.  In Outlook Copilot Chat paste the following prompt:

    ```
    Summarize my priority emails related to QBR." 

    "What meetings should I prepare for this week?
    ```
    ![](media/media/de2s20.png)

4.  Expected Outcome

    Copilot automatically uses emails, calendar, and priorities

    No manual selection of context required

    ![](media/media/image1b.png)

## Exercise 4: The Cowork Advantage

## Task 1: Launch a Cowork Session

1. Navigate to <https://m365.cloud.microsoft/chat/> and select Cowork from the left pane.

2. Start a new **Cowork** session and paste the following prompt:

    ```
    Using the Zava QBR Sales Q2.xlsx, Zava QBR Template.docx, and the executive summary and presentation we've already created in the Zava Site, do the following: 1) Verify the presentation's numbers match the latest Excel analysis, 2) Draft a leadership summary email highlighting top 3 risks and top 3 opportunities, 3) Suggest a QBR readiness checklist for this week's Teams meeting.
    ```

    ![](media/media/de2s21.png)

3. Expected Outcome:

    ![](media/media/de2s22.png)

    >**Note:** The exact output generated by Copilot Coworka may differ depending on the prompt, context, and model behavior. Minor variations in the generated content are expected.

## Lab Summary

In this lab, you experienced Microsoft 365 Copilot Cowork as a digital
coworker for ZAVA Retail's Quarterly Business Review preparation. You
began by exploring the intelligence layer, using Copilot Chat to
understand how Work IQ and Microsoft IQ unify internal enterprise data
with broader organizational intelligence.

You then built an end-to-end QBR story by creating a SharePoint site and
uploading the sales workbook, QBR template, and presentation template.
Using Copilot directly inside Excel, Word, and PowerPoint, you analyzed
regional revenue trends, converted the analysis into an executive
summary, and generated a 5-slide QBR presentation — demonstrating
context retained across apps without manual re-entry of data.

Next, you saw the invisible context advantage in Outlook, where Copilot
automatically summarized priority emails and surfaced upcoming meetings
using existing calendar and mailbox context, with no manual selection of
source data required.

Finally, you launched a Cowork session that autonomously verified the
presentation numbers against the latest Excel analysis, drafted a
leadership summary email highlighting key risks and opportunities, and
suggested a QBR readiness checklist for the team's Teams meeting.

This lab demonstrates how Microsoft 365 Copilot Cowork, powered by
Work IQ, Web IQ, and multi-model reasoning, can transform a fragmented,
manual QBR process into a coordinated, AI-driven workflow that produces
executive-ready deliverables across Excel, Word, PowerPoint, Outlook,
and Teams.

