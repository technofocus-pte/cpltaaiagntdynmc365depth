---
lab:

title: Solve customer issues faster with Copilot in Dynamics 365 Customer Service
    
description: Set up a trial environment for Microsoft Power Platform and Dynamics 365. Configure environments, Copilot capabilities, and required add-ins to prepare the environment for hands-on learning activities throughout the course.
    
duration: 30 mins
    
level: 200
    
islab: True
    
primarytopics: Dynamics365 Customer Service
---   
# Solve customer issues faster with Copilot in Dynamics 365 Customer Service

## Scenario
You are a **Dynamics 365 Customer Service administrator/representative at Contoso Coffee**, a company that sells and services coffee equipment. Your customer service team wants to reduce case resolution time and improve response quality using **Copilot**. Before rolling out Copilot to representatives, you need to provision the required trial licenses and environments, enable and configure Copilot in the **Customer Service admin center**, and validate its ability to summarize cases, answer questions, draft customer communications, and support other AI-assisted capabilities. This will help Contoso Coffee representatives resolve customer issues faster and provide more consistent support.

## Objective
Configure **Dynamics 365 Customer Service** and explore **Copilot** capabilities that help streamline case management, customer communication, knowledge creation, and data analysis.

## Exercise 1: Assign a Customer Service trial license and enable Copilot

### Task 1: Assign Customer Service trial license

In this task, you will start a **Dynamics 365 Customer Service trial**, provide the required contact information, and confirm that a **Customer Service Trial environment** has been provisioned in the Power Platform admin center.

1.  Open your browser and browse to **+++https://dynamics.microsoft.com/en-in/customer-service/overview/+++** and select **Try for free**.

    ![](./media/image1.png)

2.  Enter your Office 365 admin **tenant credentials**, select the checkbox to accept the agreement and click on **Start your free trial**.

    ![](./media/image2.png)

3.  Provide Contact Information as below and then select **Submit**.

    - **Job Title**: Your job title

    - **Country/region**: United States

    - **Phone number**: Your phone number

    ![](./media/image3.png)

4.  If requested, enter your Office 365 admin tenant password.

    ![Screenshot](./media/image4.png)

5.  You will land on the **Copilot Service Workspace** portal.

    ![](./media/image5.png)

6. Go to the **Power Platform admin** center by navigating to **+++https://admin.powerplatform.microsoft.com/+++** and, if required, **sign in** using your provided Microsoft 365 tenant administrator credentials.

7. From the left navigation pane, select **Manage** > **Environments**. In the list of environments, verify that the **Customer Service Trial** environment is available.

    ![](./media/image6.png)

### Task 2: Enable the Copilot feature

1.  Navigate back to the **Copilot Service** **workspace** portal. Select the **Copilot Service workspace** at the top.

    ![](./media/image7.png)

2.  Under **Apps**, select **Copilot Service Admin Center**.

    ![](./media/image8.png)

3.  Select **Productivity** under **Support experience**.

    ![](./media/image9.png)

4.  In the **Productivity** pane, select **Manage** for **Copilot settings**.

    ![](./media/image10.png)

5.  Enable Copilot help - **Ask a Question**. Enable **Copilot immersive (preview)**.

    ![](./media/image11.png)

6.  Open Customer **Support > Settings**

    ![](./media/image12.png)

    ![](./media/image13.png)

7.  Configure the required **Copilot features** for representatives across the available tabs:

    - Overview

    - Immersive settings

    - Email settings

    - Prompts

    - Extend agent

#### **Configure the Overview Tab**

    In the Instructions box, add:
    +++Respond in a professional and friendly tone.
       Provide clear, concise explanations.
       Use short paragraphs and bullet points when appropriate.
       If the knowledge base doesn't contain a clear answer, advise the representative to escalate the case.+++

8.  Select **Save**.

    ![](./media/image14.png)

#### **Immersive Settings**

