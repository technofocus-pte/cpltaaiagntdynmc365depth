---
lab:

title: Use Service Agent in Dynamics 365 Customer Service

description: Explore Service Agent in Dynamics 365 Customer Service to review cases, generate summaries, find knowledge, draft responses, identify next steps, and update case records using natural language.

duration: 30 mins

level: 200

islab: True

primarytopics: Dynamics 365 Customer Service
---

# **Use Service Agent in Dynamics 365 Customer Service**

## Scenario

You are a **Customer Service Representative at Contoso Electronics**. A customer has reported an issue with the **Coffee Machine Not Brewing - 3rd Floor Pantry**. To investigate and resolve the issue efficiently, you will use **Service Agent** in **Dynamics 365 Customer Service** to review the case, summarize activities and customer interactions, retrieve troubleshooting guidance, update case information, add notes, and create a child case for further follow-up if necessary.
By leveraging **Service Agent**, you can reduce manual effort, improve productivity, and provide faster and more consistent customer service experience.
To resolve the issue efficiently, you'll use **Service Agent** in **Dynamics 365 Customer Service** to:
  - Review existing cases and identify priority issues.
  - Understand case history and customer interactions.
  - Retrieve troubleshooting information from knowledge articles.
  - Update case records and add notes.
  - Create a follow-up child case for additional investigation if required.

## **Overview and objective **

In this lab, you'll use Service Agent in Dynamics 365 Customer Service to manage customer cases more efficiently. You'll learn how to review and prioritize cases, generate summaries, retrieve knowledge articles, draft responses, update case records using natural language, and create follow-up activities and child cases.

By the end of this lab, you will be able to:
  - Access and use Service Agent.
  - Review and prioritize customer cases.
  - Generate case and interaction summaries.
  - Retrieve relevant knowledge articles.
  - Update case records using natural language.
  - Create follow-up activities and child cases.

## **Lab Prerequisites**

Before starting this lab, ensure that:
  - Dynamics 365 Customer Service is deployed.
  - Microsoft 365 Copilot is available.
  - Service Agent is enabled.
  - Sample customer cases are available.

## **Task 1: Assign a Customer Service trial license and enable Copilot**

In this task, start a **Dynamics 365 Customer Service trial**, provide the required information, and verify that the **Customer Service Trial** environment is provisioned in the **Power Platform admin center**.

1.  Open your browser and browse to **+++https://dynamics.microsoft.com/en-in/customer-service/overview/+++** and select **Try for free**.

  ![](./media/image1.png)

2.  Enter your Office 365 admin tenant credentials, select the checkbox to accept the agreement and click on **Start your free trial**.

  ![](./media/image2.png)

3.  Provide Contact Information as below and then select Submit.

    - **Job Title:** Your job title
    
    - **Country/region:** United States
    
    - **Phone number:** Your phone number

  ![](./media/image3.png)

4.  If prompted, enter your **Microsoft 365 admin password**.

  ![Screenshot](./media/image4.png)

5.  You will land on the **Copilot Service Workspace** portal.

  ![](./media/image5.png)

6.  Open the +++ https://admin.powerplatform.microsoft.com/ +++ and sign in with your **Microsoft 365 tenant admin credentials**, if prompted. From the left navigation pane, select **Manage \> Environments**, and verify that the **Customer Service Trial** environment is listed.

  ![](./media/image6.png)

## **Task 2: Enable the Copilot feature**

In this task, you will enable Copilot in the **Customer Service Admin Center**, configure Copilot's productivity, immersive, email, and prompt settings, and turn on case and conversation summaries, so Copilot's capabilities are ready to use.

1.  Navigate back to the **Copilot Service** **workspace** portal. Select the **Copilot Service workspace** at the top.

  ![](./media/image7.png)

2.  Under Apps, select **Copilot Service Admin Center**.

  ![](./media/image8.png)

3.  Select **Productivity** under **Support** **experience**.

  ![](./media/image9.png)

4.  In the **Productivity** pane, select **Manage** for **Copilot
    settings**.

  ![](./media/image10.png)

5.  Enable Copilot help - **Ask a Question**. Enable **Copilot immersive
    (preview)**.

  ![](./media/image11.png)

6.  Open **Customer Support \> Settings**

  ![](./media/image12.png)

  ![](./media/image13.png)

7. Configure the required **Copilot** **features** for representatives across the available tabs:

    - Overview
    
    - Immersive settings
    
    - Email settings
    
    - Prompts
    
    - Extend agent

#### Configure the Overview Tab
In the Instructions box, add:
+++Respond in a professional and friendly tone.
Provide clear, concise explanations.
Use short paragraphs and bullet points when appropriate.
If the knowledge base doesn't contain a clear answer, advise the representative to escalate the case.**+++

8. Select **Save**.
  
  ![](./media/image14.png)

#### Immersive Settings

Configure the following settings on the **Immersive** **settings** tab:

