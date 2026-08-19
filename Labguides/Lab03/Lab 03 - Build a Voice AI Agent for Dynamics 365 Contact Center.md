---
lab:

title: Build a Voice AI Agent for Dynamics 365 Contact Center

description: Build and configure a voice-enabled AI agent using Microsoft Copilot Studio and Dynamics 365 Contact Center, including knowledge, escalation, voice workstream integration, and live call testing.

duration: 45 mins

level: 300

islab: True

primarytopics: Dynamics 365 Contact Center
---

# Build a Voice AI Agent for Dynamics 365 Contact Center

## Scenario

Contoso receives a high volume of customer support calls related to warranty coverage, return policies, and product troubleshooting. These routine inquiries consume significant agent time, resulting in longer wait times for customers and reduced availability for complex support cases.

To improve customer service efficiency, Contoso plans to implement a voice-enabled AI agent using Microsoft Copilot Studio and Dynamics 365 Contact Center. The AI agent will answer common customer questions using approved knowledge sources, provide self-service support, and seamlessly transfer callers to a live agent when additional assistance is required.

## Overview and Objectives

In this lab, you'll create and configure a voice-enabled AI agent using Microsoft Copilot Studio and Dynamics 365 Contact Center. You'll activate the required environments, verify the voice configuration, build a voice agent, add knowledge sources, configure conversational behaviors and escalation paths, connect the agent to a voice workstream, and validate the solution through a live phone call.
By the end of this lab, you will be able to:

 - Create and configure a voice-enabled AI agent in Copilot Studio.
    
 - Add and manage knowledge sources for customer self-service.
    
 - Configure conversational topics and live-agent escalation.
    
 - Connect the AI agent to a Dynamics 365 Contact Center voice workstream.

 - Test and validate the voice agent using a live phone call.
    
 - Enable automated handling of common customer support inquiries.
## Lab Prerequisites

 Before starting this lab, ensure you have:

- A work, school, or administrator tenant account with the provided credentials.
  
- Dynamics 365 Contact Center Free Trial.
  
- Microsoft Copilot Studio Free Trial.
  
- Access to the Copilot Service Admin Center.
  
- A configured Dynamics 365 Contact Center voice channel.
  
- Warranty & Return Policy document.
  
- Troubleshooting Guide document.
  
- Internet access and a phone capable of making calls for testing purposes.

## Exercise 1: Activate Dynamics 365 Contact Center Trial

In this exercise, you activate the Dynamics 365 Contact Center trial to access the Copilot Service workspace and required administration tools.

1.  Open a **Microsoft Edge** in private window and navigate to the **+++https://www.microsoft.com/en-us/dynamics-365/products/contact-center+++** page.

2.  On the **Contact Center** page, select **Try for free**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image1.png)

3.  On the **Let's get started** page, enter the administrator tenant ID.

     @lab.CloudCredential(M365BusPrem).AdministrativeUsername

4.  Select the **agreement** check box and select **Start your free trial**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image2.png)

5.  If prompted, enter the password and select **Sign in**.

     @lab.CloudCredential(M365BusPrem).AdministrativePassword

    ![A screenshot of a login box AI-generated content may be incorrect.](./media/image3.png)

6.  Enter the required details, such as **Job title**, **Country/Region** and **Phone number**.

7.  Select the **agreement** check box and select **Get started**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image4.png)

8.  After the trial is activated, confirm that you are redirected to the **Copilot Service Workspace**.

9.  From the top app launcher, select **Copilot Service Admin Center**, and then select **Open to set up the contact center**.

    ![](./media/image5.png)

10. Verify that the **Your contact center is ready!** message appears and confirms that the **Chat setup**, **Voice setup**, and **AI experiences** are configured.

11. Select **Open contact center** to open the **Copilot Service Admin Center** and **manage** the contact center settings.

    ![](./media/image6.png)

## Exercise 2: Verify Contact Center Setup

1. Select **Chat**. Under **Test the chat service** > **Prepare the representative** app, select **Open representative app**.

    ![](./media/image7.png)

2. Select **Open representative app**. The **Copilot Service workspace** opens.
  > **Note: A green check mark on the right side of the page indicates that the representative is Available.**

  ![](./media/image8.png)

3. Select the **Voice tab**, and then select **Manage voice** setup to view the voice channel configuration.

    ![](./media/image9.png)

4. Verify that the **Contact Center voice workstream** opens and displays the default **voice channel** and **phone number** that will be used later to test the agent.

    ![](./media/image10.png)

## Exercise 3: Activate Microsoft Copilot Studio Trial