Configure the following settings on the **Immersive** **settings** tab:

    Configure Workload Prompt:
    +++Show open cases in priority order.
       Highlight overdue and escalated cases first.
       Identify customers with multiple open cases.
       Summarize key actions required for each case.
       Recommend the next best action where appropriate.+++

![](./media/image15.png)

9.  Configure **Case Overview Card.**

    Configure the settings as:

    - Case Number
    
    - Case Title
    
    - Priority
    
    - Status

    ![](./media/image16.png)

10. Select **Save**.

11. Go to the **Email Settings** tab:

    Enable:

    - Help pane - Write an email
    
    - Email sentiments (Preview) (optional)
    
    - Copilot-recommended templates (optional)

    ![](./media/image17.png)

12. Select **Save**.

13. Go to the **Prompts** tab, leave all currently checked prompts enabled. Click **Save**.

    ![](./media/image18.png)

14. Click **Save and Close**.

    ![](./media/image19.png)

15. Select **Manage** for Summaries.

    ![](./media/image20.png)

16. Select the **Make case summaries available to representatives** check box, select all the check boxes under **Live conversation summaries** and then select **Save and close**.

    ![](./media/image21.png)

## **Exercise 2: Solve customer issues faster with Copilot in Dynamics 365 Customer Service**

In this exercise, you will learn how to use **Copilot** in **Dynamics 365 Customer Service** to accelerate case resolution. You will learn how Copilot generates AI-driven case summaries, responds to         technical and troubleshooting queries using available knowledge sources, and assists in drafting customer-ready emails through predefined and custom prompts.

### Task 1: Summarize cases

In this exercise, open a sample case in the **Customer Service Representative Dashboard** and use **Copilot** to generate a case summary, helping you quickly understand the issue and resolve it efficiently.

1.  To navigate to your **Customer Service workspace**, go to the **Power Platform admin center** using the given link +++ https://admin.powerplatform.microsoft.com +++.

2.  From the left navigation pane, select **Manage** \> **Environments** and then select **Customer Service Trial** environment.

    ![](./media/image22.png)

3.  On the **Customer Service Trial** environment page, click on the **Environment URL**.

    ![](./media/image23.png)
4.  You will be navigated to the **Copilot Service admin center**. Select the **Copilot Service admin center**.

    ![](./media/image24.png)

5.  Select the **Copilot service workspace**.

    ![](./media/image25.png)

6.  Select the **Customer Service Representative Dashboard**.

    ![](./media/image26.png)

**Note**: If you receive any error regarding setting up presence, you can continue or wait till you see a **green checkmark** in the right corner of the screen.

   ![](./media/image27.png)

7.  Select one of the cases listed on the **Customer Service Representative Dashboard**. For example, **A Mineral Build Up in Water Supply**.

    ![](./media/image28.png)

8.  The **Case summary** appears as a card on the case form. When you open a case, the **Summary** card collapses by default.

    ![](./media/image29.png)

9.  Expand the **Summary** tab.

    ![](./media/image30.png)

10. You can see the generated case summary.

    ![](./media/image31.png)

### Task 2: Ask Questions About Case Data

In this exercise, you will use the Copilot pane to ask natural-language questions about a case, review Copilot's answers and sources, and refine responses through follow-up questions.

1.  From the **Customer Service Representative Dashboard** select one of the sample cases, for example, **A Mineral Build Up in Water Supply**.

    ![](./media/image32.png)

2.  In the **Copilot** pane on the right, enter **How to resolve mineral buildup** **in the water supply?**, and then select **Send**.

    ![](./media/image33.png)

**Note**: The Copilot setup process may take some time to complete. To optimize your lab session, save your progress and proceed to the next lab activity. You can return to this lab once the Copilot setup is complete to continue from where you left off.

    ![](./media/image34.png)

3.  Review the response generated by **Copilot** to view the recommended resolution for the issue.

    ![](./media/image35.png)

