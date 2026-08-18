# Lab 1- Design Intelligent Workflow Agent: Smart email triage & productivity insights with Copilot

### Duration: 30 Minutes

## Scenario

Zava Retail, a rapidly growing omnichannel retailer, faced increasing operational complexity due to high volumes of communication across customers, suppliers, and internal teams. With expansion across e-commerce platform, 50+ physical stores, vendor and supplier ecosystem, customer support and marketing teams, email became the primary but inefficient channel for critical business interactions. Zava Retail teams receive hundreds of emails daily from:

   - Customers (complaints, returns, inquiries)

   - Suppliers (inventory updates, delays)

   - Internal teams (approvals, escalations)

This results in:

   - Missed urgent emails

   - Slow response times

   - Employee burnout due to overload

   - Lack of visibility into priorities

   To address this challenge, Zava Retail is looking to implement an AI-powered Intelligent Workflow Agent using Microsoft 365 Copilot to automate email triage, highlight urgent and actionable items, deliver insights to workload and productivity, and provide real-time productivity insights.

**Key Personas**

1. **Marie Brown -- Customer Support Manager**

The customer support manager at Zava Retail manages the customer support inbox, handles escalations and SLA (Service-level agreement) compliance, and coordinates with logistics and SLA compliance.

2. **David Turner -- Supply Chain Coordinator**

The supply chain coordinator at Zava Retail tracks vendor communications, manages inventory updates and delays, and coordinates with warehouses.

3. **Patricia Gray -- Operations Head**

The operations head at Zava Retail oversees the business operations across departments, tracks productivity and workload, and ensures operational efficiency.

## Lab Prerequisites

**Licensing & Access**

- Microsoft 365 Copilot license

- Microsoft Frontier Program

- Workflows Agent (Frontier or GA) enabled.

- Access to Outlook, Teams

- Viva Insights (Work IQ data enabled)

- Permission to access:

- Microsoft Graph / Insights data

**DLP & Connector Requirements (Admin setup)**

Your organization's DLP policy must allow:

- AI actions (Power Platform connector)

- Dataverse (AI prompt)

- Power Platform

- Microsoft 365 connectors:

- Outlook

- Teams

- SharePoint

- Planner

- Approvals

These are required to ensure that workflows can read emails, post to Teams, and summarize content.

## Exercise 1: Build the Email Triage Agent

Goal: Create the first operational agent that reviews unread emails and prioritizes work.

1. Navigate to **<https://m365.cloud.microsoft/chat/>** to open Microsoft 365 Copilot.

2. Sign in o Microsoft 365 Copilot account using the following **credentials (1)** and select **Next (2)**:

   - **Email/Username:** <inject key="AzureAdUserEmail"></inject>

     ![](media/media/image1d.png)

3. Next, provide your **password (1)** and select **Sign In (2)**:

   - **Password:** <inject key="AzureAdUserPassword"></inject>

     ![](media/media/image1e.png)

4. After successful login, you will see **Copilot Chat** home page.

   ![](media/media/image4.png)

5. In the **left navigation**, select **All Agents** and explore the
    Agent store.

   ![](media/media/image5.png)

6. Scroll down and look for **Workflows (Frontier)** option under
    "Built by Microsoft" header.

   ![](media/media/image6.png)

7. Select **Add** to add the **Workflows Agent (Frontier)**.

   ![](media/media/image7.png)

## Exercise 2: Build Zava Email Triage Agent

### Task 1: Open Workflows Agent

1. Go to Microsoft 365 Copilot home page.

2. Navigate to **Agents > Workflows (Frontier)**.

   ![](media/media/imageb.png)

   >**Note:** You will see a chat interface of Workflows (Frontier).

   ![](media/media/imagec.png)

### Task 2: Describe the Workflow in Natural Language

1. Define Business Logic (Prompt)Paste the below prompt and click **Send**.

    ```
    Each weekday morning, review unread emails from the last 24 hours.
    Focus on:
    - Customer complaints and escalations
    - Supplier/vendor updates
    - Internal approvals or urgent requests

    Categorize each email into:
    - Urgent -- Needs immediate action
    - Action Required -- Needs response
    - FYI -- Informational

    For each email, extract:
    - Sender
    - Subject
    - A one-line Summary
    - Any deadlines
    - Suggested next steps

    Highlight:
    - Customer complaints impacting SLA
    - Supplier delays affecting inventory

    Limit the summary to the 15 most relevant emails if more are found.

    Send the structured summary to myself on Microsoft Teams email id --
    <inject key="AzureAdUserEmail"></inject>. Use simple section headers (Urgent, Action Required,
    FYI, Highlights) followed by a flat bullet list under each - no tables, no nested
    sub-bullets. Keep the entire message under 2000 characters. If the summary is
    longer than that, shorten each email's summary line rather than omitting emails.
    ```

    >**Note:** The email id will be changed to the username you are
currently using to execute this lab.

   ![](media/media/imaged.png)