In this exercise, you activate the Microsoft Copilot Studio trial to create and manage AI-powered agents.

1.  Open a new browser tab and navigate to the **Microsoft Copilot Studio trial** page.

2. Select **Try for free**.

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image11.jpeg)

3. In the **Email** field, enter the administrator username and select **Next**.

     @lab.CloudCredential(M365BusPrem).AdministrativeUsername

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image12.png)

4. Select **Sign in**.

5. If prompted, enter the password and select **Sign in**.

    @lab.CloudCredential(M365BusPrem).AdministrativePassword

6. If a message appears stating that a license already exists, select **Get started**.

    ![A screenshot of a computer error AI-generated content may be incorrect.](./media/image13.png)

7. Enter **Country/Region** and **Business** **phone number**, using
    fictitious details if required.

8. Select the **agreement** check box and click **Get started**.

   ![A screenshot of a computer AI-generated content may be incorrect.](./media/image14.png)

If you cannot launch **Copilot Studio** or switch to the correct environment, use the following recovery steps:

1. Open the **+++https://admin.powerplatform.microsoft.com/+++** in a new browser tab.

2. Sign in using the provided administrator tenant credentials.

    Administrator username:
    @lab.CloudCredential(M365BusPrem).AdministrativeUsername
    Administrator password:
    @lab.CloudCredential(M365BusPrem).AdministrativePassword

    ![](./media/image15.png)

3. Open the **ContactCenterTrial** environment.

    ![](./media/image16.png)

4. Copy the **Environment ID**.

    ![](./media/image17.png)

5. Return to the **Copilot Studio** page.

6. In the **URL**, remove everything after environment.

    ![](./media/image18.png)

7. Paste the copied **Environment ID** after **environment**.

    ![](./media/image19.png)

8. **Reload** the page.

    ![](./media/image20.png)

## Exercise 4: Create and Configure Contoso Voice Agent

In this exercise, you create a voice-based Copilot agent and configure its basic settings, including authentication.

### Task 1: Create Voice Agent

1. From the environment selector at the bottom of the page, select **ContactCenter Trial**.

    ![](./media/image21.png)

    If the environment selector is not visible, use the following recovery steps:

1. Open the Power Platform admin center in a new browser tab and sign in with the provided administrator credentials.

    @lab.CloudCredential(M365BusPrem).AdministrativeUsername

    @lab.CloudCredential(M365BusPrem).AdministrativePassword

    ![](./media/image22.jpeg)

2. In the left navigation, under **Manage**, select **Environments**. Select **ContactCenterTrial** to open its details.

    ![](./media/image16.png)

3.  On the **environment details** page, locate and copy the **Environment ID**.

    ![](./media/image17.png)

4.  **Return** to the **Copilot Studio** tab. In the address bar, replace the **default environment ID** with the **ContactCenter Trial** Environment ID you copied. If home is present, retain the path after the environment ID.

    ![](./media/image23.png)

5.  Select **Contact Center Trial Copilot**.

    ![](./media/image24.png)

6.  Select **Skip**.

    ![](./media/image25.png)

7.  Select **Agents**, scroll down, and select **Voice**.

    ![](./media/image26.png)

8.  Verify that the **Voice agent creation** page appears and prompts you for the agent’s name and language.

    ![](./media/image27.png)

9.  In the Name field, enter **Contoso Voice Agent**, and then select **Create**.

    ![](./media/image28.png)

### Task 2: Configure Authentication

1.  After the agent is created, select **Settings** in the upper-right corner.

    ![](./media/image29.png)

2.  Go to **Security** and select **Authentication**.

    ![](./media/image30.png)

3.  Select **No authentication** and select **Save**.

    ![](./media/image31.png)

4. Select **Save** again to confirm.

    ![](./media/image32.png)

5. Close the **Settings pane** by selecting the **Close (X)** icon.

    ![](./media/image33.png)

## Exercise 5: Add Knowledge Sources to the Agent

In this exercise, you add policy documents as knowledge sources so the agent can generate accurate responses.

1.  From the top navigation, select Knowledge, and then select **+ Add knowledge**.

    ![](./media/image34.png)

2.  Select **Select to browse**.

    ![](./media/image35.png)

3.  On the virtual machine, navigate to **C:\LabFiles**, select the following files, and select Open:

    - Warranty & Return Policy
    
    - Troubleshooting Guide

    ![](./media/image36.png)

4.  Select **Add to agent** to add the files as knowledge sources.

    ![](./media/image37.png)