4.  You can ask more questions like, **What is the customer's main issue?** and click on the **Send** icon **Copilot** will give a response to your question.

    ![](./media/image36.png)

5.  With **Copilot**, you can take the following actions:

    - **Ask a direct question**: Copilot shows the most relevant answer from the knowledge sources your organization has made available.

    - **Ask follow-up turn by turn questions**: If Copilot's response isn't immediately useful, you can ask follow-up questions and guide Copilot in a natural, conversational way.

    - **Ask Copilot to attempt a better response**: Copilot can also rephrase responses based on more guidance.

For example, **type**, **How to fix reduced water flow in Smart Brew 300 caused by mineral buildup?**

  ![](./media/image37.png)

6.  If the Copilot response meets your needs, select and use all or part of the response to address the customer's question:

- Select **Edit**. Copy part of Copilot's reply into your chat or read from it during a voice conversation.

    ![](./media/image38.png)

- Select the **Copy** icon to copy the entire response to the clipboard.

    ![](./media/image39.png)

**Note**: When you're in an active digital messaging conversation, select Send to customer to open an editing window where you can revise the response and send it to the customer. You can also change customer keywords to prompt Copilot to generate a more accurate response.

7.  Select **Check sources** to see the knowledge base or website links from which Copilot drew the response. You can use this supplemental information as a resource or share it with the customer.

    ![](./media/image40.png)

8.  Click on the **link**, and then you can see the content on the left side.

    ![](./media/image41.png)

9.  Select the **thumbs-up** or **thumbs-down** icon to rate the Copilot response.

    ![](./media/image42.png)

10. At the end of the customer conversation, or when you want to start a new context, select **Clear chat** at the top of the Copilot pane.

    ![](./media/image43.png)

### Task 3: Draft and refine emails

In this exercise, you will use Copilot's predefined and custom prompts to draft a customer email, then adjust its length and tone before copying it into your reply.

1.  Select the **Write an email** tab on the **Copilot** pane.

    ![](./media/image44.png)

2.  On the **case overview page**, select the **Related** tab, and then select **Activities**.

    ![](./media/image45.png)

3. Select **+ New Activity \> Email**.

    ![](./media/image46.png)

3.  When you start drafting an email, **Copilot** opens in the right-side pane and displays five predefined prompts and one custom prompt.

    - **Suggest a call**: Drafts a reply that suggests a call with the customer today or tomorrow.

    - **Request more information**: Drafts a reply that requests more details from the customer to help resolve the problem.

    - **Empathize with feedback**: Drafts a reply that provides an empathetic response to a customer who expresses a complaint.

    - **Provide product/service details**: Drafts a reply that offers details or answers customer questions about a particular product or service.

    - **Resolve the customer's problem**: Drafts a reply that provides a resolution---and resolution steps, if applicable---to the customer's problem.

    - **Custom**: Allows you to provide your own prompt for the reply.

    ![](./media/image47.png)

4.  Select any prompt from the predefined prompts list. For example,select **Resolve the customer’s problem** from the suggestions.

    ![](./media/image48.png)

5.  You can see that **Copilot** has generated a suggestion.

    ![](./media/image49.png)

6.  Review the **Copilot-generated email draft** and select **Keep it** to accept it, or **Discard** to remove it.

7.  To refine the draft, enter instructions in **Add details to revise the draft**, or use **Adjust**, **Translate**, or **Check sources** as needed.

    ![](./media/image50.png)

8.  Adjust the **email draft** as needed:

    - **Length:** Select **Short**, **Medium**, or **Long**.
    
    - **Tone:** Select **Friendly**, **Professional**, or **Formal**.

    ![](./media/image51.png)

9.  Review the revised response, make any necessary changes, and select
    **Copy** to add the entire response to your draft. Alternatively,
    select and copy only the required portion.

    ![](./media/image52.png)

10. Verify that the Copilot-generated response is added to the **email
    body** on the left.

    ![](./media/image53.png)