Configure Workload Prompt:
+++Show open cases in priority order.
Highlight overdue and escalated cases first.
Identify customers with multiple open cases.
Summarize key actions required for each case.
Recommend the next best action where appropriate.+++

![](./media/image15.png)

9.  Configure **Case Overview Card**.

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

13. Go to the Prompts tab, leave all currently checked prompts enabled. Click **Save**.

  ![](./media/image18.png)

14. Click **Save and Close**.

  ![](./media/image19.png)

15. Select **Manage** for Summaries.

  ![](./media/image20.png)

16. Select **Make case summaries available to representatives** check box, select all the check boxes under Live conversation summaries and then select **Save and close**.

  ![](./media/image21.png)

## **Task 3: Install the Service app for Microsoft 365 Copilot**

Install the **Service app for Microsoft 365 Copilot** to enable access to service-related capabilities and support the lab activities.

1.  Sign in to the **Microsoft 365 portal** at **+++https://m365.cloud.microsoft/+++** using your administrator credentials.

  ![](./media/image22.png)

2.  Select **Apps and more**. Search for **Service**.

  ![](./media/image23.png)

3.  Select the **Service app** and verify that the **Service** app appears in the left navigation pane.

  ![](./media/image24.png)

## **Task 2: Enable Service Agent in Dynamics 365 Customer Service**

Enable **Service Agent** in **Dynamics 365 Customer Service** and configure it to support AI-assisted case management and resolution.

1.  Go to **+++https://make.powerapps.com+++**.

2.  Select **Apps > Omnichannel for Customer Service**.

  ![](./media/image25.png)

3.  Open the app designer. Select **Create agent** and verify that **Service Agent** is available.

  ![](./media/image26.png)

4.  Confirm that the **Dynamics 365 Customer Service** app appears in the app designer.

  ![](./media/image27.png)

5.  Select **Save and Publish**.

  ![](./media/image28.png)

6. Confirm that the **Copilot** app appears in the app designer.

  ![](./media/image29.png)

7. Select **Play** to launch the application

  ![](./media/image30.png)

8. Verify that **Microsoft 365 Copilot** is available within **Dynamics 365 Customer Service**. Select the **Microsoft 365 Copilot** icon.

  ![](./media/image31.png)

9. Open the navigation menu and verify that the **Service agent** is available under Agents.

  ![](./media/image32.png)

## **Task 3: Open and review customer cases**

Open and review customer cases to understand case details, customer issues, and current case status.
 
1. Open the navigation menu. Navigate to **Service** > **Cases**.

  ![](./media/image33.png)

2.  Select **Active** **Cases**.

  ![](./media/image34.png)

**Identify cases requiring attention**

1. Open the **Service Agent** pane.

2. Enter the following prompt: **Identify open cases that require follow-up**.

  ![](./media/image35.png)

## **Task 4: Generate a case summary**

Generate a concise **case summary** using Service Agent to quickly understand the customer issue, case details, and key information needed for resolution.

**Review of customer case**

1. Open the active case: **Quarterly AMC Servicing - Pantry Coffee Machines**.

2. In Service Agent, enter the following prompt: **Summarize the activity for Quarterly AMC Servicing - Pantry Coffee Machines
    case**.

  ![](./media/image36.png)

## **Task 5: Summarize customer interactions**

Enter: **Summarize recent interactions for this customer**.

  ![](./media/image37.png)

## **Task 6: Retrieve knowledge articles and recommendations**

Retrieve relevant knowledge articles and recommendations using **Service Agent** to help identify effective solutions for customer issues.

**Find troubleshooting information**

Ask Service Agent: **Find details on how to address Coffee Machine Not Brewing case**.

  ![](./media/image38.png)

**Review recommended actions**

Ask for Next Steps: **Review case details and activity history**

![](./media/image39.png)

**Conclusion**: Service Agent retrieves relevant knowledge articles and recommends next steps to help resolve the issue.

## **Task 7: Update a case using Service Agent**

**Update case priority**

Enter the following prompt: **Update the case priority to High**.

  ![](./media/image40.png)

**Add a case note**

1. After the priority is updated, enter: **Add notes to this case: Customer contacted. Troubleshooting steps completed**.

  ![](./media/image41.png)

2. Verify that the note is added to the case timeline.

  ![](./media/image42.png)

**Create a Child Case**

Enter the following prompt: **Create a child case associated with Coffee Machine Not Brewing - 3rd Floor Pantry case. Enter Account name: Skyline Business Park.**

  ![](./media/image43.png)

## **Summary**

In this lab, you used **Service Agent** in **Dynamics 365 Customer Service** to improve customer support operations. You learned how to access **Service Agent**, review customer cases, generate AI-powered summaries, analyze customer interactions, retrieve relevant knowledge articles, and perform case updates using natural language prompts. 
By leveraging **Service Agent**, customer service representatives can reduce manual effort, resolve issues faster, and deliver a more efficient and consistent customer experience.