## Exercise 6: Configure System and Custom Topics

In this exercise, you customize system and main menu topics to control the agent's greeting and navigation flow.

### Task 1: Update Conversation Start Topic

1. From the top navigation, select Topics. Under System topics, select Conversation Start.

    ![](./media/image38.png)

2. In the **message** **node**, replace the message with:
    +++**Hello and thanks for calling Contoso Voice Agent**+++

3. Select **Save**.

    ![](./media/image39.png)

### Task 2: Update Main Menu Topic

1. Under **Custom** topics, open the **Main menu** topic.

    ![](./media/image40.png)

2. Replace the message with:
    +++**To know about our warranty and return policy, say "Warranty & Return Policy". For the troubleshooting guide, say "Troubleshooting Guide". To connect with a live agent, say "Talk to an agent."**+++

3.  Select **Save**.

    ![](./media/image41.png)

### Task 3: Delete Dummy Topics

1. Under Custom topics, **turn off** the following topics:

    - **Lesson 1**
    
    - **Lesson 2**
    
    - **Lesson 3**

    ![](./media/image42.png)

## Exercise 7: Create Warranty and Return Policy Topic

In this exercise, you create a custom topic that enables the agent to answer refund-related questions using generative AI.

1. In **Topics**, select **+ Add a topic**, and then select **From blank**.

    ![](./media/image43.png)

2. Rename the topic +++**Warranty and Return Policy**+++.

    ![](./media/image44.png)

3. On the trigger node, select **Edit**. Add +++**Warranty and Return Policy**+++ to the phrase field, and then select the **+** icon.

    ![](./media/image45.png)

4. Add the following trigger phrases:

        - **+++Information About Warranty and Return Policy+++**
    
        - **+++Return Policy details+++**

    ![](./media/image46.png)

5. Below the trigger node, select **+** and add an **Ask a question** node.

6. In the message field, enter:
    +++**Please explain your query related to troubleshooting**+++

    ![](./media/image47.png)

7.  Select the response variable **Var1** and rename it to
    +++**WarrantyandReturnQuery**+++

    ![](./media/image48.png)

8.  Below the question node, select **+,** select **Advanced**, and add a **Generative answer node**.

    ![](./media/image49.png)

9.  Select **WarrantyandReturnQuery** as the input variable.

    ![](./media/image50.png)

10. For **Data source**, select **Edit** and enable **Search only selected** **sources**.

11. Select **Warranty & Return Policy** as the data source.

    ![](./media/image51.png)

12. Verify that **Warranty & Return Policy.docx** is selected as the data source and that **Search only selected sources** are enabled.

    ![](./media/image52.png)

13. Scroll down and select **Advanced**. Under **Save the bot response**, select the **variable** **field** and choose **Create a new variable**.

    ![](./media/image53.png)

14. Select the new **Var1** variable and rename it to
    +++**WarrantyandReturnQueryAnswer**+++

    ![](./media/image54.png)

15. Under the **Generative answer node**, select **+** and add a **Send a message node**.

    ![](./media/image55.png)

16. Select the **{x}** icon and insert +++**WarrantyandReturnQueryAnswer**+++ in the message field.

    ![](./media/image56.png)

17. Verify that the **WarrantyandReturnQueryAnswer** variable is inserted in the **Send a message node**, so the generated answer is returned to the caller.

    ![](./media/image57.png)

18. Under the message node, select **+**, choose **Topic management** > **Go to another topic**, and select **Main Menu.**

    ![](./media/image58.png)

19. Select **Save** to save the topic.

    ![](./media/image59.png)

## Exercise 8: Create Troubleshooting Guide Topic

In this exercise, you create a custom topic to handle protection plan queries using a dedicated knowledge source.

1. In **Topics**, select **+** **Add a topic**, and then select **From blank**.

    ![](./media/image60.png)

2. Rename the topic to +++**Troubleshooting Guide**+++.

    ![](./media/image61.png)

3. On the trigger node, select **Edit**. Add +++**Troubleshooting Guide**+++ to the phrase field, and then select the **+** icon.

    ![](./media/image62.png)

4. Add the following trigger phrases:

    - +++Information About Troubleshooting Guide+++
    
    - +++Troubleshooting guide details+++
    
    - +++Assistance with troubleshooting+++

    ![](./media/image63.png)

5. Below the trigger node, select **+** and add an **Ask a question node**.

    ![](./media/image64.png)

6. In the message field, enter: +++**Please explain your query related to Protection policy**+++.

7.  Set **Identify** to **User's entire response**.

    ![](./media/image65.png)