11. In the **Draft with Copilot** pane, select **Suggest a call**.
    Review the generated content and verify that Copilot updates the
    email draft with a follow-up call recommendation.

    ![](./media/image54.png)

12. Review the **Copilot-generated content**, and then select **Keep
    it** to insert the suggested follow-up call text into the email
    response.

    ![](./media/image50.png)

13. Review the email, and then select **Send** to send it or **Save** to
    save it for later. Additionally, use **Draft with Copilot** to
    further refine the email response as needed.

    ![](./media/image55.png)

### Task 4: Generate knowledge drafts

In this exercise, use **Copilot** to generate a structured knowledge article draft from a resolved case. Review and refine the **Title, Issue, Cause, and Resolution** before creating the knowledge proposal.

1.  Open the **Copilot Service admin center** and, from the left
    navigation pane, select **Knowledge**.

    ![](./media/image56.png)

2.  Under **Knowledge creation**, select **Manage**.

    ![](./media/image57.png)

3.  Turn on **Case-based knowledge creation**, and then select **Save
    and close**.

    ![](./media/image58.png)

**Task: Generate knowledge draft**

1.  Select **Resolve Case**

    ![](./media/image59.png)

2.  From the **Resolve type** drop-down list, select the appropriate
    resolution type, enter a **Resolution comment**, select **Propose
    new knowledge article for this case**, and then select **Resolve**.

    ![](./media/image60.png)

3.  On the **Propose new knowledge (preview)** dialog, select a
    **template** and **language**, if required.

    ![](./media/image61.png)

4.  Select **Generate draft**.

    ![](./media/image62.png)

5.  Review the knowledge article draft generated using the selected
    template.

    ![](./media/image63.png)

6.  Review and refine the knowledge draft as needed. Use the editor to
    format the content, **Revise with instructions** to make changes,
    and **Create proposal** to save the draft as a knowledge proposal.

7.  Verify that the **Knowledge proposal created** confirmation appears
    on the right side of the screen.

    ![](./media/image64.png)

8.  You will receive resolution Email.

    ![](./media/image65.png)

### Task 5: How Copilot supports different languages

In this exercise, use **Copilot in Dynamics 365 Customer Service** to
generate and translate responses in multiple languages, helping
representatives support customers globally.

In the **Copilot** pane, select the **Translate** drop-down and choose a
language to translate the generated content. Review the translated
response.

   ![](./media/image66.png)

### Task 6: Use AI form-fill assistance

In this exercise, enable **AI Form Fill Assistance** and configure
form-fill suggestions for a table column. Test both **inline** and
**file-based** form-fill capabilities in the **Customer Service
workspace**.

#### **Enable AI Form Fill Assistance**

1.  Open **Power Platform Admin Center**
    **+++https://admin.powerplatform.microsoft.com+++**

    ![](./media/image67.png)

2.  Select your lab environment.

    ![](./media/image68.png)

3.  Navigate to: **Settings**.

    ![](./media/image69.png)

4.  Navigate to: **Product\> Features**

    ![](./media/image70.png)

5.  Under AI features, enable:

    - **AI Form Fill Assistance**
    
    - **Smart Paste** (optional)
    
    - **File Upload/Form Fill Toolbar** (optional)

    ![](./media/image71.png)

6.  In the left navigation pane, select **Service** \> **Cases**

    ![](./media/image72.png)

7.  Select **+ New Cases**.

    ![](./media/image73.png)

8.  You can view new contact form.

    ![](./media/image74.png)

9.  Create the contact information data and save it as a **CSV** file.
    Then, select the row where you want to add the contact information.

    ![](./media/image75.png)

10. Return to the **Contact** form. Click “**Smart Paste Icon**”

    ![](./media/image76.png)

11. Wait for AI-generated suggestions to appear. Click “**Accept 11
    Suggestion**.”

    ![](./media/image77.png)