2. Select **Save** on the top right corner of the **Workflow** window to run the actions automatically. Your workflow is now created and ready to test.

   ![](media/media/image1f.png)

3. Once the workflow is saved, select **Test** to review the output.

   ![](media/media/image20.png)

4. Once the testing is successful, it will show the test duration and result as success confirmation.

   ![](media/media/image21.png)

   Once the test process is completed, review that it:

   - Creates scheduled trigger (weekday mornings)

   - Connects to:

      - Outlook (email ingestion)

      - Dataverse AI (reasoning)

      - Teams (output delivery)

   - Applies AI reasoning for categorization and summarization.

You did not configure connectors manually, Copilot did it for you.

>**Note:** Test process can take 5-10 minutes. Wait until the process
is completed.

### Task 3: Validate Output 

After processing your prompt, you will see the run results:

1. Emails detected.

   >**Note:** You need to send different types of sample emails to the
account to verify that the workflow triggers a notification in Microsoft Teams. If you do not have any new unread emails in your inbox, you will need to do send test emails to validate the workflow and outputs.

3. Email categorization accuracy.

4. Ensure that the Teams message format is matching the Outlook email
details.

   ![](media/media/image11.png)

   ![](media/media/image12.png)

5. If something looks wrong:

    - Update the prompt

    - Re-test

6. Check for the following test results for Zava Retail.

    - Are customer complaints in urgent?

    - Are supplier delays highlighted?

    - Are summaries actionable?

    - Is Teams message structured clearly?

## Exercise 3: Add Human-in-the-Loop

Marie Brown (Customer Support Manager) wants approval before sending
summaries to leadership team.

1. Navigate to **<https://m365.cloud.microsoft/chat/>** to open Microsoft 365 Copilot.

2. Go to **Workflows (Frontier)** agent.

3. Paste the below prompt in the chat and select **Save**.

    ```
    When a summary is generated from Outlook emails categorized as
    Action Required:

    Before sending the summary:

    Send a Microsoft Teams approval request to me including the summary
    content.

    If approved:

    Send the summary via email.

    If rejected:

    Stop the workflow and notify me in Teams.

    Start the workflow when a new email arrives. Once the approval or
    rejection action is taken, stop sending the approval emails to the
    user.
    ```

    ![](media/media/image22.png)

4. Once the workflow is saved, select **Test**.

   ![](media/media/image23.png)

   ![](media/media/image24.png)

5. Review the output of approval prompt.

    - Approval step added

    - Control retained for critical communication

6. The approval step will be added and the email will be received with "Approve" and "Reject" options. Select **Approve** and enter "*Approved"* in the comments. Select **Submit**.

   ![](media/media/image25.png)

7. Once the approval is received, review the confirmation email.

   ![](media/media/image18.png)

## Exercise 4: Autonomous Workflow

Marie Brown (Customer Support Manager) wants to reduce missed
follow-ups.

1. Navigate to **<https://m365.cloud.microsoft/chat/>** to open Microsoft 365 Copilot.

2. Go to **Workflows (Frontier)** agent.

3. Paste the below prompt in the chat and select **Save**.

    ```
    When a new email arrives in Outlook with "Urgent" in the email
    subject:
    Send a Microsoft Teams reminder with Urgent timeline to respond to the
    email.
    If there is no email response until 5 minutes:
    Send an escalation notification on email and Microsoft Teams."

    "When a new email arrives in Outlook with "Urgent" in the email
    subject:
    Send a Microsoft Teams reminder to
    "<inject key="AzureAdUserEmail"></inject>" to respond to the email
    instantly.
    If the email is still not responded in 2 hours:
    *Send an escalation notification to Microsoft Teams.
    ```

    >**Note:** The email id will be changed to the username (Email ID) you are currently using to execute this lab.

     ![](media/media/image26.png)

4. Once the workflow is saved, select **Test**.

   ![](media/media/image27.png)

5. Review the outcome:

    - Automated follow-ups

    - Escalation logic activated

6. Review the automated follow-up message sent on Teams. It ensures that the urgent emails are not missed.

   ![](media/media/image1c.png)

7. Once the mentioned time of 2 hours is passed, review the automated escalation message on Teams.

    >**Note:** Currently, the last step of the workflow cannot be executed. The flow will send the Teams message after the 2-hour mark is reached.

## Lab Summary

In this lab, you learned how the Workflows Agent in Microsoft 365
Copilot enables a shift from static automation to AI-powered, adaptive
workflows. Instead of predefined rules, you built an intelligent agent
that understands context, makes decisions, and improves over time.

You created an Email Triage Agent for Zava Retail that runs every
weekday, reviews recent unread emails, identifies urgent items,
categorizes messages, generates summaries with next steps, and shares
structured outputs in Microsoft Teams. It also uses Work IQ to provide
productivity insights.

As a result, Zava Retail reduced email overload, improved response
times, automated task handling, and minimized missed escalations while
demonstrating how AI-driven agents can enhance operational efficiency
and decision-making.