8.  Select the **response variable** and rename it to
    +++**TroubleshootingQuery**+++

    ![](./media/image66.png)

9.  Verify that the response variable is renamed to
    +++**TroubleshootingQuery**+++ in the **Variable** properties pane.

    ![](./media/image67.png)

10. Below the **question node**, select **+**, select **Advanced**, and add a **Generative answer node**.

    ![](./media/image68.png)

11. Select **TroubleshootingQuery** as the input variable.

    ![](./media/image69.png)

12. For **Data source**, select **Edit** and enable **Search only selected sources**.

13. Select **Troubleshooting Guide** as the data source.

    ![](./media/image70.png)

14. Scroll down and select **Advanced**. Under **Save the bot response**, select the **variable field** and choose **Create a new variable**.

15. Select the new **Var1** variable and rename it to
    +++**TroubleshootingQueryAnswer**+++

    ![](./media/image71.png)

16. Under the **Generative answer node**, select **+** and add a **Send a message node**.

    ![](./media/image72.png)

17. Select the **{x}** icon and insert **TroubleshootingQueryAnswer** in the message field.

    ![](./media/image73.png)

18. Under the message node, select **+**, choose **Topic management** > **Go to another topic**, and select **Main Menu**.

    ![](./media/image74.png)

19. Select **Save** to save the topic.

    ![](./media/image75.png)

## Exercise 9: Configure Escalation Topic

In this exercise, you configure call escalation so the agent can transfer conversations to a live agent.

1.  From the top navigation, select **Topics**, and then select **System topics**.

2.  Open the **Escalate** topic.

    ![](./media/image76.png)

3. In the message node, enter: +++**Please wait while connecting**+++

    ![](./media/image77.png)

4. Below the message node, select **+** and add **Transfer
conversation** under **Topic management**.

    ![](./media/image78.png)

5. Select **Save**.

    ![](./media/image79.png)

## Exercise 10: Connect Channel and Publish Agent

In this exercise, you connect the agent to the Dynamics 365 Contact Center channel and publish it.

1. Navigate to **Channels**.

2. Select the **Dynamics 365 Contact Center** channel.

    ![](./media/image80.png)

3. Select **Connect**.

    ![](./media/image81.png)

4. After the connection is established, select **Publish** in the upper-right corner.

    ![](./media/image82.png)

5. Select **Publish** again to confirm.

![A screenshot of a computer AI-generated content may be incorrect.](./media/image83.png)

6. Verify that the agent is successfully connected to **Dynamics 365 Contact Center**.

    ![](./media/image84.png)

## Exercise 11: Connect Agent to Voice Workstream

In this exercise, you connect the AI agent to the voice workstream for handling inbound calls.

1. Return to **Contoso Voice Workstream**.

2. Scroll down and select **+** **Add AI agent**.

    ![](./media/image85.png)

3. Select **Contoso Voice Agent**.

4. Select **Connect**.

    ![](./media/image86.png)

5. Verify that **Contoso Voice Agent** appears as the connected AI agent for the voice workstream.

    ![](./media/image87.png)

6. Wait until the agent shows as connected successfully.

**Note**: Agent testing may take up to 15 minutes to become available after configuration.

   ![](./media/image88.png)

## Exercise 12: Test the Agent

1. Open the **Contoso Voice Workstream** page and scroll to the **Voice channel** section. Note the phone number displayed.

    ![](./media/image89.png)

2. Call the **phone numbe**r listed and wait for the **Copilot voice agent** to contact.

3. When prompted, say **"Troubleshooting Guide" or "Warranty & Return Policy"** to select the required option.

4. Ask Copilot, **"Give me details about the Warranty & Return Policy,"** and listen to the response.

5. To connect with a customer representative, clearly say **"Talk to an agent."**

6. Open **Copilot Service Workspace** from the top app selector.

7. Verify that the **incoming call** appears in the top-right corner of **Copilot Service Workspace**, confirming successful call routing.

    ![](./media/image90.png)

**Expected result: The incoming call appears in Copilot Service Workspace, confirming that the voice agent is receiving and routing live calls.**

## Summary

You have completed an end-to-end voice AI agent for Contoso using **Microsoft Copilot Studio** and **Dynamics 365 Contact Center**. The lab covered trial activation, contact center setup, voice agent creation, knowledge-source configuration, conversational topics, escalation, channel connection, publishing, voice-workstream integration, and live-call validation. The completed solution can answer Warranty & Return Policy and Troubleshooting Guide questions using the configured documents and transfer callers to a live representative when needed.