12. Verify that the **Contact Information** is automatically populated.

    ![](./media/image78.png)

13. Click **Save & Close**.

    ![](./media/image79.png)

14. Verify that the **Contact Information** has been added successfully.

    ![](./media/image80.png)

### Task 7: Use natural language to find data with AI and Visualize data chart

In this exercise, you will enable the Natural Language Grid and View
Search feature and use the AI search box to query case data using
plain-language search terms.

1. Enable the feature in **Power Platform Admin Center**:

**Environment > Settings > Product > Features > Natural Language Grid and View Search > Enable**

 ![](./media/image81.png)

2.  Return to the **Dynamics 365 Copilot Service workspace**. In the
    left navigation pane, select **Service > Cases**.

    ![](./media/image82.png)

3.  In **My Active Cases**, use the AI-powered natural language search
    to find the required cases. For example, enter **“List cases with
    high priority.”**

    ![](./media/image83.png)

**Visualize data as a chart with Copilot in Customer Service**

1.  In the Cases view, select **Visualize**.

    ![](./media/image84.png)

2.  Wait for Copilot to analyse the visible data. Review the
    AI-generated chart in the side pane.

    ![](./media/image85.png)

3.  Visualize Using Natural Language: Enter in search box: **Visualize
    data as a bar chart**

    ![](./media/image86.png)

4.  Select a **section** of the generated chart. Observe the case grid.

    ![](./media/image87.png)

5.  Select the **three dots (...)** in the chart pane. Select **Save
    as**.

    ![](./media/image88.png)

6.  Enter: **Incidents by Priority**. **Save** the Chart.

    ![](./media/image89.png)

7.  Create new chart with Copilot. Select option **New Chart with
    Copilot**.

    ![](./media/image90.png)

8.  You can view the chart generated by Copilot.

    ![](./media/image91.png)

### Task 8: View a Copilot-generated row summary

In this exercise, you will configure **Row Summary** for the Account table,
apply it to the main form, and view the AI-generated summary for an
account record in the Omnichannel for Customer Service app.

1.  Return to +++https://powerapps.microsoft.com+++ tab. Select **Tables** > **Accounts**

    ![](./media/image92.png)

2.  Select **Account > Row Summary**

    ![](./media/image93.png)

3.  Click **row summary** > **test**.

    ![](./media/image94.png)

4.  Review the generated **Row Summary**, and then select **Apply to main forms**.

    ![](./media/image95.png)

5.  Verify that the **Row summary (applied)** status is displayed.

    ![](./media/image96.png)

6.  In the **App Designer** left navigation pane, select **Apps**, and then open **Omnichannel for Customer Service**.

    ![](./media/image97.png)

7.  Select **Save and Publish**. Then, select **play** icon.

    ![](./media/image98.png)

8.  Click the **hamburger menu (☰)** in the upper-left corner, then navigate to **Customers \> Accounts**.

    ![](./media/image99.png)

9.  On the **My Active Accounts** page, review the list of active account records and the **Copilot** pane displayed on the right.

    ![](./media/image100.png)

10. Select the **Summary** icon next to the desired account to view it's AI-generated summary.

    ![](./media/image101.png)

### Task 9: Use timeline highlights with generative AI

In this exercise, you will open a case timeline and use Copilot **Highlights** feature to generate a bullet summary of key activities and actions.

1.  From the **Customer Service Representative Dashboard**, select the sample case **A Mineral Build Up in Water Supply**.

    ![](./media/image102.png)

2. Select **Highlights** to view a Copilot-generated bullet summary of key case activities, customer interactions, issues, and actions taken.

    ![](./media/image103.png)

## **Summary**

In this lab, you explored how **Copilot in Dynamics 365 Customer Service** helps representatives resolve customer issues faster by summarizing cases, answering questions, drafting and refining emails, creating knowledge articles, translating responses, and providing AI-assisted insights.
