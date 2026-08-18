# Lab 4- Build the Project Knowledge Assistant Copilot Agent with Microsoft IQ for trusted customer success

Duration: 30 minutes

# Objective & Scenario

This lab provides hands-on experience in building intelligent Copilot
Agents using Microsoft IQ principles. You will create a
SharePoint-integrated agent with trusted knowledge boundaries, apply the
five-step customer success framework to align it with a Core Unit of
Work, and validate it through PoC testing. The lab also covers advanced
customization using Copilot Studio, including custom instructions, topic
routing, and multi-agent orchestration by connecting with a second
specialized agent.

Store associates and shift managers often lose valuable time searching
through SOPs, policy documents, and operational guidelines during busy
trading hours, slowing response times, and impacting customer service.
The Store OperationsAssistant Copilot Agent empowers frontline retail
workers with instant, contextual access to accurate store procedures in
the flow of work---helping them resolve customer queries faster, ensure
policy compliance, and keep store operations running smoothly during
peak demand.

# Exercise 1: Creating and Configuring Your Copilot Agent 

Microsoft IQ represents a unified intelligence layer that brings
contextual, work-aware AI into your everyday apps and agents. In this
part, you will create a Copilot Agent in SharePoint that is grounded in
verified, organization-specific content --- ensuring responses are both
intelligent and trustworthy.

## Task 1: Access the Agent Creation Tool 

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

1. In the **Documents (1)** library, select **Create or upload (2)** and then choose **Files upload (3)** to upload files to the SharePoint site.

    ![](media/media/dye1t1s10.png)
    
1. Navigate to **`C:\LabFiles\labfile\lab 4 files`**, select all two files in the folder, and then choose **Open** to upload them to the SharePoint document library.

    ![](media/media/dxe1t1s11.png)

10. Download the following links and **upload** them in your SharePoint
    site:

    - Zava Project Portfolio.xlsx

    - Zava Customer Playbook.docx

        ![](media/media/dxe1t1s12.png)

>**Note:** *Before testing your Copilot Agent, ensure that all required
source documents (such as project updates, SOP files, product
specifications, shift handover notes, or any other referenced materials)
are uploaded to the appropriate SharePoint site libraries and folders.
The agent can only generate accurate, grounded responses from content
that exists in the site and is accessible through its configured
knowledge sources.*

## Task 2: Create a New Agent 

With your SharePoint site open and your frontline scenario selected, you
will now build the agent.

1.  Log in to Copilot Studio <https://copilotstudio.microsoft.com/>

    >**Note:**
    >1. On the Copilot Studio home page, turn off the **New experience** toggle to switch back to the classic Copilot Studio experience.
    >![](media/media/dxe1t1ns12.png)
    >1. In the **Submit feedback to Microsoft** dialog, select **Other (please specify) (1)** as the reason for switching back and then select **Submit (2)** to continue.
    >![](media/media/dxe1t1ns13.png)

1. From the left navigation pane, select **Agents (1)**, and then choose **Create blank agent (2)** to start creating a new agent.

    ![](media/media/dxe1t2s2.png)

1. Enter **Project Knowledge Assistant** as the agent name and verify that it appears in the agent title field before continuing with the configuration.

    ![](media/media/dxe1t2s3.png)



4. Edit the Instructions as:

    ```
    You are the project knowledge assistant for Zava Site. 
    Rules:

    - Answer questions using only approved knowledge sources 

    - Always provide source citations 

    - Clearly identify project risks 

    - Structure responses using headings and bullet points 

    - If information is unavailable, clearly state that 

    - Never generate information not found in connected knowledge sources
    ```
    ![](media/media/dxe1t2s4.png)

5. Click **+Add knowledge** to link SharePoint document with the agent.

    ![](media/media/image4c.png)

1. Paste the previously saved **SharePoint site URL (1)** into the URL field, and then select **Add (2)** to validate and connect the SharePoint site.

    ![](media/media/dxe1t2s5.png)

1. After the SharePoint site appears in the knowledge source list, select **Add to agent** to add the SharePoint site as a knowledge source for the agent.
Show more lines

    ![](media/media/dxe1t2s6.png)

## Task 3: Test Your Agent 

Testing your agent validates both grounding knowledge and the quality of
its responses. This step reflects the Trust dimension of Microsoft IQ
--- agents should only surface verified, relevant information.

1.  Open the Test pane from the right-hand side pane.

    ![](media/media/dxe1t3s1.png)

2. In the chat field, paste the following prompt and select **Execute
    button:**

    **What is the current status of Apex Financial Project**

    ![](media/media/dxe1t3s2.png)

3.  Review the output:

    ![](media/media/image4e.png)

# Exercise 2: Advanced Instruction Authoring in Copilot Studio

## Task 2: Add a Topic: Out-of-Scope Redirect

Topics in Copilot Studio are rule-based conversation flows that trigger
when specific phrases or conditions are detected. You will create a
short topic that politely redirects users who ask questions outside the
agent's domain.

1.  In Copilot Studio, navigate to **Topics** in the upper menu bar.

    ![](media/media/image14.png)

2.  Select + **Add a topic (1) \> From blank (2).**

    ![](media/media/dxe1t3s3.png)

3.  Paste the name of the topic-
    "*Out-of-Scope Redirect*."

    ![](media/media/image2e.png)

4.  In the Trigger section, paste the following phrases as trigger
    phrases (one per line):

    - *I need help with something else*

    - *Can you help me with HR?*

    - *This is not related to my work*

    - *I have a different question*

        ![](media/media/image2f.png)

5. Click **+ icon** below the trigger node to add a Message node.

    ![](media/media/image30.png)
    
1. Select **Send a Message** to add a message node.

    ![](media/media/image31.png)

6.  Paste the following text in the message description box:

    ```
    "I\'m specialized for HR & Payroll Assistant questions. For other topics, please contact your team lead or visit the company intranet. Is there anything else I can help you with in my area?"
    ```

    ![](media/media/image32.png)

7.  Click **Save(1)** topic, then **Publish (2)** the agent again.

    ![](media/media/dxe1t3s4.png)

    ![](media/media/dxe1t3s5.png)

## Task 3: Test the agent

1. Select **Test (1)** in the upper-right corner to open the **Test your agent** pane, and then select the **New chat (2)** icon to start a fresh test conversation with the agent.

    ![](media/media/dxe1t3s6.png)

2.  Paste the following prompt, and select **the Execute** button

    **Can you help me with
    HR?**
    
    ![](media/media/dxe1t3s7.png)

3.  Review the output:

    ![](media/media/dxe1t3s8.png)

# Exercise 3: Designing a Multi-Agent Orchestration Pattern

Real enterprise deployments rarely rely on a single agent. Complex
workflows --- such as a procurement request that touches both inventory
data and HR approval processes --- require multiple specialized agents
working in coordination. This exercise introduces the concept of
multi-agent orchestration and has you design (and partially configure) a
handoff pattern between your primary agent and a second specialized
agent.

## Task 1: Create the Handoff Topic

You will now create a new topic in your primary agent that triggers
whenever a user asks a question outside the primary scope. This topic
will surface a handoff message and --- when the license supports it ---
redirect the user to the second agent.

1. In Copilot Studio, navigate to **Topics**. Select **+Add a New topic
    \> From blank**.

    ![](media/media/dxe3t1s1.png)

2. Paste the following information in the topic:

    **Name** - Handoff to Secondary Agent

    **Trigger phrases**:
    *"payroll", "leave request", "HR policy", "annual leave",
    "employee record"*

    ![](media/media/dxe3t1s2.png)

3. Click **+** to add a new node.

    ![](media/media/image37.png)

4. Select **Send a Message** to add a message node.

    ![](media/media/image18.png)

5.  In the Message description box, paste the following information:
    
    ```
    "That question is outside my area. I'm connecting you to the HR &
    Payroll Agent who can help with that --- one moment please."
    ```

    ![](media/media/image19.png)

6.  Click **Save (1)** and **Publish (2)** to save the node and publish the setting
    again.

    ![](media/media/dxe3t1s3.png)

    ![](media/media/dxe1t3s5.png)

## Task 2: Configure the Secondary Agent

If your lab environment supports multi-agent connections, follow these
steps to create a lightweight secondary agent that handles the
out-of-scope queries.

1. In Copilot Studio, From the left navigation pane, select **Agents (1)**, and then choose **Create blank agent (2)** to create a new agent using the classic Copilot Studio experience.

    ![](media/media/dxe3t1s4.png)

2. In the **Name your agent** dialog, enter **HR & Payroll Assistant (1)** as the agent name, and then select **Create (2)** to create the new agent.

    ![](media/media/dxe3t1s5.png)

3. In the Instructions field, paste the following instructions:

    ```
    You are the HR & Payroll Assistant. You handle queries specifically related to store operations. Use only verified content from your connected sources. Always cite source and section. If a query falls outside your scope, say: "That's outside my remit. Please contact the appropriate team.
    ```

    ![](media/media/dxe3t1s6.png)

4.  In the Knowledge section, add the relevant [HR
    document](https://lodsprodmca.sharepoint.com/:f:/s/ZavaSite83/IgDF9aJMDXKzQYNYGImaIZrhAU1-t5HrDkAplqqKRSRnX8k?e=nUlcXI).
    You can download the file, save it to your **SharePoint** site, and
    paste the **URL** here.

    ![](media/media/image1e.png)

    > **Note:** To obtain the SharePoint site URL, repeat **Exercise 1 > Task 1 > Steps 4 through 11**, using **HR document** as the site name. After the site is created, copy and save the site URL for later use. Then, navigate to **`C:\Users\LabFiles\labfiles\lab 3 files\files (10)`** and upload the folder contents to the newly created SharePoint site.

5. Select **Publish** to publish the secondary agent.
    
    ![](media/media/image3a.png)

    ![](media/media/dxe1t3s5.png)

## Task 3: Add the Secondary Agent to the Primary Agent. 

1. Go to the **Project Knowledge Assistant** Agent.

    ![](media/media/image3b.png)

2. In the **Agents** section, Select **+Add.**

    ![](media/media/image1f.png)

3. Select the **HR & Payroll Assistant** from the list.

    ![](media/media/image20.png)

4. Paste the following description (1) in the description box and click on **Add and configure (2)**

    ```
    "Use this agent when users ask about HR or payroll matters, including
    payslips, leave balances, salary deductions, attendance, tax forms,
    employee benefits, or HR policy questions. Routes employee-related
    workforce support queries to the HR & Payroll Assistant for accurate
    resolution."
    ```

    ![](media/media/dxe1t3s9.png)

1. In the **Completion** section, verify that **Send specific response (specify below) (1)** is selected, enter the transfer message in the **Message to display (2)** box, and then select **Save (3)** to apply the changes.
Show more lines

    ```
    "Your request relates to HR and payroll support. Transferring you now
    to the HR & Payroll Assistant for accurate assistance."
    ```

    ![](media/media/dxe1t3s10.png)

6. Select **Publish** to publish the agent.

    ![](media/media/image3c.png)

    ![](media/media/dxe1t3s5.png)

## Task 4: Test the End-to-End Orchestration

With both agents published, validate the complete handoff flow using the
test scenarios below.

1.  Navigate to **Project Knowledge Assistant** agent.

    ![](media/media/image11.png)

2.  Select **Test** in the upper menu bar.

    ![](media/media/image3d.png)

3.  Paste the following prompt in the chat interface:

    ```
    "What is my leave balance?"
    ```

    ![](media/media/dxe1t3s11.png)

4.  Review the output:
    
    ![](media/media/image40.png)

# Lab Summary 

In this lab, you created and configured a SharePoint-grounded Project
Knowledge Assistant in Microsoft Copilot Studio, using verified
SharePoint content to ensure accurate and trusted responses. You scoped
and prioritized agent use cases, defined a Core Unit of Work, and mapped
capabilities using the Work IQ framework. You also conducted a
structured proof of concept, evaluated results for scaling
opportunities, authored advanced conditional instructions, created
out-of-scope redirects, and designed a multi-agent orchestration flow
with structured handoffs between primary and specialized agents.
